### On the same branch

Create branch

```sh
git switch -C feature/introduction
# or
git checkout -b feature/introduction
# or
git branch -M feature/introduction
```

Push branch to origin

```shell
git push --set-upstream origin feature/introduction
```

#### 1. Create your profile file

```shell
# Mac/Linux
touch introduction.txt

# Window
type nul > your_file.txt
```

#### 2. Development time (update introduction.txt)

```shell
Name: <your_name>
Hobby: <your_hobby>
```

#### 3. Commit code

```shell
git add .
git commit -m "add profile"
git push origin feature/introduction
```

#### 4. Commit directly on branch from GitHub console without conflict

After editing from GitHub console, then

```shell
git pull
```

#### 5. Commit directly on branch from GitHub console causing conflict

After editing from GitHub console, then

```shell
# Edit introduction.txt
vi introduction.txt #Mac/Linux
git add . commit
git commit -m 'update same file'

git pull
git rebase origin/feature/introduction

# Check git log
git log --all --decorate --oneline --graph

git push origin feature/introduction
```

#### 6. Create a pull-request to main branch

#### 7. Rebase to main branch

```shell
git rebase -i origin/main

git push origin feature/introduction -f
```

#### 8. Merge pull-request
