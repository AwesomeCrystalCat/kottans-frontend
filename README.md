# kottans-frontend
cool comunity tasks


# Using Git and GitHub (Udacity course reflections)

Git is a simple to use version control system that allows to follow the workflow and control the history of file. Here are some questions that were uncovered in Udacity course.

<h5>Lesson 1</h5>

1. How did viewing a diff between two versions of a file help you see the bug that was introduced?

Console shows which lines were changed in newer version comparing to older one. By '-' sign console shows which line was deleted and '+' stands for added line.

2. How could having easy access to the entire history of a file make you a more efficient programmer in the long term?

It helps to control workflow and versions of a file. History help to find the exact version of the file in a short priod of time.

3. What do you think are the pros and cons of manually choosing when to create a commit, like you do in Git, vs having versions automatically saved, like Google docs does?

Pros of commit:
- you can break the entire workflow on convinient chunks;
- you have easy and quik access to the workflow;
- you can do back-up to the previous version anytime you want;
- every member of your team can also see all the changes.

    Cons of commit:
- if you won't log your changes they can dissappear in some extra cases (like electricity breakdown);

4. Why do you think some version control systems, like Git, allow saving multiple files in one commit, while others, like Google Docs, treat each file separately?

Because programming for example usualy containes many file to work with. And in one commit you can make many changes with many files that are connected to each other. So it's a good way to commit few file in single commit. By the way, you can choose wich files to commit and which don't.

5. How can you use the commands git log and git diff to view the history of files?

Git log displays a set of revisions, so you can see how file was changed during the workflow. Git diff gives an exact information what is the difference between two chosen versions.

6. How might using version control make you more confident to make changes that could break something?

You can always make a chekcout if something went wrong.

7. Now that you have your workspace set up, what do you want to try using Git for?

To commit changes to the file and save the history of a workflow.

<h5>Lesson 2</h5>

1. What happens when you initialize a repository? Why do you need to do it?

The repository with needed files is created and it contains no commits. To begin version control with adding files to repository. HEAD file and master branch are created by git as well.

2. How is the staging area different from the working directory and the repository? What value do you think it offers?

Staging area is kind of transfer zone, where you can add files to be commited. It is like a node that takes all files together before commit, so you can double check the logic of the commit. Also it's possible to unstage the file using git reset command.

3. How can you use the staging area to make sure you have one commit per logical change?

I can compare the differance between staged files and original files from working derectory usind "git diff" with no arguments. It allows to check what changes in which file were added to staging area before commit. Using "git reset <file_name>" you can discard file from the staging area to keep logic clean. Also you can check the differance between staging area and the appropriate commit in the repository by "git diff --staged" command. Also if you found out that some changes you don't want to add you can use "git reset --hard". This command will discard all changes in working directory that you can't back anymore. To delete recent commit "git reset --hard HEAD^" or add "HEAD~2" to delete last two commits.

To see the differance between commit and his parent without paren't ID run "git show <commit ID>". It's good disicion when you've merged two branches and don't exactly know what was the history of each branch before merging.

4. What are some situations when branches would be helpful in keeping your history organized? How would branches help?

Branches helps to organize yout history in case you need to add an alternative version of your file and keep working on both independantly. To do it you need to create a branch with "git branch <new branch name>". After you can easily switch between them by using "git checkout <branch name>". The master branch is the main branch you work in. The HEAD is the last commit. You can imagine it as a caterpillar.

5. How do the diagrams help you visualize the branch structure?

Diagrams helps to understand when exactly the brach was added and control the history of each branch separatly. To compare the history in both branches you can use "git log --graph" to see the history of both branches also you can add "--oneline" optional to see the short history as well.

6. What is the result of merging two branches together? Why do we represent it in the diagram the way we do?

Git merge allows to merge two different branches into one. To do it you have to run "git merge <name of th branch>". Note, that you can't merge two branches if you're not in one of them, in other case all the branches will be merged. "Git gc" command clean up the history. If you have a conflict run "git merge --abort" to stop merging process and fix files. Diargamm helps to represent the behavior of commits in every branch.

