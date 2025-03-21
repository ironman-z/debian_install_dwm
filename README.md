Debian dwm安装及配置

# 安装x-window环境
apt install -y x-window-system-core

# 安装xlib库
apt install -y libx11-dev

# 安装freetype字体引擎
apt install -y libxft-dev

#Xinerama 是 Linux 下 X 窗口系统的扩展，用于支持多个显示器
apt install -y libxinerama-dev libxrandr-dev

# 安装工具
apt update -y

apt install -y x-window-system-core libx11-dev libxft-dev \
libxinerama-dev libxrandr-dev
apt install -y git tmux neovim cmake

# 下载及编译安装
git clone https://git.suckless.org/dwm
git clone https://git.suckless.org/slstatus
git clone https://git.suckless.org/dmenu
git clone https://git.suckless.org/slock
make clean install

vi .xinitrc
    exec dwm
执行
  startx
  

# 非root需要加入audio和video组
sudo usermod -a -G audio,video xxx
