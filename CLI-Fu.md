# Command Line-Fu
### **Brace Expansion**
Strings can be generated in sequence for use in naming files and directories, generating file contents, creating input to pass along in a pipeline, and scripting. To utilize brace expansion, enter either a comma-separated list of strings or range (separated by two dots, "..") of numbers between a pair of curly brackets. Optionally, a preamble and post-script can be placed before and after the brackets, respectively, to add a static portion to the output.

In the example below, brace expansion is used to insert an integer range (from 1 to 10) into a for loop to develop a list of IP addresses with the same first three octets.

<br>

<figure>
	<img src="images/BraceExp1.png">
	<figcaption>Brace Expansion Example</figcaption>
</figure>

<br>

### **Command Substitution**
When using the Linux command line to parse through data, gather artifacts, or organize files, it may be more efficient to utlize command substitution to pass output from one command to another in a way that's not possible with the pipeline. 

In the example below, command substitution is used to run the `date` command inside the naming of a file to get the current time (in HH:MM:SS format) and use it in the filename. For demonstration purposes, this example was run within a for loop, however, in reality it wouldbe more useful within a recurring command (ie. cron job) to create a unique filename.

<br>

<figure>
	<img src="images/CommandSub1.png">
	<figcaption>Command Substitution Example</figcaption>
</figure>

<br>



<br>

### **History Substitution / Event Designators**
Below is a short (not all-inclusive) list of useful shorthand ways to reference bash history and utlize all or part of commands previously used. This is not only useful for saving time on the command line, but for example avoiding typos when referencing long filepaths, or trying to recall the exact syntax of a previously run command, expecially if it involves a long pipeline or command substitution.
 
<br>

`!!` previous command, most commonly used to re-enter a command that error'ed out due  to lack of privileges (ie. ***sudo !!***)
`!$` last argument from previous command
`!#` item # from bash history
`!-#` item # lines back from most recent in bash history
`$$` the current bash process's PID
`!<string>` searches for the most recent command ***starting*** with "string" and executes it
`!?<string>` searches for the most recent command ***containing*** "string" and executes it
`^<command1>^<command2>^` searches for the most recent command starting with "command1", replaces it with "command2", and executes it
**NOTE: ** the command being searched and/or replaced can include switches (ie. replacing `ls -la` with `cat`)

<br>

In most instances of Bash, **ctrl+r** will initiate a search through the command history, where you can begin typing and match on any part of a previous command. This functionality will match on the most recent command first; to continue searching you can add text to refine the search, or press **ctrl+r** again to cycle back to the next matching command. If you cycle back too far and wish to search forward through commands, press **ctrl+s**. 

**NOTE:** In some instances of bash, **ctrl+s** will suspend the current terminal, if this happens, **ctrl+q** will resume the terminal.

If you begin to type a complex command, then wish to search the history since you know it's been used before, enter **ctrl+aryr**, which corresponds to the following actions:
- **ctrl+a**: moves cursor to the beginning of the line (same functionality of **home** in this case)
- **ctrl+r**: call reverse bash history search, copies text typed thus far
- **ctrl+y**: paste copied text back onto command line
- **ctrl+r**: move to most recent matching command in bash history

<br>

### **Loops**

[](images/loop.jpg)

#### For
#### While
#### Until

<br>

### **Standard Hotkeys**

<br>

### **Useful Examples**

Ping Sweep - 
`{ for i in {1..254}; do ping -c 1 -W 1 192.168.88.$i & done } | grep "64 bytes"`

Display current bash key bindings (hotkeys) - 
`bind -P | grep -v "not bound to any keys"`


**External References:**
- https://www.gnu.org/software/bash/manual/html_node/Pipelines.html
- https://www.commandlinefu.com/commands/browse/sort-by-votes
- https://www.thegeekstuff.com/2011/08/bash-history-expansion/
- https://www.digitalocean.com/community/tutorials/how-to-use-bash-history-commands-and-expansions-on-a-linux-vps