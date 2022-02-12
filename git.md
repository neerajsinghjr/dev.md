# Git Version Control --git --start

## Renaming branch inside git.

### Rename the local branch to the new name
git branch -m <old_name> <new_name>

### Delete the old branch on remote - where <remote> is, for example, origin
git push <remote> --delete <old_name>

### Or shorter way to delete remote branch [:]
git push <remote> :<old_name>

### Push the new branch to remote
git push <remote> <new_name>

### Reset the upstream branch for the new_name local branch
git push <remote> -u <new_name>

You can also Try another approach...

 Verify the local branch has the correct name:
git branch -a

2. Next, delete the branch with the old name on the remote repository:
git push <origin> ––delete <old-name>

3. Finally, push the branch with the correct name, and reset the upstream branch:
git push origin –u new-name

Alternatively, you can overwrite the remote branch with a single command:
git push origin :old-name new-name
Resetting the upstream branch is still required:
git push origin –u new-name