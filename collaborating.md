**<h1>COLLABORATING ON GITHUB<h1>**
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

**Git Syncing**

Git Syncing! *Turoials*
[Git Syncing](https://www.atlassian.com/git/tutorials/syncing)

**Understanding the GitHub flow**

GitHub flow is a lightweight, branch-based workflow that supports teams and projects where deployments are made regularly. This guide explains how and why GitHub flow works.

**Create a branch:**

![Create a branch](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images\flow 1.png)

**Create a branch**

When you're working on a project, you're going to have a bunch of different features or ideas in progress at any given time – some of which are ready to go, and others which are not. Branching exists to help you manage this workflow.

When you create a branch in your project, you're creating an environment where you can try out new ideas. Changes you make on a branch don't affect the `main` branch, so you're free to experiment and commit changes, safe in the knowledge that your branch won't be merged until it's ready to be reviewed by someone you're collaborating with.

**ProTip**

Branching is a core concept in Git, and the entire GitHub flow is based upon it. There's only one rule: anything in the `main` branch is always deployable.

Because of this, it's extremely important that your new branch is created off of main when working on a feature or a fix. Your branch name should be descriptive `(e.g., refactor-authentication, user-content-cache-key, make-retina-avatars)`, so that others can see what is being worked on.

**Add commits**

![Add commits](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images/flow 2.png)
Once your branch has been created, it's time to start making changes. Whenever you add, edit, or delete a file, you're making a commit, and adding them to your branch. This process of adding commits keeps track of your progress as you work on a feature branch.

Commits also create a transparent history of your work that others can follow to understand what you've done and why. Each commit has an associated commit message, which is a description explaining why a particular change was made. Furthermore, each commit is considered a separate unit of change. This lets you roll back changes if a bug is found, or if you decide to head in a different direction.

**ProTip**

Commit messages are important, especially since Git tracks your changes and then displays them as commits once they're pushed to the server. By writing clear commit messages, you can make it easier for other people to follow along and provide feedback.

**Open a Pull Request**

![pen a Pull Request](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images/flow 3.png)
**Open a Pull Request**

Pull Requests initiate discussion about your commits. Because they're tightly integrated with the underlying Git repository, anyone can see exactly what changes would be merged if they accept your request.

You can open a Pull Request at any point during the development process: when you have little or no code but want to share some screenshots or general ideas, when you're stuck and need help or advice, or when you're ready for someone to review your work. By using GitHub's @mention system in your Pull Request message, you can ask for feedback from specific people or teams, whether they're down the hall or ten time zones away.

**ProTip**

Pull Requests are useful for contributing to open source projects and for managing changes to shared repositories. If you're using a Fork & Pull Model, Pull Requests provide a way to notify project maintainers about the changes you'd like them to consider. If you're using a Shared Repository Model, Pull Requests help start code review and conversation about proposed changes before they're merged into the main branch.

**Discuss and review your code**

![Discuss and review your code](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images/flow 4.png)

**Discuss and review your code**

Once a Pull Request has been opened, the person or team reviewing your changes may have questions or comments. Perhaps the coding style doesn't match project guidelines, the change is missing unit tests, or maybe everything looks great and props are in order. Pull Requests are designed to encourage and capture this type of conversation.

You can also continue to push to your branch in light of discussion and feedback about your commits. If someone comments that you forgot to do something or if there is a bug in the code, you can fix it in your branch and push up the change. GitHub will show your new commits and any additional feedback you may receive in the unified Pull Request view.

**ProTip**

Pull Request comments are written in Markdown, so you can embed images and emoji, use pre-formatted text blocks, and other lightweight formatting.

**Deploy**

![Deploy](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images/flow 5.png)

**Deploy**

With GitHub, you can deploy from a branch for final testing in production before merging to main.

Once your pull request has been reviewed and the branch passes your tests, you can deploy your changes to verify them in production. If your branch causes issues, you can roll it back by deploying the existing main branch into production.

Different teams may have different deployment strategies. For some, it may be best to deploy to a specially provisioned testing environment. For others, deploying directly to production may be the better choice based on the other elements in their workflow.

**Merge**

![Merge](/C:\Users\sh667\MiniProject\MiniProj_NTSH_601Fall20\images/flow 6.png)


Now that your changes have been verified in production, it is time to merge your code into the main branch.

Once merged, Pull Requests preserve a record of the historical changes to your code. Because they're searchable, they let anyone go back in time to understand why and how a decision was made.