




2. example 

   - `cd /usr/share/`
   - `pwd`
       
           /usr/share

   - `cd doc`
   - `pwd`

           /usr/share/doc

   - `cd`
   - `pwd`

         /home/chris

    **Note:** - The `/usr/share` option represents the absolute path to a directory on the system. Because it begins with a slash `(/)`, this path tells the shell to start at the root of the filesystem and take you to the share directory that exists in the usr directory. The doc option to the `cd` command looks for a directory called doc that is relative to the current directory. So that command made `/usr/share/doc` your current directory.


3. example

   -  `cd ~`
   -  `pwd`

           home/cloud_user

   -  `cd ~/Music`
   -  `pwd`
   -  
           home/cloud_user/Music

   -  `cd ../../../usr`
   -  `pwd`


4. example
- Try out some of these file-matching metacharacters by first going to an empty directory (such as the test directory described in the previous section) and creating some empty files:
  
   - `touch apple banana grape grapefruit watermelon`

- The touch command creates empty files. The commands that follow show you how to use shell metacharacters with the ls command to match filenames. Try the following commands to see whether you get the same responses:
    - `ls a*`
    - 
          apple

    - `ls g*`

          grape grapefruit

    - `ls g*t`

          grapefruit

    - `ls *e*`
    - 
          apple grape grapefruit watermelon

    - `ls *n*`
    - 
          banana watermelon


5. example
- Here are a few examples of pattern matching with the question mark `(?)`:

    - `ls ????e`

          apple grape

    - `ls g???e*`

          grape grapefruit

6. example
- The following examples use braces to do pattern matching:
  
  - `ls [abw]*`
  
         apple banana watermelon
  
  - `ls [agw]*[ne]`

         apple grape watermelon
            
7. examplee
- The following are some examples of command lines where information is directed to and from files:
- 
  - `cat /var/log/auth.log | grep "12:17:01" > demo.txt`

  - `more demo.txt`
   
  - `echo "I finished the project on $(date)" >> ~/projects`

8. example
- The following chmod command results in this permission: rwxrwxrwx

  - `chmod 777 file`
        
        The following chmod command results in this permission: rwxr-xr-x

  - `chmod 755 file`

        The following chmod command results in this permission: rw-r--r--

  - `chmod 644 file`

        The following chmod command results in this permission: ---------

  - `chmod 000 file`
  
            The chmod command also can be used recursively. For example, suppose that you wanted to give an entire directory structure 755 permission `(rwxr-xr-x)`, starting at the `$HOME/ myapps` directory. To do that, you could use the `-R` option, as follows:

  - `chmod -R 755 $HOME/myapps`


9. example

       The following chmod command results in this permission: r-xr-xr-x

  - `chmod a-w file`
        
        The following chmod command results in this permission: rwxrwxrw-

  - `chmod o-x file`
    
        The following chmod command results in this permission: rwx------

  - `chmod go-rwx file`

        Likewise, the following examples start with all permissions closed (---------). The plus sign is used with chmod to turn permissions on.

        The following chmod command results in this permission: rw-------

  - `chmod u+rw files`
        
        The following chmod command results in this permission: --x--x--x

  - `chmod a+x files`
        
        The following chmod command results in this permission: r-xr-x---

  - `chmod ug+rx files`

   - Using letters to change permission recursively with chmod generally works better than using numbers because you can change bits selectively instead of changing all permission bits at once. 

   - For example, suppose that you want to remove write permission for “other” without changing any other permission bits on a set of files and directories. You could do the following:
  
  - `chmod -R o-w $HOME/myapps`
  
  - This example recursively removes write permissions for “other” on any files and directories below the myapps directory. 
  - If you had used numbers such as 644, execute permission would be turned off for directories; using 755, execute permission would be turned on for regular files. Using o-w, only one bit is turned off and all other bits are left alone.