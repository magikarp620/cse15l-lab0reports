## lab report-1-week-2
# VisualStudioCode MacOS Install Tutorial  
1. Click [here](https://code.visualstudio.com/download) to download VSCode
2. Double Click VSCode in download(top right corner for Safari Users) to activate package  
![Image](https://user-images.githubusercontent.com/98373624/162593115-966351c6-ba5a-406c-80cb-974580ac371f.png)
3. Drag the file to application folder
4. Double click on VSCode Icon to launch the application
5. The welcome page should look similar to this
![Image](https://user-images.githubusercontent.com/98373624/162593354-53568e58-6452-4157-9398-4c33e062e3da.png)
---
# Remotely Connecting
1. Click [here](https://sdacs.ucsd.edu/~icc/index.php) to check your account for connecting
2. Your account name should begin with cs15lsp22
![Step4](https://user-images.githubusercontent.com/98373624/162593767-f95c8535-4a22-4b75-b906-58dd42c5568e.png)
3. Go back to VSCode and Open a new terminal from the toolbar(top-left)
![Step3](https://user-images.githubusercontent.com/98373624/162593644-6e7dd03d-36c1-4fe1-b17f-dbd4880b284f.png)
4. After loading there should be name of computer and your user name follow by $  
type `ssh [YourAccount]@ieng6@ucsd.edu`
![step5](https://user-images.githubusercontent.com/98373624/162593983-06ea65c1-10b2-4cbf-9745-439466bfd6c2.png)
5. For first-time login type **yes** when asked "Are you sure you want to continue connecting?"
6. Enter Your Password to connect to the server
Successful login should look like this
![step6](https://user-images.githubusercontent.com/98373624/162594082-fce3c48d-9f82-4c66-a096-45fb6e9b05c9.png)
---
# Trying Some Commands
After a successful connection to the server we can try out some terminal commands  
Check out the [link](https://dev.to/kymiddleton/reference-guide-common-commands-for-terminal-6no) for some useful commands  
![step7](https://user-images.githubusercontent.com/98373624/162594373-9c446423-da15-47e1-b22c-74ca12cc19b9.png)
Play around with the commands!
---
# Moving files with csp
1. Create a file on your computer
2. Run and Compile the file(javac & java)  
![step9](https://user-images.githubusercontent.com/98373624/162595503-201dab1f-fb20-4ee7-89a2-f74af45677f4.png)
![step8](https://user-images.githubusercontent.com/98373624/162595510-6ab56592-e57f-43ce-b1cd-53498b93e572.png)
3. Type the following command to move file to server  
scp **[FileName]** **[AccountName]@ieng6.ucsd.edu:~/**
![step10](https://user-images.githubusercontent.com/98373624/162595774-b4b339d0-a9ce-4b29-9bd3-1f2d143f66b1.png)
4. Using the ls command we can see the file is moved to our server account
![step11](https://user-images.githubusercontent.com/98373624/162595778-710d95f3-5a49-41ec-a20c-c04a2c8e6e12.png)
---
# Setting an SSH Key
To avoid typing password everytime you login, we use a program called ssh-keygen, it's like the "Remember Me" button on many websites
1. type `$ ssh-keygen`(On client/Your Computer)
2. Press Enter for Empty Passphrase
3. The program generates a pair of key, you should see this message  
![step12](https://user-images.githubusercontent.com/98373624/162596264-5add05e5-e82e-45dd-ae9e-5761bb6fc195.png)
4. Log on to the server and create a directory called .ssh by typing `$ mkdir .ssh` 
5. log out and move the file to the directory we just created by typing 
```
$ scp /Users/<user-name>/.ssh/id_rsa.pub
cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys 
```
6. You Should be able to login to remote server without Password from now!
---
# Optimizing Remote Running
Even without the password it is a bit annoying to log in and out
Here is some tips
* Write a command in quotes at the end of an ssh command to directly run it on the remote server, then exit. For example, this command will log in and list the home directory on the remote server:
`$ ssh cs15lsp22aqm@ieng6.ucsd.edu "ls"`
This line of code is significantly shorter than 
```
$ssh cs15lsp22zz@ieng6.ucsd.edu
Password:         
$ls
$exit
```
Here are the comparison between the actual process  
Before Optimizing(with genkey set up)  
![Screen Shot 2022-04-27 at 11 17 15 PM](https://user-images.githubusercontent.com/98373624/165689409-c0d630c5-41ad-419e-9af5-27eefb19b360.png)  
After Optimizing(run program on client)  
![Screen Shot 2022-04-27 at 11 16 41 PM](https://user-images.githubusercontent.com/98373624/165689417-2450c553-9fc2-40b3-9242-e7c8ea6a202e.png)  

April 9th, 2022
Roger Lin





