# Mini GIT course

@css[byline right](Marco Chiapello)
---
## Version control

@fa[code-fork fa-3x]

+++?image=assets/img/bg/black.jpg&position=right&size=50% 100%
@snap[east text-white span-45]
@ol[split-screen-list](false)
- The whole idea behind any **version control** system is to **store “safe” copies** of a project 
- You never have to worry about irreparably breaking your code base
@olend
@snapend

@snap[west span-50]
![Logo](assets/img/phd101212s.png)
@snapend

+++

**Version control** software keeps track of _every modification_ to the code in a special kind of database. 

If a mistake is made, developers can

@ul[roman]
- turn back the clock
- compare earlier versions of the code
- minimize disruption to all team members @note[Collaborative repository]
@ulend

+++

@snap[north span-100]
@size[1.5em](Benefits of version control)
@snapend

### FIRST

**A complete long-term change history of every file** 

@ul
- This means every change made by many individuals over the years. 

- Changes include the creation and deletion of files as well as edits to their contents

- File can be followed along their history @note[Even if the file change name - git follow the file based on the content and not the name]
@ulend

+++

@snap[north span-100]
@size[1.5em](Benefits of version control)
@snapend

### SECOND 

**Branching and merging** 

Having team members work concurrently is a **no-brainer**, but even individuals
working on their own can benefit from the ability to work on **independent
streams of changes**. 

Creating a "branch" in VCS tools keeps multiple streams of
**work independent from each other** while also providing the facility to merge
that work back together, enabling developers to **verify that the changes on each
branch do not conflict** 

+++

@snap[north span-100]
@size[1.5em](Benefits of version control)
@snapend

### THIRD

**Traceability**

Being able to **trace each change** made to the software and connect it to project
management and being able to **annotate
each change** with a message describing the purpose and intent of the change can
help not only with root cause analysis and other forensics. 

Having the
**annotated history** of the code at your fingertips when you are reading the code,
trying to understand what it is doing and why 

---

## Git

@snap[south-east span-40] @quote[By far, the most widely used modern version control system in the world
today is Git](Bitbucket website) @snapend

+++

Git is good

Git has the functionality, performance, security and flexibility that most teams and individual developers need. These attributes of Git are detailed above. In side-by-side comparisons with most other alternatives, many teams find that Git is very favorable.

+++

Git is a de facto standard

Git is the most broadly adopted tool of its kind. 

Git also means that many third party software tools and services are already integrated with Git including IDEs, and our own tools like DVCS desktop client Sourcetree, issue and project tracking software, Jira, and code hosting service, Bitbucket.

+++

Git is a quality open source project

Git is a very well supported open source project with over a decade of solid stewardship.

Git enjoys great community support and a vast user base. Documentation is excellent and plentiful, including books, tutorials and dedicated web sites. 

+++

Criticism of Git

One common criticism of Git is that it can be difficult to learn. Some of the terminology in Git will be novel to newcomers and for users of other systems

---

Git Tutorial

+++

What is a Git repository?

A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed. 

+++

@snap[north span-100]
@size[1.5em](How it works)
@snapend

@snap[center span-80]
![Logo](assets/img/git-operations.png)
@snapend

+++
## Three Trees of Git

@ol(false)
- The working directory
- Staging index
- Commit history
@olend

+++
The working directory

The first tree we will examine is "The Working Directory". This tree is in sync with the local filesystem and is representative of the immediate changes made to content in files and directories.

+++
Staging index

Next up is the 'Staging Index' tree. This tree is tracking Working Directory changes, that have been promoted with git add, to be stored in the next commit. This tree is a complex internal caching mechanism. Git generally tries to hide the implementation details of the Staging Index from the user.

+++

Commit history

The final tree is the Commit History. The git commit command adds changes to a permanent snapshot that lives in the Commit History. This snapshot also includes the state of the Staging Index at the time of commit.


+++
## Initializing a new repository: 

