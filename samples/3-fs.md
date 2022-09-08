




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
        apple
  - `ls g*`
        grape grapefruit
  - `ls g*t`
        grapefruit
  - `ls *e*`
        apple grape grapefruit watermelon
  - `ls *n*`
        banana watermelon