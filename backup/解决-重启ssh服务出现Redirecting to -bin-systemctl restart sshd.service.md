1、启动ssh服务

`systemctl start sshd.service`

2、重启 sshd 服务

`systemctl restart sshd.service`

3、设置服务开启自启

`systemctl enable sshd.service`

### 最后查看一下状态

`systemctl status sshd.service`

![chrome_uxF673W9IQ.png](https://img.987531.xyz/file/1748696268336_chrome_uxF673W9IQ.png)

### 看到running就代表成功了
