# Lab5 Report

#### This lab was very interesting and important to me! It was a wonderful opportunity to work with `vim`!


### Part 1 – Debugging Scenario

#### Student:
Hi everyone, I'm having an issue with my Java program. I'm trying to run a script that compiles and runs a simple Java application, but I'm getting some unexpected behavior. When I run my bash script, it seems like the Java program isn't executing correctly. Here's a screenshot of the error I'm seeing:

SHOULD BE IMAGE
Error: Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 0 out of bounds for length 0

I'm guessing it has something to do with how I'm passing arguments to the Java program, but I'm not sure. The input to the bash script should trigger this issue.

#### TA:
Hi! It looks like the issue might be related to how the arguments are being handled in your Java program. Could you try running the Java program directly from the terminal with the same arguments you're using in the script? Also, please share the contents of your bash script and the command you're using to run it.

#### Student:
Thanks for the suggestion. Here's what I tried based on your advice. I ran the Java program directly with no arguments and got the following output:

!Image

It seems like the program is trying to access an array element that doesn't exist. Here's the relevant part of my code and the bash script:

!Image


Looka like the issue is with accessing args[0] without checking if any arguments were passed. What do you think?


#### TA:
Great, it looks like you've identified the problem. The issue is that your Java program is trying to access the first argument without checking if any arguments were passed. To fix this, you should add a check to ensure that args is not empty before accessing it. Here's how you can modify your MyProgram.java:

!Image

Try updating your code with this check and then run your script again.

#### Student:
Thanks, that worked! After adding the check, the program runs correctly whether or not arguments are provided. Here's the updated output:


And with an argument:
