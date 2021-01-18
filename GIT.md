### Step1:  Create a local git repo

```shell
git init
```

Go to the folder where you want to put the project in, and It will initialize a git repo here.



### Step2: Add a new file

Git will **NOT TRACK** the new file in the repo unless you tell it to do so, by `git add [filename]`. After being tracked, the file can be committed by `git commit `.

The whole process:

```shell
#First add the file into staging environment
#add: 添加到缓存区
git add [filename]

#Create a commit from staging environment
#commit: 添加到本地库
git commit -m "Your message about this commit..."
```

Message is important for future.



### Step3: Create a new branch

> A branch in Git is simply a lightweight movable pointer to one of these commits.

Branches allow you to move back and forth between different versions of the project. It's safe to modify the branches rather than the origin.

```shell
#Show all branches
git branch -a

#Create a new branch
git branch [branchname]

#Switch to this branch
git checkout [branchname]

#Swith to the branch if exists, or create if not
git checkout -b [branchname]

#Delete the branch
git branch -d [branchname]
git branch -D [branchname]

```





### Step4: Push a branch onto GitHub repo

Now we will push the commit in the branch onto GitHub repo, then merge it into the primary branch if approved.

```shell 
git push [remote_branch] [your_local_branch]
```

Note that git will create an alias name **origin** for remote branch.



```shell
git merge [branchname]
```

Note that you need to switch to the master branch first if you want this branch be merged into master. 



### Step5: Create a pull request (PR)

Now A pull request is a way to alert the owner about the new uploaded branch.

