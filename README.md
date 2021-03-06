# LCBot Linux中国微信机器人

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/bestony/LCBot/blob/master/LICENSE) ![](https://img.shields.io/badge/Language-Python-blue.svg) ![](https://img.shields.io/badge/Python-3.X-red.svg)

![](https://postimg.aliavv.com/mbp/b69eb.png)

LCBot 是一个为 Linux 中国服务的微信机器人，主要为 Linux 中国下的微信群做管理、维护等工作。

##  演示
![linux_cn](https://ooo.0o0.ooo/2017/06/26/5950e555835b2.png)

扫描二维码或搜索微信号`china_linux`，回复关键词 `机器人` ，即可拉入本项目微信讨论群

视频教程地址：[点我查看视频教程集合](http://dwz.cn/lcbot) | [Linux/macOS 使用教程](https://v.qq.com/x/page/k03996ry5o1.html) |[完整版 Win 10 使用教程](https://v.qq.com/x/page/y03990en5qu.html) | [单群版机器人使用教程](https://v.qq.com/x/page/p05007bqjv1.html)

免登录意见反馈：[我要新功能！](https://wj.qq.com/s/1334670/bb03/)

## 特性

1. 关键词添加好友自动拉群
2. 私聊发送关键词自动加群
3. 新用户进群自动发送欢迎
4. 设定管理员，管理员可以通过发送命令T人（需要机器人是群主）
5. 监控群每小时发送心跳包
6. 管理员踢人监控群内留底
7. 被拉黑的用户，无法被再次拉群。需要管理员手动释放。
8. 管理员在监控群发送指令获取状态或进行特定操作（现支持“状态”、“重启”）

## 需要
- Python 3
- wxpy

## 安装
下载源码
```
git clone https://github.com/LCTT/LCBot.git
```
安装拓展
```
cd LCBot
pip3 install -U -r  requirements.txt
```
## Docker 版本
感谢 [@OSMeteor](https://github.com/OSMeteor/pythonlcbot) 提供的 Docker 版本

使用方法：

```
docker pull osmeteor/pythonlcbot
docker run -i -t osmeteor/pythonlcbot /bin/bash
cd /opt/LCBot
python export_puid.py
python bot.py
```



## 使用
首先，获取 puid
```
python3 export_puid.py
```
执行成功后，在当前目录下会生成一个 data 文件，在 data 文件中，你可以看的用户的 puid 和群的 puid

> 如果执行后，二维码展示不正常 ，可以执行`sudo localectl set-locale LANG=C.UTF-8`

编辑 config.py 中第 10 行和 20 行，分别填入管理员的 puid 和群的 puid

编辑 config.py 中第 56 行和 69 行，填入管理群名称和监控群名称

编辑 config.py 中第 71 行，填入图灵机器人的 ID

执行命令
```
python3 bot.py
```
## FAQ
查看 [FAQ](https://github.com/LCTT/LCBot/wiki/FAQ)
## Todo

查看 [Todo](TODO.md)

## 贡献指南

查看 [CONTRIBUTING](CONTRIBUTING.md)

## LICENSE

代码基于 [MIT](LICENSE) 协议开源

文档以 [CC-BY-ND](https://creativecommons.org/licenses/by-nd/4.0/) 协议分享

## 致谢

- [wxpy](https://github.com/youfou/wxpy) : 微信机器人 / 优雅而强大的微信个人号 API
