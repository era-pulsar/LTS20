## LTS20

- 安装完……第一次进系统……联网……立刻安装ssh-server

  ``` sudo apt install openssh-server``` 

  ```ip a``` 查看ip地址

- 远程连接这台机器

  ```ssh racing@192.168.0.107```

- 修改新立得软件源

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

- 更新软件

  ```sudo apt-get update && sudo apt-get install -y vim curl ifstat firefox && sudo update-alternatives --set editor /usr/bin/vim.basic```
