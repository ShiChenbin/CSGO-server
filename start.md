# 参考文档
b站up 牧也Muyea [传送门](https://www.bilibili.com/video/BV1h4411W7LZ) 

# 教程正文

## 一、租购一个属于自己的服务器

### 服务器购买链接
[传送门](http://t.cn/AiKKE3Vl)


![在这里插入图片描述](https://img-blog.csdnimg.cn/20210328174324921.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMzgyMzUw,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/2021032817444337.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMzgyMzUw,size_16,color_FFFFFF,t_70)
### 为服务器创建一个csgo需要的端口
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210328180129748.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMzgyMzUw,size_16,color_FFFFFF,t_70)
端口信息如图所示，一模一样即可。

### 说明
除地域和购买市场可以根据自身情况选择外，其余一致即可

### 下载SteamCmd

1.选择一个剩余空间较大的盘，可以是C盘D盘，我选择的是F盘，以下以X盘或X：代替使用硬盘以及地址相关信息

2.下载steamCMD + 下载Notepad++
下载地址
**链接：https://pan.baidu.com/s/1hd8p3rhlxOcRtVE45GbsLA 提取码：a9oe** 


2.复制并保存下面的内容到：X:\steamcmd\1.bat(如果没有1.bat请自行创建)然后运行1.bat

```cpp
steamcmd +login anonymous +app_update 740 validate +quit
```

3.X:\steamcmd\steamapps\common\Counter-Strike Global Offensive Beta - Dedicated Server
创建一个2.bat,然后将代码复制进去并且运行

```cpp
srcds.exe -game csgo -console -ip 0.0.0.0 -usercon +game_type 0 +game_mode 0 +port 27015 +map de_dust2 -tickrate 128 -maxplayers_override 32 +mapgroup mg_active
```

4.为服务器设置1个token密钥 如果没有设置 则会提示只允许内网连接
**申请服务器秘钥您steam账号必须具备的条件**

> Your Steam account must not be currently community banned or locked.
> 你的Steam账号 必须非被ban和锁定状态 Your Steam account must not be limited.
> 你的账号必须不是限制状态，CDKEY/礼物不能解除限制，必须充值/消费5刀以上 Your Steam account must have a
> qualifying registered phone.  你的账号必须绑定手机 Your Steam account must own
> the game for which you are creating a game server account.
> 你的Steam账户必须有对应游戏 Your Steam account may create 1000 game server
> accounts. 你可能最多 可以建 1000个 游戏服务器账号

 https://steamcommunity.com/dev/managegameservers
填写 730 （CSGO服务器端） ，下面是备注可选
然后点击create创建
![在这里插入图片描述](https://img-blog.csdnimg.cn/2021032817552082.png)
登录令牌就是我们所需要的秘钥

之后打开服务器中的文件夹
csgo/cfg 下的
server.cfg 文件 **建议使用Notepad++ 编辑此文件 不要用记事本.**
（如果没有server.cfg则自己创建一个，并且填入下面这句指令）

```cpp
sv_setsteamaccount   "XXXX" 
```

5.直连命令 使用connect命令加入游戏。
打开国际服，点击“~”键打开控制台，输入“connect 加上空格加IP”
```cpp
connect + IP
```
IP可以在2.bat运行的cmd页面看到。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210328180526671.png)

> G就是表示外网的社区服搭建成功A则是只能在局域网上游玩


# 安装插件

CSGO 所有插件运行 依赖于SourceMod（SM） + MetaMod（MM）
SM  http://www.sourcemod.net/snapshots.php   
MM http://www.sourcemm.net/downloads.php


