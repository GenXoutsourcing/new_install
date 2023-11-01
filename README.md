# VICIDIAL INSTALLATION SCRIPTS (Default is Eastern Time Zone US)
# AlmaLinux Vicidial Install pre_requisites 

```

hostnamectl set-hostname xxxxxx.xxxxx.xxx
### Use YOUR SubDomain

vi /etc/hosts
##Change domain name for actual server ip (xxx.xxx.xxx.xxx   complete domain name    subdomain only)

timedatectl set-timezone America/New_York

yum check-update
yum update -y
yum -y install epel-release
yum update -y
yum install git -y
yum install -y kernel*

#Disable SELINUX
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config    

reboot

````
  Reboot Before running this script

# Install VICIDIAL scripts

```
cd /usr/src/
git clone https://github.com/GenXoutsourcing/new_install
cd new_install
```

# Execute Alma8 Linux Vicidial Install
```
chmod +x Alma8-installer.sh
./Alma8-installer.sh
```


# Install Webphone and SSL cert for VICIDIAL
# DO THIS IF YOU HAVE PUBLIC DOMAIN WITH PUBLIC IP ONLY

```
chmod +x vicidial-enable-webrtc.sh
./vicidial-enable-webrtc.sh
```
