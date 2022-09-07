## 🔷 Using the Shell

- **Shell** - On UNIX systems, from which Linux was derived, the program used to inter-
pret and manage commands was referred to as the **shell**.

- **shell** provides 
  - a way to create executable script files, 
  - run programs, work with filesystems, 
  - compile computer code, and manage the computer.

    ### 🔹 Using the shell prompt
      - the default prompt for a regular user is simply a dollar sign: - **$**
      - The default prompt for the **root** user is a pound sign (also called a number sign or a hash tag): - **#**

    ### 🔹 Using Shell Variables
      
      - **Environment variables** are variables that are exported to any new shells opened from the current shell. Type env to see environment variables.
      
      - You can refer to the value of any of those variables by preceding it with a dollar sign `($)` and placing it anywhere on a command line. For example: -  ` echo $USER`


    ### 🔹 Command-line completion
      - To save you a few keystrokes, the bash shell offers several different ways of **completing partially typed values**. 
      
      - To attempt to complete a value, type the first few characters and press **Tab**. Here are some of the values you can type partially from a bash shell: 
        
        - **Command, alias, or function** 
          - If the text you type begins with regular characters, the shell tries to complete the text with a command, **alias**, or **function name**.
        
        - **Variable** 
          - If the text you type begins with a dollar sign `($)`, the shell completes the text with a variable from the current shell.
        
        - **Username** 
          - If the text you type begins with a tilde (~), the shell completes the text with a username. As a result, `~username` indicates the home directory of the named user.
        
        - **Hostname** 
          - If the text you type begins with the at symbol `(@)`, the shell completes the text with a hostname taken from the `/etc/hosts` file.
    ### 🔹Creating and using aliases
      - Using the alias command, you can effectively create a shortcut to any command and options that you want to run later.  
    












▪️▫️◽️⚫️🟢⚪️◼️◾️1️⃣2️⃣3️⃣4️⃣♾➖➕➗🔺🔸🔻🔹🔶🔷

                           ***⚪️**HOMEWORK**⚪️***

1. Create aliases that It should be executable after reopening
2. Using variables, find out **what your hostname**, **username**, **shell**, and home directories are currently set to.
3. Run the date command in such a way that the output from that command produces the current day, month, date, and year. Have that read into another command line, resulting in text that appears like the following (your date, of course, will be different): **Bugun Juma, Sentabrning 19-sanasi, 2022-yil**.
4. Create an alias called mypass that displays the contents of the `/etc/passwd` file on your screen in such a way that it is available every time you log in or open a new shell from your user account.