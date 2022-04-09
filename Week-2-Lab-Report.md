# Week 2 Lab Report by Rachelle Kanounji

### Installing VScode
Before you start anything, you must download Visual Studios on your computer. 

1. First go to to the [Visual Studio code website](https://code.visualstudio.com/) and then install the version you have for your computer. I downloaded and installed the one for mac.
2. Once it successfully installs you should see something like this ![Image of VSCode](Screen%20Shot%202022-04-01%20at%202.16.41%20PM.png)
3. Once you see this image you successfully downloaded Visual Studios Code and you can now start! 

### Remotely Connecting
The next step is connceting our computer/machine to a remote computer over the Internet.  
1. First step is getting your course-specific account for CSE15L here: [your specific account](https://sdacs.ucsd.edu/~icc/index.php) 
2. After you have your course-specific account, you are going to open up terminal in Visual Studio Code 
3. The command that you will write in the terminal should look like this: $ ssh cs15lsp22agk@ieng6.ucsd.edu Replace right before the @ symbol with your course-specific account
4. Once you press enter, you may be receiving messages (if it's your first time), type in yes and press enter then give your password. You should see something like this in your terminal ![image for part 2](part2.png)
5. Your computer is now connected to another computer in the CSE basement. Meaning anything you run/write a command in the terminal will run on the other computer. Your computer is the client while the other computer in the CSE basement is the server. 

### Trying Some Commands
Now try some commands in your terminal. 
 * cd (Changes directory, meaning it will change the directory to the specific input you give)
 * ls (This lists all the files in the current directory)
 * Cd ~ (Similar to cd it changes the current directory to main)
 * mkdir (Creates a new directory with a name you give) 
 * Cat (Concatenate files, creates multiple or single files, lets you view whats on the file, and redirects the output to the terminal or to files)
 * rm -r (Removes a directory, you have to put the name of the directory you want to remove after the "-r" with a space in between) 
 * exit (Terminates session)

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

The following image is what your terminal should look like successfully using ssh ![image for part 6a](part6a.png)

The following image is what your terminal should look like successfully using scp ![image for part 6b](part6.png)



