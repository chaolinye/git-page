### 分支的新建、切换、合并

Git 是怎么创建新分支的呢? 很简单，它只是为你创建了一个可以移动的新的指针。比如创建一个 testing 分支

```sh
git branch testing
```

![创建一个新分支指针](https://ws4.sinaimg.cn/large/006tNbRwgy1fyr434g2woj314u0ngdkn.jpg)

切换分支

```sh
git checkout testing
```

另外, 创建与切换分支可合成一步

```sh
git checkout -b testing
```

![HEAD 指向当前所在的分支](https://ws3.sinaimg.cn/large/006tNbRwgy1fyr4nv0z5nj314o0nowje.jpg)

添加新的提交

![分支随着提交操作自动向前移动](https://ws2.sinaimg.cn/large/006tNbRwgy1fyr4omfnmzj31460h80w9.jpg)

切换回master分支

```sh
git checkout master
```
合并testing分支到master

```sh
git merge testing
```

合并时，可能会有冲突，这时需要解决冲突，解决冲突用GUI比较为方便, 命令行可以使用`git mergetool`
