升级系统到最新
sudo pacman -Syyu

sudo pacman-mirrors -i -c China -m rank //更新镜像排名
sudo pacman -Syy //更新数据源

/etc/pacman.conf

[archlinuxcn]

SigLevel = Never
Server = https://mirrors.ustc.edu.cn/archlinuxcn/$arch

sudo pacman -Syyu //更新数据源
sudo pacman -S archlinuxcn-keyring //安装导入GPG key

aur源
修改/etc/yaourtrc，去掉 # AURURL 的注释，修改为

AURURL=”https://aur.tuna.tsinghua.edu.cn”
