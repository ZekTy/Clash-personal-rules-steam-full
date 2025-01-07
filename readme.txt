
        解决各种分流规则steam不能满速下载，开启ipv6后不能满速下载，dns泄露问题
        实现效果开启ipv6后steam满速下载，商店个人等页面走代理，下载走直连
        开启允许解析ipv6，不勾选ipv6代理可能导致sg节点不解锁奈飞
        勾选ipv6代理，勾选绕过大陆，节点不支持ipv6不影响正常使用

模板文件前置添加Lhie1的special.yaml
https://github.com/dler-io/Rules/blob/main/Clash/Provider/Special.yaml
steam商店个人等页面域名列表
https://github.com/dler-io/Rules/blob/main/Clash/Provider/Steam.yaml
手动更改
参考思路文档
https://shuaiyang.wang/index.php/archives/5/


自建subconverter订阅转换 支持vless hy2 
https://sub.inklazy.com/
后端
https://suc.inklazy.com/sub

#禁止Netflix解析ipv6   防止Netflix解析到ipv6导致SG节点无法解锁
#/etc/dnsmasq.conf添加
server=/netflix.com/#
address=/netflix.com/::
server=/netflix.net/#
address=/netflix.net/::
server=/nflxext.com/#
address=/nflxext.com/::
server=/nflximg.net/#
address=/nflximg.net/::
server=/nflxvideo.net/#
address=/nflxvideo.net/::

#实在不行可以禁止steam ipv6解析，
#禁止steam的域名解析为ipv6地址
#/etc/dnsmasq.conf添加
# 禁止这些 Steam 相关域名走 IPv6
server=/steambroadcast.akamaized.net/#
address=/steambroadcast.akamaized.net/::
server=/steamcommunity-a.akamaihd.net/#
address=/steamcommunity-a.akamaihd.net/::
server=/steampipe.akamaized.net/#
address=/steampipe.akamaized.net/::
server=/steamstore-a.akamaihd.net/#
address=/steamstore-a.akamaihd.net/::
server=/steamusercontent-a.akamaihd.net/#
address=/steamusercontent-a.akamaihd.net/::
server=/steamuserimages-a.akamaihd.net/#
address=/steamuserimages-a.akamaihd.net/::
# 禁止这些 Steam 域名后缀走 IPv6
server=/fanatical.com/#
address=/fanatical.com/::
server=/humblebundle.com/#
address=/humblebundle.com/::
server=/playartifact.com/#
address=/playartifact.com/::
server=/steam-chat.com/#
address=/steam-chat.com/::
server=/steamcommunity.com/#
address=/steamcommunity.com/::
server=/steamgames.com/#
address=/steamgames.com/::
server=/steampowered.com/#
address=/steampowered.com/::
server=/steamserver.net/#
address=/steamserver.net/::
server=/steamstat.us/#
address=/steamstat.us/::
server=/steamstatic.com/#
address=/steamstatic.com/::
server=/underlords.com/#
address=/underlords.com/::
server=/valvesoftware.com/#
address=/valvesoftware.com/::
