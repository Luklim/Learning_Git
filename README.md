1. 'git init'->powers your folder to br mamaged by git
and initializes a new empty repository.It also cretes a .git floder that has all
the releveant logic to manage version control.

2. 'Working area'->there can be a bunch of files that are not 
currently handeled by git.It means that changes
done in those files are not managed by git yet.
A file which is in working area is considered not to be in staging area.
When we do 'git status' and we see a bunch of 
'untracked files' then these are actually called to be in 
working area.

3. 'Staging are'->what all files are goint to be the part of the next version we will create.
This staging area is the place where git knows what changes will be done from the last version 
to the next version.

4. 'repository area'-> this area acutally contains the details of all your previous registered versions and 
the files in the area,git already manages them and knows their version history.

5. 'git add <file>'->moves file from working area to staging area.

6. 'git rm --cached <file>'->moves file from staging area to working area.

7. 'commit'-> commit is a particular version of the project.It caputres a snapshot of the project'seestaged changes
and creates a version out of it.

8. 'git commit' ->registers staging changes to commit.A version  is created.

9. 'git log' ->lists down all commits of th repo.If you want to exit out of git log prompt 
press 'q'. 

10. 'git restore' -> it removes all file from the staging area to be committed.
This can we be useful ,if you did some dirty piece of code and now no more wants it .Instead of deleting every changes
line by line, we can restore it or you can say restore last clean version of the file.

11. All the changes doneafter the last commit are still in the working area, so to take the chanegs to the staging area ,
git add README.txt

12. 'git restore --staged README.txt'-> removes the area that was previously added to staged area back to the working area.
This only works if changes are in staging  area.

13. Difference between rm and restore :If we want to move the whole file back to the untracked state, the we do git rm, 
otherwise id we just want the changes to be moved in working area or staging area then we do git restore.To use git rm,
there must be nothing in the staged area after a commit.

14. 'git diff'-> gives the difference of all file changes between two commits.

15. 'git commit -m "your commit message"->if you want to avoid opening a text editor like add commit message we
use this following command.

16. 'git remote'->lists down all remote connections.

17. Remote connections->helps us to link two git repositories for uploading and downolading 
changes from each other.

18. 'git remote add <name of remote> <link of remote>'-> this command is to add a new link to the 
remote repo and give it a name.

19. 'git remote re <name of remote>'->this is to delete a remoteconnection.

20. 'git remote rename <oldname> <newname>'-> this command renames a remote connection.

note: the name of the remote connections is always used to establish communications between repos.

21. 'git add <file1> <file2> <file3>' : this command will add multiple file changes together in the staging area.

22. 'git add . ' -> this command will add all files from working repo to staging area.In current folder, add all of the files to the staging area.

23. 'git pull <remote name> <branch name>' : downloads latest changes from the branch of the mentioned remote to my local repo. [here local: PC from github]

24. Recommended Paractice to do:
-make changes 
-git add <files>
-git commit
-git pull
-git push

25. merge confilcts can occur if multiple people try to make changes to the same file in collaboration.

26. 'git stash'-> suppose say we wish to no commit a file but also not delete it, except for that file we wish to commit all other file in the folder as soon as adding the file "git add <filename>" use the command git stash.Ther must be an initial commit though. Stashed files is not visible in git status.

27. 'git list'-> gives the stashed file.

28. 'git stash apply' ->bring the stash back. Whatever is the last stash will be unstashed.

29. 'git stash show stash@{1}' -> shows the contents of the 1st stash.