7. What are the pros and cons of Git's automatic merging vs. always doing merges manually?

Automatic merging gives ability to easily merge branches when there is no possible conflicts. Manual merging is better for files with working on the same file, what takes more accurate solving.

<h5>Lesson 3</h5>

1. When would you want to use a remote repository rather than keeping all your work local?

When I afraid that my computer can shut down and stop working. It's really good idea to keep a copy of any important file you work on on the remote server just for case. Also you can use remote repository if you or your partner work on another machine on the same project, so you can share your project free. And if you want to show your project to another people. Any case it's a good idea. To create a remote repository you need to run "git remote" to check if there any remote servers and then "git remote <remote name> <remote http adress>" also you can use SSH key. To push your changes to the remote repository push you run "git push <remote name> <branch name>". To verify your remote run "git remote -v".

2. Why might you want to always pull changes manually rather than having Git automatically stay up-to-date with your remote repository?

Because automatically up-to-date can provocate a conflict or even erase your latest commits.

3. Describe the differences between forks, clones, and branches.  When would you use one instead of another?

Clone is ability to copy the repository with all the history and every changes and save it on your local machine for example.. Fork is GitHub local clone feature that copies the repository on the remote side. Both of them are teamwork opportunities. Branch is an independant vector of the repository. You can work localy on your own project. 

4. What is the benefit of having a copy of the last known state of the remote stored locally?

To avoid conflicts and staying up-to-date.

5. How would you collaborate without using Git or GitHub?  What would be easier, and what would be harder?

It's possible to use another version control systems or clouds.

List of Git Commands:
https://git-scm.com/docs


## Linux CLI, and HTTP

# Learn the Command Line (Codecademy course)

Command Line is a way of navigation, managing derictories and running files by using keyboard only. What is much convinient and faster especially after Typing course:) Configuring CLI for your personal usage can be very helpful during workflow. One of the most popular opensource CLI is Bash what stands for Bourne-Again-Shell named for it's creator Bourne and the word game in the same time. Here are some most usable commands, that were uncovered in Codecademy course for CLI:

cd - changes directory;
ls - list all files and directories;
ls -a - -a flag modifies ls command and shows hidden files and directories, they starts with dot;
ls -l - -l option modifies ls command and shows files and directories in a long format;
ls -l - -t option modifies ls command and shows files and directories in a order they were last modified;
ls -alt - -alt option is combination of previous operations;
pwd - prints the working directory;
mkdir - creates a directory;
touch - creates a file;
echo - write a text message;
cat - command output of the file to the terminal;
cp - copies content of one file to another or copies file or directory from one directory to another;
mv - moves file or directory from one directory to anotother or moves content from one file to another what in fact renames the file;
rm - removes file;
rm -r - -r option stands for recursive modifies rm command and allows to remove the directory and files permanently;
wc - couns lines, words and characters;
sort - sorts content of the file;
uniq - outputs unique strings in file;
grep -  stands for global regular expression print search file for line that match the pattern and output the result. It's case sensetive unless you use -i option which stands for ignoring case;
grep -R - searches all files in a directory and outputs filenames and lines containing matched results;
grep -Rl - searches all files in a directory and outputs only filenames;
sed - stream editor that finds and replace needed text; ine the expressions of sed 's/text/another_text/' s stands for substitution from the 'text' that is searching and replacing it with another_text. It will change only the first instance of the line unless you using 's/text/another_text/g' where g stands for global and make changes to the all matches.

Using * (which stands for 42 in the ASCII tables) means you can replace the astrisk with any symbol. So you can apply to find all file that ends with *.txt extention.

Pro tip: to make your operation quiklier you can type only begginig of the name then push Tab button for autofilling;

stdin - standart input;
stdout - standart output;
stderr - standart error;
> - directs input to the file;
| - the pipe takes the standard output of the command on the left and pipe it as a standard input to the command on the right;

- Using command cat with redirection operator > can rewrite the content of the file with another file.
- Using command cat with redirection operator > can add the content of one file to another.
- Using command cat with redirection operator < takes standart output of the file and input it to the programm on the left;
- Best practice of using uniq command is using sort command and pipe the output of sort to uniq;

