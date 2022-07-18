# GIT CLI

## 版本回退
```
# 方法一
git reset --hard HEAD^

/**
- HEAD 表示当前的版本。
- 一个 ^ 表示上一个版本号, n个^表示,上n个版本。
**/


# 方法二
git reflog // 查看每次commit生成的id
git reset --hard [id号] // 回退到指定的id

```
## 文件在工作区进行时撤销操作

```
git restore [filename]

/**
  - 情况一: 一种是file自修改后还没有被放到暂存区，现在撤销就会回到最近的一次commit
  - 情况二: 一种是file已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

**/
```

## 文件在暂存区时进行撤销

```
git restore --staged [filename] //将文件退回到工作区
git restore [filename+] // 执行 文件在工作区进行时撤销操作
```
## 删除文件
```
git rm [filename] // 等于删除文件, 并把此操作添加到暂存区
// 这一步的前提是该文件已经已经被commit
```