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
function add(a, b) {
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
[https://github.com/signup](https://github.com/signup) and create a new account with your school or personal
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

### Task 01.03 - Git clone
Git has a copy of the code history on each person's computer so you can work offline and combine your changes later. Github acts like a special computer that you can combine your changes with using Pull Requests. You can also make a copy of the code history from Github using `git clone`.

This task is complete when you have run `git clone https://github.com/frc-8234-panthinators/2027-training.git` to make a copy of the training on your computer

### Task 01.04 - Git branches
Git allows multiple branches so that you can work on multiple things at the same time without needing to constantly combine your changes with everyone else.
You can also have different versions of the code for experimenting, or even multiple versions with different features. For our team we will
have the main code running on the robot in the `main` branch and individual people's work on `<name>-<description>` branches like `travis-tracking`

This task is complete when you have run `git branch <yourname>-tracking` to create your own branch for tracking your progress and `git switch <yourname>-tracking` to use that branch on your computer

### Task 01.05 - Git Commits
Git commits use a two-step process: First you "stage" your changes and then once everything is staged and ready you "commit" the change. You
can stage your changes in VSCode or on the command line with `git add <file>` and then commit them in VSCode or on the command line with `git commit -m "<description>"` like `git commit -m "Update tasks for 09/12/26"`

This task is complete when you have made a copy of `github/travis.md` named for yourself instead of "travis", staged the file, and committed your change on your computer.

### Task 01.06 - Git Push
Git lets you send changes to a server using `git push`. You can also push changes using VSCode. Github accepts pushes from your computer when you are logged in to github correctly. On the team you should always push changes to your own branch and not `main` so that you can use a pull request and have
someone else check that your changes are right.

This task is complete when you've pushed your tracking branch to Github

### Task 01.07 - Github Pull Request
Github merges changes for you using pull requests. Pull requests let you see the changes on the website, comment on changes, and approve or reject changes. Github will usually show a banner right after you push a change that lets you open a pull request, or you can create one from the pull requests tab

This task is complete when you've opened a pull request from your branch to `main`

### Task 01.08 - Making More Changes
You can keep using a branch to make more changes or create a fresh one for each pull request. I recommend using a fresh branch so that you don't 
need to keep your branch up to date with other changes to `main`. 

This task is complete when you have updated your tracking file to mark the previous tasks as complete by putting an 'x' in the boxes like `[x]`, 
committed the change, pushed the branch to github, created a Pull Request (PR) and merged the Pull Request

## Unit 02 - Robotics Coding
If you are not familiar with Java, go check out [RESOURCES.md](RESOURCES.md) and follow the java resources before continuing.

### Task 02.01 - WPIlib
Read the WPILib zero to robot tutorial at https://docs.wpilib.org/en/stable/docs/zero-to-robot/introduction.html so you understand the basics of how robots are set up to run using WPILib

### Task 02.02 - Command Robot
We will do mostly command-based control of the robot. Read the wpilib documentation about commands https://docs.wpilib.org/en/stable/docs/software/commandbased/commands.html

### Task 02.03 - Mechanisms
We will use YAMS to help set up our subsystems so that it is easier to configure and simulate the motors correctly. Read the documentation at https://yams.yassrobotics.com/documentation/why-yams

### Task 02.04 - Swerve Drive
We will use YAGSL to help set up the swerve drive. YAGSL uses YAMS but lets you configure the drive using JSON files

## Unit 03 - Example Robot
The goal of this unit is to learn by coding for a fake robot with some common mechanisms.

### Task 03.01 - New Repository
ALL OF THE CODE IN THIS UNIT WILL BE SAVED IN https://github.com/frc-8234-panthinators/2027-Training-ExampleBot

First, make sure you have the 2026 version of WPILib installed from https://github.com/wpilibsuite/allwpilib/releases/tag/v2026.2.1
Then, create a new command robot project and run `git init` to initialize the repository and then `git remote add origin https://github.com/frc-8234-panthinators/2027-Training-ExampleBot.git` to link your local repository to the GitHub. Finally, make your own branch with `git switch --create <yourname>-main` and push it with `git push origin --set-upstream <yourname>-main`

This task is complete when you've successfully pushed your branch to GitHub

### Task 03.02 - Subsystems
Each mechanism of the robot will have a subsystem in the code to control it in the `src/main/java/frc/robot/subsystems` folder. For some examples
look at https://github.com/Yet-Another-Software-Suite/YAMS/blob/master/examples/hooded_shooter/java/frc/robot/subsystems/FlywheelSubsystem.java

Our example robot will have the following subsystems:
* Drivetrain - Swerve drive, reused design from the 2026 robot
* Flywheel - Single flywheel shooter that launches foam dodgeballs toward a basket
* Shooter Feeder - Single motor belt mechanism that feeds balls into the flywheel when it is spinning fast enough to make a basket
* Intake - Single motor mechanism that pulls dodgeballs into the robot so they can be launched later

This task is complete when you have created all 4 Subsystem classes extending `SubsystemBase` in the subsystems folder and pushed your changes to Github

### Task 03.03 - Configure the Swerve Drive
We will do swerve the "hard" way (not really) by configuring it in the code rather than using YAGSL to load JSON files.
Take a look at https://github.com/Yet-Another-Software-Suite/YAMS/blob/master/examples/swerve_drive/java/frc/robot/subsystems/SwerveSubsystem.java 
to see how this works, and then configure your swerve subsystem based on the config in 
https://github.com/frc-8234-panthinators/2027-Redux-Rewrite/tree/main/src/main/deploy/swerve

This task is complete when you have configured your swerve subsystem and pushed your changes to Github

### Task 03.04 - Configure the Flywheel
The flywheel is powered by a single Kraken x60 motor. The target speed is 4000 RPM when active

Look at https://github.com/Yet-Another-Software-Suite/YAMS/blob/master/examples/hooded_shooter/java/frc/robot/subsystems/FlywheelSubsystem.java as an example 
and set up the flywheel subsystem to control a single Kraken x60 motor with closed loop PID control,
not inverted, and 40A of current limit. You do not need to configure the simulation settings

This task is complete when you have configured your Flywheel subsystem and pushed your changes to Github

### Task 03.05 - Configure the Feeder
The feeder is powered by a single Kraken x44 motor. The target speed is 6500 RPM when active and geared with a 5-to-1 planetary gearbox 
to reduce the motor speed while increasing torque

Look at https://github.com/Yet-Another-Software-Suite/YAMS/blob/master/examples/hooded_shooter/java/frc/robot/subsystems/FlywheelSubsystem.java as an example 
and set up the flywheel subsystem to control a single Kraken x44 motor with closed loop PID control,
not inverted, 5:1 gearing, and 30A of current limit. You do not need to configure the simulation settings

This task is complete when you have configured your Feeder subsystem and pushed your changes to Github


### Task 03.06 - Configure the Intake
The feeder is powered by a single Kraken x44 motor. The target speed is 7500 RPM when active

Look at https://github.com/Yet-Another-Software-Suite/YAMS/blob/master/examples/hooded_shooter/java/frc/robot/subsystems/FlywheelSubsystem.java as an example 
and set up the flywheel subsystem to control a single Kraken x44 motor with closed loop PID control,
inverted, and 30A of current limit. You do not need to configure the simulation settings

This task is complete when you have configured your Intake subsystem and pushed your changes to Github

### Task 03.07 - Configure the Controller
Now that your subsystems are set up you can control them using commands. For this training we will use the following Xbox control scheme:
* Left Trigger - Enable Flywheel
* Right Trigger - Feed ball if and only if flywheel is at target speed
* X button - Run Intake
* Left Stick - Move robot in translation
* Right Stick X - Rotate robot

First, you should create the XBoxContainer to handle setting up the Xbox controls and triggers. See the example from last year https://github.com/frc-8234-panthinators/2026-Robot-Code/blob/main/src/main/java/frc/robot/XBoxContainer.java

This task is complete when you've created the XBoxContainer class, set up named Trigger member variables for the Flywheel, Feeder, and Intake, 
and added driveX, driveY, and rotate methods that get the joystick values.

### Task 03.08 - Configure the Commands for Triggers
With a controller and all of the subsystems set up you can make the controls run commands.

Look at https://github.com/frc-8234-panthinators/2026-Robot-Code/blob/main/src/main/java/frc/robot/RobotContainer.java for an example of running
commands based on triggers and set them up in your RobotContainer for the Flywheel, Feeder, and Intake

This task is complete when the bindings are configured for the Flywheel, Feeder, and Intake and you've pushed your changes to Github

### Task 03.09 - Configure the Drive Command
The last step is to set up the drive system to follow the joystick inputs. Look at https://github.com/frc-8234-panthinators/2026-Robot-Code/blob/5358f7a65eda04053c1dda1ab45d984d22cffd0f/src/main/java/frc/robot/Robot.java#L187 as an example and configure your robot code
to work as described in 03.07

This task is complete when you have configured the drive controls and you've pushed your changes to Github
