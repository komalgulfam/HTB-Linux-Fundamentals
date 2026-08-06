# Linux Commands - Quick Revision

## Files
ls
ls -l
ls -la
pwd
cd
mkdir
cp
mv
rm
rm -rf
cat
nano
find

## Permissions
chmod +x file.sh
chown user:group file
ln -s source target

## Users
useradd
passwd
usermod
su -

## Networking
ip addr
ip route
ping -c 4 8.8.8.8
traceroute -I google.com
netstat -tulnp

## Services
systemctl status SERVICE
systemctl start SERVICE
systemctl restart SERVICE
systemctl enable SERVICE

## Logs
journalctl
journalctl -k
journalctl -u ssh
journalctl _COMM=sudo

## Firewall
iptables -L
iptables -L --line-numbers
iptables -A INPUT -j DROP

## SSH
ssh user@IP
ssh-keygen
ssh-copy-id user@IP

## File Transfer
rsync -av source destination
wget URL
python3 -m http.server 8080

## Storage
mount
umount
fdisk -l
swapon --show

## Docker
docker images
docker ps
docker build
docker run
docker exec
docker stop
docker start

## LXC
lxc-ls -f
lxc-start
lxc-attach
lxc-stop
