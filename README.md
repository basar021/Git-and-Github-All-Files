# Git & GitHub Documentation

### Tutorial - 2 -> Introduction to git and GitHub

1. git?
    - git is a version control software
    - It keep track of code changes
    - It helps to collaborate in a project
    - It is installed and maintained locally
    - It provides Command Line Interface (CLI)
    - Released in April 7, 2005
    - Developed by Linus Torvalds & Junio C Hamano
2. github?
    - GitHub is a hosting service where we can keep our git repositiory/folders
    - It is maintained on cloud/web
    - It provides Graphical User Interface (GUI)
    - Founded in 2008

### Tutorial - 3 -> How to set git environment and configuration

    -> Download and install git on your pc: https://git-scm.com/
    -> check git version: open terminal or cmd then use the command `git --version`
    to find out whether git is installed or not. if git is installed it will
    return a version number of git.

\*\* git configuration

1.  check all configuartion options: `git config`
2.  set global user name and user email for all repository/git folders (if you
    want to set different username and email for different git repository then
    remove --global)
    -   set global user name: `git config --global user.name "basar021"`
    -   set global user email:
        `git config --global user.email "mrwebcoder.me@gmail.com"`
3.  list all git configuration:
    -   list all the configuration: `git config --list`
    -   list user name: `git config user.name`
    -   list user email: `git config user.email`
4.  change global username & email
    -   change global user name:
        `git config --global user.name "PUT_NEW_USER_NAME_HERE"`
    -   change global user email:
        `git config --global user.email "PUT_NEW_USER_EMAIL_HERE"`

### Tutorial - 4 -> creating git repo and adding new files

1.  creating a git folder

-   ls -a : list all files inside of a directory

    ```
    mkdir DIRECTORY_NAME_HERE
    cd DIRECTORY_NAME_HERE
    git init

    Example:
    mkdir T-4
    cd T-4
    git init
    ls -a
    ```

2.  adding new files in git folder

-   git status : displays the state of the working directory and staging area

    ```
    ls -a
    echo > fineName.extension or touch fileName.extension
    start fileName.extension / open fileName.extension
    git status

    Example:
    echo > day1.txt or touch day1.txt
    start day1.txt or open day1.txt
    write something inside the file
    ```

-   Git is aware of the file but not added to our git repo
-   Files in git repo can have 2 states – tracked (git knows and added to git
    repo), untracked (file in the working directory, but not added to the local
    repository)
-   To make the file trackable stagging or adding is required

### Tutorial - 5 -> how to add files in staging area & remove files

1.  adding files to stagging area:

-   `git add fileName` add a file in staging area / index
-   `git add .` add all files of directory to stagging area not subdirectory
-   `git add -A` add all files of directory and subdirectory to stagging area
-   `git rm --cached fileName` unstage a file from staging area
-   `git diff` - checking the differences of a staged file
-   `git restore fileName` - restore the file

### Tutorial - 6 -> practice-1

### Tutorial - 7 -> commit & uncommit

-   `git commit -m "message"` move the file to local repository from stagging
    area
-   `git add . && git commit -m "message"` stagging and commit at the same time
    or if it not working then follow this method ->
    `git add -A ; git commit -m "message"`
-   `git add -A ; git commit -m "message"` stagging and commit at the same time
-   `git log` check the commit history

-   `git reset --soft HEAD^` uncommit the commit in HEAD and move to staging
    area
-   `git reset --soft HEAD~2` it's uncommit 2 commits
-   `git reset --soft HEAD~3` it's uncommit 3 commits
-   `git reset HEAD^` uncommit the commit in HEAD and move to unstaging /
    working area
-   `git reset --hard HEAD^` uncommit the commit in HEAD and delete the commit
    completely with all the changes

### Tutorial - 8 -> git HEAD and undo theory

-   `git log` check the commit history
-   `git log --oneline` -> just show one line -> commit id(7 character), HEAD
    and massage
-   `git show` -> show last commit detail
-   `git show HEAD^` -> show previous number commit detail
-   `git show commit-id` -> show detail information for a specific commit
-   `git checkout commit-id` -> go to specific commit
-   `git checkout filename` -> it discard(cancel)/undo that was changed or
    modification
