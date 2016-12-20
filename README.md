OPX object model schemas
================
The YANG models in this repo define the object model for all of the components
in the NAS host adapter. 

Model overview
--------------
Applications/scripts can use existing and build new models for behavior on the
system.
Read the Application Programming Guide for more information on the CPS
interfaces.

The YANG class parser go through each file and generate the following
items:

- C/C++ headerfiles with all of the class names and attributes, enums,
typedefs, and so on 

- C++ metadata files that are compiled to loadable models which are then
available to CPS enabled applications

- XML files with metadata that can be used by other languages for which
loadable models are not suitable

> **NOTE**: The name of the YANG model is reflected in the symbol prefix -
class names, types, enums, and so on. We describe in the documentation how we map YANG classes and attributes to C/C++ headers.

Where are the outputs?
----------------------

Good question... 

There are two main packages created from this source repository:

- `libsonic-model-dev` (model header files)
- `libsonic-model1` (model meta data in compiled format)

After installing the
`libsonic-model-dev`, the header files will be stored in the _/usr/include/open-switch_
folder (unless you change the prefix).

The library metadata files will be stored in the _usr/lib/x86_64-linux-gnu/_
directory (assuming default debian 64-bit build).

You can see the metadata from Python using the cps.type API or the cps.info API
or one of the many other python extension APIs.

Add new model
------------------
To add a new model to the system, add a model file into the _yang-model_
directory you need to:

**1**. Create a new YANG model (extension should be .yang).

**2**. Copy the YANG model into the yang-model directory.

**3**. Update the Makefile.ini with the appropriate model.

**4**. Run a build.

Change/enhance model
--------------------------
Adding attributes and deleting attributes are as easy as modifying the model,
and recompiling.

The history files need to be kept in sync with the YANG model - that history
file provides upgradability between model changes.

Use models
================
Platform example
----------------
For example, using a class from the `dell-base-pas.yang` model.

The model prefix is `base-pas`.
The class we want to use in this example is `entity`.

The key for the entity class (within the `dell-base-pas.yang`) is
`base-pas/entity`.

Networking example
------------------
For example, let's say that an application needs to get the LAG interfaces via
script (ignoring that the LAG can be queried through the Linux bonding
commands). The interface class that
holds the LAG information is in the the `dell-base-if.yang` file.

In this file, the class is actually an augment of the `/if:interfaces/if:interface`.
Prefix in the file is `dell-base-if-cmn`.

Since the mode is an augment, normally you would communicate using the key from
the augmented object which is in this case `if/interfaces/interface`.

But looking at the details in the YANG model (description) itself (in
`dell-base-if.yang`), the documentation states that access to the class can be
through the `dell-base-if-cmn/if/interfaces/interface` model.

From a CPS perspective, you can use the key
`dell-base-if-cmn/if/interfaces/interface`.

But it also states that to do a query of lags, you need to specify the `ietf`
interface type.

Using the `cps_get_oid.py` script you would use:

    cps_get_oid.py target dell-base-if-cmn/if/interfaces/interface
    if/interfaces/interface/type=ianaift:ieee8023adLag

Models
======

Platform models
---------------
- `dell-base-platform-common.yang`
- `dell-base-env-tempctl.yang`  
- `dell-base-media.yang`            
- `dell-base-pas.yang`

Management interface (eth0)
---------------------------
- `dell-base-mgmt-interface.yang`   

Network models
--------------
- ACL and QoS config
- `dell-base-acl.yang`        

Networking interfaces
---------------------
The following set of models provides the networking access-related
models/classes:

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

Build
========
See the instructions in the opx-nas-manifest repo for more details on
the common build tools. 

[opx-nas-manifest](https://github.com/open-switch/opx-nas-manifest)

Development Dependencies:
- opx-logging
- opx-common-utils
- opx-object-library

Package Dependencies:
   libsonic-logging1 libsonic-logging-dev
libsonic-common1 libsonic-common-dev libsonic-object-library1
libsonic-object-library-dev sonic-yang-utils 

BUILD CMD: base_build libsonic-logging1 libsonic-logging-dev libsonic-common1
libsonic-common-dev libsonic-object-library1 libsonic-object-library-dev
sonic-yang-utils-dev -- clean binary

(c) 2016 Dell
