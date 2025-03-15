<b>demo_1</b><br>

<h3>Author : Krishna Nagiri</h3><br>

<H2>GIT AND GITHUB</H2><br>

<H4>What is git? </H4>
<P>Git is a version control system that helps to track changes in code.</P><br>

<B>Features:</B><br>
1.popular<br>
2.free and open source<br>
3.fast and scalable<br>
<br>
<b>Used to :<b><br><br>
1.track history of code.<br>
2.to colobrate.<br>

<br>
<b>GITHUB<b><br>
<p> A website that allows developers to store and manage their code using git.<br>
Files of code or project is uploaded into github, and these files are known as "Repositories".<br>
</p>

## Create a New Repository.(in Github)<br>

1. click on create repository<br>
2. set repo name.<br>
3. description is optional.<br>
4. public/private.<br>
5. Add readme.md(md = markdown)(later edit optionally).<br>
6. create repository.<br>

## COMMIT<br>
Changes in github is known as commit.<br>
changes comes in two steps in local files(git)<br>
  1. adding changes (add)<br>
  2. commit changes (commit)<br>


## Configuring git account.
    --> git config --global user.name "user_name" 
    -->git config --global user.email "user_email"
<br>............................................<br>
To view list of all users.<br>
   -->git config --list <br>


# CLONE 
   --> git clone //link//<br>

## STATUS
   --> git status  

    1. If any changes have been done to the cloned file this will show the modifications and 
           (M)  intimate us to stage and commit changes.

    2. If created any new file in the local directory this will flag that newly created file as 
          untracked file (U)

      modified    === M (made changes but not added or commited)
      untracked   === U (newly added files, not added or commited)
      staged      ===   (Changes were added but not commited)
      unmodified  ===   (Changes were added and commited)


## Add and Commit.
    1. add     = conforming the changes made.{To conform all changes:(git add.)}
    2. commit  = saving the changes.(git commit -m "message")

## PUSH<br>
    used to upload local repo content to remote repo
    --> git push origin main 

  ????????? 
  origin = every repository in github is remote repo.<br>
  And we have cloned into one such repository whose name is by default "Origin"<br>
  the name origin can be changed by the user.<br>
  main = branch.<br>

  ///////
## INIT<br>
  Used to initilize a new git repository in the local machine.<br>
  steps:<br>
  1.Create a new directory.<br>
  --> mkdir _new_directory_ <br>
  --> git init _repo_name_<br>

## Adding new repo from local machine.<br>
 create a new git repository with the same name as the folder created in local repo<br>
  -->git add remote origin _link_  <br> 
(link => link of the newly created repository)<br>

## Checking if given(link) remote existed or not<br>
  -->git remote -v <br>

## BRANCH<br>
Every branch has a copy of the main project() = master branch<br>
By default everyone changes the master branch as "main"<br>
Changes may or may not commited in the master branch.<br>
 To Do this<br>
--> git branch -m _new_name_<br>
All branches are connected to main branch.<br>
To push changes or files commited in local machine to github we need to push the files into repo.<br>
 To do this<br>
--> git push -u origin _branch_name   <br>
// it is  recommended to add -u flag only once during the first push.<br>
 After first push<br>
--> git push<br>

## To change from current branch<br>

--> git checkout<br>

## To create new branch<br>

--> git checkout -b _new_branch_name<br>

## To delete the branch<br>

--> git branch -d _branch_name_<br>

## Merging code<br>

<p>There are 2 ways to merge code</p><br>

-->1. 
    <b>To compare commits,branches, files and more</b><br>
      --> git diff _branch_name_ <br>
      To merge branches ,to avoid merge Conflicts<br>
      --> git merge _branch_name <br>
<br>
-->2.<br>
      <b>Creating PULL REQUESTS</b><br>
        <p>Lets you tell others about changes you've pushed to a branch in a repository on GitHub.
        ( Main/senior developers checks if the change has to be merged or not.!)</p>

## PULL
<p>Used to fetch and download content form a remote repo and immediately update the local repo to match that content.
(Add changes only to main branch.)</p><br>
 --> git pull origin main<br>

## Merge Conflicts<br>

Git automatically tries to merge two branches when a pull request is created.<br>
An event that takes place when git is unable to automatically resolve the difference in code between two commits.<br><br>

## Resloving merge Conflicts<br>
--> git merge _branch_name<br>
resolve Conflicts manually and commit the changes.<br>

## Undoing changes.<br><br>
<p>
(Undoing changes at stage:
    1. add              -->git reset _file_name_<br>
    2. ommit            --> git reset HEAD~1 <br>
    3. multiple commits --> git reset _commit_hash_  <(<commit hash: The unique code assosiated with each commit>)><br>
    4. Hard reset       --> git reset --hard _commit_hash_ <(< --hard : Removes changes from visual code too.>)><br>
    )
</p><br>
## Checking commit logs(history) <br>
<br>
  --> git log

# FORK<br>
A fork is a new repo that shares code and visibility settings with the original "upstream" repo.<br>
Fork is a rough copy(of another github repo)<br>
