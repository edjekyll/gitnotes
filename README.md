Git notes from [http://try.github.io/](http://try.github.io/)

###1.1 Got 15 minutes and want to learn Git?
Git allows groups of people to work on the same documents (often code) at the same time, and without stepping on each other's toes. It's a distributed version control system.

Our terminal prompt below is currently in an octobox directory. To initialize a Git repository here, type the following command: git init

<pre>
> git init

Initialized empty Git repository in /.git/
</pre>

<pre>
edjekyll@ubuntu:~/gitnotes$ git init
Initialized empty Git repository in /home/edjekyll/gitnotes/.git/
</pre>

Advice
Directory:
A folder used for storing multiple files.

Repository:
A directory where Git has been initialized to start version controlling your files.

Clicky Click:
Click on the instructions preceded by an arrow. They will be copied into the terminal prompt.

The .git directory
On the left you'll notice a .git directory. It's usually hidden but we're showing it to you for convenience.

If you click it you'll notice it has all sorts of directories and files inside it. You'll rarely ever need to do anything inside here but it's the guts of Git, where all the magic happens.

###1.2 Checking the Status
Good job! As Git just told us, our octobox directory now has an empty repository in /.git/. The repository is a hidden directory where Git operates.

To save your progress as you go through this tutorial -- and earn a badge when you successfully complete it -- head over to create a free Code School account. We'll wait for you here.

Next up, let's type the git status command to see what the current state of our project is: git status

<pre>
$ git status
 
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
</pre>

Advice
Tip:
It's healthy to run git status often. Sometimes things change and you don't notice it.

###1.3 Adding & Committing
I created a file called octocat.txt in the octobox repository for you (as you can see in the browser below).

You should run the git status command again to see how the repository status has changed: git status

<pre>
$ git status

# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	octocat.txt
nothing added to commit but untracked files present (use "git add" to track)
</pre>

<pre>
edjekyll@ubuntu:~/gitnotes$ touch README.md
edjekyll@ubuntu:~/gitnotes$ git status
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       README.md
nothing added to commit but untracked files present (use "git add" to track)
</pre>

Advice
staged:
Files are ready to be committed.

unstaged:
Files with changes that have not been prepared to be commited.

untracked:
Files aren't tracked by Git yet. This usually indicates a newly created file.

deleted:
File has been deleted and is waiting to be removed from Git.

###1.4 Adding Changes
Good, it looks like our Git repository is working properly. Notice how Git says octocat.txt is "untracked"? That means Git sees that octocat.txt is a new file.

To tell Git to start tracking changes made to octocat.txt, we first need to add it to the staging area by using git add: git add octocat.txt

<pre>
$ git add octocat.txt

Nice job, you've added octocat.txt to the Staging Area
</pre>

<pre>
edjekyll@ubuntu:~/gitnotes$ git add README.md
edjekyll@ubuntu:~/gitnotes$ git status
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#       new file:   README.md
#
</pre>
