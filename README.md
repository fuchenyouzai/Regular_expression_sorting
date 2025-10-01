悠哉 IPTV节目列表 → M3U格式转换工具 是一个纯前端 HTML + JS 工具正则整理小工具
核心概念
正则表达式整理IPTV节目列表
查找目标
^.*ChannelNa\+?me="(.+?)"\,UserChannelID="(.+?)"\,ChannelURL="(.+?)://(.+?)".time.*$

替换为：
#EXTINF:-1,\1\n\http://0.0.0.0:0000/udp/\4

0.0.0.0:0000改为你的udpxy代理地址

然后再删除掉不需要的部分，保存为m3u格式文件。


测试内容
复制测试内容予以填写测试
xxxChannelName="CCTV1",UserChannelID="1001",ChannelURL="udp://239.1.1.1:1234".timexxx
ChannelName="BBC",UserChannelID="2002",ChannelURL="http://media.example.com/path/stream.m3u8"
ChannelName="MyRTSP",UserChannelID="3003",ChannelURL="rtsp://192.168.2.50/stream"

假设输出结果示例为

#EXTM3U
#EXTINF:-1,CCTV1
http://192.168.1.100:4022/udp/239.1.1.1:1234
#EXTINF:-1,BBC
http://media.example.com/path/stream.m3u8
#EXTINF:-1,MyRTSP
http://192.168.1.100:4022/rtsp/192.168.2.50/stream
