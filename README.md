$ git config --global user.name "CodeHippo"
        >for user name
$ git config --global user.email "sanjibsil98@gmail.com"
        >for user email

$ cd >for change directry
$ cd ..+Enter >for get out from directory
$ mkdir >for new directory 
-------->i create (mkdir LocalRepo) file name (LocalRepo).
$ ls -a >for checking the hidden file in repo.
$ git init 
        ----->Initailized empty git Repository in c:/Users/ASUS/Onedrive/Desktop/gitdemo/LocalRepo/.git/

before push we have to run a command 
$ git remote add origin <-link->
---------$ git add <-file name-> / $ git add .>for add in Github REpo
         
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Astyle.css
        new file:   Boxm.html
        new file:   a1.jpg
        new file:   a10.jpg
        new file:   a11.jpg
        new file:   a12.jpg
        new file:   a2.jpg
        new file:   a3.jpg
        new file:   a4.jpg
        new file:   a5.jpg
        new file:   a6.jpg
        new file:   a7.jpg
        new file:   a8.jpg
        new file:   amazon.html
        new file:   amazon_logo.png
        new file:   box1_image.jpg
        new file:   box3_image.jpg
        new file:   box4_image.jpg
        new file:   hero1.jpg
        new file:   hero2.jpg
        new file:   hero3.jpg
        new file:   hero4.jpg
        new file:   hero5.jpg
        new file:   hero6.jpg
        new file:   hero7.jpg
        new file:   hero_image.jpg
        new file:   index.html
        new file:   pexels-tom-fisk-3023502.jpg
        new file:   pngimg.com - amazon_PNG3.png
        new file:   style.css
************ready for comitted*********

ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git commit -m "Amazon Clone"
[master (root-commit) df5369f] Amazon Clone
 30 files changed, 548 insertions(+)
 create mode 100644 Astyle.css
 create mode 100644 Boxm.html
 create mode 100644 a1.jpg
 create mode 100644 a10.jpg
 create mode 100644 a11.jpg
 create mode 100644 a12.jpg
 create mode 100644 a2.jpg
 create mode 100644 a3.jpg
 create mode 100644 a4.jpg
 create mode 100644 a5.jpg
 create mode 100644 a6.jpg
 create mode 100644 a7.jpg
 create mode 100644 a8.jpg
 create mode 100644 amazon.html
 create mode 100644 amazon_logo.png
 create mode 100644 box1_image.jpg
 create mode 100644 box3_image.jpg
 create mode 100644 box4_image.jpg
 create mode 100644 hero1.jpg
 create mode 100644 hero2.jpg
 create mode 100644 hero3.jpg
 create mode 100644 hero4.jpg
 create mode 100644 hero5.jpg
 create mode 100644 hero6.jpg
 create mode 100644 hero7.jpg
 create mode 100644 hero_image.jpg
 create mode 100644 index.html
 create mode 100644 pexels-tom-fisk-3023502.jpg
 create mode 100644 pngimg.com - amazon_PNG3.png
 create mode 100644 style.css
 *************commit done************

 ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git status
On branch master
nothing to commit, working tree clean

**************before push*********

$ git remote add origin <-link->
=$ git remote add copycat <-link-> 

---------origin >origin is a name that you can change [in this git repo i change the name of origin "copycat"]
---------link > (<-link copied from github-> )
         $ git remote add copycat https://github.com/CodeHippo-sanjib/clone-webpage.git

ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git remote add copycat https://github.com/CodeHippo-sanjib/clone-webpage.git


ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git remote -v     (to verify remote)
copycat https://github.com/CodeHippo-sanjib/clone-webpage.git (fetch)
copycat https://github.com/CodeHippo-sanjib/clone-webpage.git (push)

**********name change***********
local machine           remote/github
LocalRepo               clone-webpage

ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (main)
$ git branch (to check branch)
* main

# what is branch ???????????
------Working with Git Branches
In Git, a branch is a new/separate version of the main repository.

Let's say you have a large project, and you need to update the design on it.

How would that work without and with Git:

Without Git:

Make copies of all the relevant files to avoid impacting the live version
Start working with the design and find that code depend on code in other files, that also need to be changed!
Make copies of the dependant files as well. Making sure that every file dependency references the correct file name
EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
Save all your files, making a note of the names of the copies you were working on
Work on the unrelated error and update the code to fix it
Go back to the design, and finish the work there
Copy the code or rename the files, so the updated design is on the live version
(2 weeks later, you realize that the unrelated error was not fixed in the new design version because you copied the files before the fix)
With Git:

With a new branch called new-design, edit the code directly without impacting the main branch
EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
Create a new branch from the main project called small-error-fix
Fix the unrelated error and merge the small-error-fix branch with the main branch
You go back to the new-design branch, and finish the work there
Merge the new-design branch with main (getting alerted to the small error fix that you were missing)
Branches allow you to work on different parts of a project without impacting the main branch.

When the work is complete, a branch can be merged with the main project.

You can even switch between branches and work on different projects without them interfering with each other.

Branching in Git is very lightweight and fast!

ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git branch
* master    {github main branch is a default branch.----master branch is not main branch-----we have rename master branch as main branch}

ASUS@LAPTOP-VFEQNECK MINGW64 ~/OneDrive/Desktop/gitdemo/LocalRepo (master)
$ git branch -M main    (to rename branch)

PUSH UPSTREAM******************
$ git push -u copycat main
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 12 threads
Compressing objects: 100% (32/32), done.
Writing objects: 100% (32/32), 6.62 MiB | 1.81 MiB/s, done.
Total 32 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/CodeHippo-sanjib/clone-webpage.git
 * [new branch]      main -> main
branch 'main' set up to track 'copycat/main'.

ORIGIN=COPYCAT

**********Git Branches*********

PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git --version
git version 2.42.0.windows.2
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git branch
* main
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git checkout -b feature1
Switched to a new branch 'feature1'
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git branch
* feature1
  main
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git checkout main
Switched to branch 'main'
Your branch is up to date with 'copycat/main'.
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git branch       
  feature1
* main
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git checkout feature1
Switched to branch 'feature1'
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git branch
* feature1
  main
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git checkout -b feature2
Switched to a new branch 'feature2'
PS C:\Users\ASUS\OneDrive\Desktop\gitdemo\LocalRepo> git branch
  feature1
* feature2
  main

  ---exseptional---
  Hi i am sanjib sil.i am a coder based on kolkata .