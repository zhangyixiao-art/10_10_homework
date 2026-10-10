# 图像矩阵编程作业

## 1. 进入下载作业的目录

打开终端，使用 `cd` 进入你想存放作业的目录。例如，将作业下载到“下载”目录：

```bash
cd ~/Downloads
```

也可以将 `~/Downloads` 替换为你自己的目录路径。路径包含空格时，请用英文双引号包住路径。

## 2. 使用 Git 下载作业

在终端运行：

```bash
git clone https://github.com/inspirepassion/10_10_homework.git
```

Git 会在当前目录下创建 `10_10_homework` 文件夹，并将作业文件下载到其中。此命令需要电脑已安装 Git。

## 3. 完成 starter.py 中的四个函数

打开下载后的 `starter.py`，完成以下函数：

- `build_grayscale`：将一维像素序列转换为二维灰度图像。
- `edit_pixel`：在图像副本中修改指定像素。
- `grayscale_to_rgb`：将二维灰度图像转换为三维 RGB 数组。
- `adjust_brightness`：调整像素亮度，并将数值限制在 0–255 范围内。

每个函数中都有一行 `raise NotImplementedError(...)`。**删除这一行，在原位置编写你的代码，并使用 `return` 返回结果。**

请阅读 `starter.py` 中各函数的说明、示例输入和预期输出，了解具体要求。其他已提供的检查代码和绘图流程无需修改。

## 4. 在终端运行并检查结果

回到终端，进入下载后的作业文件夹。如果你按照上面的例子下载到了“下载”目录，请运行：

```bash
cd ~/Downloads/10_10_homework
```

如果你选择了其他下载位置，请相应修改路径。

检查当前所在目录和其中的文件：

```bash
pwd
ls
```

`pwd` 显示当前目录的完整路径，确认它是你的作业文件夹；`ls` 列出该目录中的文件，确认其中有 `starter.py`。

使用 Python 3 运行代码：

```bash
python3 starter.py
```

如果终端提示缺少 `numpy` 或 `matplotlib`，请先安装，再重新运行：

```bash
python3 -m pip install numpy matplotlib
python3 starter.py
```

程序会分别显示四个函数的检查结果：`通过`、`未通过`、`未完成`或`运行出错`。根据提示修改代码，保存文件后再次运行。四个函数全部通过时，会显示图像对比窗口。

关闭图像窗口即可结束程序；也可以在终端按 `Ctrl + C` 停止运行。

## 5. 将完成的作业上传到自己的 GitHub

确认程序显示 `4/4 个函数通过` 后，按照以下步骤提交。

### 创建自己的仓库

1. 登录自己的 GitHub 账号，打开 [新建仓库页面](https://github.com/new)。
2. 在 Owner 中选择自己的账号。
3. Repository name 必须填写 **`10_10_homework`**，拼写完全一致。
4. 选择 Public（公开），方便老师查看作业。
5. 不要添加 README、.gitignore 或 License，保持新仓库为空。
6. 点击 Create repository 创建仓库。

### 提交代码并推送

回到终端，进入本地作业目录，并确认其中有你已完成的 `starter.py`：

```bash
cd ~/Downloads/10_10_homework
pwd
ls
```

如果下载位置不同，请修改上述路径。

将下载时设置的远程地址改为**自己的仓库地址**。下面的 `myname` 是占位符，必须替换为你的 GitHub 用户名：

```bash
git remote set-url origin https://github.com/myname/10_10_homework.git
git remote -v
```

确认显示的地址属于你自己的账号，然后依次运行：

```bash
git add starter.py
git commit -m "完成图像矩阵作业"
git push -u origin HEAD:main
```

这些命令会记录你对 `starter.py` 的修改，并将当前分支的代码上传到自己仓库的 `main` 分支。请按终端提示完成 GitHub 身份验证；HTTPS 身份验证不能使用普通的 GitHub 登录密码。

如果 `git commit` 提示未设置姓名或邮箱，请先运行以下命令，将内容替换为你自己的姓名和 GitHub 账号邮箱，然后重新执行提交与推送：

```bash
git config user.name "你的姓名"
git config user.email "你的邮箱"
```

如果提示 `nothing to commit`，表示没有新的修改需要记录。确认你已保存完成的代码后，可以继续执行推送命令。

上传后，打开自己的 GitHub 仓库，确认 `main` 分支中的 `starter.py` 已包含你的实现。

相关操作可参考 [GitHub 官方上传指南](https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github) 和 [修改远程仓库地址说明](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories)。

## 6. 在芯位蜜线网站提交仓库链接

1. 登录 **芯位蜜线网站**。
2. 找到 **“10_10 Matrix”作业**。
3. 将你刚刚上传的个人仓库的完整链接粘贴到对应的作业内容中，并完成提交。例如：

```text
https://github.com/myname/10_10_homework.git
```

请将 `myname` 替换为自己的 GitHub 用户名。提交的是你自己的仓库链接，不是老师提供的 `inspirepassion` 仓库链接。
