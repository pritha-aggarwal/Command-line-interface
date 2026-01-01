## **Command Line Interface Graded Lab Assignment, submitted by Pritha Aggarwal**

Linux Commands testing assignment
Personal Ubuntu Used-

###Question1
You have just joined IxD Systems as a junior systems engineer. On your first day, the Linux administrator asks you to perform a basic environment verification on the lab machine using your own login account.

**1** User Identity Verification.
Command: **id**
Output:

Explanation: **'id'** is the command used for user identity verification. This command returns **UID, GID and all groups** associated with user.

**2** Workspace Validation. Display the current working directory and list all files and directories in that location using long format listing command.
Command:** pwd && ls -l**
Output:

Explanation: **'pwd'** returns the present working directory i.e. the directly being used currently and **'ls -l'** gives the list of the files in it in the long format (permissions, group, owner, date, size, time and name of file).

**3** Environment Confirmation File. Create a file named user_info.txt and write the line:&quot;Linux user environment verified&quot.
Command: **echo "Linux user environment verified" > user_info.txt**
Output:

Explanation: **'echo'** writes the given text in the file and **'>'** creates or overwrites (if already existing) the file.

**4** File Integrity Check. Display the number of characters present in user_info.txt.
Command: **wc -m user_info.txt**
Output:

Explanation: **'wc'** counts the words, lines  and characters. **-m** specifies that characters are to be counted and not lines or bytes. **user_info.txt** is the target file to be checked.

**5** Learning the Tools. Identify one useful option and briefly explain what it does.
command: **man mkdir**
Output:

Explanation: **'man mkdir'** opens the manual for all the options of mkdir command. **-p** is one of the options, it allows us to create parent directories without having to specify. eg- **'mkdir -p project/2025/data'** , will create any intermediate folders if missing.

**6** Home Directory Inspection. List the contents of your home directory sorted alphabetically.
Command: **ls -l ~**
Output:

Explanation: **'ls'** command gives the list of all content. **'-l'** gives the list in long format. **'~'** specifies that list is to be given from the Home Directory. **'ls'** command by default gives the result in the alphabetic format.

**7** Log Investigation. Search for the word &quot;admin&quot; inside a file named log.txt and display only the matching lines.
Command: **grep "admin" log.txt**
Output:

Explanation: **'grep'** command is the standard linux command for searching text patterns in a file. **'"admin"'** is the word to be searched. **'log.txt'** is the file where a text pattern is to be searched.

**8** System Information Check. Display the Linux kernel version currently running.
Command: 
```bash
**uname -r**
```
Output:

Explanation: **'uname'** prints the system information. **'-r'** specifically returns the kernel version information.

