# **Standard Linux Directories**

#### **Basic Directory Descriptions**
- **/** - The root directory is the base of the whole filesystem in Linux, and everything in the Filesystem falls beneath it. 
- **/bin** - Contains all of the essential system binaries for "single user mode" (basic functionality.
- **/boot** - Contains all files necessary to boot the system (ie. GRUB bootloader files, Linux Kernels, etc.).
- **/dev** - Contains represenations of devices as special files, which do not exist on the physical filesystem, but can be used to interact with the devices they represent.
- **/etc** - Contains system-wide configuration files with can be typically viewed/altered with a text editor to understand how a service is configured (ie. /etc/ssh/sshd.conf).
- **/home** - Contains home folders for each user.
- **/lib** - Contains essential shared libraries required by system binaries.
- **/lost+found** - Contains files deemed corrupted at boot to aid data recovery.
- **/media** - Default location for special file representations of removable / temporary media.
- **/mnt** - Traditionally used for mountpoints for temporary filesystems.
- **/opt** - Traditionally used to store optional software packages or binaries and their associated files.
- **/proc** - Typically referred to as a [Virtual Filesystem](vfs-proc), since all items within are special file representations of things like processes. The files to not exist on the physical filesystem, and the entire directory is built at boot and destroyed at shutdown. 
- **/root** - The root user's home folder. 
- **/sbin** - Contains binaries typically used by the root user for system administration.
- **/tmp** - Contains temporary files which are deleted at shutdown / restart. 
- **/usr** - Contains user binaries and applications.
-**/var** - Contains variable data files that are written to by various applications (log files for a service in /var/log/*\<service>*)

<br>

**NOTE:** The explanations provided above are the default \*NIX file locations and standard practice. However, given the proper permissions, there is nothing preventing a user from storing files in non-standard locations.


<br>

**Online References:**
- https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/
- https://www.linuxtrainingacademy.com/linux-directory-structure-and-file-system-hierarchy/