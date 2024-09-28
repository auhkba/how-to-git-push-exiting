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

## Push to GitHub
```
git push -u -f origin main
```

The `-u` (or `--set-upstream`) flag sets the remote `origin` as the upstream reference. This allows you to later perform `git push` and `git pull` commands without having to specify an `origin` since we always want GitHub in this case.

The `-f` (or `--force`) flag stands for force. This will automatically overwrite everything in the remote directory. We’re using it here to overwrite the default README that GitHub automatically initialized
