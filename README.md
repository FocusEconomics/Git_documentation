# Git - Manual


Git is a free and open-source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It can be used in different platforms such as Gitlab, Github or Azure DevOps.

As Git is the technology behind we can use the same commands on all these platforms.

There are two options create a new repository or clone a repository to your local device.

## 1. Create a new repository:

- 1.1. We go to Github https://github.com/:

In Repositories, we can create a new repository (go to step 2) or clone an existing repository (go to step 3). In case we create a new repository do not add README or .ignore by default (in case you want to do this way then you should clone the repository to your local folder as is shown in step 3).

## 2. If we start a new repository and we already have files in our folder:

- 2.1. Init a new repository in the folder.

```bash
git init
```

- 2.2. add files

```bash
git add .
```

In case we want only add some files:

```bash
git add file_example.txt second_file.py
```

- 2.3. Commit your current version <- you can come back to this commit if needed in the future
To commit changes to your local repository, use the git commit command:

```bash
git commit -m "first commit"
```

- 2.4. Now, we can remotely add the repository that we created in point 1.

```bash
git remote add origin https://github.com/Your_Git_Name/Repository_Name.git
```

- 2.5. **Push** your work to the remote repository

```bash
git push -u origin master
```
This will push your commits to the master branch of the origin repository.

## 3. In case the repository is already in the remote repository you can clone in your local:

```bash
git clone https://github.com/user/repo.git
```
This will create a local copy of the repository in a new directory.

## 4. In case we already clone or init a repository in our local, we can **pull** the latest changes from a remote repository:

```bash
git pull origin master
```


# Good practices

## Create a README
from git bash (a simulator of GNU/Linux command line as cmd in Windows) we can create as follows:

```bash
echo "# Title example" >> README.md
```
This will create a markdown (`.md`) file with the title *Title example*.
As well we can create a .txt and then change the format to `.md`.

The README file could be the documentation of the files and scripts that the repository contains. You can find an easy markdown tutorial in this [link](https://www.markdownguide.org/basic-syntax/).


## Create a branch
A good practice is to create a new branch each time you want to fix some bug or add new features. To create a new branch we will do the following:

```bash
git branch branch_name
```

or

```bash
git checkout -b branch_name
```
This last command will create a new *branch_name* and also switch to it.

You can switch over branches:

```bash
git checkout branch_name_to_switch
```

## Once the feature/bug is done we can merge our branch to **development** and **main/origin**:

- 1. Switch to the next branch in this case **development**:

```bash
git checkout development
```

- 2. Merge your branch into **development**:

```bash
git merge branch_name
```
This will merge the branch_name branch into the current branch (development).

You can do it again same steps from **development** to **main/origin**.

The workflow show looks like this:


<img src=".\git_workflow.png" alt="Git Workflow" />