# 一、注册和验证谷歌云账号

1、注册账号，用[“美国人信息生成器”](https://www.meiguodizhi.com/)的信息填写
[注册地址](https://cloud.google.com/?hl=zh_cn)
[美国人信息生成器](https://www.meiguodizhi.com/)

 2、添加付款方式：需要外币信用卡或借记卡！！（可重复使用）![G1.png](https://img.987531.xyz/file/blog/1753186014483_G1.png)
_注意：不要立即点击“激活完整账号”，三个月试用期过后再点击。原来已撸过3个月试用的旧账号，依然有效。_

# 二、创建完全免费的VM实例
## 完全免费的配置选择：
1、地区：俄勒冈、爱荷华或南卡罗来纳（建议俄勒冈）
![G2.png](https://img.987531.xyz/file/blog/1753186089988_G2.png)
2、机器配置：E2-micro
![g3.png](https://img.987531.xyz/file/blog/1753186271759_g3.png)

3、操作系统：Linux系统（推荐Debian）

4、存储空间：标准永久性磁盘 30GB （数据保护 - 快照时间表，要改为“无备份”，否则会收费）
![g4.png](https://img.987531.xyz/file/blog/1753186164997_g4.png)

5、网络服务层级：标准
![g5.png](https://img.987531.xyz/file/blog/1753186349957_g5.png)
# 三、创建防火墙规则（vps创建完后）:名称随便填写、目标：网络中所以实例、来源范围：0.0.0.0/0
![g6.png](https://img.987531.xyz/file/blog/1753186380250_g6.png)
_图示为开放所以端口，根据实际情况修改_

# 四、DD系统（谷歌的系统个人觉得不好用）非必须
1、点击右侧SSH连接到VPS

2、切换到root权限
`sudo -i`

3、执行一键重装系统命令（示例是Debian11）
`bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/MoeClub/Note/master/InstallNET.sh') --ip-addr 10.138.0.12 --ip-gate 10.138.0.1 --ip-mask 255.255.255.0 -d 11 -v 64 -p 12345 -port 22 `

参数解释：
10.138.0.12  谷歌云VPS内网IP 谷歌云后台去找

10.138.0.1  谷歌云VPS内网IP的网关 前三位数和IP相同 第四位数为1

系统参数

-d 10  【7、8、9、10，11】Debian

-u 20.04  【14.04、16.04、18.04、20.04】Ubuntu


密码参数，可以改成别的

-p 12345

端口参数

port 22



# 最后等待大约半小时左右用你设置的IP和端口，输入密码登录就可以了。