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

<h3>Summary</h3>

Earlier I thought that Git is used only to for file exchange like a cloud. But following this course I found out that using Git allows to control every step of your workflow. Manipulating history with numerous commands let your own mind keep clear without remembering every detail of your code as I was trying to do before and looking for bug manualy. The second important thing I learnt is commiting. Now I know that the best practice of commiting is a logical chunks that makes the history much more clean and accurate. Fetch, pull and merging aren't so scary words anymore. Conflicts resolving can be even fun^^

## Linux CLI, and HTTP

# Learn the Command Line (Codecademy course)

<img src="/task_linux_cli/codecademy_cli.png" />

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

<ul>
    <li>stdin - standart input;</li>
    <li>stdout - standart output;</li>
    <li>stderr - standart error;</li>
    <li>> - directs input to the file;</li>
    <li>| - the pipe takes the standard output of the command on the left and pipe it as a standard input to the command on the right;</li>
</ul>

<ul>
    <li>Using command cat with redirection operator > can rewrite the content of the file with another file.</li>
    <li>Using command cat with redirection operator > can add the content of one file to another.</li>
    <li>Using command cat with redirection operator < takes standart output of the file and input it to the programm on the left;</li>
    <li>Best practice of using uniq command is using sort command and pipe the output of sort to uniq;</li>
</ul>
    
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

<h5>Scripting</h5>
    
<p>Scripting allows to write fitsystem presets and commands to execute every time termnal is opened. This file must have a .sh extension to run them with bash. To make system understand it better in the very top of document run #!/bin/bash, as a result system will use bash interpreter to run the code below this line. Script file should be placed in the "~/bin/" directory and have execute permisin, which can be provided by running change mode command chmod with an -x option what stands for execute and the name of the file chmod -x filename.sh. To make your script file run from anywhere, not only from his parent directory change the PATH variable to "PATH=~/bin:$PATH".</p>

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

<h5>HTTP</h5>

HTTP stands for Hypertext Transfer Protocol, it's a stateless protocol what allows to make request-respond pair quik and lightweight. The communication set by using TCP/IP (Transmission Control Protocol/Internet Protocol) what includes three important ingredients: URL (Uniform Recourse Locator), verb and status. URL is kind of a a path to the server according to request and containes protocol, host, port, resource path, query. Verbs are keywords to operate server. Status is a server answer to the request.

First of all client and server must set the connection. After connection is estebished client can send a request to server. Every request should include starter line, header and message body (not important). Server parses the request and creates a respond to send it back to client. Status helps to form the message.

Dammit! it's soooooo hard-to-understand:(

<h5>Summary</h5>

Never thought it's possible to set everything only via keyboard. It makes navigation and operations easy and quick. The best part was bash_profile. Alias, setting variables is very amusing and allows to customize everything in bash.


## Git Collaboration

<img width="600" height="auto" src="/task_git_collaboration/github&coolab.png" />
<img width="600" height="auto" src="/task_git_collaboration/vc_wtih_git.png" />

So far it's possible to create two directories parent/child with one command mkdir with -p option and by using && I can collaborate my commands. I haven't think about that before.

Git works as a pager. Who could know that? So when you have a lot of content in a window to scroll down all the content you can use up arrow or K key and down arrow or J key to scroll down. To move half page hit D for down and U for up. To move full page hit F for down and B for up. To quit press Q key.

Recall for previous course. git log --oneline shows history in short format.

Git log --stat (--stat for statistics) gives more information about changes that were made.

More fun with flags! git log --patch or git log -p shows all changes of each file. But it takes a lot of space and not really convinient.

If you want to add all files at once use git add . command where . refers to the current directory with all files and directories with their content. If you added some files you didn't want to stage you can run git rm --cached <file_name>. Or you can use magic .gitignore. Add files you want to be ignored by git.

.gitignore magic. Using this feature on command line is much more efficient, imho. well, as you know, adding name of the file or a folder to this file will be ignored by git and won't display at your working area. One more useful tip is globbing. "#" - marks line as a comment, "*" - is 42 or 0 or more symbols, "?" - for one symbol, "[abc]" - matches a, b, or c, "** " - nested directories, like that "folder / ** / file_name". One astrix can be used for one-level folders. To make one of the same extension file not ignored use "!" before file name like this !file_name.ext. You can also choose one file from the directory to be ignored, not all the directory by adding this file like this /file_name.ext. To ignore file with the same name in all the directories you have type file_name/.

Tagged commits works the same as sha, it's a great helper since you just follow the tag to checkout the needed version. To add tag you need to run git tag -a tag_name and add a comment in the editor and the latest commit will be tagged. To tag earlier commit run it tag -a tag_name commit_sha. To delete a tag run git tag -d tag_name where -d stands for delete. 

