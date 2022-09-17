### On the different branch

Task:
Add row `"University"` and `"Year"` for the file: introduction.text but on different git branch and merge them to main

Example
on branch feature/introduction_1

```shell
Name:
Hobby:
University: BK, HCMC #new line
```

on branch feature/introduction_2

```shell
Name:
Hobby:
Year: 3rd #new line
```

#### 1. Create development branch

```sh
git switch main # switch to main branch
git pull # get latest code
git switch -C feature/introduction_1 # create new branch

# edit introduction.txt file
vi introduction.txt #Mac/Linux

git add .
git commit -m "add row university"
git push --set-upstream origin feature/introduction_1
```

```sh
git switch main  # switch to main branch
git pull # get latest code

git switch -C feature/introduction_2 # create another new branch

# edit introduction.txt file
vi introduction.txt #Mac/Linux

git add .
git commit -m "add row Year"
git push --set-upstream origin feature/introduction_2
```

#### 2. Combine source

##### a. Merge

```shell
git switch feature/introduction_1 # switch branch

git switch -C feature/merge_introduction # create a merge branch
git merge feature/introduction_2

# resolve conflict if any
echo 'please resolve conflict if any'

git add .
git commit -m 'combined commits'
git push --set-upstream origin feature/merge_introduction
```

##### b. Rebase

```shell
git switch feature/introduction_2 # switch branch

git rebase feature/introduction_1

# resolve conflict if any
echo 'please resolve conflict if any'

git add .
git rebase --continue
git push -f --set-upstream origin feature/introduction_2
```

#### 6. Create a pull-request to main branch

#### 7. Merge
