# Week one and two lab report
[Index page link](https://abigailshilts.github.io/cse15l-lab-reports/)


## This report is covering remote access

### **Step 1:** Setting up VS code

>In order to set up VS code go to [this webpage](https://code.visualstudio.com/). Chose the version that corresponds to your computer OS and download.

![Image](/lib/vscode-download.png)

>After downloading open an editor:

![Image](/lib/vscode-window.png)

### **Step 2:** Connecting remotely

>First go to [this webpage](https://sdacs.ucsd.edu/~icc/index.php) to find your account. Once you know this you can use the ssh command in the terminal to access your account, it should look like "ssh (your account)" or:
![Image](/lib/ssh-command.png)
> When then prompted answer yes and enter your school password. Your terminal should now look like this:

![Image](/lib/logged-into-ssh.png)

> To exit server use ctrl-d

### **Step 3:** Trying some commands

> Type some commands into the terminal for the server and the client, some command include:
* cd (changes directory)
* ls (lists contents of current directory)
* ls -al (lists contents of current directy including hidden files with more specific data pertaining to each item)
* cp (copies an item)
* pwd (gives current location in file system)

> An example of ls -al:

![Image](/lib/ls-al.png)

> An example of using cd and pwd:

![Image](/lib/cd&pwd.png)

### **Step 4:** Moving files with scp

> This will use the scp command. Typed in the client it will look something like: scp (name of file to transfer) (ssh account). Example:![Image](/lib/scp-command.png) From there you xan re-log onto the server. If you use ls you will be able to see it in the files and you can even run javac and java on it in the server:

![Image](/lib/scp-fulluse.png)