Voala! Branches works the same as tags do! You can attach new branch to the specific commit by running git branch branch_name commit_sha. The same for deletion. Use -D to force deletion. To add branch with checkout command use git checkout -b branch_name.

New about git log. To expose all branches add --all flag to the git log command.

If you've forgotten to add file to commit or you have to fix smth related to last commit then you can use git commit --amend for the last file and it will automatically added to your commit after you add a comment.

One more feature is reverting commits. In case you want to make changes of the last commit back you can use get revert commit_sha. and your last commit will be reverted. For example, if you deleted a line and commited it git revert command will bring th3e deleted line back. Attention! Tricks with revert can cause conflicts.

You already know, but here's a reminder to delete a commit use command git reset --hard HEAD^ for last commit and git reset --hard HEAD~number to delete the n-th parent commit. New thing is flag --mixed which is the default flag in the same time and it returns commit to the working directory with both commands git reset HEAD^ or git reset --mixed HEAD^, other words your changes will be unstaged. Command git reset --soft HEAD^ will return commit to the staging area and you can commit it back anytime but with appropriate timestamp.
Pro tip: before you doing any type of reset just for case run git branch backup to make reset more safe. after needed changes you can merge backup branch into master.

Deleted everything on the Earth in your repo? No worries run git reflog command. It saves all the history of your commits for a while. By adding --all flag you will see more detailed history.

GitHub is a remote server to save and share repositories. To add the remote repository use command git remote add remote_shortname remote_link. For remote shortname is usualy used name origin, but you can call it as you wish by adding the name while typing command. Then run git remote -v to verify your remote server.

After you made a commit you probably want to share or push your files to the remote. You can do it by typing git push -u remote_shortname branch_name, e .g. git push -u origin master. The opposit command is git pull. It wroks the same way as git push do but takes the changes from the remote and pull it to your computer. Commands is similar too: git pull remote_shortname branch_name. If you have changes on the both local and remote repositories that can cause a conflict good idea to run git fetch. It's kind of half git pull command. It works this way: git fetch remote_shortname branch_name and makes only your local origin/master up-to-date while your local master still stays without changes. Later you can fast-forward merge it. The same story if you have two different commits that can be self erased while pulling. Better idea to do git fetch and after merge both branches origin/master and master. Don't forget to push your changes to remote to keep it up-to-date.

