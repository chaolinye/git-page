### 初次运行 Git 前的配置

Git 自带一个 git config 的工具来帮助设置控制 Git 外观和行为的配置变量。这些变量存储 在三个不同的位置:

1. `/etc/gitconfig`
2. `~/.gitconfig`
3. ` .git/config`

当安装完 Git 应该做的第一件事就是设置你的用户名称与邮件地址

```sh
git config --global user.name "chaolinye"
git config --global user.email "yechaolin1@huawei.com"
```

既然用户信息已经设置完毕，你可以配置默认文本编辑器了

```sh
git config --global core.editor vim
```

检查配置

```sh
git config --list
# 检查某项配置
git config user.name
```

