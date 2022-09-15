# git-workshop-2022

### Github
#### Setup personal access token


Truy cập vào địa chỉ https://github.com/new để tạo kho chứa trên Github

#### Tạo kho chứ ở local




### Create a branch and commit to the origin
```sh

git switch -C featuea/issue<issue_number>-<your_full_name>
git push origin featuea/issue<issue_number>-<your_full_name>
```


### Rebase

```shell
git rebase -i origin/develop
 
# View git graph
git log --graph --all --abbrev-commit --date=relative --pretty=format:'%C(red)%h %C(reset)-%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'
```


### Git flow in team work
ブランチ
main, develop, dev-release, stg-release, prd-release, feature/***


### Release
