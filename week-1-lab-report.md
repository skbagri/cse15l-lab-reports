# Week 1 Lab Report
## 1. Installing VScode  
* Follow the instructions on the Visual Studio Code website to dowload and install VS Code on your device.
* Once it is installed, open it up. You should see something like this.  
![Image](vscode.png)

## 2. Remotely Connecting  
* Now, we are going to connect to the remote computer. To do this, open a new terminal in VS Code and type in *ssh cs15lfa22zz@ieng6.ucsd.edu* but replace the zz with your own account letters.
* Enter the password and you are connected. Your computer is the client and then computer in the CSE basement is the server. You may see this.  
![Image](remotestep.png)

## 3. Trying Some Commands
* There are multiple commands you can try to run now.
* Try them both on your computer and on the remote computer after ssh-ing. Here is a screenshot.  
![Image](commands.png)
## 4. Moving Files with scp
* scp allows you to copy files from your computer to a remote computer. It is run from the client. First compile and run the file with javac and java.
* In the terminal where the file is made, run *scp filename.java cs15lfa22zz@ieng6.ucsd.edu:~/* and enter the password.
* Log into ieng6 with ssh and use ls. Run the program on the ieng6 computer, again using javac and java. The terminals should look like this.  
![Image](move1.png)  
![Image](move2.png)

## 5. Setting an SSH Key
* Next, we will use ssh keys to create a public and private key by running *ssh-keygen -t ed25519*.
* Follow the prompts and then copy the public key to the .ssh directory of the user account on the server. Here is an example.  


## 6. Optimizing Remote Running
* 
*   