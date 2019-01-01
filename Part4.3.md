### 分支管理

查看分支

```sh
git branch
# 查看每一个分支的最后一次提交
git branch -v
# 查看已经合并到当前分支的分支
git branch --merged
# 查看尚未合并到当前分支的分支
git branch --no-merged
```

删除分支

```sh
# 删除已经合并的分支，否则会报错
git branch -d testing
# 强制删除
git branch -D testing
```

