# xray for Alwaysdata

在 Alwaysdata 虚拟主机上部署 xray 节点

## 项目特点

* 本项目用于在 Alwaysdata 上部署 xray ，采用的方案为 xray + WebSocket + VMess/Vless/Trojan/Shadowsocks + TLS
* vmess 和 vless 的 uuid 或 trojan 和 shadowsocks 的密码，路径既可以自定义，又或者使用默认值
* 部署完成如发现不能上网，请检查域名是否被墙，如域名被墙，可使用 Cloudflare CDN 或者 worker 解决。

## 部署

* 注册 [Alwaysdata](https://www.alwaysdata.com/)
* 创建一个 Web 项目
* 进入其的 SSH，输入以下命令，以下载项目文件

```shell
wget -N && chmod +x web.sh
```

* 在网站设置中，按照下图设置启动项并设置环境变量
* 项目用到的环境变量
  | 变量名 | 是否必须 | 默认值 | 备注 |
  | ------------ | ------ | ------ | ------ |
  | UUID         | 否 | de04add9-5c68-8bab-950c-08cd5320df18 | 可在线生成 https://www.uuidgenerator.net/ |
  | VMESS_WSPATH | 否 | /vmess | 以 / 开头 |
  | VLESS_WSPATH | 否 | /vless | 以 / 开头 |
  | TROJAN_WSPATH | 否 | /trojan | 以 / 开头 |
  | SS_WSPATH | 否 | /shadowsocks | 以 / 开头 |
  | NEZHA_SERVER | 否 |        | 哪吒探针服务端的 IP 或域名 |
  | NEZHA_PORT   | 否 |        | 哪吒探针服务端的端口 |
  | NEZHA_KEY    | 否 |        | 哪吒探针客户端专用 Key |

## 免责声明

* 本程序仅供学习了解, 非盈利目的，请于下载后 24 小时内删除, 不得用作任何商业用途, 文字、数据及图片均有所属版权, 如转载须注明来源。
* 使用本程序必循遵守部署免责声明。使用本程序必循遵守部署服务器所在地、所在国家和用户所在国家的法律法规, 程序作者不对使用者任何不当行为负责.

## 赞助

爱发电：https://afdian.net/a/Misaka-blog

![afdian-MisakaNo の 小破站](https://user-images.githubusercontent.com/122191366/211533469-351009fb-9ae8-4601-992a-abbf54665b68.jpg)