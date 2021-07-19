# **Bash Basics**

#### **MAN Pages and Help Files**
Manual pages, also known as man pages, are simply reference manuals, most commonly used to understand the functionality of any given command. There are different categories that man pages fall into, depicted in the table below. 
<br>
Man pages can be accessed by typing <code> man ***command*** </code> , which will open them with the ***less*** manual pager. Additionally, most commands also have abbreviated help files that can be accessed by typing <code> ***command*** -h </code> **OR** <code> ***command*** --help </code> . 
<br>

**NOTE:** Since manual pages are opened with ***less***, you can initiate a test search by typing "/", as well as utilize any other functionality that ***less*** possesses. 

<br>

|Manual Page Number   | Description
|----------------|-----------------------------------------------------------------------|
| 1   					  | Executable programs or shell commands    											 |
| 2   					  | System calls (functions provided by the kernel)   									|
| 3                       | Library calls (functions within program libraries)    								  |
| 4                       | Special files (usually found in /dev)   													  |
| 5                       | File formats and conventions, e.g. /etc/passwd   								   |
| 6                       | Games   																									 |
| 7                       | Miscellaneous (including macro packages and conventions)		        |
| 8   					  | System administration commands (usually only for root)   					|
| 9   					  | Kernel routines (Non standard)																  |


<br>

### **FS navigation / operation**
- **pwd**: displays the present working directory
- **cd**: change directory
- **ls**: list contents of a directory
- **touch**: create a file; update timestamp
- **mkdir**: make a directory
- **rmdir**: remove directory
- **chmod**: change permissions
- **chown**: change ownership
- **cp**: copy files
- **mv**: move or rename a file
- **more**: page through the contents of a file
- **less**: page through the contents of a file (like more, but with more functionality)
- **cat**: output the contents of a file
- **head**: display the beginning of a file (10 lines by default)
- **tail**: display the end of a file (10 lines by default)
- **wc**: count lines, characters, or bytes of a file
- **gpg**: encrypt a file 
- **sha#sum / md#sum**: hash a file or data
- **dd**: dump data from various sources (hard drive, partition, process memory)

<br>

### **System Survey**
- **fdisk**: disk partitioning functions
- **free**: display memory usage statistics
- **dmesg**: prints the kernel message buffer, including device driver messages
- **uname**: retrieve general system information (kernel version, architechture, os, etc.)
- **lshw**: display hardware devices
- **lscpu**: display cpu information
- **lsblk**: display block devices (hard drives / partitions, mountpoints, usb devices, etc.)
- **lsusb**: display currently available usb devices
- **df**: display free / used space on the filesystem


<br>
### **Common Redirection**
- **">"**: sending standard output to ***overwrite*** a designated file
- **">>"**: sending standard output to ***append to*** a designated file
- **"<"**: retrieve contents from a file or source, send to standard input
- **"2>/dev/null"**: suppress errors 
<br>
### **Process / Service Info Retrieval**
- **ps**: list processes
- **pidof**: retrieve the pid of a process(es)
- **systemctl / service**: retrieve service information (systemd)
<br>
### **Network Information Retrieval**
- **ip / ifconfig**: display information about network interfaces
- **netstat / ss**: display current connection information
- **lsof**: list open files associated with processes / network connections
<br>
### **User Information**
- **who / w**: displays currently logged in users
- **last**: display all users logged in / out since /var/log/wtmp was created
- **id**: simple command line utility for displaying a real and effective user and group IDs
- **groups**: used to show all the groups a user belongs to
- **finger**: used to search information about a user (ie. real name, home directory, default shell, time logged in, etc., as applicable). **NOTE:** Not installed by default on all linux distros.
<br>
### **Variables**
<br>
### **Aliases**
<br>
### **ID'ing installed software / installing software**
<br>
### **Content Search / Output Manipulation**
- **grep**: search file / output content by keyword
- **egrep**: search file / output content by regular expression (same as grep -e)
- **awk**: retrieve specified ***columns*** from files / output 
- **sed**: edit files / output
- **tr**: 
- **cut**: 
- **sort**: 
<br>

**References:**
- https://phoenixnap.com/kb/linux-commands-cheat-sheet
- https://www.tecmint.com/find-user-account-info-and-login-details-in-linux/
