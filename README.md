# git-upload
要在Debian系统上将本地Git仓库上传到GitHub，可以按照以下步骤操作：

### **步骤 1：安装 Git**
如果您的系统尚未安装 Git，可以运行：
```bash
sudo apt update
sudo apt install git
```

### **步骤 2：配置 Git 用户信息**
设置您的Git用户名和邮箱（用于提交代码时记录身份）：
```bash
git config --global user.name "您的GitHub用户名"
git config --global user.email "您的GitHub邮箱"
```

### **步骤 3：初始化 Git 仓库**
如果您的项目尚未初始化 Git，可以执行：
```bash
cd /path/to/your/project  # 进入项目目录
git init
```

如果您已经在Git初始化过，只需继续下一步。

### **步骤 4：关联 GitHub 仓库**
在GitHub上新建一个仓库（可以在[GitHub官网](https://github.com/)创建），然后运行以下命令，将本地仓库与GitHub远程仓库关联：
```bash
git remote add origin https://github.com/您的GitHub用户名/您的仓库.git
```

如果您的 GitHub 账户启用了 **SSH 访问**，可以改用：
```bash
git remote add origin git@github.com:您的GitHub用户名/您的仓库.git
```

### **步骤 5：添加文件并提交**
将项目中的文件添加到 Git：
```bash
git add .
git commit -m "上传代码到GitHub"
```

### **步骤 6：推送到 GitHub**
执行以下命令，将代码推送到 GitHub：
```bash
git push -u origin main
```
如果您的主分支是 `master`，请使用：
```bash
git push -u origin master
```

### **额外提示**
- 如果您的仓库是私有的，需要使用 **GitHub 访问令牌** 而不是密码进行身份验证（可在 GitHub "Settings > Developer settings > Personal access tokens" 创建）。
- 如果您需要拉取更新，可以使用：
  ```bash
  git pull origin main
  ```

这样就成功将本地 Git 仓库上传到 GitHub 了！如果您需要更多帮助，请告诉我 😊
