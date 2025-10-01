# redesigned-garbanzo
正则表达式整理IPTV节目列表


正则表达式整理IPTV节目列表
查找目标
^.*ChannelNa\+?me="(.+?)"\,UserChannelID="(.+?)"\,ChannelURL="(.+?)://(.+?)".time.*$

替换为：
#EXTINF:-1,\1\n\http://0.0.0.0:0000/udp/\4

0.0.0.0:0000改为你的udpxy代理地址

然后再删除掉不需要的部分，保存为m3u格式文件。
