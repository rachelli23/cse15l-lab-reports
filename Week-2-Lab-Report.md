# Week 2 Lab Report by Rachelle Kanounji

### Installing VScode
Before you start anything, you must download Visual Studios on your computer, which you can go on [Visual Studio code website](https://code.visualstudio.com/) and download the version you need. The image below is what Visual Studios Code looks like successfully downloaded. 
 ![Image of VSCode](Screen%20Shot%202022-04-01%20at%202.16.41%20PM.png)

### Remotely Connecting
1. Write in the terminal $ ssh <course specific account>@ieng6.ucsd.edu
2. Type in yes, if you recieved messages and give password when asked 
 You should see something like this in your terminal ![image for part 2](part2.png)


### Trying Some Commands
      
Now try some commands in your terminal. I tried ls which lists all the files in the current directory. The image shows running the command ls my terminal ![image for part 2](part2.png)


### Moving Files with scp
In order to copy a file or files, we must use the command scp. We will run it on our computer (the client) and we will always run it from the client. 
1. First step is to create a new file called WhereAmI.Java 
      In this file, you will have the following contents in it: 
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}

2. Now in terminal write javac WhereAmI.java (press enter) and then write java WhereAmI to run it 
3. After compiling it and running, write this in your terminal scp WhereAmI.java cs15lsp22agk@ieng6.ucsd.edu:~/ (remember to replace before the @ symbol with your course-specific account. 
4. Now you should see it asking for your password (write your password) then go to/log into ieng6 (the server) with ssh again and use ls. You should view the file that you created in the home directory. 
5. Once you see it in you home directory, you can run it using javac and java like in step 2 (above) on the ieng6 (the server the CSE basement computer)

The following image is what your terminal should look like successfully using ssh ![image for part 5a](part6a.png)

The following image is what your terminal should look like successfully using scp ![image for part 5b](part6.png)

### Setting an SSH Key
To fix wasting time on entering your password everytime, we will be using ssh keys. 
1. Go to your computer's (the client) terminal and run $ ssh-keygen and press enter until you see "Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa" here for username you will add the username from your computer. Then continue to press enter (do not type anything) and you should see the key's randomart image in your terminal. 
2.  Now you need to copy the public key to the .ssh directory of your user account on the server.






