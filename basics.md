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
- **pidof / pgrep**: retrieve the pid of a process(es)
- **systemctl / service**: retrieve service information (systemd)
- **top / htop**: displays processes and their associated resource utilization in live output. **NOTE:** Due to the live output, top and htop are not recommended for incorporation into scripts.
- **kill**: send termination signal to a process by PID
- **pkill**: send termination signal to a process by process name
- **killall**: send a termination signal to all processes with a specific process name
- **pstree**: displays processes in a parent-child relational format

<br>

### **Network Information Retrieval**
- **ip / ifconfig**: display information about network interfaces
- **netstat / ss**: display current connection information
- **lsof**: list open files associated with processes / network connections

<br>

### **User Information**
- **who / w**: displays currently logged in users
- **last**: display successful login / logout events as recorded in /var/log/wtmp
- **lastb**: displays unsuccessful login events recorded in /var/log/btmp 
- **id**: simple command line utility for displaying a real and effective user and group IDs
- **groups**: used to show all the groups a user belongs to
- **finger**: used to search information about a user (ie. real name, home directory, default shell, time logged in, etc., as applicable). **NOTE:** Not installed by default on all linux distros.
- **lslogins**: displays information about user accounts on the system such as UID, username, number of owned running processes, last login time, and user [GECOS](https://en.wikipedia.org/wiki/Gecos_field) field
- **users**: displays users currently logged in to the system
- **who**: displays users currently logged in to the system, the terminal they are connected to, last login date/time, and the address they are connected from ( "(:0)" for locally logged-in, or an IP address for a remote connection)
- **w**: displays system uptime, number of users logged in, and basic information about their login session (ie. username, terminal, address connected from, login time, etc.)

<br>

### **Variables**
Local Variables in bash can be assigned by typing the "naked" variable name on the left side of an equals sign, and the assigned value on the right.  The variable can later be recalled by prepending a "$" to the variable name (ie. a=b, and the variable is later recalled by typing $a) from within the current terminal / context only. **NOTE:** Variable names are case sensitive, as with most things in Linux.

[Brief example of setting a variable](images/Variables1.png)

Environment Variables can be declared by prepending "export" to a normal variable declaration (ie. export a=b). This will allow the variable to be used by the current terminal / context, as well as any children spawned.

Global Variables are in reference to a variable declared at the beginning of a bash script that can be used throughout in various functions or commands, unless over-written.

Lastly, bash has standard environment variables that can be queried for information and / or manipulated to affect attributes of a user's shell experience. They can be found [here](https://www.gnu.org/software/bash/manual/html_node/Bash-Variables.html).
<br>

### **Aliases**
When typed with no arguments, the ***alias*** command will display current aliases. To set a new alias, type <code> alias shortname=command </code>, where shortname is the alias you want to type / run, and command is the the action you want to perform.

[Setting / Using a custom Alias](images/Aliases1.png)

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

### **Brace Expansion**

<br>



<br>

**References:**
- https://phoenixnap.com/kb/linux-commands-cheat-sheet
- https://www.tecmint.com/find-user-account-info-and-login-details-in-linux/
- https://www.gnu.org/software/bash/manual/html_node/index.html
