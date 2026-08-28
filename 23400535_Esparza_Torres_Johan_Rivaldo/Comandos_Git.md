# Comandos en git 

## git-add  
Add file contents to the index.         
>[!EXAMPLE]
         > `git add <file_name>`
         >
## git-am
Apply a series of patches from a mailbox.  
>[!EXAMPLE]
         > `git am <path/to/file.patch>`
         >
## git-archive
Create an archive of files from a named tree.  
>[!EXAMPLE]
         >`git archive --format=<format> --output=<file> <ref>`
         >
## git-backfill
Download missing objects in a partial clone.  
>[!EXAMPLE]                                                                      
         > 1. Clone with blob filtering (downloads commits/trees/tags, but no file contents)
         >  `git clone --sparse --filter=blob:none git@github.com:git/git.git`
         > 2. Navigate into the repository
         > `cd git`
         > 3. Define which paths you want to work with (optional but recommended for large repos)   
         > `git sparse-checkout add builtin`
         > 4. Backfill historical blobs for the sparse-checkout paths                               
         > `git backfill --sparse`
         >                  
## git-push
Update remote refs along with associated objects.
>[!EXAMPLE]
         > `git push origin main`
         >
## git-branch
List, create, or delete branches.
>[!EXAMPLE]
         >`git branch -d <branch_name>`
         >
## git-rebase
Reapply commits on top of another base tip.
>[!EXAMPLE]
         > Basic Rebase To rebase the current branch onto main:
         > `git fetch origin main`  
         > `git checkout my-branch`  
         > `git rebase origin/main`
         >
## git-checkout
Switch branches or restore working tree files.
>[!EXAMPLE]
         > `git checkout <branch-name>`
         >
## git-restore
Restore working tree files.
>[!EXAMPLE]
         > `git restore <filename>`
         >
## git-revert
Revert some existing commits.
>[!EXAMPLE]
         > `git revert --no-edit a1b2c3d`
         >
## git-rm
Remove files from the working tree and from the index.
>[!EXAMPLE]
         > `git rm <filename>`
         >
## git-shortlog
Summarize git log output.
>[!EXAMPLE]
         > `git shortlog -sn`
         >
## git-show
Show various types of objects.
>[!EXAMPLE]
         > `git show <commit_hash>`
         >
## git-sparse-checkout
Reduce your working tree to a subset of tracked files.
>[!EXAMPLE]
         > Clone with sparse checkout and partial clone in one command
         > `git clone --filter=blob:none --sparse https://github.com/example/monorepo.git`
         > `cd monorepo`
         > Set the specific directories you need (e.g., frontend and docs)
         > `git sparse-checkout set --cone frontend docs`
         > Checkout the main branch to populate the working directory
         > `git checkout main`
         > 
## git-stash
Stash the changes in a dirty working directory away.
>[!EXAMPLE]
         > `git stash list`
         >
## git-status
Show the working tree status.
>[!EXAMPLE]
         > `git status`
         >
## git-submodule
Initialize, update or inspect submodules.
>[!EXAMPLE]
         > `git submodule add https://github.com/my-account/my-library.git lib`
         >
## git-switch
Switch branches.
>[!EXAMPLE]
         > `git switch <branch_name>`
         >
## git-tag
Create, list, delete or verify tags.
>[!EXAMPLE]
         > `git tag v1.0.0   `
         >
## git-worktree
Manage multiple working trees.
>[!EXAMPLE]
         > `git worktree add ../my-feature-branch my-feature-branch   `
         >
