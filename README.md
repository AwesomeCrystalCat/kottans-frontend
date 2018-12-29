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
