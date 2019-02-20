# SAP WebIDE for Linux
## installation
* download latest version from https://tools.hana.ondemand.com/#sapui5 (``sap-webide-personal-edition-X.XX.X-trial-win32.win32.x86_64.zip``)
* copy ``./eclipse/orion`` and ``./eclipse/plugins/org.eclipse.equinox.launcher.gtk.linux.x86_64_1.1.200.v20140603-1326/`` from https://download.eclipse.org/orion/drops/R-10.0-201510301610/index.html (Eclipse Orion V.8.0 http://download.eclipse.org/orion/drops/R-8.0-201502161823/index.html is not available any more) to WebIDE ``./eclipse/..``
* modify orion.ini 
````
--launcher.library
plugins/org.eclipse.equinox.launcher.gtk.linux.x86_64_1.1.200.v20140603-1326
````

## start
* run ``./orion``
* start http://localhost:8080/webide/index.html in browser (chrome..)

## work files
stored under ``./eclipse/serverworkspace/<language>/<user>/OrionContent``

## backend system (abap repository for UI5)
* add system file to ``./eclipse/config_master/service.destinations/destinations``
* System-Files-Content:
````
#ServiceDestination
Description=XXX
Type=HTTP
TrustAll=true
Authentication=NoAuthentication
Name=XXX
ProxyType=Internet
URL=http\://xxx.xxx.xxx.xxx\:xxxx
WebIDEUsage=odata_abap,dev_abap,ui5_execute_abap,bsp_execute_abap
WebIDESystem=XXX
WebIDEEnabled=true
sap-client=xxx
````
  
## GIT
* clone repositiory
* create project
* stage all -> commit
* push
