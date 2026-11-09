# bibb 的文章播客

把文章按信息密度提炼成单人讲解音频，保留可订阅的系列记录。本仓库存放 **节目音频、封面与 RSS**；生成工作流位于 [article-to-podcast](https://github.com/veasil/article-to-podcast)。

## 订阅入口

当前 [podcast.xml](podcast.xml) 中的音频地址使用 GitHub Pages：

- RSS 预期地址：[podcast.xml](https://veasil.github.io/podcast-host/podcast.xml)
- 音频目录：[audio/](audio/)
- 封面：[cover.jpg](cover.jpg)

以上 RSS 公开地址需在 Pages 部署成功后使用；本文没有对线上服务可达性或客户端兼容性作验证。

## 已收录节目

以下信息来自当前 RSS，共 5 集：

| 日期 | 节目 | 时长 |
| --- | --- | --- |
| 2026-08-22 | DeepSeek Harness 热门插件鉴赏 | 04:02 |
| 2026-08-22 | 我用 AI 管理 10 家跨境店铺，月入百万：17 个流程和全部工具公开 | 11:56 |
| 2026-08-22 | Codex as a Platform：把 Codex 当作平台来构建 | 06:28 |
| 2026-08-26 | AI 原生 SDLC 实战指南：Anthropic 六大实践 | 10:37 |
| 2026-08-28 | 制造现代人：如果不工作、不消费，你是谁？+ 我问了几十个人是做什么的 | 13:24 |

标题按 feed 原文保留，用于识别文章内容。

## 维护一集节目的步骤

1. 在生成工作流中准备口播稿并合成音频，审听后保存 MP3。
2. 用稳定、唯一的文件名加入 `audio/`，避免覆盖已有节目的文件。
3. 在 `podcast.xml` 中追加条目，核对标题、来源、音频 URL、唯一 GUID、发布日期与实际时长。
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
