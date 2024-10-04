# how-to-git-push-exiting

## Step 1 — Create a new GitHub Repo
Sign in to GitHub and create a new empty repo. You can choose to either initialize a README or not. It doesn’t really matter because we’re just going to override everything in this remote repository anyway.

## Step 2 — Initialize Git in the project folder
```
git init
```

```
git add .
```

```
git commit -m 'initial'
```

## Add a new remote origin
```
git remote add origin git@github.com:<username/projectname.git>
```

1.  Remove the Existing Remote:(if done somthing wrong)
```
git remote remove origin
```

2. After remove, add back 
```
git remote add origin git@github.com:auhkba/LINE.git
```

## Push to GitHub
```
git push -u -f origin main
```

The `-u` (or `--set-upstream`) flag sets the remote `origin` as the upstream reference. This allows you to later perform `git push` and `git pull` commands without having to specify an `origin` since we always want GitHub in this case.

The `-f` (or `--force`) flag stands for force. This will automatically overwrite everything in the remote directory. We’re using it here to overwrite the default README that GitHub automatically initialized

# Troubleshooting
— error: src refspec main does not match any — usually happens because you are trying to push a branch that does not exist yet in your local repository.
1.	Check the Current Branch:
```
git branch
```

2. Rename the Current Branch to main (if needed):
  ```
git branch -m master main
```

3. Push the Local Branch to the Remote:
   ```
   git push -u -f origin main
   ```




# git still shows files as modified after adding to .gitignore
```
git rm -r --cached .
git add .
git commit -m 'Removing ignored files'
git push
```

# Ignore files that have already been committed
1. commit any outstanding code changes, ' . ' meaning any, to removes everything from the index
```
git rm -r --cached .
```

or stop tracking the file but not delete it from your system use: `git rm --cached filename`

2. run
```
git add .
```

3. commit it:
```
git commit -m ".gitignore is now working"
```


