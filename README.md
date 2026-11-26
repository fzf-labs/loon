# loon

个人维护的 [Loon](https://nsloon.app/) 远程规则仓库。

只放规则文件，不放完整配置。`.lcf`、机场订阅链接、证书等敏感内容不要提交到本仓库。

## 目录

```text
rules/
  Telegram.list        # 按原先 Telegram.lsr 整理，40 条
  TikTok.list          # 按原先 TikTok.lsr 收成后缀
  OpenAI.list          # OpenAI / ChatGPT / Sora
  Claude.list          # Anthropic / Claude
  Gemini.list          # Gemini、AI Studio、DeepMind、Antigravity
  Copilot.list         # GitHub Copilot
  Perplexity.list
  Mistral.list
  Kimi.list            # Kimi / Moonshot
  Poe.list
  HuggingFace.list
  Groq.list
  Meta.list
  Ollama.list
  OpenRouter.list
  JetBrains.list
  Trae.list
  Alibaba.list         # 阿里云国际
  Zhipu.list           # 智谱国际
  StepFun.list         # 阶跃星辰国际
  SiliconFlow.list     # 硅基流动国际
  MiniMax.list
  Xiaomi.list          # 小米国际 Token Plan
  Zed.list
  Devin.list
  Nvidia.list
  SpaceXAI.list        # Cursor、Grok、Grok Bot、登录域名和 X
  LLM-Gateway.list     # 其余模型 API 与网关
  Speedtest.list       # 按原先约 18500 条测速主机名压缩
  LAN.list             # 私网地址，DIRECT
  China.list           # GEOIP,cn，DIRECT
configs/
  自动.lcf            # 当前使用的配置，订阅地址和证书已换成占位
```

## 在 Loon 中使用

在配置的 `[Remote Rule]` 中添加：

```ini
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Telegram.list, policy=兜底后备策略, tag=Telegram, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/TikTok.list, policy=TikTok策略, tag=TikTok, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/OpenAI.list, policy=日本时延优选, tag=OpenAI, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Claude.list, policy=日本时延优选, tag=Claude, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Gemini.list, policy=日本时延优选, tag=Gemini, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Copilot.list, policy=日本时延优选, tag=Copilot, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Perplexity.list, policy=日本时延优选, tag=Perplexity, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Mistral.list, policy=日本时延优选, tag=Mistral, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Kimi.list, policy=日本时延优选, tag=Kimi, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Poe.list, policy=日本时延优选, tag=Poe, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/HuggingFace.list, policy=日本时延优选, tag=HuggingFace, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Groq.list, policy=日本时延优选, tag=Groq, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Meta.list, policy=日本时延优选, tag=Meta, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Ollama.list, policy=日本时延优选, tag=Ollama, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/OpenRouter.list, policy=日本时延优选, tag=OpenRouter, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/JetBrains.list, policy=日本时延优选, tag=JetBrains, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Trae.list, policy=日本时延优选, tag=Trae, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Alibaba.list, policy=日本时延优选, tag=Alibaba, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Zhipu.list, policy=日本时延优选, tag=Zhipu, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/StepFun.list, policy=日本时延优选, tag=StepFun, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/SiliconFlow.list, policy=日本时延优选, tag=SiliconFlow, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/MiniMax.list, policy=日本时延优选, tag=MiniMax, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Xiaomi.list, policy=日本时延优选, tag=Xiaomi, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Zed.list, policy=日本时延优选, tag=Zed, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Devin.list, policy=日本时延优选, tag=Devin, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Nvidia.list, policy=日本时延优选, tag=Nvidia, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/SpaceXAI.list, policy=日本时延优选, tag=SpaceXAI, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/LLM-Gateway.list, policy=日本时延优选, tag=LLM-Gateway, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/Speedtest.list, policy=兜底后备策略, tag=Speedtest, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/LAN.list, policy=DIRECT, tag=LAN, enabled=true
https://raw.githubusercontent.com/fzf-labs/loon/main/rules/China.list, policy=DIRECT, tag=CN REGION, enabled=true
```

这些服务规则互不重叠，改某一条的 `policy` 不会影响其他服务。仓库需要公开，Loon 才能拉取 `raw.githubusercontent.com` 链接。添加后在 Loon 中更新远程规则。

## 配置

`configs/自动.lcf` 是当前正在使用的配置副本。订阅地址和 MITM 证书已换成空占位，导入后需要自己填回本机的订阅链接。本机完整配置仍以 iCloud 里的 `自动` 为准，不要把带订阅 token 的文件提交到这个仓库。

## 规则说明

`rules/SpaceXAI.list` 覆盖 Cursor、Grok、Grok Bot、登录域名和 X：`cursor.sh`、`cursor.com`、`cursorapi.com`、`cursor-cdn.com`、`cursorvm.com`、`anysphere.inc`，以及 `spacexsi.com`、`grok.com`、`grokbot.com`、`x.ai`、`grokusercontent.com`、`grokipedia.com`、`x.com`、`twitter.com`。`rules/OpenAI.list` 只包含 OpenAI 相关域名，共 23 条，不包含整站 `stripe.com`、`sentry.io`、`auth0.com`。ChatGPT 自己的 `o33249.ingest.sentry.io` 和 `o207216.ingest.sentry.io` 单独保留。原先 `AI.lsr` 里的其他服务按产品拆成独立规则，`LLM-Gateway.list` 只放剩余的模型 API 和网关。`googleapis.com`、`microsoft.com`、`aliyuncs.com` 只保留具体主机，不包含整站 `bing.com`。`rules/China.list` 只有 `GEOIP,cn`。

`rules/Speedtest.list` 把原先约 18500 条测速服务器主机名收成 `speedtest`、`ookla` 两个关键词。`rules/TikTok.list` 把原先同一 CDN 下的多条主机名收成后缀，并去掉 `cocacola.co.jp`、`courses.snapsolve.com`、`api.snapkit.com`、`engagements.appsflyer.com` 这几个与 TikTok 无关的域名。

## 参考

配置写法以 Loon 官方文档为准。下面这些仓库只作来源说明，本仓库不是它们的镜像。可莉的 `.lsr` 和插件正文没有放进本仓库，插件仍从原地址加载。

### 文档

- [Loon](https://nsloon.app/)
- [Loon 手册](https://nsloon.app/LoonManual/)
- [规则](https://nsloon.app/docs/Rule/)
- [策略](https://nsloon.app/docs/Policy/)
- [策略组](https://nsloon.app/docs/Policy/policygroup)

### 仓库

- [luestr/ShuntRules](https://github.com/luestr/ShuntRules)：可莉的分流规则。`configs/自动.lcf` 的配置段和插件入口沿用这份自动配置，作者为 [iKeLee](https://t.me/iKeLee)，插件中心是 [hub.kelee.one](https://hub.kelee.one)。`Telegram`、`TikTok`、`Speedtest`、`AI`、`LAN`、`China` 按本机旧 `.lsr` 重写。
- [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)：`rules/Telegram.list` 的 40 条与其中的 [Telegram.list](https://github.com/blackmatrix7/ios_rule_script/blob/master/rule/Loon/Telegram/Telegram.list) 一致，许可证为 GPL-3.0，全文见 `LICENSE-GPL`。
- [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)：`geoip-url` 使用的 `Country.mmdb`。数据来自 [MaxMind GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)。
- [P3TERX/GeoLite.mmdb](https://github.com/P3TERX/GeoLite.mmdb)：`ipasn-url` 使用的 GeoLite2 ASN 库。
- [sub-store-org/Sub-Store](https://github.com/sub-store-org/Sub-Store)：`resource-parser` 使用的订阅解析脚本。
- 策略组图标：[Orz-3/mini](https://github.com/Orz-3/mini)、[Koolson/Qure](https://github.com/Koolson/Qure)、[shindgewongxj/WHATSINStash](https://github.com/shindgewongxj/WHATSINStash)。