git shortlog displays an alphabetical list of names and the commit messages that go along with them. If you just want to see just the number of commits that each developer has made, you can add a couple of flags: -s to show just the number of commits (rather than each commit's message) and -n to sort them numerically (rather than alphabetically by author name).

If your project is full of developers and you need to find out which commits were made by the exact autor run git log --author=name. If name contains two or more words in this case use quotes git log --author="name surname" to avoid error.

You can use git --grep indicator or git --grep=indicator (the situation with two or more words is pretty the same) to find all commits with the specific indicator e. g. git --grep=bug will find all commits with "bug" in the description.

While working with the forked repository on your local repo you can still keep all file up-to-date with the original repository by following it. To do it you need to hit a star on the page of the original repo and hit watching. To pull last commits from original repository you have to add one more repo that usually called upstream, but the name still can be absolutely everything. Dapends on your amigination. To do it run command: git remote upstream original_repo_url. After running varification git remote -v you will see new remote repository. If you want you can rename your local remote repo by running git remote rename old_name new_name.

To get the latest changes from the original repo just run git fetch original_repo_shortname branch_name.

If your pull request was asked to be updated usually you should make the rebase. If you afraid to do a mistake it's actually ok, so you can just make git backup for the current branch. After you can start a rebase by running git rebase -i HEAD~number_of_commits_to_rebase, where -i stands for interactive what gives you numerous hints how to make rebase more painless. After you run the command you wiil be promted to the editor where you can choose the role of each commit. Squashing is actually something like merging commits into one. So you should put a s indicator what stands for squashing to all commits that a child and r that stands for rewrard to change the commit message. After you will be promted to editor again where you can add a comment. After you have to push your newmade rebased commit to the original remote to finish pull request. Server will not allow to do that, so you should run git push -f original_remote_shortname branch_name where -f stands for force. After you will see that commit history had been changed on the original repository page.

<h5>Summary</h5>

The best part of course is magic of git ingorse and command line. Adore this collaboration. Will use it in the future for sure. Hightlighting of collaborative work on github helps to understand that you won't brake anything if you start collaborate with somebody, so you can be more confident in using GitHub and forking projects.

## Intro to HTML and CSS

<img width="600" src="/task_html_css_intro/html_udacity.png" />
<img width="600" src="/task_html_css_intro/html_htmlacademy.png" />
<img width="600" src="/task_html_css_intro/css_htmlacademy.png" />

<p>&lt;figure&gt; is a element that allows to add the image when you have no copyright for using it. You can also add a &lt;figcaption&gt; tag to make give short description and add a link to the source.</p>

<p>There are 16777216 colors</p>

<p>Description list includes tags &lt;dl&gt; - for list, &lt;dt&gt; - for the define term/name and &lt;dd&gt; - for define description.</p>

<p>&lt;blockqoute&gt; tag is great for long fragment of quoted text, even paragraphs. &lt;q&gt; tag works with short quotes inside of the text and decorets with qoutes " automatically. &lt;cite&gt; tag is used for quote sorces or the name of the author.</p>

<p>If you need to work with algebra or other formulas you should try Math Markup Language. It works like HTML but work based on XML files.</p>

<p>Tags &lt;del&gt; and &lt;ins&gt; are used for computing and to understand what text was deleted and what was is inserted approximately.</p>

<p>&lt;pre&gt; is a tag that spaces in code snippet since they don't in general.</p>

<p>&lt;mark&gt; tag used to highlight the text with yellow background by default.</p>

<p>While adding a link you can also use attribute title which gives a popup hint when the link is hovered.</p>

<p>&lt;table&gt; tag allows to create a table. To add a row use tag &lt;tr&gt; that stands for table row, and to add a cell add &lt;td&gt; that stands for table data. Also you can use tag &lt;th&gt; to add table header cells. To add a table heading use &lt;caption&gt; tag inside of the &lt;table&gt; tag in the very top. You can place your table heading anywhere you want by using caption-side CSS property with values top or bottom to move it up and down, to place it left, center or right use text-align property appropriatly.</p>

<p>You can create a border in the table by adding the border attribute with a numeral line weight to the &lt;table&gt; tag. But for better practice set border with CSS. To make border more accurate add in your CSS file border-collapse with value collapse to the table selector or the appropriate class. To make cell spacing regular apply value separate for border-collapse since you can't edit border-spacing value if it's needed in the CSS file to make cell outer space. You can set cellspacing as a attribute in the &lt;table&gt; tag, but it's defenetly isn't the best practice. Also with attribute cellpadding in the &lt;table&gt; tag you can add an inner padding of the cells. But of course it's better to use CSS</p>

<p>To collapse cells in the row you should use attribute colspan and a numeric value, e.g. setting colspan="2" to &lt;td&gt; or &lt;th&gt; tags will expand the cell one more cell on the right, so the width of the cell will be equal to 2 columns. Notice that if you applied colspan in the existing table oyou should delete the existing unwanted cells of the row.</p>

<p>To collapse cells in the column use rowspan attribute. It works the same as a colspan attribute but from top to bottom.In this case extra cells will create a new r=column on the right, so they should be deleted as well.</p>

<p>To align the content of the table you can use text-align property with values left, center or right and vertical-align property to align content top, middle, bottom with the appropriate values.</p>

<p>Forms in html are extremely useful. Tag &lt;form&gt; takes two important attributes: action for setting URL and method to sets sending method. By default method in html set to get. This method gets a query and is visible in the URL after ? symbol. One more method for the form is post which allows to post values.</p>

<p>To create the input you can use &lt;input&gt; tag inside of the &lt;form&gt; tag. &lt;input&gt; takes two important attributes: type which shows the type on the field e.g. number, text, submit, radio, file, checkbox, password or hidden value and name that sets the name of the field. One more attribute for input is value which to set the signification of the field as a default..</p>

<p>To set a label for the input you can use &lt;label&gt; tag. It's better practice, because it creates the logical connection between input and label and when you clicking on the label input is acrivated. First way to do it is to put input inside of the &lt;label&gt; tag. If it's impossible to set label as a parent of input, you can use attribute for in &lt;label&gt; tag with the referance to id of the &lt;input&gt; tag, so they will be connected.</p>

<p>To change the value of the password field to the hidden symbols use type attribute with password value.</p>

<p>To create a submit button we also use &lt;input&gt; tag with type attribute with submit value. To name your button use value attribute. If there are few different buttons use the name attribute to make server understand which exactly button was actioned.</p>

<p>If you have to create a miltiple input field you should use &lt;textarea&gt; tag with attribute name to make it unique for server, id to make it unique for user, rows and cols attribute will sett the width and height of the textarea. But textarea has no value attribute. To set the value you should write the appropriate text inside of the &lt;textarea&gt; tag</p>

<p>To create a checkbox fields create &lt;input&gt; tag with the type checkbox. It has a boolean value and it's not important to set the value. To make the checkbox checked by default add checked attribute to the &lt;input&gt; tag. If there are few checkboxes they require different name attribute.</p>

<p>To create radiobuttons use &lt;input&gt; tag with type atrribute radio. Notice, the name as well as an id attribute for radiobutton group must be the same and values must be different. For the checked radio by default use checked attribute. Nest each inputs for radiobuttons in the unique &lt;label&gt; tag.</p>

<p>Select list can be created by using &lt;select&gt; tag with attributes name and id. Nest inside of the &lt;select&gt; tag multiple &lt;option&gt; tag. The attribute value for &lt;option&gt; tag must contain the value of the answer and the label of the option is nest inside of the &lt;option&gt; tag. Setting value is crucial for &lt;option&gt;, because otherwise the text inside the tag will be sent to server. To make your select multiple add the attribute multiple to the &lt;select&gt; tag. Choose multiple can be performed by tapping cntrl or cmnd key on the keybord and clicking on the selects with mouse. Attribute size can set height of &lt;select&gt; tag. To choose selected by default add to the &lt;option&gt; tag selected value. To make select properly on the backend side set name attribute with square brackets after its value like this value[].</p>

<p>Download field can be performed by setting type attribute with file value in the &lt;input&gt; tag. The important attribute for this type of input is name attribute. To make download field work you must add to the &lt;form&gt; tag attribute enctype with the value multipart/form-data.</p>

<p>To make your field hidden use &lt;input&gt; tag with the type attribute hidden.</p>

<p>clear property in CSS allows to clear an inhereted float property for the element with values both for both left and right, right only for right, left only for left, inherit will be unherited, initial will be set to the default and none for no value.</p>

<p>Selector by type good for input fields since allattributows to appeal to the attribute of the tag. To declare the selector use class_name[attribute_name] or class_name[type="value"].</p>

<h5>Summary</h5>
Since I familiar with html and css a little bit it wasn't much informative. But practice makes perfection. Discovering is forms and inputs. Very powerful tags for interactive resources. Tables aren't that ineteresting, but gives more understanding about how html works.

## Responsive Web Design
<img width="600" src="/task_responsive_web_design/responsive_udacity.png" />
<img width="600" src="/task_responsive_web_design/frogs.png" />

<p>The pixel is npt always the pixel! Device Independant Pixels (dip) is a browser measurement that relates pixel to a real distance and usualy a half of pixels of a device. That means that hardware pixels of device aren't the same as a browser pixels.</p>

<p>Font boosting is an ability of font to be fitable for a device and make the content readable.</p>

<p>Setting resposibility starts with setting a &lt;meta&gt; tag on the &lt;head&gt; section. Add an attribute name with the value viewport and set it's content attribute to the value width=device-width,initial-scale=1. It refers the CSS pixels to dip pixels in proportion 1:1 and match device with ro the device independant pixels. So the page will be reflowed to match the size of the screen.</p>

<p>To prevent oversizing the content set the width in relative units and set the value of the property max-width: 100% for img, embed, video and object. In this case content will fit the width of the device.</p>

<p>Fun fact! Fingers are nearly 10mm width what is equal to 40 CSS pixels. So keep in mind that it's a good practice to make interactive elements big enogh to make it comfortable for even big fingers. Make your element at least 48x48 pixels and make enoght room around the element 40x40 pixels to prevent mistakes in users experience.</p>

<p>Design and code from small to large!</p>

<p>One more <del>and probably more accurate</del> way to apply media queries is to use different CSS files for different device width styling and set the media query as the value of an attribute media in the &lt;link&gt; tag while adding new CSS stylesheet in the head section of your html. Example: &lt;link rel="stylesheet" media="screen and (min-width: 350px)" href="app350.css"&gt;</p>

<p><ins>No, making a lot of files isn't good idea, since it take a lot of queries. So continue writing media queries as usual @media screen and (min-width: 350px) in your CSS file.</ins></p>

<p>Cool idea for flexbox, while using a shifting model of the content layout. If you want to change the order of the block apply value -1 to order property since all blocks have a default value of 0 the block will move one step left. To move the block forwars use the 1 value for order property.</p>

<h5>Summary</h5>

<p>Recall issue about forgetting to add &lt;meta&gt; tag to the webpage to avoid struggeling "why a heck doesn't it work properly?" Good idea to learn more interesting layouts for webpages. Favorite are a content shifting and mostly liquid models. Never thought that starting with smaller device is better idea, but it is. Making table displayed as block for small device seems not really good desicion since it takes a lot scrooling down. Anyway the best is to remake the table content appropriate to each resolution. Order! Order:-1 was a great discovering. And playing with frogs is much amusing.</p>