[git init](https://git-scm.com/docs/git-init)

To create a new repo, you'll use the git init command. git init is a one-time command you use during the initial setup of a new repo. Executing this command will create a new .git subdirectory in your current working directory. This will also create a new master branch. 

DEMO @note[create a local repository]

+++

## Saving changes

When working in Git, or other version control systems, the concept of "saving" is a more nuanced process than saving in a word processor or other traditional file editing applications. The traditional software expression of "saving" is synonymous with the Git term "committing"

Git committing is an operation that acts upon a collection of files and directories.

+++

## Saving changes

[git add](https://git-scm.com/docs/git-add)

The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way—changes are not actually recorded until you run git commit.

In conjunction with these commands, you'll also need git status to view the state of the working directory and the staging area.

+++

## Saving changes

the staging area

Instead of committing all of the changes you've made since the last commit, the stage lets you group related changes into highly focused snapshots before actually committing it to the project history. This means you can make all sorts of edits to unrelated files, then go back and split them up into logical commits by adding related changes to the stage and commit them piece-by-piece

+++

## Saving changes

[Git commit](https://git-scm.com/docs/git-commit)

Stores the current contents of the index in a new commit along with a log message from the user describing the changes.

+++

## Saving changes

[Git diff](https://git-scm.com/docs/git-diff)

Diffing is a function that takes two input data sets and outputs the changes between them. git diff is a multi-use Git command that when executed runs a diff function on Git data sources. 

git diff can be run on binary files. Unfortunately, the default output is not very helpful.

+++

## Saving changes

[.gitignore](https://git-scm.com/docs/gitignore)

Git sees every file in your working copy as one of three things:

    tracked - a file which has been previously staged or committed;
        untracked - a file which has not been staged or committed; or
            ignored - a file which Git has been explicitly told to ignore.


+++
## Inspecting a repository

[git status](https://git-scm.com/docs/git-status)

The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git. Status output does not show you any information regarding the committed project history. For this, you need to use git log.

+++
## Inspecting a repository
[git log](https://git-scm.com/docs/git-log)

+++
git syncing

The git remote command lets you create, view, and delete connections to other repositories. Remote connections are more like bookmarks rather than direct links into other repositories. Instead of providing real-time access to another repository, they serve as convenient names that can be used to reference a not-so-convenient URL.

+++

[git clone](https://git-scm.com/docs/git-clone)

git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository. 

+++

[git pull](https://git-scm.com/docs/git-pull)
The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content. Merging remote upstream changes into your local repository is a common task in Git-based collaboration work flows.

The git pull command is actually a combination of two other commands, git fetch followed by git merge.

+++

[git push](https://git-scm.com/docs/git-push)
The git push command is used to upload local repository content to a remote repository. Pushing is how you transfer commits from your local repository to a remote repo. It's the counterpart to git fetch, but whereas fetching imports commits to local branches, pushing exports commits to remote branches. 

+++
## Finding what is lost: Reviewing old commits
The whole idea behind any version control system is to store “safe” copies of a project so that you never have to worry about irreparably breaking your code base. Once you’ve built up a project history of commits, you can review and revisit any commit in the history.

+++

## Viewing an old revision

git checkout

You can look at files, compile the project, run tests, and even edit files without worrying about losing the current state of the project. Nothing you do in here will be saved in your repository. To continue developing, you need to get back to the “current” state of your project

Checking out a specific commit will put the repo in a "detached HEAD" state. This means you are no longer working on any branch. In a detached state, any new commits you make will be orphaned when you change branches back to an established branch. Orphaned commits are up for deletion by Git's garbage collector. 

From the detached HEAD state, we can execute git checkout -b new_branch_without_crazy_commit. This will create a new branch named new_branch_without_crazy_commit and switch to that state.

+++

## How to undo a commit with 

[git reset](https://git-scm.com/docs/git-reset)

The git reset command is a complex and versatile tool for undoing changes. It has three primary forms of invocation. These forms correspond to command line arguments --soft, --mixed, --hard. The three arguments each correspond to Git's three internal state management mechanism's, The Commit Tree (HEAD), The Staging Index, and The Working Directory.


---
## Github

@fa[github fa-3x]

+++

GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.


+++

## DEMO

@ul
- Create a repo
- Clone a repo
- Open and manage issues
- Gist
- [Git GUI](https://git-scm.com/downloads/guis/)
@ulend
---

## References

@ol[](false)
- [Bitbucket](https://www.atlassian.com/git/tutorials)
- [Github guides](https://guides.github.com/)
@olend
