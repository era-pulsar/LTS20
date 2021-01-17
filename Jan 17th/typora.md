## LTS20

- 安装完……第一次进系统……联网……修改新立得软件源……更新软件

  ```sudo vi /etc/apt/sources.list```
  
  替换成以下内容
  
  ```
  deb http://mirrors.aliyun.com/ubuntu/ focal main restricted
  deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted
  deb http://mirrors.aliyun.com/ubuntu/ focal universe
  deb http://mirrors.aliyun.com/ubuntu/ focal-updates universe
  deb http://mirrors.aliyun.com/ubuntu/ focal multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-updates multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted
  deb http://mirrors.aliyun.com/ubuntu/ focal-security universe
  deb http://mirrors.aliyun.com/ubuntu/ focal-security multiverse
  ```
  
  更新软件

  ```sudo apt-get update && sudo apt-get install -y openssh-server vim curl ifstat firefox && sudo update-alternatives --set editor /usr/bin/vim.basic```

  查看ip地址

  ```ip a``` 

- 远程连接这台机器

  ```ssh racing@192.168.0.107```

- 下载官方VBox

  ```https://download.virtualbox.org/virtualbox/6.1.16/virtualbox-6.1_6.1.16-140961~Ubuntu~eoan_amd64.deb```

- 安装VBox

  ```sudo dpkg -i virtualbox-6.1_6.1.16-140961~Ubuntu~eoan_amd64.deb ```

  ```sudo apt-get install -f```

  提示不能build内核模块

  This system is currently not set up to build kernel modules.

  Please install the gcc make perl packages from your distribution.

  This system is currently not set up to build kernel modules.

  Please install the gcc make perl packages from your distribution.

  

  There were problems setting up VirtualBox. To re-start the set-up process, run

   /sbin/vboxconfig

  as root. If your system is using EFI Secure Boot you may need to sign the

  kernel modules (vboxdrv, vboxnetflt, vboxnetadp, vboxpci) before you can load

  them. Please see your Linux system's documentation for more information.

  那么继续

  ```sudo apt-get install build-essential module-assistant```

  ```sudo m-a prepare```

  ```sudo /sbin/vboxconfig```

  vboxdrv.sh: Stopping VirtualBox services.

  vboxdrv.sh: Starting VirtualBox services.

  vboxdrv.sh: Building VirtualBox kernel modules.

  最后一步
  
  ```sudo adduser racing vboxusers```
  
  搞定！
