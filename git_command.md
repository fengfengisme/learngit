## 创建版本库

git init;

1. 分支
   2.1.创建一个分支
       repo start <name> --all     // 创建一个分支，名称为name
       git branch -b <name>        // 创建一个分支，名称为name
       git branch <name>           // 创建一个分支，名称为name
   2.2 切换分支
       repo checkout <name>
       git checkout <name>
       git checkout <name>         // 创建并切换到分支name
   2.3 删除分支
       git branch -d <name>
   2.4 查看分支
       git branch
       repo branch
   2.5 合并分支
       git merge <name>
2. v

## 创建一个版本

git add <name>
git commit -m "name"
git commit --amend              // 追加

## 提交到远端

```
git 
银联提交：git push origin HEAD:refs/for/dev
```

## 获取远端最新代码

```
git pull origin dev // 拉取远端dev分支代码，自动合并到本地
git fetch origin dev // 拉取远端dev分支代码，不会自动合并到本地
```



## stash入栈and出栈

```
git stash       // 入栈
git stash pop   // 出栈（同时删除栈空间）
git stash apply // 出栈（不删除栈空间）
git stash list  // 查看栈空间
git stash drop  // 删除栈空间
```

## 撤销

```bash
git checkout -- 文件名   // 撤销当前工作区的修改，如果缓冲区有内容就替换成缓冲区，否则恢复成上一个提交的版本
git checkout .          // 撤销当前工作区的修改

git reset HEAD 文件名    // 撤销缓冲区的内容放回到工作区(撤销add)

git reset HEAD^         // 撤销commit，并撤销add，但不删除工作区改动
git reset --soft HEAD^  //撤销commit，并保留add
git reset --hard HEAD^  // 撤销commit，并撤销add，并删除工作区改动 （变为上一个版本）
```



1. 查看版本记录
    git log
    git reflog  // 查看本地版本记录

2. 切换版本
    git reset --hard HEAD^          // 撤销commit，跳至上一个版本
    git reset --hard 版本号          // 根据版本号跳转到指定的版本

3. 查看当前工作树的状态
    git status      // 查看变更情况
    
4. 撤销

    

    差异
    git diff        // 比较工作区和缓冲区文件的差异
    git diff 文件名    // 比较某文件工作区和缓冲区的差异

    
