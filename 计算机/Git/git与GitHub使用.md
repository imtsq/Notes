- 参考[Hello World - GitHub 文档](https://docs.github.com/zh/get-started/using-github/hello-world)

# 1. 本地仓库和github配置

##  设置用户名&邮箱

```
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```



## 初始化仓库

```
# 需要进入对应的仓库目录
git init -b main
git add .
git commit -m "首次提交"
```

## 在本地生成一个ssh

```
# 本地生成一个ssh，Windows电脑在c盘/用户目录下面
ssh-keygen -t rsa -b 4096 -C "你的邮箱"
# 查看ssh并复制到GitHub中的ssh（在设置里面找）
cat ~/.ssh/id_rsa.pub
# 测试连接s'b'f
ssh -T git@github.com
```



## 管理GitHub仓库

```
# 管理仓库
git remote add origin git@github.com:用户名/仓库名.git
# 先下拉GitHub仓库，不然推送不了
git pull origin main
# 将本地代码推送给GitHub仓库
git push -u origin main
```



# 2. 之后修改笔记提交

```bat
# 可以写个bat文件保存到里面每次提交运行下就行
git add .
git commit -m "提交信息"
git push
```

