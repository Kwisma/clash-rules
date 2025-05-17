# 简介

本项目生成适用于 [**Clash Premium 内核**](https://github.com/Dreamacro/clash/releases/tag/premium)的规则集（RULE-SET），同时适用于所有使用 Clash Premium 内核的 Clash 图形用户界面（GUI）客户端。使用 GitHub Actions 北京时间每天早上 6:30 自动构建，保证规则最新。

## 说明

添加了 mihomo MRS 格式文件，将 txt 文件修改为 yaml

本项目规则集（RULE-SET）的数据主要来源于项目 [@Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 和 [@v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)；[`Apple`](https://github.com/Loyalsoldier/clash-rules/blob/release/apple.mrs) 和 [`Google`](https://github.com/Loyalsoldier/clash-rules/blob/release/google.mrs) 列表里的域名来源于项目 [@felixonmars/dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list)；中国大陆 IPv4 地址数据使用 [@17mon/china_ip_list](https://github.com/17mon/china_ip_list)。

本项目的规则集（RULE-SET）只适用于 Clash **Premium** 版本。Clash Premium 相对于普通版，增加了 **TUN 增强模式**，能接管设备所有 TCP 和 UDP 流量。

### Clash Premium 各版本下载地址

> ⚠️ 由于 Clash 及其部分周边生态项目于 2023 年 11 月上旬删库跑路，现提供部分官方原版安装包、可执行文件，详情见 [**hidden**](https://github.com/Loyalsoldier/clash-rules/tree/hidden) 分支。

- Clash Premium **命令行**版：
  - [官方版](https://github.com/Loyalsoldier/clash-rules/tree/hidden/software/clash-premium)（适用于 Windows、macOS、Linux、OpenWRT 等多种平台）
  - [衍生版 Clash.Meta](https://github.com/MetaCubeX/Clash.Meta/releases)（适用于 Windows、macOS、Linux、OpenWRT 等多种平台）
- Clash Premium **图形用户界面**版：
  - [ClashN](https://github.com/2dust/clashN/releases)（适用于 Windows）
  - [ClashX Pro](https://github.com/Loyalsoldier/clash-rules/tree/hidden/software/clashx-pro)（适用于 macOS）
  - [Clash-verge](https://github.com/zzzgydi/clash-verge/releases)（适用于 Windows、macOS、Linux）
  - [Clash for Windows](https://github.com/Loyalsoldier/clash-rules/tree/hidden/software/clash-for-windows)（适用于 Windows、macOS、Linux）
  - [Clash for Android](https://apkpure.com/clash-for-android/com.github.kr328.clash/versions)（适用于 Android）

## 规则文件地址及使用方式

### 在线地址（URL）

> 如果无法访问域名 `raw.githubusercontent.com`，可以使用第二个地址（`cdn.jsdelivr.net`），但是内容更新会有 12 小时的延迟。以下地址填写在 Clash 配置文件里的 `rule-providers` 里的 `url` 配置项中。

- **直连域名列表 direct.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/direct.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/direct.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/direct.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/direct.mrs)
- **代理域名列表 proxy.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/proxy.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/proxy.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/proxy.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/proxy.mrs)
- **广告域名列表 reject.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/reject.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/reject.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/reject.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/reject.mrs)
- **私有网络专用域名列表 private.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/private.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/private.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/private.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/private.mrs)
- **Apple 在中国大陆可直连的域名列表 apple.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/apple.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/apple.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/apple.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/apple.mrs)
- **iCloud 域名列表 icloud.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/icloud.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/icloud.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/icloud.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/icloud.mrs)
- **[慎用]Google 在中国大陆可直连的域名列表 google.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/google.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/google.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/google.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/google.mrs)
- **GFWList 域名列表 gfw.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/gfw.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/gfw.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/gfw.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/gfw.mrs)
- **非中国大陆使用的顶级域名列表 tld-not-cn.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/tld-not-cn.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/tld-not-cn.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/tld-not-cn.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/tld-not-cn.mrs)
- **Telegram 使用的 IP 地址列表 telegramcidr.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/telegramcidr.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/telegramcidr.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/telegramcidr.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/telegramcidr.mrs)
- **局域网 IP 及保留 IP 地址列表 lancidr.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/lancidr.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/lancidr.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/lancidr.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/lancidr.mrs)
- **中国大陆 IP 地址列表 cncidr.mrs**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/cncidr.mrs](https://raw.githubusercontent.com/Kwisma/clash-rules/release/cncidr.mrs)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/cncidr.mrs](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/cncidr.mrs)
- **需要直连的常见软件列表 applications.yaml**：
  - [https://raw.githubusercontent.com/Kwisma/clash-rules/release/applications.yaml](https://raw.githubusercontent.com/Kwisma/clash-rules/release/applications.yaml)
  - [https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/applications.yaml](https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/applications.yaml)

### 使用方式

要想使用本项目的规则集，只需要在 Clash 配置文件中添加如下 `rule-providers` 和 `rules`。

#### Rule Providers 配置方式

```yaml
rule-providers:
  reject:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/reject.mrs"
    path: ./ruleset/reject.mrs
    interval: 86400

  icloud:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/icloud.mrs"
    path: ./ruleset/icloud.mrs
    interval: 86400

  apple:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/apple.mrs"
    path: ./ruleset/apple.mrs
    interval: 86400

  google:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/google.mrs"
    path: ./ruleset/google.mrs
    interval: 86400

  proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/proxy.mrs"
    path: ./ruleset/proxy.mrs
    interval: 86400

  direct:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/direct.mrs"
    path: ./ruleset/direct.mrs
    interval: 86400

  private:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/private.mrs"
    path: ./ruleset/private.mrs
    interval: 86400

  gfw:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/gfw.mrs"
    path: ./ruleset/gfw.mrs
    interval: 86400

  tld-not-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/tld-not-cn.mrs"
    path: ./ruleset/tld-not-cn.mrs
    interval: 86400

  telegramcidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/telegramcidr.mrs"
    path: ./ruleset/telegramcidr.mrs
    interval: 86400

  cncidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/cncidr.mrs"
    path: ./ruleset/cncidr.mrs
    interval: 86400

  lancidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/lancidr.mrs"
    path: ./ruleset/lancidr.mrs
    interval: 86400

  applications:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/Kwisma/clash-rules@release/applications.yaml"
    path: ./ruleset/applications.yaml
    interval: 86400
```

#### 白名单模式 Rules 配置方式（推荐）

- 白名单模式，意为「**没有命中规则的网络流量，统统使用代理**」，适用于服务器线路网络质量稳定、快速，不缺服务器流量的用户。
- 以下配置中，除了 `DIRECT` 和 `REJECT` 是默认存在于 Clash 中的 policy（路由策略/流量处理策略），其余均为自定义 policy，对应配置文件中 `proxies` 或 `proxy-groups` 中的 `name`。如你直接使用下面的 `rules` 规则，则需要在 `proxies` 或 `proxy-groups` 中手动配置一个 `name` 为 `PROXY` 的 policy。
- 如你希望 Apple、iCloud 和 Google 列表中的域名使用代理，则把 policy 由 `DIRECT` 改为 `PROXY`，以此类推，举一反三。
- 如你不希望进行 DNS 解析，可在 `GEOIP` 规则的最后加上 `,no-resolve`，如 `GEOIP,CN,DIRECT,no-resolve`。

```yaml
rules:
  - RULE-SET,applications,DIRECT
  - DOMAIN,clash.razord.top,DIRECT
  - DOMAIN,yacd.haishan.me,DIRECT
  - RULE-SET,private,DIRECT
  - RULE-SET,reject,REJECT
  - RULE-SET,icloud,DIRECT
  - RULE-SET,apple,DIRECT
  - RULE-SET,google,PROXY
  - RULE-SET,proxy,PROXY
  - RULE-SET,direct,DIRECT
  - RULE-SET,lancidr,DIRECT
  - RULE-SET,cncidr,DIRECT
  - RULE-SET,telegramcidr,PROXY
  - GEOIP,LAN,DIRECT
  - GEOIP,CN,DIRECT
  - MATCH,PROXY
```

#### 黑名单模式 Rules 配置方式

- 黑名单模式，意为「**只有命中规则的网络流量，才使用代理**」，适用于服务器线路网络质量不稳定或不够快，或服务器流量紧缺的用户。通常也是软路由用户、家庭网关用户的常用模式。
- 以下配置中，除了 `DIRECT` 和 `REJECT` 是默认存在于 Clash 中的 policy（路由策略/流量处理策略），其余均为自定义 policy，对应配置文件中 `proxies` 或 `proxy-groups` 中的 `name`。如你直接使用下面的 `rules` 规则，则需要在 `proxies` 或 `proxy-groups` 中手动配置一个 `name` 为 `PROXY` 的 policy。

```yaml
rules:
  - RULE-SET,applications,DIRECT
  - DOMAIN,clash.razord.top,DIRECT
  - DOMAIN,yacd.haishan.me,DIRECT
  - RULE-SET,private,DIRECT
  - RULE-SET,reject,REJECT
  - RULE-SET,tld-not-cn,PROXY
  - RULE-SET,gfw,PROXY
  - RULE-SET,telegramcidr,PROXY
  - MATCH,DIRECT
```

## 致谢

- [@Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)
- [@Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)
- [@gfwlist/gfwlist](https://github.com/gfwlist/gfwlist)
- [@v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)
- [@felixonmars/dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list)
- [@17mon/china_ip_list](https://github.com/17mon/china_ip_list)

## 项目 Star 数增长趋势

[![Stargazers over time](https://starchart.cc/Loyalsoldier/clash-rules.svg)](https://starchart.cc/Loyalsoldier/clash-rules)
