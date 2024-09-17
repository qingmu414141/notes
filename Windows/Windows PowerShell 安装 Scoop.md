在 Windows 系统上经常需要安装一些工具或软件，使用 Scoop 来进行安装和管理是非常方便的，下面是使用 PowerShell 安装 Scoop 的操作步骤。
1. 首先从网上拉取 Scoop 的安装脚本，其中 irm 是 Invoke-RestMethod 的缩写，用来发送 HTTP 请求并获取响应。在这个命令中，它从远程 URL get.scoop.sh 获取内容。get.scoop.sh 是 Scoop 包管理器的安装脚本所在的 URL，-outfile 'install.ps1' 指定将下载的脚本文件保存为本地文件 "Scoop_Install.ps1"。
	```
	irm get.scoop.sh -outfile 'Scoop_Install.ps1'
	```
2. 开始安装 Scoop，并设置 Scoop 的安装目录(s)和使用 Scoop 安装应用的目录，不设置默认安装在用户目录。需要注意的是如果使用管理员（Admin）安装，默认是不允许的，需要添加一个参数："-RunAsAdmin"，即可安装成功。
	```
	.\install.ps1 -ScoopDir 'E:\Applications\Scoop' -ScoopGlobalDir 'E:\GlobalScoopApps' 
	```