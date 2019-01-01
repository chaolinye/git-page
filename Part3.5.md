### 撤销操作

有时候我们提交完了才发现漏掉了几个文件没有添加，或者提交信息写错了。
可以运 行带有 --amend 选项的提交命令尝试重新提交:

```sh
git commit --amend 
```

#### 取消暂存的文件

```sh
git reset HEAD README.md
```

#### 撤销对文件的修改

```sh
git checkout -- README.md
```

