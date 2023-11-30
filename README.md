create README.md

Step by step manual to reproducing all actions

Doing auth to the GitHub ( password auth was deprecated at the 2021 )
```
gh auth login
```

Creating remote repository, making it public
```
gh repo create new-project --public
```

Creating new project folder
```
mkdir new-project
```

Changing folder
```
cd new-project
```
Doing git init for new progect - creating all files, which needed
```
git init
```

Adding new remote URI for the this project ( we mean - this remote not exists yet )
```
git remote add origin git@github.com:ashyshka/new-project.git
```

Creating README.md
```
echo "create README.md" > README.md
```

Adding README.md to local git - preparing to commit
```
git add README.md
```

Doing initial commit
```
git commit -m "init"
```

Creating new branch - development
```
git checkout -b development
```

Writing this manual
```
code README.md
```

Adding modified README.md to local git to the branch development
```
git add README.md
```

Checking - if we doing all
```
git status
```

Commiting changes
```
git commit -m "Added manual to reproduce to README.md"
```

Switching to the branch main and mergibg from development
```
git checkout main
git merge development
```

Pushing cnanges to remote repo
```
git push --set-upstream origin main
```
