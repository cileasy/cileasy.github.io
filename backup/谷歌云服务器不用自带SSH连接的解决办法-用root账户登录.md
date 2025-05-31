# 修改ssh配置文件并设置root密码

1、用自带的SSH登录到服务器

2、切换到root账户

`sudo -i`

![Joplin_HcPJgnYlj7.png](https://img.987531.xyz/file/1748694342060_Joplin_HcPJgnYlj7.png)

3、编辑sshd配置文件

`vim /etc/ssh/sshd_config`

![Joplin_Uk0e8mvf3l.png](https://img.987531.xyz/file/1748694476796_Joplin_Uk0e8mvf3l.png)

4、修改以下内容

按键盘【i】进入编辑，按【Esc】退出编辑，再输入 **:wq** 保存并退出

![Joplin_YoYmbsyamo.png](https://img.987531.xyz/file/1748694557144_Joplin_YoYmbsyamo.png)

5、重启sshd服务

`service sshd restart`

![123.png](https://img.987531.xyz/file/1748694889351_123.png)

6、为root账户设置密码

`passwd`

![Joplin_TNZyFH4WCj.png](https://img.987531.xyz/file/1748694634460_Joplin_TNZyFH4WCj.png)

输入密码的时候不会显示出来，所以直接输入密码，然后回车，再然后重复输入密码回车

![1234.png](https://img.987531.xyz/file/1748694987569_1234.png)


# 然后用SHELL工具用root账号密码连接就可以了。