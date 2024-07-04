1.'git init'->powers your folder to br mamaged by git
and initializes a new empty repository.It also cretes a .git floder that has all
the releveant logic to manage version control.

2.'Working area'->there can be a bunch of files that are not 
currently handeled by git.It means that changes
done in those files are not managed by git yet.
A file which is in working area is considered not to be in staging area.
When we do 'git status' and we see a bunch of 
'untracked files' then these are actually called to be in 
working area.

3.'Staging are'->what all files are goint to be the part of the next version we will create.
This staging area is the place where git knows what changes will be done from the last version 
to the next version.

4.'repository area'-> this area acutally contains the details of all your previous registered versions and 
the files in the area,git already manages them and knows their version history.

5.'git add <file>'->moves file from working area to staging area.

6.'git rm --cached <file>'->moves file from staging area to working area.

7.'commit'-> commit is a particular version of the project.It caputres a snapshot of the project'seestaged changes
and creates a version out of it.

8.'git commit'->registers staging changes to commit.A version  is created.

9.'git log' ->lists down all commits of th repo.If you want to exit out of git log prompt 
press 'q'. 

10.'git restore'-> it removes all file from the staging area to be committed.
This can we be useful ,if you did some dirty piece of code and now no more wants it .Instead of deleting every changes
line by line, we can restore it or you can say restore last clean version of the file.

11.All the changes doneafter the last commit are still in the working area, so to take the chanegs to the staging area ,
git add README.txt

12.'git restore --staged README.txt'-> removes the area that was previously added to staged area back to the working area.
This only works if changes are in staging  area.

13.Difference between rm and restore :If we want to move the whole file back to the untracked state, the we do git rm, 
otherwise id we just want the changes to be moved in working area or staging area then we do git restore.To use git rm,
there must be nothing in the staged area after a commit.