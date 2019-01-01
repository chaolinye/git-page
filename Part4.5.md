### 远程分支

远程跟踪分支是远程分支状态的引用。 它们是你不能移动的本地引用，当你做任何网络通信 操作时，它们会自动移动。 远程跟踪分支像是你上次连接到远程仓库时，那些分支所处状态的书签。它们以 (remote)/(branch) 形式命名

假设你的网络里有一个在 git.ourcompany.com 的 Git 服务器。如果你从这里克隆，Git 的 clone 命令会为你自动将其命名为 origin ，拉取它的所有数据，创建一个指向它的 master 分支的指针，并且在本地 将其命名为 origin/master 。 Git 也会给你一个与 origin 的 master 分支在指向同一个地方 的本地 master 分支，这样你就有工作的基础

![克隆之后的服务器与本地仓库](https://ws2.sinaimg.cn/large/006tNbRwgy1fyr58birnxj313e0s0dnl.jpg)

#### 更新远程分支

```sh
git fetch [remote]
```

#### 推送到远程分支

```sh
git push [remote] [branch]
```

#### 检出远程分支

```sh
git checkout -b [branch] [remote]/[branch]
```

#### 跟踪分支

从一个远程跟踪分支检出一个本地分支会自动创建一个叫做 跟踪分支''(有时候也叫做 上游分 支'')。 跟踪分支是与远程分支有直接关系的本地分支。 如果在一个跟踪分支上输入 git pull ，Git 能自动地识别去哪个服务器上抓取、合并到哪个分支。

设置当前分支的跟踪分支

```sh
# 随时调用设置跟踪分支
git branch -u [remote]/[branch]
# 提交时设置跟踪分支
git push -u [remote] [branch]
```

查看每个分支的跟踪分支

```sh
git branch -vv
```

#### 删除远程分支

```sh
git push [remote] -d [branch]
```