-   `git checkout master` -> it restore all file

### Tutorial - 9 -> git HEAD and undo practical

### Tutorial - 10 -> git revert

### Tutorial - 11 -> git ignore

-   create a .gitignore file and add the things you do not want to add in the
    stagging area
-   Inside .gitignore we can keep secret files, hidden files, temporary files,
    log files
-   `secret.txt` secret.txt will be ignored
-   `*.txt` ignore all files with .txt extension
-   `!main.txt` ignore all files with .txt extension without .main.txt
-   `test?.txt` ignore all files like test1.txt, test2.txt, test3.txt
-   `temp/` all the files in temp folders will be ignored

### Tutorial - 12 -> how to create github repository and commits

-   sign in to your github account
-   create a git repo

### Tutorial - 13 -> README.md

--- Markdown---

1. what & README.md?
2. How to make a comment
3. Normal text & new line
4. Horizental rule
5. Heading
6. Paragraph
7. italic
8. bold
9. strikethrough
10. inline code block
11. multiple line code block
12. List
13. Link
14. Image
15. Emoji
16. Table

-   6 heading levels: number of hashes define heading levels. check the
    following examples:
    -   `# heading 1 level text is here`
    -   `## heading 2 level text is here`
-   bold syntax: `**text goes here**`
-   italic syntax: `_text goes here_`
-   bold and italic syntax: `**_text goes here_**`
-   strikethrouh syntax: `~~this is~~`
-   single line code syntax: `` place code inside backticks
-   multiple line code syntax: ``` place code inside three open and closing
    backticks
-   multiple line code syntax language specific: ```html for specific lanaguage
    use language name when starting; not closing
-   Ordered List syntax

        ```
             1. HTML
              2. CSS

                 1. Fundamental
                 2. CSS Architecture - BEM
                 3. CSS Preprocessor - SASS

              3. JS
        ```

-   Unordered List syntax ->
    ```
     - html
     - css
       - Fundamental
       - CSS Architecture - BEM
       - CSS Preprocessor - SASS
     - js
    ```
-   Task List
    ```
       - [x] Task1
       - [x] Task2
       - [x] Task3
    ```
-   adding link

    ```
       <!-- automatic link -->

       http://www.studywithanis.com

       <!-- markdown link syntax -->
       [title](link)
       [studywithanis](http://www.studywithanis.com)
       [studywithanis][websitelink]

       <!-- all link is here  -->

       [websitelink]: http://www.studywithanis.com

    ```

-   adding image syntax -> `![alt text](imageURL)`
    `![1800 milestone](https://i.postimg.cc/qvZpmxKF/1-800-Uploads-Milestone.png)`

