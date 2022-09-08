## 🔷 Linux File System

- **The Linux filesystem** - is the structure in which all of the information on your computer is stored. In fact, one of the defining properties of the UNIX systems on which Linux is based is that nearly everything you need to identify on your system (`data`, `commands`, `symbolic links`, `devices`, and `directories`) is represented by items in the filesystems.

- **In Linux**, files are organized within a **hierarchy** of directories. Each directory can contain files as well as other directories. You can refer to any file or directory using either 
  - a **full path** (for example, `/home/joe/myfile.txt`) or 
  - a **relative path** (for example, if` /home/joe` were your current directory, you could simply refer to the file as `myfile.txt`).

- If you were to map out the files and directories in Linux, it would look like an **upside-down** tree. At the top is the `root` directory (not to be confused with the root user), which is represented by a single slash `(/)`. 
- Below that is a set of common directories in the Linux system, such as `bin`, `dev`, `home`, `lib`, and `tmp`, to `name` a `few`. 
- Each of those directories, as well as directories added to the `root` directory, can contain subdirectories.

**The Linux filesystem is organized as a hierarchy of directories.**
        ![](./../img/1.linux-file.png)

    ### 🔹 Using the shell prompt
      - the default prompt for a regular user is simply a dollar sign: - **$**
      - The default prompt for the **root** user is a pound sign (also called a number sign or a hash tag): - **#**

    ### 🔹 Using Shell Variables
      
      - **Environment variables** are variables that are exported to any new shells opened from the current shell. Type env to see environment variables.
      
      - You can refer to the value of any of those variables by preceding it with a dollar sign `($)` and placing it anywhere on a command line. For example: -  ` echo $USER` 