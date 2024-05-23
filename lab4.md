# Lab4 Report

#### This lab was very interesting and important to me! It was a wonderful opportunity to work with `vim`!


### Log into ieng6

![Image]()

#### Keys pressed:
  
  `ssh<space>iangel@ieng6.ucsd.edu<enter>`

#### Summary:

This command logs you into the ieng6 server.


### Clone the Repository

![Image]()

#### Keys pressed:

  `git<space>clone<space>git@github.com:iangel11/lab7.git<enter>` This command clones the forked repo of week 7 lab.
  
  `cd<space>lab7<enter>` This command changes the directory to lab7.

#### Summary: 

These commands clones your fork of the repository and changes the directory to the cloned repository.


### Run the Tests

![Image]()

#### Keys pressed:

  `javac<space>-cp<space>.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar<space>*.java<enter>`

  `java<space>-cp<space>.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar<space>org.junit.runner.JUnitCore<space>ListExamplesTests<enter>`

#### Summary: 

These commands compile the Java files and run the JUnit tests, demonstrating their failure.



### Edit the Code with Vim to Fix the Failing Test

![Image]()

#### Keys pressed:

  `vim<space>ListExamples.java<enter>`
  `/index1<enter>`
  `n
   n
   n
   n
   n
   n
   n
   n
   n`
  `i`
  `<right><right><right><right><right><right><backspace>2`
  `<esc>`
  `:wc`

#### Summary: 

`vim ListExamples.java<enter>`: Opens the file in Vim.
`/index1<enter>`: Searches for the term "index1".
`n`: Finds the next occurrence (did it 9 times to get to the desired index1).
`i`: Enters the text editor in Vim.
`<right>`: Moves cursor to the right once in the editor (done 6 times to get to the number `1`).
`<backspace>`: To delete `1` from index and then `2` to change from the blank.
`<esc>`: To quit text editor.
`:wc`: Saves and quits Vim.


### Re-run the Tests

![Image]()

#### Keys pressed:

  `<up><up><up><up><enter>`
  `<up><up><up><up><enter>`

#### Summary:

`<up><up><up><up><enter>`: Runs the previous javac command from history.
`<up><up><up><up><enter>`: Runs the previous java command from history.




