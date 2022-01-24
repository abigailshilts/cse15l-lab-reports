# Week one and two lab report
[Index page link](https://abigailshilts.github.io/cse15l-lab-reports/)


## This report is covering remote access

### **Step 1:** Setting up VS code

>In order to set up VS code go to [this webpage](https://code.visualstudio.com/). Chose the version that corresponds to your computer OS and download.

![Image](/lib/vscode-download.png)

>After downloading open an editor:

![Image](/lib/vscode-window.png)

### **Step 2:** Connecting remotely

>First go to [this webpage](https://sdacs.ucsd.edu/~icc/index.php) to find your account. Once you know this you can use the `ssh` command in the terminal to access your account, it should look like 

```ssh (your account)```
or:
![Image](/lib/ssh-command.png)
> When then prompted answer yes and enter your school password. Your terminal should now look like this:

![Image](/lib/logged-into-ssh.png)

> To exit server use `ctrl-d`

### **Step 3:** Trying some commands

> Type some commands into the terminal for the server and the client, some commands include:
* `cd` (changes directory)
* `ls` (lists contents of current directory)
* `ls -al` (lists contents of current directy including hidden files with more specific data pertaining to each item)
* `cp` (copies an item)
* `pwd` (gives current location in file system)

> An example of `ls -al`:

![Image](/lib/ls-al.png)

> An example of using `cd` and `pwd`:

![Image](/lib/cd&pwd.png)

### **Step 4:** Moving files with `scp`

> This will use the `scp` command. Typed in the client it will look something like:

```scp (name of file to transfer) (ssh account)```

 Example:![Image](/lib/scp-command.png) From there you can re-log onto the server. If you use `ls` you will be able to see it in the files and you can even run `javac` and `java` on it in the server:

![Image](/lib/scp-fulluse.png)

### **Step 5:** Setting up an SSH key

> In replace of your password you can use a private key housed on the client and a public one housed on the server. These keys are files created by the command `ssh-keygen`. The steps for this are as follows:

1. Run `ssh-keygen` in the client
2. Enter the path and file that you want the key saved to
3. Click the enter key to have no password

> An example of me making a dummy one since I already completed the steps:

![Image](/lib/ssh-keygen.png)

4. Log into the server and use the `mkdir` command to create a new directory .ssh
5. Log out of the server and use the `scp` command to copy the public key created in the previous steps into the .ssh directory it should look something like: 

```scp (file path and name) (account log in and location to copy to)```

 Example:

![Image](/lib/copying-in-key.png)
> Now you should be able to log into the server without a password like this:

![Image](/lib/server-log-in-nopw.png)

### **Step 6:** Optimizing remote running
> There are a number of techniques that can improve efficieny when working with a remote server and the terminal. For one, using a ; seperates commands on the same line allowing you to run multiple at once. By pairing "" with a command and an `ssh` log in you can run the command on the server and then exit back into the client. Additionally, the up and downarrows on your keyboard allow you to easily navigate between recently used command in the terminal. Example with 3 keystrokes (two up arrows and enter):

![Image](/lib/quick-commands.png)
