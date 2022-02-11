# Group Choice 3 : Copy Whole Directory with scp -r

1) Copying whole markdown-parse directory to ieng6 account:
 - We can use scp command to copy the whole directory to the remote server.
 - the -r tells scp to work recursively meaning it will copy a directory and all the files and directories within it, and all the files and directories within those, and so on.
 - If we do this, then we can log into the server with ssh and see all of our files there in a directory called markdown-parse.
 - `scp -r *.java *.md lib/ cs15lwi22@ieng6.ucsd.edu:markdown-parse` this command gives more control as to what gets copied.

![image](https://user-images.githubusercontent.com/97641897/153657624-c2b92af3-81d2-4d12-9d80-1ee459ef7037.png)

2) Compiling and Running the tests:
 - We can now log in using ssh and run the tests for the repo using javac and java commands on the remote server.

![image](https://user-images.githubusercontent.com/97641897/153672811-442db9db-b794-4b66-8c53-766abfac2c1a.png)

3) Combining commands in one line :
 - The command line below copies the whole directory and compiles and runs the tests in one single command line making it faster and efficient.

![image](https://user-images.githubusercontent.com/97641897/153674153-1cb765c4-d6e1-47bb-886a-6858c65481a2.png)
