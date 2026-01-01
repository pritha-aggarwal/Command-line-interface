## **Command Line Interface Graded Lab Assignment, submitted by Pritha Aggarwal**

Linux Commands testing assignment  
Personal Ubuntu Used-

### **Question3**  
You have been asked to understand how Linux manages files using links and disk usage information.As part of your role, you will perform the following operations within your own user space.

**1** File Creation. Create a file named sample_data.txt in your home directory and add some sample text to it.  
**Command**:
```bash
echo "This is sample data for the Linux exercise." > ~/sample_data.txt
```
**Output**:

Explanation: **'echo'** writes the text in the file. **'>'** is used to direct the text in file (creating file if does not exist). **'~/sample_data.txt'** is the file where text is to be written.

**2** Hard Link Creation. Create a hard link to sample_data.txt named sample_hard.txt.  
**Command**:
```bash
ln ~/sample_data.txt ~/sample_hard.txt
```
**Output**:

Explanation: **'ln'** command creates a link. **'~/sample_data.txt'** is the source file. **'~/sample_hard.txt'** is the name of the hard link created. 

**3** Symbolic Link Creation. Create a symbolic (soft) link to sample_data.txt named sample_soft.txt.  
**Command**:
```bash
ln -s ~/sample_data.txt ~/sample_soft.txt
```
**Output**:

Explanation: **'ln'** command used to create a link. **'-s'** specifically creates a soft link. **'~/sample_data.txt'** is the source file. **'~/sample_soft.txt'** is the name of the soft link created.

**4** Inode Verification. Display the inode numbers of sample_data.txt, sample_hard.txt, and sample_soft.txt.  
**Command**:
```bash
ls -i sample_data.txt sample_hard.txt sample_soft.txt
```
**Output**:

Explanation: **'ls -i'** gives the list of files along with inode numbers **'sample_data.txt sample_hard.txt'** will have the same inode number. **'sample_soft.txt'** will have a unique inode number.

**5** Inode Analysis. Identify which files share the same inode number and briefly explain the reason.  
**Command**:
```bash
sample_data.txt and sample_hard.txt share the same inode number.
```
**Output**:

Explanation:  
**Hard Link Nature**: A hard link is not a copy but an additional directory entry pointing directly to the same physical data on the disk.  
**Shared Identity**: Because both filenames refer to the same underlying data (inode), changes to one are immediately reflected in the other.

**6** File Metadata Inspection. Display detailed file information (permissions, ownership, size, timestamps) of sample_data.txt.  
**Command**:
```bash
ls -l sample_data.txt
```
**Output**:

Explanation: **'ls'** command is used to list all the files and directories. **'-l'** gives the list in long format i.e. permissions, owner, group, size and timestamps.

**7**  Disk Usage Check. Display the disk usage of your home directory in a human-readable format.  
**Command**:
```bash
du -s-h ~
```
**Output**:

Explanation: **'du'** command is used to check the disk usage of files and directories. **'-s'** gives only the total size of directory. **'-h'** gives the size from raw bytes to human readable form. **'~'** is a shortcut to target the home directory.

**8** File Size Overview. Display the size of each file present in your home directory in a human-readable format.  
**Command**:
```bash
ls -l-h ~
```
**Output**:

Explanation: **'ls'** command lists all the directories. **'-l'** uses the long listing format. **'-h'** converts file size from bytes to human readable format. **'~'** directs to the home directory.

**9** Link Deletion Test. Delete the symbolic link sample_soft.txt and verify that the original file sample_data.txt is unaffected.  
Command:
```bash
rm sample_soft.txt && ls -l sample_data.txt
```
Output:

Explanation: **'rm'** is the command to remove directory or any content. **'sample_soft.txt'** is the soft lnk to be deleted. **'&&'** ensures that 2nd command runs after 1st is successful. ** ls -l sample_data.txt** lists the content in file in long format for verification.

**10** Disk Utility Demonstration. Demonstrate the usage of du and df commands using various useful options and briefly explain the output.  
Command:
```bash
du -h --max-depth=1
```
Output:

Explanation: **'du'** command gives the disk usage of the directories and files. **'-h'** converts the raw size from bytes to human readable form i.e. Kb, Gb, etc.