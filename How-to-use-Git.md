# How to use Git

## Setup
1. 创建账号

2. 在本地生成ssh key, 粘贴复制到账户设置中

可参考 [Git for Windows](https://www.jianshu.com/p/662d9bb9cadc)


## Usage
![git](/assets/git.jpg)

大的模型和数据集可以不push到Git

考虑到项目合作可能会导致代码版本冲突，下面列举常见流程：

1. 从远程第一次拉代码到本地
```git bash
git clone https://github.com/NJUDCA/ChineseNER.git
```


2. 如果成员不会修改同一个文件，那么一起在master上工作即可
```bash
git add <file_name>
git commit <specific_msg>
git push origin master
```

3. 如果成员会修改同一个文件，或者开发新模块的同时想保留旧版本的代码，那么需要创建新分支
```bash
git checkout -b <branch_name>
git add <file_name>
git commit <specific_msg>
git push origin <branch_name>:<branch_name>
```

4. 从远程更新代码（非第一次，即本地已有项目）
```bash
# 直接从主分支拉
git pull origin matser
# 拉某个分支的代码
git checkout master
git pull origin <branch_name>:<branch_name>
```

5. 用主分支的代码覆盖本地的代码 
```bash
git checkout <branch_name> 
git rebase master
```


6. 在Github上merge完成后，删除本地分支并提交
```bash
git checkout master
git pull —rebase
git branch -D <branch_name>
git push origin :<branch_name>
```
