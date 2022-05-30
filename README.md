# 安装更新运行环境（Debian系统）
apt update -y && apt dist-upgrade -y && apt install -y curl && apt install -y socat

apt-get install -y xz-utils openssl gawk file wget screen && screen -S os

# 更改SSH终端中文语言
wget -N --no-check-certificate https://github.com/picknone/buildsite/raw/main/LocaleCN.sh && bash LocaleCN.sh

# 更改服务器时区为上海
timedatectl set-timezone 'Asia/Shanghai'

# 首先宝塔面板7.7原版
curl -sSO https://github.com/picknone/buildsite/raw/main/install_panel.sh && bash install_panel.sh

# 然后执行一键开心脚本
curl -sSO https://github.com/picknone/buildsite/raw/main/one_key_happy.sh && bash one_key_happy.sh

# 最后执行下一键优化补丁
wget -sSO https://github.com/picknone/buildsite/raw/main/optimize.sh && bash optimize.sh⠀
