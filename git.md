**MOst use Commands:**

    $ touch .gitignore

    $ git init
    $ git add .

    $ git commit -m "initial commit"

    $ git status

    $ git remote add origin REPOSITORY NAME

    $ ssh-keygen -t rsa -b 4096 -c "your_email@codewithharry.com"
    $ tail <path to id_rsa.pub> # add this key to git hub
    $ cat PATH(/c/Users/Amit/.ssh/id_rsa.pub)

1.  What is git?

    => Git is a popular version control system(VCS).

        It is used for:

        - Tracking code changes
        - Tracking who made changes
        - Coding collaboration

2.  What does Git do?

    - Manage projects with Repositories
    - Clone a project to work on a local copy
    - Control and track changes with Staging and Committing
    - Branch and Merge to allow for work on different parts and versions of a project
    - Pull the latest version of the project to a local copy
    - Push local updates to the main project

3.  Configure Git:

    $ git config --global user.name amt-g
    $ git config --global user.email amit.gajare01@gmail.com

4.  git init => This command is used to start a new repository.

    Usage: git init [repository name]

5.  git clone => This command is used to obtain a repository from an existing URL.

    Usage: git clone [url]

6.  git add => This command adds a file to the staging area.

    Usage: git add [file] => for single file
    Usage: git add . => for one or more files

7.  git Branch => This command lists/shows all the local branches in the current repository.

    Usage: git branch => show branch
    Usage: git branch [branch name] => create new branches
    Usage: git branch -d [branch name] => delete branch
