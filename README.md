# 学习Git

## 初始化
```bash
git init
```

## 暂存
> `.`表示所有修改的文件
```bash
git add .
```

## 提交到本地仓库
```bash
git commit -m "注释"
```

## 推送
> 把本地仓库的 main 分支的更改，推送到远程仓库 origin 的 main 分支上。
```bash
git push origin main
```

## Fetch
> 从远程仓库抓取最新信息
```bash
git fetch origin
```

### 查看远程 main 分支的提交情况
```bash
git log origin/main --oneline
```

### 把远程 main 合并进当前分支
```bash
git merge origin/main
```

## 更新代码
以下等价
```bash
git pull origin main
```

```bash
git fetch origin
git merge origin/main
```

## 分支

> 查看当前所有分支，当前分支会带`*`
```bash
git branch
```

### 创建分支
```bash
git branch 新分支名
```

### 创建分支
```bash
git checkout 分支名
```

### 创建并切换分支
```bash
git checkout 新分支名
```

### 推送新分支
```bash
git push -u origin 新分支名
```

## Merge
> 加入要把`feature`分支内容合并到`main`分支中

### 切换到`main`分支
```bash
git checkout main
```

### 拉取远程最新代码
> 建议先同步远程
```bash
git pull origin main
```

### 合并`feature`到`main`
```bash
git merge feature
```

### 解决冲突
> 打开有冲突的文件，Git 会标记冲突部分，按需编辑
> 编辑完成后，执行：
```bash
git add 冲突文件
git commit
```

### 推送合并后的`main`分支到远程
```bash
git push origin main
```