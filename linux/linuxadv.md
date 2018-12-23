## linux实操篇
### 一、xshell(远程登录linux操作系统)
    用法：
### 二、xftp5(远程上传，下载)
### <h2 style="color:red">三、Vi、vim的使用（类似于Windows的记事本）（略）<br>
### 四、关机重启注销（略）</h2>
### 五、用户管理
- 添加用户
        useradd [option] hostname     //添加用户
        useradd -d /home/ltc ltc      //指定(自动)目录添加用户
        passwd ltc                    //更改用户密码
- 删除用户
        userdel ltc                   //保留家目录式删除用户
        userdel -r ltc                //删除家目录式删除
### 六、使用指令
#### 运行级别
<b>级别设置原因</b>：为了在一些领域或某些用户而设置的权限大小

> 指令级别图示

![](/linux/jibie.jpg)
> 切换命令

        # init [0123456]
> 找回root密码<br>
> 进入单用户模式（进入此模式不需要密码），直接passwd修改命令

##### 帮助指令（man [指令]）
##### 文件目录类
1.pwd (print working directary)<br>
2.ls (默认 -a:包括隐藏文件  -l:以列表方式显示)<br>
3.mkdir  (mkdir -p /home/demo/rs     --创建多级目录)  <br>
4.rm [-r,-f] filename <br>
5.touch(某人说了句“摸一下”) <br>
6.cp (copy)<br>
        # cp a.md b/      //copy a.md to b
        # cp -r test/ b/   //复制目录到目录，-r是递归作用
7.mv ()<br>
        # mv oldnamefile newnamefile   //重命令
        # mv file newfile        //移动命令
8.查找<br>
        # cat -n FileName | more
        # cat -n FileName
        # more FileName
        # less FileName



