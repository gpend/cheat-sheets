procedure to extend lvm?? in linux/ubuntu

fdisk to extend partition
sudo pvresize /dev/sda3
sudo lvextend -l +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
sudo resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv

sudo vgdisplay
sudo vgdisplay ubuntu-vg
sudo lsblk
sudo pvs
sudo pvscan

docs
https://serverfault.com/questions/378086/how-to-extend-a-linux-pv-partition-online-after-virtual-disk-growth
https://askubuntu.com/questions/1269603/resize-the-root-partition-of-ubuntu-20-04-with-an-lvm-partition