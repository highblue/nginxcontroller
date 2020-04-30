# nginxcontroller

1. please run the 

```
cd controller-installer
./uninstall.sh
sudo kubeadm reset
```
follow the instruction to delete the config files and the iptables

2. configure the hostname using this:

```
sudo hostnamectl set-hostname --static [xxx.com]
```

3. update the host file

```
sudo vim /etc/hosts
127.0.0.1 xxx.com ctrl.xxx.com
```

4. reboot

5. run the installation again

```
cd controller-install
./install.sh -n
```
input the parameters example:

  smtp: localhost;
  smtp port: 25;
  FQDN: ctrl.demo.io;
  username: admin@demo.io;
  passwd: xxxxxx;
