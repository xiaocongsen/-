# Git学习

    git init
    git clone
    git add
    git status         -s 参数，以获得简短的结果输出
    AM
    git diff          --cached     / HEAD        /--stat
    git commit  -m/ -a
    git reset HEAD
    git rm   -f   /--cached  / –r
    git mv
    git branch /(branchname)  /-d
    git checkout (branchname)  /-bgit merge
## 删除分支
1. 删除本地分支
    git branch -d 分支名
2. 删除远程分支
    git push origin --delete 分支名

3. 删除未跟踪文件   加上-n打印会删除的文件
    git clean -f
4. 未跟踪的目录也一起删掉
    git clean -fd
5. 连 gitignore 的未跟踪的文件/目录也一起删掉 （慎用，一般这个是用来删掉编译出来的 .o之类的文件用的）
    git clean -xfd
 

## 初始化流程
    git init
    git add -A
    git commit -m "init"
    git remote add origin ssh://git@ds-project.cn:10022/xiaocs/hiRedisTest.git
    git push origin master:master


## 加分支流程
    git checkout -b 新分支名字
    git add -A
    git commit -m "init"
    git push origin 新分支名字:新分支名字


## 合并分支流程
    当前分支没有修改
    git merge 需要合并过来的版本名

## 放弃本地修改
    git status 查看当前文件状态
1. 未使用 git add 缓存代码
    git checkout -- filepathname
2. 已经使用了  git add 缓存了代码
    git reset HEAD filepathname
3. 已经用 git commit  提交了代码
    git reset --hard commitId
    commitId 可以通过git log输出    (HEAD -> master)为当前所在分支