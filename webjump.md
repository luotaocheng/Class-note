## 省流量，校园科学上网
### 1.准备工具
### 2.服务器配置
### 3.xshell配置
### 4.VPN设置
### 5.科学网页展示
<hr>
#### 1.准备工具<br>
- 云服务器
- 打包软件（xshell,openvpn,se-vpn，都放在文件中，请自取）
 
#### 2.服务器配置<br>

推荐购买阿里云轻量级服务器，学生价9.5元/月。
![](/internet/centos.jpg)
<b>重置密码
![](/internet/manager.jpg)
<b>设置防火墙
![](/internet/fire1.jpg)
![](/internet/fire2.jpg)

#### 3.xshell配置

![](/internet/x1.jpg)
![](/internet/x2.jpg)
![](/internet/x3.jpg)
![](/internet/x4.jpg)
![](/internet/x5.jpg)

<b>安装软件
        
        > 安装gcc环境
            yum install gcc gcc-c++ make tar -y
        > 安装wget
            yum install -y wget
        > 安装Linux版的softenter
            wget -e -robots=off http://files.mawenjian.net/SoftEtherVPN/softether-vpnserver-v4.10-9473-beta-2014.07.12-linux-x64-64bit.tar.gz
        > 下载下来后进行解压：
            tar -zxvf softether-vpnserver-v4.10-9473-beta-2014.07.12-linux-x64-64bit.tar.gz
        > 安装
            1 cd vpnserver
            2 ./.install.sh
            期间连续输入三个“1”。
            这时候启动vpn。
                ./vpnserver start
            输入
                ./vpncmd
            分别输入：“1” “回车” “回车”。提示符变为“VPN Server”时输入：
             输入 ServerPasswordSet
         > 设置密码（这个很关键，后边要使用）
             vpn server>
             
#### 4.vpn设置
 
  打开softenter server
  ![](/internet/4.1.jpg)
  ![](/internet/4.2.jpg)
  ![](/internet/4.3.jpg)
  ![](/internet/4.4.jpg)
  ![](/internet/4.5.jpg)
  ![](/internet/4.6.jpg)
  ![](/internet/4.7.jpg)
  ![](/internet/4.8.jpg)
  ![](/internet/4.9.jpg)
  ![](/internet/4.10.jpg)
  
  
  <b>把保存的压缩文件解压
  
  ![](/internet/4.11.jpg)
  把这个ovpn文件提取出来，然后放在openvpn config 目录下
  ![](/internet/4.12.jpg)
  我已经把名字命名为测试

#### 5.科学网页展示
    
<b>把所有登陆校园网的账号退出<br>
<b>打开openvpn，在隐藏栏右键连接
![](/internet/5.1.jpg)
<b>输入之前我们设置的用户的账号和密码，0，0
![](/internet/5.2.jpg)
<b>电脑图标变成绿色，打开浏览器，就可以畅快的使用网络了
注意哦：可能网速有点慢，本人已写了一个，大家可以直接用openvpn打开使用，地址在根目录位置

吃饭了。。。。。。
  
