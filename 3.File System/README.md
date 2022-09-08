## 🔷 Linux File System

- **The Linux filesystem** - is the structure in which all of the information on your computer is stored. In fact, one of the defining properties of the UNIX systems on which Linux is based is that nearly everything you need to identify on your system (`data`, `commands`, `symbolic links`, `devices`, and `directories`) is represented by items in the filesystems.

- **In Linux**, files are organized within a **hierarchy** of directories. Each directory can contain files as well as other directories. You can refer to any file or directory using either 
  - a **full path** (for example, `/home/joe/myfile.txt`) or 
  - a **relative path** (for example, if` /home/joe` were your current directory, you could simply refer to the file as `myfile.txt`).

- If you were to map out the files and directories in Linux, it would look like an **upside-down** tree. At the top is the `root` directory (not to be confused with the root user), which is represented by a single slash `(/)`. 
- Below that is a set of common directories in the Linux system, such as `bin`, `dev`, `home`, `lib`, and `tmp`, to `name` a `few`. 
- Each of those directories, as well as directories added to the `root` directory, can contain subdirectories.

  - **The Linux filesystem is organized as a hierarchy of directories.**
        ![](./../img/1.linux-file.png)

**************************************************


### 🔹Using Basic Filesystem Commands
    
    
- **Commands to Create and Use Files**
   - **cd**  -  Changes to another directory
   - **pwd**  -  Prints the name of the current (or present) working directory
   - **mkdir**  -  Creates a directory
   - **chmod**  - Changes the permission on a file or directory
   - **ls**  -  Lists the contents of a directory



### 🔹Using file-matching metacharacters

- To save you some keystrokes and enable you to refer easily to a group of files, the bash shell lets you use **metacharacters**. 
- Anytime you need to refer to a file or directory, such as to list, open, or remove it, you can use metacharacters to match the files you want. Here aresome useful metacharacters for matching filenames:


  - **\*** -  Matches any number of characters.
  - **?** - Matches any one character.
  - **[...]** - Matches any one of the characters between the brackets, which can include a hyphen-separated range of letters or numbers.

### 🔹Using file-redirection metacharacters

- Commands receive data from **standard input** and send it to **standard output**. 
- Using **pipes** (described earlier), you can direct standard output from one command to the standard input of another.
- With files, you can use **less than** `(<)` and **greater than** `(>)` signs to direct data to and from files. Here are the file-redirection characters

  - **`<`**  - Directs the contents of a file to the command. In most cases, this is the default action expected by the command and the use of the character is optional; using less bigfile is the same as less < bigfile.
 
  - **`>`**  - Directs the standard output of a command to a file. If the file exists, the content of that file is overwritten.

  - **`2>`** - Directs standard error (error messages) to the file.

  - **`&>`** - Directs both standard output and standard error to the file.

  - **`>>`** - Directs the output of a command to a file, adding the output to the end of the existing file.

### 🔹Using brace expansion characters
- By using curly braces `({})`, you can expand out a set of characters across `filenames`, `directory names`, or other arguments to which you give commands.

  - `touch memo{1,2,3,4,5}`
  - `ls`


  - `touch {John,Bill,Sally}-{Breakfast,Lunch,Dinner}`
  - `ls`
  - `rm -f {John,Bill,Sally}-{Breakfast,Lunch,Dinner}`
  - `touch {a..f}{1..5}`
  - `ls`


### 🔹Understanding File Permissions and Ownership
- After you’ve worked with Linux for a while, you are almost sure to get a **Permission denied** message. Permissions associated with files and directories in Linux were designed to keep users from accessing other users’ private files and to protect important system files.
- The nine bits assigned to each file for permissions define the access that you and others have to your file. Permission bits for a regular file appear as `-rwxrwxrwx`. Those bits are used to define who can read, write, or execute the file.
 


- **Note**
  - For a regular file, a dash appears in front of the nine-bit permissions indicator. Instead of a dash, you might see a 
    - `d` - (for a directory), 
    - `l` - (for a symbolic link), 
    - `b` - (for a block device), 
    - `c` - (for a character device), 
    - `s` - (for a socket),
    - `p` - (for a named pipe).

### 🔹Setting Read, Write, and Execute Permissions
  - **Read**  ◾️  View what’s in the file. See what files and subdirectories it contains.

  - **Write** ◾️  Change the file’s content, rename it, or delete it. Add files or subdirectories to the directory.Remove files or directories from the directory.

  - **Execute** ◾️  Run the file as a program. Change to the directory as the current directory, search through the directory, or execute a program from the directory. Access file metadata (file size, time stamps, and so on) of files in that directory.


### 🔹Changing permissions with chmod (numbers)
- If you own a file, you can use the chmod command to change the permission on it as you please. In one method of doing this, each permission (`read, write, and execute`) is assigned a 
  - number — 
    - r=4, 
    - w=2, and 
    - x=1
  - —and you use each set’s total number to establish the (ex8)


### 🔹Changing permissions with chmod (letters)
- You can also turn file permissions on and off using plus `(+)` and minus `(–)` signs, respectively, along with letters to indicate what changes and for whom. 
- Using letters, for each file you can change permission for the user `(u)`, group `(g)`, other `(o)`, and all users `(a)`.
- What you would change includes the read `(r)`, write `(w)`, and execute `(x)` bits. For example, start with a file that has all permissions open (rwxrwxrwx). Run the following chmod commands using minus sign options. The resulting permissions are shown to the right of each command.