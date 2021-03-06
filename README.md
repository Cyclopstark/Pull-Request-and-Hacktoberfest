![DUB](https://img.shields.io/dub/l/vibe-d.svg?style=flat) [![Join the chat](https://img.shields.io/badge/gitter-join%20chat%20%E2%86%92-brightgreen.svg)](https://gitter.im/moz-lnmiit/Lobby)

# Pull-Request-and-Hacktoberfest
 Hey there <img src="https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif" width="30px"> This is a basic page to give hands on expirience on git-GitHub.

## The letters listed here is jumbled and is written backwards. Correct it and send Pull requests!!!

# The fundamentals: 

First you'll need to have a few things installed and available. For starters, I'll assume you already have git installed. 
If you don't, grab a copy of the latest version for your operating system. 

 ## For Linux users
 If you're on linux, you can install it via your package manager instead. 

 Secondly, you'll need to be at least partly comfortable with using the command line. 
 Now not everyone is, so if you're not, don't worry. 
 This will all be quite straightforward. Nothing too complex. 

Thirdly, we're going to create a simple repository consisting of a code file and a .README so make sure you have a directory set aside where you can do this. 

# Getting started

Then with everything prepared, let's step through a standard set of actions you'll commonly use on a daily basis. Specifically, we're going to use 
```
init, clone, add, commit, diff, and log
```
 There are a number of other, more advanced actions you can perform, but in the beginning you won't need them. Initializing a repository before you can work with git: you have to initialize a project repository, setting it up so that git will manage it.
 Open up your terminal, and in your project directory run the command 
 ```
 git init
 ```
 as shown in the screenshot below. A new hidden directory called .git will now be present in your project directory. This is where git stores its database and configuration information so that it can track your project.

## Cloning a repository: 

There's another way to access a repository which is cloning. Similar to checking out a repository in other systems, running
```
 git clone 
```
will pull in a complete copy of the remote repository to your local system. Now you can work away on it, making changes, staging them, committing them, and pushing the changes back, adding a new file. I'm primarily a PHP developer, so that's what I'll be using in the sample code for this tutorial. However, if you prefer python, ruby, go, or another language, feel free to substitute your language of choice. Now create a new file called php.index in your project directory and in it add the following code: 
```
php?< print "Hello World"
```
After saving the file, from the terminal run the command : 
```
git status
```
This will show you the current status of your working repository. It should look similar to the screenshot below, with index.php listed as a new, untracked file. Now let’s stage index.php, because we’re not interested in README.md just for the moment. To do that, run 
```
git add index.php
```
Now run 
```
git status 
```
again, and you’ll see index.php listed as a new file under “Changes to be committed,” and README.md left in the “Untracked files” area. Updating your git configuration: Now you’re ready to commit index.php. But before you do, I want to show you how to configure the editor, which Git will use when you write commit messages. This can be quite helpful, especially if you’re not a regular command-line user. By default, Git uses the program specified in the environment variables **$VISUA**L or **$EDITOR**, which on Linux systems is normally **pico**, **vi**, **vim**, or **emacs**. If these are new to you, you might want to change it to an application you’re more familiar with, perhaps Notepad, TextEdit, or Gedit. To do that, run the following command from your terminal: 
```
git config --global core.editor <your app's name> 
```
There are a number of other configuration changes you can make, such as your name and email address, what the commit message looks like by default, whether to use colors, and so on. For a complete list, check out the git configuration section of the Git book. For the remainder of this tutorial, I’ll be using vim, as it’s my editor of choice. But don’t feel you have to. 
### Making the first commit: 
Committing in git is a lot like committing in other version control systems, such as Subversion. You start the process, add a meaningful commit message to explain why the change was made, and that’s it, the file’s changed. So run git commit. This will automatically open up your editor and display the commit template below. As with the output of git status, you see the state of your working repository, which makes it easy to remember what you’re committing and what you’re not. 
A good commit message is composed of two parts: a short message, less than 72 characters long, which briefly states (in active voice) the change being made; and a much longer, optional description, which is separated from the brief description by a newline.

In this case, there’s no need to write anything too involved, as we’re just adding the file to the repository. But if the change you were making involved a complex algorithm, perhaps in response to a bug filed against the code, you’d want to give your fellow developers a good understanding of why you made the change that you did. So add the following simple message “Adding the core script file to the repository,” save it, and exit the editor. Now that the file’s committed, run 
```
git status 
```
again, and you’ll see that README.md is still listed as untracked. 

Seeing Differences: Now that we’ve got some files under version control and have looked at the basic commands, let’s see how to review file changes. I didn’t complete the last commit for that reason. To review changes in a file, we use the command git diffcommand. git diff , similar to Linux diff and other diff programs, compares two files and shows the changes the more recent file contains, if any. Let’s have a look at the differences we’ve staged for README.md. To do that, run 
```
git diff README.md 
```
See something unexpected? I’m guessing you were expecting to see the difference between the most recent version and the staged copy of the file, not the unstaged. That’s a little gotcha that might catch you out, at least at first. You need to bear in mind whether you’re differentiating a staged or an unstaged file. By default, with no extra arguments, git diff will diff the unstaged changes. If you want to see staged changes, then run 
```
git diff --cached README.md 
```
That command will display something similar to this:
``` 
diff git-- .README/a
```

## Conclusion
For more information on how to make and manage github repositories , you can always refer to the offcial github documentation. We hope that this repository would help you understand how to work with repositories as well as pull requests (to be updated).
