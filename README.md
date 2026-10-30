# Mihomo-Party-ACL4SSR
Mihomo Party的覆写库包含作者分享的和自己写的

`custom_config.yaml` 的 DNS 与本地通信规则：

- `ChinaDomain` 规则集、`.cn`、`shumeitv.com` 和 `duodiantong.net`（含子域名）使用阿里 DNS DoH，并通过 `DIRECT` 查询。
- 其余域名使用 Cloudflare / Google DoH，通过现有的「☑️ 手动切换」代理组查询。
- `localhost.weixin.qq.com` 排除 Fake-IP 并强制直连，避免微信快速登录的本地通信被发送到代理节点。
- `duodiantong.net` 及其子域名的网站流量也强制直连；DNS 解析规则和网站流量规则分别配置。

此模板仅包含分流规则，不包含节点凭证。更改其他模板时需分别同步对应规则。
