### 一、安装 Jekyll
1. 安装 Jekyll：`gem install jekyll`
2. 你可以通过命令来验证 Jekyll 是否正确安装：`jekyll -v`
    - 如果输出 Jekyll 的版本信息，说明安装成功。

### 二、可能会出现的问题1
[![pAN6Nk9.png](https://s21.ax1x.com/2024/10/16/pAN6Nk9.png)](https://imgse.com/i/pAN6Nk9)
- 'jekyLL' 不是内部或外部命令，也不是可运行的程序或批处理文件。
- 说明Jekyll 已经成功安装了，但命令行无法识别 jekyll 命令。问题可能是由于 jekyll 安装后没有将其路径正确添加到环境变量中。
1. **确保 Jekyll 已正确安装**
- 你已经看到命令行中显示 Jekyll 的相关组件都成功安装。现在我们来检查 Jekyll 是否真的被安装到了正确的位置。你可以通过以下命令来查看 Jekyll 的路径：`where jekyll`
- 如果返回了 Jekyll 的安装路径，那么它已经正确安装。如果没有返回结果，说明它没有被添加到系统路径中。

### 三、可能会出现的问题2
[![pAN60l6.png](https://s21.ax1x.com/2024/10/16/pAN60l6.png)](https://imgse.com/i/pAN60l6)
- 系统提示需要安装 MSYS2。MSYS2 是一个轻量级的开发工具集，Ruby 依赖它来编译某些 gem（比如 Jekyll）。你可以通过以下步骤安装 MSYS2 并解决这个问题。
1. **运行 ridk install 安装 MSYS2**
    - 你可以在命令行中运行以下命令来自动安装 MSYS2：`ridk install`

2. **手动安装 MSYS2**
- 如果 ridk install 出现问题或安装不成功，你可以手动安装 MSYS2：
  1. 前往MSYS2 官网下载适用于Windows 的安装包。
  2. 下载完成后，按照提示安装MSYS2。
  3. 安装完成后，打开MSYS2的终端并运行以下命令来更新包管理器和安装工具：`pacman -Syu`
  4. 然后，运行以下命令来安装开发工具：`pacman -S base-devel mingw-w64-x86_64-toolchain`

3. 重新安装Jekyll
    - 安装 MSYS2 后，再次尝试安装Jekyll:`gem install jekyll`
    - 这样 Jekyll 应该能够顺利安装，并且 MSYS2 会解决缺少编译工具的问题。

### 四、MSYS2安装选择
[![pAN62tA.png](https://s21.ax1x.com/2024/10/16/pAN62tA.png)](https://imgse.com/i/pAN62tA)
1. 选择选项 3（MSYS2 和 MINGW 开发工具链）。
2. 直接按下 3 键，然后按 Enter。系统将会自动下载并安装所需的 MSYS2 和 MINGW 工具链。
3. 完成安装后，你可以重新尝试安装 Jekyll：`gem install jekyll`

### 五、下载报错
[![pAN65X8.png](https://s21.ax1x.com/2024/10/16/pAN65X8.png)](https://imgse.com/i/pAN65X8)
1. 出现了 404 Not Found 错误，这意味着 MSYS2 的下载链接无效。
2. 手动下载 MSYS2
    - 前往 MSYS2 的官网。
    - 在页面中找到下载链接并点击下载适用于 Windows 的安装程序。
    - 安装时，一直下一步就行，安装路径可以自己选择。
3. 更新 MSYS2 和安装开发工具
    - 安装完成后，打开 MSYS2 的终端，更新包管理器：`pacman -Syu`
    - 安装开发工具链：`pacman -S base-devel mingw-w64-x86_64-toolchain`

### 六、安装 mingw-w64-x86_64-toolchain
[![pANciN9.png](https://s21.ax1x.com/2024/10/16/pANciN9.png)](https://imgse.com/i/pANciN9)
1. 按 Enter 键（回车键）直接使用默认选项 all，这将安装所有列出的工具。
2. 完成后，你的 MSYS2 环境将配置完毕，然后你可以返回到命令行，继续 Jekyll 的安装步骤：`gem install jekyll`

### 七、配置环境变量
[![pANcmnO.png](https://s21.ax1x.com/2024/10/16/pANcmnO.png)](https://imgse.com/i/pANcmnO)
1. Ruby 提示找不到 MSYS2，则需要配置环境变量。
2. 配置步骤：
    - 打开 系统属性 → 高级系统设置 → 环境变量。
    - 在 系统变量 中找到 Path，点击 编辑。
    - 添加 MSYS2 的路径，例如：`E:\RuBy\rubyinstaller-3.3.5-1-x64\Environment\MSYS2`
    - 点击 确定 保存设置。
3. 重新运行 `ridk install`

### 八、ridk install 提示
[![pANcdEQ.png](https://s21.ax1x.com/2024/10/16/pANcdEQ.png)](https://imgse.com/i/pANcdEQ)
1. 选项 3，即 MSYS2 and MINGW development toolchain。这样可以确保 MSYS2 基础安装和开发工具链都被安装。

### 到此为止**MSYS2 和 MINGW 的开发工具链已经成功安装，接下来需要激活 MSYS2 工具**