# 树莓派的配置


## pip


### 使用中科大的 PyPI 软件仓库镜像
编辑文件 `${HOME}/.pip/pip.conf`，添加如下配置：

	[global]
	index-url = https://pypi.mirrors.ustc.edu.cn/simple


### 使用中科大的 apt 软件仓库镜像
编辑文件 `/etc/apt/sources.list`，将内容替换为：

	deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessie main non-free contrib
	deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessie main non-free contrib

执行 `aptitude update` 更新软件列表。


