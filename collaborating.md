#**COLLABORATING ON GITHUB**
**GIT VS GITHUB**

**GIT**

* Git is the command line version control system (VCS) software which works on your local computer.

* Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

* You need Git to use GitHub. You can use Git locally without GitHub.

**GITHUB**

* GitHub is an internet hosting service for git repositories. Public repos are free; private repos are paid.
* As a shared space for repos, it allows you to do collaborative work.
 
**TWO COMMON COLLABORATIVE WORK FLOWS**

**SHARED REPOSITORY MODEL**
 * For small projects where you are basically in the same physical space (e.g. lab with offices near each other).
 * Be careful! You are cloning the main repository.
 * Everyone has push and pull access to the central repo, so be careful and:
     * Never commit to the master directly.
     * Always do your work on a different branch from master.

**BASIC SHARED REPOSITORY WORKFLOW**

* update your local repo with _Command:_
  
  ```
  git pull origin master,
  ```

 * create a working branch with 
 _Command:_
  
  ```
  git checkout -b MyNewBranch
  ```
 
 * make your changes on your branch and stage them with 
 _Command:_
  
  ```
  git add,
  ```
 
* commit your changes locally with 
_Command:_
  
  ```
  git commit -m "description of your commit"
  ```
  , and
* upload the changes (including your new branch) to GitHub with 
_Command:_
  
  ```
  git push origin MyNewBranch
  ```
* Go to the main repo on GitHub where you should now see your new branch
* click on your branch name
* click on “Pull Request” button (URC)
* click on “Send Pull Request”

**FORK AND PULL MODEL**

* This is the model used by U of T Coders on its own website and repos.
* The “owner”/”Project Leader” of the upstream repo assigns rights to “Collaborators”
* Collaborators do not have push access to main (upstream) repo
* Project Lead accepts Pull Requests (PRs) fro collaborators, reviews them, then merges them into main repo.

**FORK AND PULL WORKFLOW**

 * to be demonstrated during lesson

**SOME GIT TERMINOLOGY/JARGON**

**REPOS AND BRANCHES**

Term| Description
------------ | -------------
Origin (repo)| Your remote repo (on Github); it is the “origin” for your local copy. Either it is a repo you created yourself or it is a fork of someone else’s GitHub repo.
Upstream (repo)| The main repo (on GitHub) from which you forked your GiHub repo.
Local (repo) |	The repo on your local computer.
Master	|The main branch (version) of your repo.
 
BASIC COMMANDS| ACTIONS
------------ | -------------
Term 	|Explanation
Fork	|Make a copy of someone else’s GitHub repo in your own GitHub account.
Clone	|Make a copy of the your GitHub repo on your local computer. In CLI: ‘git clone’ copies a remote repo to create a local repo with a remote called origin automatically set up.
Pull	|You incorporate changes into your repo.
Add	|Adding snapshots of your changes to the “Staging” area.
Commit	|Takes the files as they are in your staging area and stores a snap shot of your files (changes) permanently in your Git directory.
Push	|You “push” your files (changes) to the remote repo.
Merge	|Incorporate changes into the branch you are on.
Pull Request	|Term used in collaboration. You “issue a pull request” to the owner of the upstream repo asking them to pull your changes into their repo (accept your work).