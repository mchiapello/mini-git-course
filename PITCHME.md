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

Branching and merging. Having team members work concurrently is a no-brainer, but even individuals working on their own can benefit from the ability to work on independent streams of changes. Creating a "branch" in VCS tools keeps multiple streams of work independent from each other while also providing the facility to merge that work back together, enabling developers to verify that the changes on each branch do not conflict. Many software teams adopt a practice of branching for each feature or perhaps branching for each release, or both. There are many different workflows that teams can choose from when they decide how to make use of branching and merging facilities in VCS.

+++

@snap[north span-100]
@size[1.5em](Benefits of version control)
@snapend

### THIRD

Traceability. Being able to trace each change made to the software and connect it to project management and bug tracking software such as Jira, and being able to annotate each change with a message describing the purpose and intent of the change can help not only with root cause analysis and other forensics. Having the annotated history of the code at your fingertips when you are reading the code, trying to understand what it is doing and why it is so designed can enable developers to make correct and harmonious changes that are in accord with the intended long-term design of the system. This can be especially important for working effectively with legacy code and is crucial in enabling developers to estimate future work with any accuracy.

---

## Git

@fa[git fa-3x]

+++

By far, the most widely used modern version control system in the world today is Git

open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel

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

## Initializing a new repository: git init

To create a new repo, you'll use the git init command. git init is a one-time command you use during the initial setup of a new repo. Executing this command will create a new .git subdirectory in your current working directory. This will also create a new master branch. 

DEMO @note[create a local repository]

+++

## Saving changes

When working in Git, or other version control systems, the concept of "saving" is a more nuanced process than saving in a word processor or other traditional file editing applications. The traditional software expression of "saving" is synonymous with the Git term "committing"

Git committing is an operation that acts upon a collection of files and directories.



## Github

@fa[github fa-3x]

+++

blablba

---

## References

https://www.atlassian.com/git/tutorials

