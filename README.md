# bibb 的文章播客

把文章按信息密度提炼成单人讲解音频，保留可订阅的系列记录。本仓库存放 **节目音频、封面与 RSS**；生成工作流位于 [article-to-podcast](https://github.com/veasil/article-to-podcast)。

## 订阅与收听

复制 [RSS 订阅地址](https://veasil.github.io/podcast-host/podcast.xml) 到支持手动添加 RSS 的播客客户端，也可从下方直接打开单集 MP3。

## 已收录节目

以下信息来自当前 RSS，共 5 集：

| 日期 | 节目 | 时长 | 收听 |
| --- | --- | --- | --- |
| 2026-08-22 | DeepSeek Harness 热门插件鉴赏 | 04:02 | [MP3](https://veasil.github.io/podcast-host/audio/episode-20260822-dsh-plugins.mp3) |
| 2026-08-22 | 我用 AI 管理 10 家跨境店铺，月入百万：17 个流程和全部工具公开 | 11:56 | [MP3](https://veasil.github.io/podcast-host/audio/episode-20260822-crossborder.mp3) |
| 2026-08-22 | Codex as a Platform：把 Codex 当作平台来构建 | 06:28 | [MP3](https://veasil.github.io/podcast-host/audio/episode-20260822-codex-platform.mp3) |
| 2026-08-26 | AI 原生 SDLC 实战指南：Anthropic 六大实践 | 10:37 | [MP3](https://veasil.github.io/podcast-host/audio/episode-20260826-sdlc-playbook.mp3) |
| 2026-08-28 | 制造现代人：如果不工作、不消费，你是谁？+ 我问了几十个人是做什么的 | 13:24 | [MP3](https://veasil.github.io/podcast-host/audio/episode-20260828-modern-people.mp3) |

标题按 feed 原文保留，用于识别文章内容。

## 维护一集节目的步骤

1. 在生成工作流中准备口播稿并合成音频，审听后保存 MP3。
2. 用稳定、唯一的文件名加入 `audio/`，避免覆盖已有节目的文件。
3. 在 `podcast.xml` 中追加条目，核对标题、来源、音频 URL、唯一 GUID、发布日期、实际时长与附件字节数（`enclosure` 的 `length`）。
4. 检查 XML 可解析、条目对应的音频文件存在；公开部署后再验证 RSS、封面与音频直链，并用播客客户端试听。

生成仓库的 RSS 辅助脚本仍需人工核对日期格式、频道元信息与重复条目。XML 格式正确只说明文件能解析，音频下载与播放仍需单独验证。

## 文件职责

| 路径 | 用途 |
| --- | --- |
| [podcast.xml](podcast.xml) | 频道与节目元信息 |
| [audio/](audio/) | MP3 节目资产 |
| [cover.jpg](cover.jpg) | 节目封面 |
| [.github/ISSUE_TEMPLATE/podcast.yml](.github/ISSUE_TEMPLATE/podcast.yml) | 已有播客 Issue 表单 |

更新节目时，以 RSS 与对应音频为依据同步本页清单。
