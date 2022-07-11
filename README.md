# My-Tools

铜豌豆软件源：
https://www.atzlinux.com/atzlinux/pool/main/a/atzlinux-archive-keyring/atzlinux-archive-keyring_lastest_all.deb

软件源后加上non-free
vim /etc/apt/sources.list

deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free
deb http://mirrors.ustc.edu.cn/debian stable-updates main contrib non-free

sudo apt-get update

查看网卡型号：
lspci -nn

wifi:
sudo apt-get install firmware-iwlwifi firmware-intelwimax firmware-realtek firmware-atheros
sudo apt-get install gnome-control-center

显卡：
sudo apt install nvidia-settings

双显卡方案：
sh NVIDIA-Linux-x86_64-xxx.xxx.run -no-x-check -no-nouveau-check -no-opengl-files --kernel-source-path=/usr/src/kernels/$(uname -r)

-no-x-check：安装驱动时关闭X服务
-no-nouveau-check：安装驱动时禁用nouveau
-no-opengl-files：只安装驱动文件，不安装OpenGL文件
--kernel-source-path: 指定安装路径
