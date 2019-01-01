### 远程仓库

#### 查看远程仓库

```sh
# 名称
git remote
# 基本信息
git remote -v
```

#### 添加远程仓库

```sh
git remote add pb https://github.com/paulboone/ticgit
```

#### 从远程仓库中抓取与拉取

```sh
git fetch [remote-name]
```

#### 推送到远程仓库

```sh
git push origin master
```

#### 远程仓库的移除与重命名

```sh
# 重命名
git remote rename pb paul
# git remote rm paul
```
