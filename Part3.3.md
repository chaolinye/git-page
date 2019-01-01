### 记录每次更新到仓库

文件的状态变化周期

![文件的状态变化](https://ws1.sinaimg.cn/large/006tNbRwgy1fyr0gileyzj31810u0gqm.jpg)

#### 查看文件状态

```sh
git status
# 状态简览
git status -s
```

#### 跟踪新文件, 暂存已修改文件

```sh
git add README.md
```

git add 命令是个多功能命令:

* 跟踪新文件
* 把已跟踪的文件放到暂存区
* 还能用于合并时把有冲突的文件标记为已解决状态等等

可以将这个命令理解为"添加内容到下一次提交中"

#### 忽略文件

一般我们总会有些文件无需纳入 Git 的管理，也不希望它们总出现在未跟踪文件列表。 通常都是些自动生成的文件，比如日志文件，或者编译过程中创建的临时文件, IDE配置文件等。 在这种情况下，我们可以创建一个名为 .gitignore 的文件，列出要忽略的文件模式。

```sh
# 查看忽略的文件
cat .gitignore
```

#### 查看文件更新内容

```sh
# 查看工作目录中当前文件和暂存区域快照之间的差异
git diff
# 查看已暂存的将要添加到下次提交里的内容
git diff --cached
```

使用插件查看文件更新内容

```sh
git difftool
```

#### 提交更新

每次准备提交前，先用 git status 看下，是不是都已暂存起来了， 然后再运行提交命令

```sh
git commit
# 带提交message
git commit -m "commit mesage"
```

另外一些有用的提交方式:

```sh
# 跳过暂存区的提交
git commit -am "commit message"
# 修改上一个提交
git commit --amend
```

