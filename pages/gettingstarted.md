# **Getting started**




##**Setting up a repository**



   ![GitHub Logo](../images/git_repositories.png)

A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed. 

  ###1. Initializing a new repository: git init
  
  To create a new repo, you'll use the git init command. git init is a one-time command you use during the initial setup of a new repo. Executing this command will create a new .git subdirectory in your current working directory. This will also create a new master branch.
  
  _Command:_
  
  ```
  git init
  ```
   
  
  ###2. Cloning an existing repository: git clone
  If a project has already been set up in a central repository, the clone command is the most common way for users to obtain a local development clone. Like git init, cloning is generally a one-time operation. Once a developer has obtained a working copy, all version control operations are managed through their local repository.
    
  _Command:_
  
  ```
  git clone
  ```

  ###3. Saving changes to the repository: git add and git commit
  Now that you have a repository cloned or initialized, you can commit file version changes to it. The following example assumes you have set up a project at _path/to/project_. 
  
  
   _Command:_
   
   ```
cd /path/to/project echo "test content for git tutorial" >> CommitTest.txt git add CommitTest.txt git commit -m "added CommitTest.txt to the repo"
   ```
  In this example the following steps are taken-
  
  * Change directories to _/path/to/project_
  
  * Create a new file ``` CommitTest.txt ``` with contents ``` ~"test content for git tutorial"~ ```
  
  * git add ``` CommitTest.txt ``` to the repository staging area
  
  * Create a new commit with a message describing what work was done in the commit
  
  
  ###4. Repo-to-repo collaboration: git push
  Git’s collaboration model is based on repository-to-repository interaction. You push or pull commits from one repository to another.
  
     
  ###5. Configuration & set up: git config
  Once you have a remote repo setup, you will need to add a remote repo url to your local git config, and set an upstream branch for your local branches. The git remote command offers such utility.
  
  _Command:_
  
  ```
  git remote add
  ```

 Once you have mapped the remote repo you can push local branches to it.
 
 ```
git push -u
```

**_Summary of learning so far:_**

Here we demonstrated how to create a git repository using two methods: git init and git clone. This guide can be applied to manage software source code or other content that needs to be versioned. Git add, git commit, git push, and git remote were also introduced and utilized at a high level.

*** 
  
  
  
##**Saving changes**


When working in Git, or other version control systems, the concept of "saving" is a more nuanced process than saving in a word processor or other traditional file editing applications. The traditional software expression of "saving" is synonymous with the Git term "committing". A commit is the Git equivalent of a "save". Traditional saving should be thought of as a file system operation that is used to overwrite an existing file or write a new file. Alternatively, Git committing is an operation that acts upon a collection of files and directories.


_Commands:_ 
```
git add
```

``` 
git status
```

``` 
git commit
```

Above commands are all used in combination to save a snapshot of a Git project's current state.

A Git repository can be configured to ignore specific files or directories. This will prevent Git from saving changes to any ignored content. Git has multiple methods of configuration that manage the ignore list.  

```
Git ignore
```

***

##**Git Status: Inspecting a repository**

The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git. Status output does not show you any information regarding the committed project history. For this, you need to use git log.

_Related commands:_

```
git tag
```
  
Tags are ref's that point to specific points in Git history. git tag is generally used to capture a point in history that is used for a marked version release (i.e. v1.0.1).

``` 
git blame
```

The high-level function of git blame is the display of author metadata attached to specific committed lines in a file. This is used to explore the history of specific code and answer questions about what, how, and why the code was added to a repository.

```
git log  
```

The git log command displays committed snapshots. It lets you list the project history, filter it, and search for specific changes. 


***

##**Undoing Commits & Changes**

It is first important to note that Git does not have a traditional 'undo' system like those found in a word processing application. It will be beneficial to refrain from mapping Git operations to any traditional 'undo' mental model. Additionally, Git has its own nomenclature for 'undo' operations that it is best to leverage in a discussion. This nomenclature includes terms like reset, revert, checkout, clean, and more.

Necessary skills to work with previous revisions of a software project-

 * Finding what is lost: Reviewing old commits
  
      One of the best utilities for reviewing the history of a Git repository is the ```git log``` command.

 * Viewing an old revision
 
      Let's assume that you’ve started developing a crazy experiment, but you’re not sure if you want to keep it or not. To help you decide, you want to take a look at the state of the project before you started your experiment.
      
      you can use either ```git revert``` or ```git reset``` to undo any undesired changes.
      
      ```git clean```
      Git clean is to some extent an 'undo' command. Git clean can be considered complementary to other commands like git reset and git checkout. Whereas these other commands operate on files previously added to the Git tracking index, the git clean command operates on untracked files. Untracked files are files that have been created within your repo's working directory but have not yet been added to the repository's tracking index using the git add command.
      
      ```git rm```
      The git rm command is used to remove files from a Git repository. It can be thought of as the inverse of the git add command.
      
 *** 
 
 [**Return to Readme**](../README.md)
      