<h5>Configuring Command Line</h5>

The enviroment refers to specific settings that can be applyed with editor like nano. Nano is a simple editor that works only with keyboard and very convinient for command line. The current lessons tells about configuring enviroment. ~/.bash_profile is a file used to store enviroment settings. The .bash_profile is a hidden file which CLI identifies and run it. Here in the bash profile you can alias commands by using alias your_command_name="command_name",and set variables for example, change username by using export command and setting USER="your name", command prompts can be change by using export and setting PS1="whatever_you_want" etc. The changes will be able in the current session already after you run source ~/.bash_profile. Source command allows to run command in current session.

source - uses for bash profile file and allows to configure the file in current session;
clear - cleans up the command line;
history - shows command history in the command line;
date - shows current date;
head - shows begginig of a file or piped data;
less - the same as cat but works better for large files;
-N option - shows line number;
env - stands for enviroment and returns the current variables settings (PATH, PWD, PS1, HOME, USER etc);
env | grep VAR - returns piped enviroment with needed variable;

nano commands:
cntrl + o - save. where o stands for output;
cntrl + x - exit, where x  stands for exit;
cntrl + g - opens help menu;

Vasiables in .bash_profile:

PATH - shows the list of directories separated by a colon;
HOME - the home directory;
USER - name of the current user;
PS1 - the command prompt;
LESS - variable for less command

More commands <a href="https://www.codecademy.com/articles/command-line-commands">here</a>

<h5>Scripting</h5
    
Scripting allows to write fitsystem presets and commands to execute every time termnal is opened. This file must have a .sh extension to run them with bash. To make system understand it better in the very top of document run #!/bin/bash, as a result system will use bash interpreter to run the code below this line. Script file should be placed in the ~/bin/ directory and have execute permisin, which can be provided by running change mode command chmod with an -x option what stands for execute and the name of the file chmod -x filename.sh. To make your script file run from anywhere, not only from his parent directory change the PATH variable to PATH=~/bin:$PATH.

Variables in your file can be initialize just by adding them like this variable="value", to access the variable use $ sign, e.g. $variable_name. Conditions have a specific syntax. The if statement starts with if then in square brackets [] conditions are set, and then command runs in new line, after runs else construction and statement ends with fi. More about specific syntax with option:

-eq - equal;
-ne - not equal;
-lt - less than;
-gt - greater than;
-le - less or equal;
-ge - greater or equal;
-z - null;

To compare strings use qoutes while accessing the variable like this "$variable_name". It prevents syntax errors. For strings works syntax == - means equal and != - menas not equal. While echo your variables you don't need qoutes.

Loops are provided with three operators: while, for and until.
For - good for running through the list and execute command on each step with do operator. For end with done operator. Variable defined in the condition right after for statement like this [varible_name -option $another variable] for variable in $another_variable (list, arrey, etc).
While and Until are pretty similar in bash. Both of them are looping, but while runs until finds the fitting condition, and until runs until the condition is true. The syntax is pretty the same as for conditions, but end with done statement. The good part is as usual while and until can be replaced by each other like this

while [$variable -lt number]
do
some commands
variable=$((variable + 1))
done

until [$variable -eq number]
do
some commands
variable=$((variable + 1))
done

Important! Doing math in bash means using accessor $ before double parahtnesis (()) and inside paranthesis add only variable without accessor sign like this $((variable + 1))

To make an iput add 'read variable' command. It will accept the users input for futher operations. The variable initialization sets the same like in the for loop without accessor $. Another ability to set input is to set it for user to enter it with variable name while running script like variable value1 value2 value3 etc. To use this variables you should use $1 what stands for first value $2 for second etc. If you need the internal number of values set them to $@.

Alias. To shorten the operation we can alias it as we did with commands for command line like this alias command_name="./file_name.sh". More than that, you can use constant variable value for the current alias like this alias command_name="./file_name.sh" "value".

More: head <a href="http://www.linfo.org/head.html">here</a>
