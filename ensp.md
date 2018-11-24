---
title: ensp模拟搭建
date: 2018-11-20 22:53:03
tags:
---
#### 计算机网络折腾计
> 生命在于折腾
<!--more-->
##### 一、工具准备
> ensp模拟器，wireshark
> 难点：路由器的设置和网络地址

##### 二、连接设备
![](/img/ensp/1.jpg)
##### 三、R的配置(<p style="color:red">设备开启后操作)
    [HUAWEI] sys            //打开设置权限
    [HUAWEI] sysname R1         //重命名
    [R1] interface e0/0/0          //配置端口e0/0/0
    [R1] ip add xxx.xxx.xxx.xxx xx;      //设置端口的地址,格式为ip地址 掩码
    [R1] q       //退出端口设置
    [R1] rip         //rip协议网络设置
    [R1] network xxx.xxx.xxx.0        //设置网络地址
    [R1] q         //关闭路由器设置
    [R1] save all          //保存设置

###### <p style="color:green">图图来了（R1的配置）
![](img/ensp/2.jpg)![](img/ensp/3.jpg)![](img/ensp/4.jpg)![](img/ensp/5.jpg)![](img/ensp/6.jpg)![](img/ensp/7.jpg)

> R2的配置
![](img/ensp/8.jpg)![](img/ensp/9.jpg)![](img/ensp/10.jpg)![](img/ensp/11.jpg)![](img/ensp/12.jpg)![](img/ensp/13.jpg)![](img/ensp/14.jpg)![](img/ensp/15.jpg)

##### 四、ping ip地址
> PC1 ping PC3
> ![](img/ensp/16.jpg)

<a href="img/ensp.rar" >文件下载</a>