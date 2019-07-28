# Quick start to Git and GitHub for Managing Your Research

## Git

[Git](https://git-scm.com/?source=post_page---------------------------) is a free and open source distributed vesion control system (VCS), which allows you to backup your file changes and track those changes in case you screw up something. It's by far the most popular VCS both for individual and company use. 

## Why we choose Git

Here are [seven reasons](https://codeburst.io/number-one-piece-of-advice-for-new-developers-ddd08abc8bfa) that you should be using **Git**.

*1. Version Control*

Every version of your code or work is available to you. It's different than the `save` command in Microsoft Word. With Git, every time you commit/upload your code, Git will create a local message to record your changes. So you never lose any changes because they are all saved in the git repository. If you want to revert back three months on a project, you can use a very simple Git command to do that.

*2. Branches*

![Git_branch](img/git_branch.png)

In Git repository, every change is organized as the time sequence. In some point, you may come up with new ideas to test. 

For instance, you want to build a **Rotational-Raman lidar**. In the beginning, you may think about applying the double-grating to extract the Rotation-Raman signal. But when you finish all the lidar hardware and try to install the double-grating, you may think what about using Narrowband IFs (Feature one) or Etalons (Feature two). Then at this point, you can setup new branches to really try those nice ideas without influencing the original plan (master). 

Git will allow you to create branches at any point and you can also track the changes at each branch, and roll back if you found this idea is like shit.

*3. Working in teams*

Unlike the centralized VCS, which allows only one repository to save the code and documents, Git will enable to create your own repository. 

Git simplifies the process of working with other people and makes it really easy to collaborate on projects. Everybody can have a copy of the project and start the development locally. And then push their own cool features to the project. Everyone in the group can decide whether to accept the feature and merge it into the code.

## How to use Git

First of all, if you don't install `Git`, you need to download it, which you can follow the instructions in [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

The basic operations in Git are: 

- Initialize
- Add
- Commit 
- Pull
- Push

Some advanced Git operations are:

- Branching
- Merging
- Rebasing

Below is the architecture of Git:

![Git_workflow](img/git_operations.png)

*1. Initialize the Git repository*

> Git is a command line tool, which means you need to type in each command to really apply each operation.

- Windows only: Go to your project folder. Right click and select 'Git Bash here'. This will activate the Git terminal for you.

![Git_Bash](img/Git_Bash_windows.png)

In the Git terminal, type in 

```
git init
```

- Linux or MacOS: 

```
cd work_folder
git init
```

`git init` creates an empty Git repository or re-initializes an existing one. It basically creates a `.git` folder in the work directory, which will save all the changes you will make in this work directory.

*2. add and commit your changes to Git*

After you intialize the Git repository, Git will detect any your changes inside the work directory. You can use `git status` to see your changes. 

Let's say it's an empty work directory before, and now you create two files: **MUA1.txt** and **MUA2.txt**.

![git_status](img/git_status.png)

Right now, you still didn't tell Git to record your changes. In order to do that, you need two steps: `git add MUA1.txt MUA2.txt` and `git commit -m "add MUA1 and MUA2"`. The first command will tell git to remember the changes and the second command will tell git to put a group of changes into the branch. One git commit can contain a lot of changes, which you will do during a couple of days. After the commit, the changes are fixed and they can be rolled back according to commit number.

![git_add](img/git_add.png)

*3. pull from and push to remote git repository*

As we mentioned before, Git enables teamwork. Git provides two mechanisms to synchronize your work with others: `git pull` and `git push`. The former one can help you download the work from remote repository and the latter can upload your work. 

Before you use these two commands, you need to tell which repository you want to synchronize with. This is done with using `git remote add origin <url>`. The **url** is the bridge to connect you with others. Normally you can go to the next chapter of [GitHub](#github) to know how to get this **url** easily.



## GitHub

### What is GitHub

### How to use GitHub

## Workflow of Git and GitHub

## Examples

## References

[1] https://www.quora.com/What-is-Git-and-why-should-I-use-it
[2] https://www.liaoxuefeng.com/wiki/896043488029600