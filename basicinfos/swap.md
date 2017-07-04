cd /home
dd if=/dev/zero of=swap bs=1G count=10

swapoff -a #停止所有的swap分区
mkswap /home/swap

swapon /home/swap
swapoff /home/swap
