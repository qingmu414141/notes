![[Pasted image 20240917172417.png]]
由于 mac 的 oh-my-zsh 默认是没有设置字符集的，所以在使用 SSH 远程连接时，遇到中文显示时会出现乱码的问题，因此要为 oh-my-zsh 手动设置字符集，设置过程如下：
1. 编辑 ~/.zshrc 文件，并在其中添加两条命令设置使用 UTF-8 字符集
```
vim ~/.zshrc

# 添加的命令
export LC_ALL=en_US.UTF-8 
export LANG=en_US.UTF-8
```
2. 重新加载 ~/.zshrc 文件使其生效
```
source ~/.zshrc
```
3. 进行验证,如下显示则配置成功
```
local
```
![[Pasted image 20240917172517.png]]