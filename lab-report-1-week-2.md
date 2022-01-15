1. Setting up Visual Studio Code:
   - I already had VSCode installed from previous classes but if need be, it can be downloaded from : https://code.visualstudio.com/ for Windows or OSX(Mac)
   - Once downloaded, open the VSCode window
   - It will look something like this
   
      ![image](https://user-images.githubusercontent.com/97641897/149424347-a3918030-49b1-4ea8-bcbb-5cacd6e48a77.png)
 
 2. Remotely Connecting :
    - Install OpenSSH for Windows laptop
    - Open a terminal in VSCode and input the command $ ssh cs15lwi22zz@ieng6.ucsd.edu with zz replaced with the letters in course specific account. 
    - It will then show you a message confirming if you wish to continue connecting. 
    - After saying yes, it will ask for your password. 
    - After all the steps it will look like this in the terminal

        ![image](https://user-images.githubusercontent.com/97641897/149426038-a5de1d38-6fcf-4554-bd13-2a83fba76172.png)

3. Trying some commands : 
    - type some commands in terminal to test on remote server 
    - Examples of few to try : cd, ls, ls-lat, ls-a
    - Output of ls -a and ls -a on my terminal shown below
    
      ![image](https://user-images.githubusercontent.com/97641897/149426825-fc7f8023-2d88-4e12-8c97-db3a56e02c23.png)

4. Moving files with scp
    - Create a file WhereAmI.java on your computer and run it on the terminal using javac and java
    - Next, run this command scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/ on the terminal
    - When prompted for password, enter the same password
    - This copies the file from the client to the server
    - Now log into your remote server using ssh and then run the same commands in the terminal
    - The output of the whole process is shown below

      ![image](https://user-images.githubusercontent.com/97641897/149428043-66a3c22d-aad5-4cfc-8668-1809b1848e8d.png)
      
5. Setting an SSH Key
    - https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation using instructions from here set up the SSH key
    - Then copy the public key file to the directory of user account on server
    - Do this by following commands
    - $ ssh cs15lwi22zz@ieng6.ucsd.edu and $ scp /Users/username/.ssh/id_rsa.pub cs15lwi22@ieng6.ucsd.edu:C:\Users\username/.ssh/authorized_keys 
    - After this you will be able to use ssh and scp commands without being asked for password.

   ![image](https://user-images.githubusercontent.com/97641897/149431993-01c50847-77f8-4e1f-b04b-3b4e029314d6.png)
   ![image](https://user-images.githubusercontent.com/97641897/149600016-62e3911a-f5f2-446c-b05e-902693af1645.png)
   
6. Optimizing remote running
    - We can combine all of the commands into one on both the local machine and the server as such:
    - scp WhereAmI.java cs15lwi22ain@ieng6.ucsd.edu:~/; ssh cs15lwi22ain@ieng6.ucsd.edu "javac WhereAmI.java && java WhereAmI"
    
    




