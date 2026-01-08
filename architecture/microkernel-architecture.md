# microkernel architecture

* it also refers as "plug-in architecture"
* users can add features or additionality in terms of plugins
* examples - many operating systems are developed based on this architecture
* examples - product or package based applications are developed in this architecture

## topology

<img src="./asserts/microkernel-architecture-1.png" width="200" height="400" alt="Alt text">


* it consists of two types of architectural components
    - core systems
    - plug-in modules

* application code is split between core systems and plug-in modules, which gives
    - extensibility
    - flexibility
    - and isolations

* the core system can have
    - minimum functionality required to function - examples IDEs. The rest of the features can be given as plug-ins
    - some cases, it can also be a full features - examples chrome browsers. The extensions can be provided as plug-ins
 
* plug-in modules
    - they are stand alone, provide enhanced additional features to enhance core system capabilities
    - they are developed as separate modules and connected to the core system by
        + jars or dlls
    - they are managed through frameworks such as OSGI (Open Service Gateway Initiative), Java Modularity, Jigsaw, Penrose and Prism
    - monolithic architecture - these plugins can be deployed as runtime components which can be loaded without-restarting or restarting the core systems.
    - distributed architecture - these plugins can also be deployed as REST endpoint or messaging systems which can be integrated with the core services.

* plug-in registry
    - the core system needs to know what are the plugins are available.
    - the plugins are added to the plugin registry. It have the information about the plugins
        + name
        + contract details and protocol details on how plugins are connected to the core system
          



