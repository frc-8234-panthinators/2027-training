# 2027-training
Code training for 2026-27 season. This training is organized into units with activities
and links to other training resources. We won't be using AI for coding in this training 
because it [negatively impacts learning](https://arxiv.org/pdf/2605.21629v1),
and learning how to write, debug, and improve code is a valuable part of robotics and
the whole point of this training.

### Before You Start
People have a lot of opinions on the best software, the best code, the best coding language, and just
about everything else in coding (and in life). In this training, we will make a lot of choices so that
everyone is doing the same thing and can help each other out. For example, the training is written in 
__Markdown__ which is a type of code that lets you format text and can be viewed in your web browser on Github.
This works well for showing example code and commands, which you will use in the training. Here is some code:
```javascript
fun add(a, b) {
  return a + b;
}
```
There should be a button on the top right corner of the code with 2 squares that lets you copy the code
and paste it somewhere else. Markdown also allows _italics_, __bold__, and `code` mixed in with other text.

## Unit 00 - Computer Stuff
We will use several programs for robotics. The main one during the season is the WPILib version of vscode
with special robotics plugins to help write code and run it on the robot. There are also programs to
simulate the robot and game field so that we can start working on the code before the robot is built and 
test changes without needing a robot and space to drive. In this training we will use vscode and git.

You will be typing a lot as part of coding, so if you don't know how to touch-type (type without looking at the keyboard)
it is a good idea to start practicing. You will also need to use the terminal to run some programs instead of the program
opening a window that you can use your mouse with. On windows there is the `cmd` program, sometimes called command prompt, and `powershell`

## Unit 01 - Github introduction
You're probably reading this on the github website right now. Github lets us
work together on code and share code with other teams and people. The team
has an organization (frc-8234-panthinators) that is used to help keep track of everyone's accounts and
protect our projects from vandalism.

### Task 01.01 - Set up Github account
Github requires an account before you can do a lot of things. If you already have an account you should
log in now. If you don't have an account you should go to the sign up page at
(https://github.com/signup)[https://github.com/signup] and create a new account with your school or personal
email and a strong password. I don't think the "Continue with Google" option works with school emails. Once
you are able to log in you should let a mentor know and we will add your account to the organization.

This task is complete when you've been added to the github organization

### Task 01.02 - Git basics
Github makes it easier to work together while using Git. Git is a "version control system" that helps
keep track of changes to code. Three important concepts are Commits, Branches, and Repositories:
* Commits are used to save a version of the code. Every commit has one parent commit except for the special first commit
* Branches are used to keep track of the newest commit so that people can work together. Because each commit has a parent, each branch has a history from the newest commit back to the special first commit
* Repositories are used to keep track of history for some code and have at least 1 main branch. All of the branches in a repository have the same special first commit

This task is complete when you are able to run `git --version` on your computer in the Git shell, command prompt, or Powershell and it outputs
the version of git installed on the computer