-   adding emoji  
     [emoji src](https://getemoji.com/) ### Smileys 😀 😃 😄 😁 😆 😅 😂 🤣 🥲 ☺️
    😊 😇 🙂 🙃 😉 😌 😍 🥰 😘 😗 😙 😚 😋 😛 😝 😜 🤪 🤨 🧐 🤓 😎 🥸 🤩 🥳 😏 😒
    😞 😔 😟 😕 🙁 ☹️ 😣 😖 😫 😩 🥺 😢 😭 😤 😠 😡 🤬 🤯 😳 🥵 🥶 😱 😨 😰 😥 😓
    🤗 🤔 🤭 🤫 🤥 😶 😐 😑 😬 🙄 😯 😦 😧 😮 😲 🥱 😴 🤤 😪 😵 🤐 🥴 🤢 🤮 🤧 😷
    🤒 🤕 🤑 🤠 😈 👿 👹 👺 🤡 💩 👻 💀 ☠️ 👽 👾 🤖 🎃 😺 😸 😹 😻 😼 😽 🙀 😿 😾

        ### Gestures and Body Parts
        👋 🤚 🖐 ✋ 🖖 👌 🤌 🤏 ✌️ 🤞 🤟 🤘 🤙 👈 👉 👆 🖕 👇 ☝️ 👍 👎 ✊ 👊 🤛 🤜 👏 🙌 👐 🤲 🤝 🙏 ✍️ 💅 🤳 💪 🦾 🦵 🦿 🦶      👣 👂 🦻 👃 🫀 🫁 🧠 🦷 🦴 👀 👁 👅 👄 💋 🩸

-   adding table
    ```
       table syntax
       | heading1 | heading2 |
       | ----- | ----- |
       | data1 | data2 |
       | data3 | data4 |
       | data5 | data6 |
    ```

### Tutorial - 14 -> Connecting local repo to remote repo

-   check remote connection: `git remote` or `git remote -v`
-   `git remote add name <REMOTE_URL>` example: git remote add origin http://...
-   to clone a remote repository: `git clone <REMOTE_URL>`

### Tutorial - 15 -> push and pull

-   push `git push -u origin`
-   push a branch `git push -u origin branch_name`
-   push all branches `git push --all`
-   pull from a repo: `git pull` which is equivalent to git fetch + git merge

### Tutorial - 16 -> branching and merging

-   Branch is a new and separate branch of master/main repository
-   create a branch `git branch branch_name`
-   List branches `git branch`
-   move to a branch `git checkout branch_name`
-   create and move to a branch `git checkout -b branch_name`
-   delete a branch: `git branch -d branch_name`
-   List all remote branches `git branch -r`
-   List all local & remote branches `git branch -a`
-   See the 'Note about fast-forwards' in `git push --help` for details
-   push local to remote branches `git push -u origin branch_name`
-   merge branches:
    ```
      git checkout branchName
      git merge branchName
    ```
-   `git log --oneline --all --graph`

### Tutorial - 17 -> branching and merging locally

-   create a branch `git branch branch_name`
-   List branches `git branch`
-   move to a branch `git checkout branch_name`
-   create and move to a branch `git checkout -b branch_name`
-   must active master/main branch before merging `git checkout master/main`
-   merge in master/main branch from other branch `git merge branchName`

### Tutorial - 18 -> git and GitHub practice - 2

1. How to create git repository
    - `mkdir foldername`
    - `git init`
2. How to add files (such as .gitignore and README.md)
    - `echo > filename.extention`
3. How to stage changes
    - `git add .`
4. How to commit changes
    - `git commit -m "message"`
5. How to create branch and switch to branch
    - to check active branch and all branches `git branch`
    - `git branch branchName`
    - `git checkout branchName` or
    - `git checkout -b branchName`
6. How to make changes in new branch
    - create a file and add some text -> `echo > test.txt`
7. How to merge branches

-   must active master/main branch before merging `git checkout master/main`
-   merge in master/main branch from other branch `git merge branchName`

8. How to connect local repo and remote repo
    - at first create a new repository in Github Account
    - and add this in command line
      `git remote add origin https://github.com/basar021/git-github-practise.git`
    - git push `git push -u origin master`
9. How to push changes
    - `git pull`
    - `git push -u origin master`
10. How to make changes in GitHub
    - add some text in test.txt file in Github
11. How to pull GitHub changes in locl repository
    - create a new branch -> feature2
    - then add some text in test.txt file from feature2 branch in Github
    - then pull request and merge feature2 -> master branch
    - `git pull`

### Tutorial - 19 -> GitHub Issues

### Tutorial - 20 -> fast-forward merge in Git - 2-way merges

-   Reeference:

    -   https://git-school.github.io/visualizing-git/
    -   https://www.tutorialspoint.com/what-is-a-fast-forward-merge-in-git
    -   https://www.tutorialspoint.com/what-is-3-way-merge-or-merge-commit-in-git
    -   https://medium.com/@koteswar.meesala/git-fast-forward-merge-vs-three-way-merge-8591434dd350

    -   https://git-school.github.io/visualizing-git/
    -   `git commit -m "second commit"`
    -   `git commit -m "third commit"`
    -   `git branch feature`
    -   `git checkout feature`
    -   `git commit -m "fourth commit"`
    -   `git commit -m "fifth commit"`
    -   `git commit -m "sixth commit"`
    -   `git checkout master`
    -   `git merge feature`
    -   You have performed a fast-forward merge.

### Tutorial - 21 -> 3-way merges

-   Reeference:

    -   https://git-school.github.io/visualizing-git/
    -   https://www.tutorialspoint.com/what-is-a-fast-forward-merge-in-git
    -   https://www.tutorialspoint.com/what-is-3-way-merge-or-merge-commit-in-git
    -   https://medium.com/@koteswar.meesala/git-fast-forward-merge-vs-three-way-merge-8591434dd350

    -   https://git-school.github.io/visualizing-git/
    -   `git commit -m "second commit"`
    -   `git commit -m "third commit"`
    -   `git branch feature`
    -   `git checkout feature`
    -   `git commit -m "fourth commit"`
    -   `git commit -m "fifth commit"`
    -   `git commit -m "sixth commit"`
    -   `git checkout master`
    -   `git commit -m "seventh commit"`
    -   `git commit -m "eighith commit"`
    -   `git commit -m "ninth commit"`
    -   `git commit -m "tenth commit"`
    -   `git merge feature`
    -   `git log`
        > 1a6a093 Merge b19852b tenth commit 75b9263 ninth commit c4d77a0
        > eighith commit 0c6f7d8 seventh commit 3364a9d sixth commit b5df88d
        > fifth commit 264a758 fourth commit 1b08b75 third commit 299b2e7 second
        > commit e137e9b first commit

### Tutorial - 22 -> Resolve Merge Conflicts on Git

-   https://www.tutorialspoint.com/what-is-merge-conflict-in-git-how-to-handle-merge-conflicts

-   create directory -> `mkdir T-22-merge-conflicts`
-   `git init`
-   create file -> `echo > story.txt`
-   open file -> `start story.txt`
-   git add and commit -> `git add .` `git commit -m "added about bashar"` or
-   `git add -A ; git commit -m "added about bashar"`
-   create a new branch and moved -> `git checkout -b feature`
-   check files -> `ls`
-   `start story.txt`
-   `git add -A ; git commit -m "added some data from feature branch"`
-   `git checkout master`
-   `start story.txt`
-   `git add -A ; git commit -m "added some data from master branch in story.txt"`
-   `git merge feature` -> here must comes a conflict because you add some data
    in the same line in master and feature branches
-   `start story.txt` -> resolve conflict
-   `git add -A ; git commit -m "resolve conflict from master branch in story.txt"`

### Tutorial - 23 -> Resolve Merge Conflicts on GitHub

### Tutorial - 24 -> Fork clone and contribution a GitHub repository

### Tutorial - 26 -> How to create and setup Secure Shell SSH key

### Tags

In GitHub, "tags" typically refer to Git tags. Git tags are a way to mark
specific points in a Git repository's history as being important or significant.
They are often used to label specific commits, such as releases or version
numbers, to make it easier to reference those commits in the future.

Here's how Git tags work:

1. **Creating a Tag:** You can create a Git tag by running a command like
   `git tag <tag-name>`, where `<tag-name>` is the name you want to give to the
   tag. For example, you might create a tag for a release like this:
   `git tag v1.0.0`.

2. **Tagging Commits:** Tags are typically associated with specific commits.
   When you create a tag, it's linked to the current commit, but you can also
   specify a different commit if needed.

3. **Listing Tags:** You can list all the tags in a Git repository using the
   `git tag` command.

4. **Annotated vs. Lightweight Tags:** Git supports two types of tags: annotated
   and lightweight. Annotated tags are recommended for most use cases because
   they store extra metadata like the tagger's name, email, date, and a tagging
   message. Lightweight tags are just a name for a specific commit and don't
   include extra information.

5. **Pushing Tags:** By default, when you push changes to a remote Git
   repository, tags are not automatically pushed. You need to use
   `git push --tags` to push tags to a remote repository. This is important when
   you want to share tags, especially when creating releases on GitHub.

6. **Using Tags on GitHub:** On GitHub, you'll often see tags associated with
   releases. When you create a release on GitHub, it typically creates a Git tag
   behind the scenes to mark the specific commit associated with that release.
   Users can then download or reference that release by its tag name.

GitHub also has its own concept of "releases" that are closely related to Git
tags. A release on GitHub is a way to package and distribute software versions,
and it often corresponds to a Git tag. When you create a GitHub release, you can
upload release assets (e.g., binaries, documentation) and provide release notes.

In summary, GitHub tags are essentially Git tags, and they are used to mark
important points in a repository's history, often associated with releases or
significant commits. They help users easily reference and work with specific
versions of a project.
