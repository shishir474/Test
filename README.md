# Git assignment:
----Shishir Singh
    Tas131
    
    
### Create a repo named Test

Clone the empty repository

```
git clone <repo url>
```

Create a file in main branch and push it to remote.
```
touch main.txt
git add .
git commit -m "created main file"
git push origin main
```
Creating a branches named Integration and push it to remote.

```
git checkout -b Integration
git push origin Integration
```

Create another branch named HotFix nad push it to remote

```
git checkout -b HotFix
git push origin HotFix
```

Switch to integration branch and create two branch(Featur1 & Festure2) from it

```
git switch Integration
git checkout -b Feature1 Integration
git switch Integration
git checkout -b Feature2 Integration
```

Switch to Feature2 branch make some changes and push it to remote

```
git switch Feature2
touch Feature2.txt

git add .
git commit -m "changes: Feature2"
git push origin Feature2
```

Now go to github and Create a PR to Integration branch.

Merge the PR and delete the Feature2 branch after successfull merge.

Switch to Feature1 branch and make some changes and rebase it to integration branch

```
git switch Feature1

touch Feature.txt
git add .
git commit -m "changes: Feature1"

git rebase Integration Feature1
```

Switch to Integration branch and push the changes to remote

```
git switch Integration

git pull origin Integration

git add .
git commit -m "changes: after rebase"
git push origin Integration
```

Go to github and Create a PR from Integration to HotFix and main branch and merge the changes after review

Switch to Feature1 branch add some changes and push it to remote.

```
git switch Feature1

git pull origin Feature1
touch feature1-1.txt

git add .
git commit -m "chnages #2:Feature1"
git push origin Feature1
```
Go to github and Create a PR from Feature1 to Integration, HotFix and main branch and merge the changes after review.

Delete the Feature1 branch.

Switch to HotFix branch commit some changes anf push it to remote.

```
git switch HotFix

git pull origin HotFix
touch HotFix.txt

git add .
git commit -m "chnages: HotFix"
git push origin HotFix
```

Go to github and Create a PR from HotFix  to Integration and main branch and merge the changes after review.
