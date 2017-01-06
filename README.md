# opx-base-model
This repository contains the YANG models which define the object model for all software components.

## Model overview
Applications/scripts can use existing models, and build new models for behavior on the system.

Read the _Application Programming Guide_ for more information on CPS interfaces.

The YANG class parser go through each file and generate the following:

**1**. C/C++ header files with all of the class names and attributes, enums, typedefs, and so on. 

**2**. C++ metadata files compiled to loadable models which are available to CPS-enabled applications.

**3**. XML files with metadata can be used by other languages for which loadable models are not suitable.

> **NOTE**: Generally, the name of the YANG model is reflected in the symbol prefix - class names, types, enums, and so on. We describe how we map YANG classes and attributes to C/C++ headers in the documentation.

## Where are the outputs?
Good question...
There are two main packages created from this source repository:

- `libopx-model-dev` (model header files)  
- `libopx-model1` (model meta data in compiled format)

After installing the `libopx-model-dev`, the header files are stored in the _/usr/include/opx_ folder (unless you change the prefix).

The library metadata files are stored in the _usr/lib/x86_64-linux-gnu/_ directory (assuming default Debian 64-bit build).

You can see the metadata from Python using the `cps.type` API, or the `cps.info` API or one of the many other Python extension APIs.

## Adding a new model
To add a new model to the system, add a model file into the _yang-model_ directory:

**1**. Create a new YANG model (extension should be .yang).

**2.** Copy the YANG model into the _yang-model_ directory.

**3**. Update the makefile.ini with the appropriate model.

**4**. Run a build.

## Changing/enhancing a model
Adding attributes and deleting attributes are as easy as modifying the model, and recompiling.

The history files need to be kept in sync with the YANG model - that history file provides upgradability between model changes.

## Using models
### Platform example
Use a class from the `dell-base-pas.yang` model.

- The model prefix is `base-pas`, and the class we want to use in this example is _entity_
- The key for the entity class (within the `dell-base-pas.yang`) is _base-pas/entity_

### Networking example
Let's say that an application needs to get the LAG interfaces via script (ignoring that the LAG can be queried through the Linux bonding commands). The interface class that holds the LAG information is in the `dell-base-if.yang` file.

- In this file, the class is actually an augment of the `/if:interfaces/if:interface`
- Prefix in the file is `dell-base-if-cmn`

Since the mode is an augment, normally you would communicate using the key from the augmented object which is in this case `if/interfaces/interface`.

Looking at the details in the YANG model (description) itself (`dell-base-if.yang`), the documentation states that access to the class can be through the `dell-base-if-cmn/if/interfaces/interface` model.

From a CPS perspective, you can use the key `dell-base-if-cmn/if/interfaces/interface`.

It also states that to do a query of LAG interfaces, you need to specify the `ietf` interface type.

Using the `cps_get_oid.py` script you would use:    

    cps_get_oid.py target dell-base-if-cmn/if/interfaces/interface if/interfaces/interface/type=ianaift:ieee8023adLag
    
## Models
### Platform models

- `dell-base-platform-common.yang`
- `dell-base-env-tempctl.yang`  
- `dell-base-media.yang`            
- `dell-base-pas.yang`

### Management interface (eth0)

- `dell-base-mgmt-interface.yang`   

### Network  models

- ACL and QoS configurations
- `dell-base-acl.yang`  

### Networking interfaces
The following set of models provides the networking access-related models/classes:

- `dell-base-if.yang`          
- `dell-base-if-lag.yang`       
- `dell-base-if-phy.yang`       
- `dell-base-if-vlan.yang`     
- `dell-base-if-mgmt.yang`     
- `dell-base-if-linux.yang`    
- `dell-base-qos.yang`
- `dell-base-ip.yang`                
- `dell-base-routing.yang`
- `dell-base-l2-mac.yang`           
- `dell-base-sflow.yang`
- `dell-base-lag.yang`              
- `dell-base-statistics.yang`
- `dell-base-stg.yang`
- `dell-base-switch-element.yang`
- `dell-base-mirror.yang`           
- `dell-base-vlan.yang`
- `dell-base-packet.yang`            
- `dell-interface.yang`

(c) 2017 Dell
