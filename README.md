# วิธีติดตั้ง OpenVPN Server และวิธีใช้งาน OpenVPN

## 1. Update ubuntu
```sh
sudo apt update
sudo apt -y upgrade
```

## ทำการค้นหา Local IP ของเครื่อง
```sh
ip a
ip a show eth0
```

## ค้นหาร Public IP
```sh
dig +short myip.opendns.com @resolver1.opendns.com
```
หรือ
```sh
dig TXT +short o-o.myaddr.l.google.com @ns1.google.com | awk -F'"' '{ print $2}'
```

## ทำการ Download ไฟล์ติดตั้ง
```sh
wget https://git.io/vpn -O openvpn-install.sh
```

## Set Permistion ให้กับไฟล์ติดตั้ง
```sh
chmod +x openvpn-install.sh
```

## ทำการ Run ไฟล์
```sh
sudo ./openvpn-install.sh
```

