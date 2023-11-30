create README.md

Step by step manual to reproducing all actions

# Doing auth to the GitHub ( password auth was deprecated at the 2021 )
gh auth login
# creating remote repository, making it public
gh repo create new-project --public
# creating new project folder
mkdir new-project
# changing folder
cd new-project
# doing git init for new progect - creating all files, which needed
git init
# adding new remote URI for the this project ( we mean - this remote not exists yet )
git remote add origin git@github.com:ashyshka/new-project.git
# creating README.md
echo "create README.md" > README.md
# adding README.md to local git - preparing to commit
git add README.md
# doing initial commit
git commit -m "init"
# creating new branch - development
git checkout -b development
# writing this manual
code README.md
# adding MODIFIED README.md to local git to the branch development
git add README.md
# checking - if we doing all
git status
# commiting changes
git commit -m "Added manual to reproduce to README.md"
# switch to the branch main and mergibg from development
git checkout main
git merge development
# push cnangest to remote repo
git push --set-upstream origin main
