### 一、准备 GitHub 仓库
#### 创建一个新的 GitHub 仓库
1. 点击右上角的“+”图标，选择 New repository（新建仓库）。
2. 仓库名称填写为 `GitHub用户名.github.io`。
3. 添加一个 README 文件，用于介绍你的仓库。
4. 点击下方的 Create repository 按钮，创建这个新的仓库。
  
### 二、将本地博客推送到 GitHub
1. 打开你的终端（命令行），导航到你本地的博客文件夹（例如 E:\MyBlog\Learning_Notes）。
2. 初始化本地的 Git 仓库：`git init`
3. 添加文件到 Git 仓库：`git add .`
   - 如果出现警告是正常的，它们告诉你文件在 Windows 和 Unix 系统之间的换行符差异（LF 和 CRLF）。这些警告不会影响你上传到 GitHub 的过程。
4. 提交更改： 提交你刚刚添加的文件，创建一个初始提交：`git commit -m "Initial commit for my Jekyll blog"`
5. 将本地仓库连接到远程仓库：`git remote add origin https://github.com/仓库名称.git`
6. 推送到 GitHub：`git push -u origin main`


### 三、可能会遇到的问题
[![pANWcW9.png](https://s21.ax1x.com/2024/10/16/pANWcW9.png)](https://imgse.com/i/pANWcW9)
1. 如果出现以上报错，是因为你的本地仓库中还没有名为 main 的分支。
2. 解决方式：
    - 创建名为 main 的分支：`git branch -M main`
    - 推送到远程仓库：`git push -u origin main`

[![pANW6JJ.png](https://s21.ax1x.com/2024/10/16/pANW6JJ.png)](https://imgse.com/i/pANW6JJ)
1. git push 操作被拒绝，这是因为远程仓库已经有一些内容，与你本地的内容冲突了。
2. 解决步骤：
    - 拉取远程仓库的最新更改：`git pull origin main --rebase`
    - 错误提示 `OpenSSL SSL_read: SSL_ERROR_SYSCALL`，通常是由于网络连接问题或 SSL 证书的问题导致的。
    - 如果还无法解决，请将电脑连接手机热点
    - 然后执行：
      - `git pull origin main --rebase`
      - `git push -u origin main`
  
### 四、登录查看
1. 接下来，你可以通过访问 `https://GitHub用户名.github.io` 来查看你的博客。如果访问时页面显示有问题，需要稍等几分钟，等待 GitHub 完成构建和渲染。

# 到此所有的博客配置就全部完成啦！如果有不明白的地方，请私信我！