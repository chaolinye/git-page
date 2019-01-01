### 分支简介

假设现在有一个工作目录，里面包含了三个将要被暂存和提交的文件。暂存操作会为每一个文件计算校验和(SHA-1 哈希算法)，然后会把当前版本的文件快照保存到 Git 仓库中(Git 使用 blob 对象来保存它 们)，最终将校验和加入到暂存区域等待提交

```sh
git add README test.rb LICENSE
git commit -m 'The initial commit of my project'
```

当使用 git commit 进行提交操作时，Git 会先计算每一个子目录(本例中只有项目根目录) 的校验和，然后在 Git 仓库中这些校验和保存为树对象。 随后，Git 便会创建一个提交对象， 它除了包含上面提到的那些信息外，还包含指向这个树对象(项目根目录)的指针

现在，Git 仓库中有五个对象:三个 blob 对象(保存着文件快照)、一个树对象(记录着目 录结构和 blob 对象索引)以及一个提交对象(包含着指向前述树对象的指针和所有提交信 息)。

![首次提交对象及其树结构](https://ws4.sinaimg.cn/large/006tNbRwgy1fyr30safmdj315e0lqqd5.jpg)

做些修改后再次提交，那么这次产生的提交对象会包含一个指向上次提交对象(父对象)的指针。

![提交对象及其父对象](https://ws1.sinaimg.cn/large/006tNbRwgy1fyr31nnv69j313k0da7be.jpg)

Git 的分支，其实本质上仅仅是指向提交对象的可变指针。 Git 的默认分支名字是 master 。 在多次提交操作之后，你其实已经有一个指向最后那个提交对象的 master 分支。 它会在每次的提交操作中自动向前移动。

![分支及其提交历史](https://ws1.sinaimg.cn/large/006tNbRwgy1fyr36vbk3sj313s0ksdlx.jpg)


