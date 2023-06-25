## Kernel Component

-uname -a    -> # To know the Kernel
cd /usr/src to see the kernel and build a custom kernel 
yum install kernel-devel  # On Cent Os
standard location  for Kernel -> usr/src/linux
Alternate Kernel doc location for CentOS ->  /usr/share/doc/kernl-doc/Documnet

/boot directory and kernel compression 
-compiling the system kernel and preparing the system dependies 
##### Kernel runtime management & Troublehsooting
-Kernel that are loadable only when they are need. 
  - uname "Prints system info" a;though people assocaite with kernel
  - uname -a "Kernel name, host name, release.
  - uname -r " Kernel Version
  -  uname -o "OS"
Running Kernel modues ar elocted -> /lib/modules/<kernel-version>/kernel/<loadable-directory>
man depmod - program to generate modules dependency and map files.
cat lib/modules/<kernel-version>/moubles.dep    -> this files shows all dependecies modules on the system - {field 1- kernel module:} Hence field 1 depends on fields 2 to run. 
                                                *-> If there's only one field that means the modules doesn't have any dependcies.

In the cd /lib/modules/<kernel-version> directory there files that are called map files having  map at the end examples include i) modules.usbmap ii) moudules.pcimap
 - And they explain what kernel module & devices are mapped to what types of hardware information.

###### Listing, Adding & Removing Loadable Kernel Modules
**lsmod** - "list modules" 
**rmmod** - "remove a module"
**insmod** {insmod lp /<path>}- "Insert a module" -> You need to know the module and the ar tto the moudule. i.e the full path name
            modinfo -> modinfo <lp>   #To get the path

**modprobe**  - modprobe <module-name>  "add/oinsert a module" 
cd /etc/modprobe.d/ -> a standard directory  that contains files allowing you to make changes on how your modules are loaded. 
                     4 types. i)Force install ii) Remove device that will automatically allow the module to be loaded iii) alias - call it something else iv) balcklist.conf - prevent/overwrite the conf.      

###### Viewing and Changing Kernel Parameters in the system both temporary or Persistent Modules
- using /proc/sys and sysctl
**Temporary change**
- /proc/sys file system is not really a fs, its amemory based fs mounted under /proc  #Everything relaated under modules is stored in memory
-  cd /proc/sys #ls we see dev,net,kernel etc.
-  Temporary -> and change the value and wq!
-  **List all Kernel Runtime MOdule parameter**   -> sysctl -a
-  Set a kernel runtime module for palport..ie sysctl -a | grep palport then you get the dev modules and
-      sysctl <module>=35 # Temporary set the module, Note do not put spaces

-   **Permanent Chnages**
-   cd /etc/ and edit vi sysctl.conf and enter the module.


##### Displaying Information About System Hardware 
which includes device on the system. 
- lspci -> list all the pci devices
- 00:00:0 host bridge - means device 0, bus 0, port 0 is my host bridge
- lspci -v -> More info
- lspci -k -> device,subsystem related to and  the kernel driver and modules

- lsdev -display info about installed hardware - from the ioports in the /proc/
- lsusb - display devices connected  {-v ,-d <devicename>}
- /var/log/message -hardware info is loggged {Redhat, Centos }     
- /var/log/syslog -hardware info is loggge {Ubuntu}
- 
**/dev fs**
  /dev or /etc/udev/rules.d
 **udevadm  monitor - >command to print/monitor when a device is connected to the system**



  Make" targets are valid for "cleaning" a system prior to compiling the kernel
   - make mrproper will do everything make clean does, plus remove your config file, the dependency files, and everything else that make config creates.
   - The typical standard is make clean which will remove all intermediate files.
   - make distclean makes the tree just the way it was when it was un-tarred (or something pretty close) including removing any configure script outpu
