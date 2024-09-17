1. 首先更 好Homebrew 源代码仓库源
```
git -C "$(brew --repo)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
```
2. 查看 “/opt/homebrew/Library/” 目录下面是否含有 “core” 和“cask”两个目录，这两个分别是管理 Homebrew 核心软件仓库 和 提供 macOS 应用和大型二进制文件的工具
3. 没有需要安装这两个库
```
brew tap homebrew/core 
brew tap homebrew/cask		
```
4. 替换 brew-core 源
```
git -C "$(brew --repo homebrew/core)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git
```
5. 替换 brew-cask 源
```
git -C "$(brew --repo homebrew/cask)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask.git
```
6. zsh 替换 brew bintray 镜像，并立即生效
```
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.zshrc

source ~/.zshrc
```
7. bash 替换 brew bintray 镜像，并立即生效（可选）
```
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.bash_profile

source ~/.bash_profile
```
8. 刷新源
```
brew update
```