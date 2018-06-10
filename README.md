### Задание на  слайде 34
```
git init
echo "First file initial content" >first-file.txt
git add .
git commit -m "Initial commit (Commit1)"
echo "Additional line for commit 2" >>first-file.txt
git -am "Second commit (Commit 2)"
echo "Second file content for third commit" >>second-file.txt
git add second-file.txt
git commit -m "Third commit (Commit 3)"
git checkout -b branch1
echo "Branch1 feature for branch 'branch1'" >>branch1-specific-file.txt
git add .
git commit -m "Branch1 commit (Commit 4)"
git checkout main
git branch branch2
echo "Content of fifth commit in master" >>second-file.txt
git commit -am "Fifth commit (Commit 5)"
git checkout branch2
echo "branch2 feature content" >>branch2-specific-file.txt
git add branch2-specific-file.txt
git commit -m "Commit 6"
git checkout master

git log --all --decorate --oneline --graph

* f5a927e (branch2) Commit 6
| * cafbec0 (HEAD -> master) Fifth commit (Commit 5)
|/  
| * 0618beb (branch1) Branch1 commit (Commit 4)
|/  
* 91a93f7 Third commit (Commit 3)
* 4a92159 Second commit (Commit 2)
* cc56cf8 Initial commit (Commit1)
```

