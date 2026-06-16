## Differences between a 
| Sl. No. | Forking | Cloning |
| --- | --- | --- |
| 1. | Creates a copy of the original repository under the name of the person who forked the repository on cloud (Github) | Clones/downloads the contents of a repository from a remote server into the user's laptop which the user can modify offline |
| 2. | Usually used to contribute to a project/repository owned by someone else | It is used to write, test, debug and run the code offline |
| 3. | The user would finish their task and then submit a PR/MR to merge the new code into the original codebase | The user would pull or push the code directly (To a different branch usually, if on production, say feature, or a forked version of the codebase) to the repository |

## Commonly used git commands:
- `git branch`: Lists all the branches in the local repository, the one next to a '*' is the branch you are currently on
- `git add <path_to_file_from_root>`: Adds the file to the staging area, ready to be committed, use `git add .` to add all files to the staging area
- `git commit`: Used to commit the files from the staging area, use the flag `-m "<Your-message>"` to add a message to the commit
- `git checkout <branchname>`: Used to checkout the branch mentioned
- `git branch <branchname>`: Used to create a new branch 
- `git push <remote> <branch>`: Used to push the local commits to the remote repository to the specified branch (can use -u to make it upstream)