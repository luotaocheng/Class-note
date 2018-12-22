# linux实操篇
## 一、xshell(远程登录linux操作系统)
    用法：
## 二、xftp5(远程上传，下载)
<h2 style="color:red">三、Vi、vim的使用（类似于Windows的记事本）（略）<br>
四、关机重启注销（略）</h2>
## 五、用户管理
- 添加用户
        useradd [option] hostname     //添加用户
        useradd -d /home/ltc ltc      //指定(自动)目录添加用户
        passwd ltc                    //更改用户密码
- 删除用户
        userdel ltc                   //保留家目录式删除用户
        userdel -r ltc                //删除家目录式删除
