opx-base-model
==============
The YANG models in this repo define the object model for all of the components in the OPX base modules. 

Model Overview
--------------
Applications/scripts can use existing and build new models for behavior on the system.
Read the Application Programming Guide for more information on the CPS interfaces.

Generally each YANG model is contained in a YANG prefix.  In this prefix are all of the classes, types, enums, etc are defined.

The YANG class parser go through each file and generate the following items:
1) C/C++ headerfiles with all of the class names and attributes, enums, typedefs, etc 
2) C++ metadata files that are compiled to loadable models which are then available to cps enabled apps
3) xml files with metadata that can be used by other languages for which loadable models are not suitable

NOTE: In the documentation, we describe how we map YANG classes and attributes to C/C++ headers.

Where are the Outputs?
----------------------

Good question... 
There are two main packages created from this source repository. 
libopx-base-model-dev - model header files
libopx-base-model1 - model meta data in compiled format

After installing the libopx-base-model-dev, the header files will be stored in the /usr/include/opx folder (unless you change the prefix).

The library metadata files will be stored in the usr/lib/x86_64-linux-gnu/ directory (assuming default debian 64-bit build)

You can see the metadata from Python using the cps.type API or the cps.info API or one of the many other python extension APIs.

Adding a New Model
------------------
To add a new model to the system, add a model file into the yang-model directory you need to:
1) Create a new YANG model (extension should be .yang)
2) Copy the YANG model into the yang-models directory
3) Update the Makefile.am with the appropriate model
4) Run a build


Changing/Enhancing a Model
--------------------------
Adding attributes and deleting attributes are as easy as modifying the model, and recompiling.

The history files need to be kept in sync with the YANG model - that history file provides upgradability between model changes.


Using the Models
================
Platform Example
----------------
For example, using a class from the dell-base-pas.yang model.

The model prefix is base-pas.
The class we want to use in this example is "entity".

Therefor the key for the entity class (within the dell-base-pas.yang) is base-pas/entity


Networking Example
------------------
For example, lets say that an application needs to get the LAG interfaces via script (ignoring that the LAG can be queried through the Linux bonding commands).  The interface class that holds the LAG information is in the the dell-base-if.yang file.

In this file, the class is actually an augment of the /if:interfaces/if:interface.

Prefix in the file is dell-base-if-cmn.

Since the mode is an augment, normally you would communicate using the key from the augmented object which is in this case if/interfaces/interface.

But looking at the details in the YANG model (description) itself (in dell-base-if.yang), the documentation states that access to the class can be through the dell-base-if-cmn/if/interfaces/interface model.

Therefore from a CPS perspective, you can use the key "dell-base-if-cmn/if/interfaces/interface".

But it also states that to do a query of lags, you need to specify the ietf interface type.

Therefore.. using the cps_get_oid.py script you would use:
cps_get_oid.py target dell-base-if-cmn/if/interfaces/interface if/interfaces/interface/type=ianaift:ieee8023adLag


Models
======

Platform Models
---------------
dell-base-platform-common.yang
dell-base-env-tempctl.yang  
dell-base-media.yang            
dell-base-pas.yang

Management Interface (eth0)
---------------------------
dell-base-if-mgmt.yang   

Network Models
--------------
ACL and QoS Config
dell-base-acl.yang        

Networking Interfaces
The following set of models provides the Networking Access related models/classes.
dell-base-if.yang          
dell-base-if-lag.yang       
dell-base-if-phy.yang       
dell-base-if-vlan.yang     
dell-base-if-mgmt.yang     
dell-base-if-linux.yang    
dell-base-qos.yang
dell-base-ip.yang                
dell-base-routing.yang
dell-base-l2-mac.yang           
dell-base-sflow.yang
dell-base-lag.yang              
dell-base-stg.yang
dell-base-switch-element.yang
dell-base-mirror.yang           
dell-base-packet.yang            
dell-interface.yang

(c) Dell 2016
