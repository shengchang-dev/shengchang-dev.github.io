---
layout: default
title: 开源 TTS 分类排名：24 个语音合成项目按用途排完
description: 开源语音合成（TTS）分类排名：音色克隆、多人对话、成品工具、端侧部署、基础框架六大类共 24 个项目，星标/协议/更新为 2026-11-22 GitHub 实查，附排名依据与避坑标注。
---

选开源 TTS 最容易犯的错，是按星标从高到低挨个试——星标高可能只是出道早，协议坑、已停更、中文不行，个个都能让你白折腾一周。这份排名按**用途分类、类内排名**：先找到你的场景，再看类内顺序。数据（星标 / 协议 / 最近更新）为 2026-11-22 当日从各项目 GitHub 仓库逐个实查。

**排名依据**（类内综合排序）：维护状态（是否还在更新）> 协议友好度（MIT/Apache 优先，自定义与 AGPL 标注风险）> 中文可用性 > 社区与文档。效果类判断来自公开评测与社区共识，本页不冒充逐个实测；标 ⚠️ 的是协议或状态有坑，看到先停一下。

## 综合推荐榜（做有声书 / 有声内容）

赶时间就看这张，按「省事程度 × 产出质量」综合排：

| 名次 | 项目 | 为什么排这里 |
| --- | --- | --- |
| 1 | GPT-SoVITS | 克隆音色做长篇的默认答案：中文社区最大、教程最多、MIT |
| 2 | VibeVoice | 多人长篇（播客/有声剧）的新标杆，微软出品、MIT |
| 3 | VoxCPM | 克隆 + 音色设计，势头最猛的新项目，Apache-2.0 |
| 4 | CosyVoice | 团队集成首选，工程化完整、方言强 |
| 5 | Abogen | 不折腾引擎、整本书直接转音频的成品工具 |
| 6 | ChatTTS | 对话自然度标杆（短句），但 AGPL 协议先想清楚 |
| 7 | F5-TTS | 干净、易复现，研究和二次开发友好 |
| 8 | sherpa-onnx | 要离线、要端侧部署时的基础设施 |

不想部署任何东西的，看本站的 [在线语音服务分类收录](online-tts.html)；找文本的，看 [公版文本来源站分类收录](text-sources.html)。

## 一、音色克隆与零样本合成

给几秒到一分钟参考音频，用这个音色读任意文本。有声书自建工作流的主力品类。

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) | 64,191 | MIT | 2026-11 | 1 分钟样本训音色，中文教程与答疑全网最多，新手首选 |
| 2 | [VoxCPM](https://github.com/OpenBMB/VoxCPM) | 42,874 | Apache-2.0 | 2026-11 | 清华系，无 Tokenizer 架构，还能按描述「设计」音色 |
| 3 | [Fish Speech](https://github.com/fishaudio/fish-speech) | 33,829 | 自定义 ⚠️ | 2026-11 | 效果第一梯队；协议非标准开源，商用前读完 LICENSE |
| 4 | [IndexTTS](https://github.com/index-tts/index-tts) | 25,235 | 自定义 ⚠️ | 2026-09 | B 站出品，可控性强；同上，先看协议 |
| 5 | [CosyVoice](https://github.com/FunAudioLLM/CosyVoice) | 24,477 | Apache-2.0 | 2026-05 | 阿里系，多语言与方言好，适合团队集成而非个人折腾 |
| 6 | [F5-TTS](https://github.com/SWivid/F5-TTS) | 15,634 | MIT | 2026-11 | 架构干净、复现友好，研究圈口碑好 |
| 7 | [OpenVoice](https://github.com/myshell-ai/OpenVoice) | 38,303 | MIT | 2025-04 | 即时克隆代表作，跨语言音色迁移好；更新放缓，星标高但排位靠后就是因为这个 |
| 8 | [Spark-TTS](https://github.com/SparkAudio/Spark-TTS) | 10,982 | Apache-2.0 | 2025-04 | 国产新秀，建模简洁；更新放缓，观望 |

## 二、多人对话与长篇播客

2025 年后最卷的品类：直接生成多人对话音频，做播客、有声剧、访谈类内容看这里。

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [VibeVoice](https://github.com/microsoft/VibeVoice) | 57,490 | MIT | 2026-10 | 微软出品，专为长篇多说话人设计（播客场景），星标与完成度双高，本类标杆 |
| 2 | [Dia](https://github.com/nari-labs/dia) | 19,417 | Apache-2.0 | 2025-11 | 直接从对话脚本生成双人音频，非语言细节（笑声等）丰富 |
| 3 | [Higgs Audio](https://github.com/boson-ai/higgs-audio) | 8,391 | Apache-2.0 | 2026-06 | 表现力强、多语言，更新活跃 |
| 4 | [Orpheus-TTS](https://github.com/canopyai/Orpheus-TTS) | 6,415 | Apache-2.0 | 2025-12 | 基于 LLM 的情感语音路线，更新新，值得跟踪 |
| 5 | [Zonos](https://github.com/Zyphra/Zonos) | 7,250 | Apache-2.0 | 2025-03 | 声音克隆 + 情感控制；更新停在 2025-03，先观望 |

## 三、对话语音（短句日常对话）

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [ChatTTS](https://github.com/2noise/ChatTTS) | 40,037 | AGPL-3.0 ⚠️ | 2026-04 | 日常对话自然度标杆，笑声停顿都像真人；AGPL 传染性强，联网服务也要开源，商用慎重 |
| 2 | [Bark](https://github.com/suno-ai/bark) | 39,379 | MIT | 2024-08 | Suno 的多语言生成式音频先行者，能出音乐和音效；已一年多未更新，只适合把玩和原型 |

## 四、成品工具（不碰引擎，拿来就用）

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [Abogen](https://github.com/denizsafak/abogen) | 6,262 | MIT | 2026-11 | EPUB / PDF / TXT 拖进去出有声书 + 同步字幕；底层 Kokoro，英文最稳，中文先试一章 |
| 2 | [Kokoro](https://github.com/hexgrad/kokoro) | 10,301 | Apache-2.0 | 2025-08 | 82M 小模型，质量/体积比惊人，是上面 Abogen 等一批工具的底座 |
| 3 | [edge-tts](https://github.com/rany2/edge-tts) | 12,618 | 自定义 * | 2026-11 | 调微软 Edge 在线语音的 Python 库，出活最快；依赖在线服务，稳定性与条款自担 |

## 五、端侧与轻量部署

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | 16,098 | Apache-2.0 | 2026-11 | 离线语音全家桶（合成 + 识别），手机/嵌入式都能跑，做产品落地的硬通货 |
| 2 | [Piper](https://github.com/rhasspy/piper) | 11,336 | MIT | 2025-08 | 轻量本地 TTS，智能家居圈标配；⚠️ 仓库已归档，新项目建议从 sherpa-onnx 起步 |
| 3 | [MeloTTS](https://github.com/myshell-ai/MeloTTS) | 7,724 | MIT | 2024-12 | 中英混读当年很能打；近一年未更新，观望 |

## 六、基础框架与老牌项目

| 名次 | 项目 | 星标 | 协议 | 最近更新 | 点评 |
| --- | --- | --- | --- | --- | --- |
| 1 | [PaddleSpeech](https://github.com/PaddlePaddle/PaddleSpeech) | 12,713 | Apache-2.0 | 2026-08 | 百度飞桨系语音全栈工具箱，中文工业落地资料多 |
| 2 | [Coqui TTS](https://github.com/coqui-ai/TTS) | 46,268 | MPL-2.0 | 2024-08 | 曾经的标杆，XTTS 克隆影响深远；⚠️ 公司停运、仓库停更，新项目不要再基于它起步 |
| 3 | [VITS](https://github.com/jaywalnut310/vits) | 7,903 | MIT | 2023-12 | 一代经典架构，大量项目的源头；作为研究基座看，作为产品别直接用 |

## 三个避坑提醒

1. **协议先于效果**：自定义协议（Fish Speech、IndexTTS）和 AGPL（ChatTTS）是商用最常见的翻车点，下载模型之前先读 LICENSE。
2. **更新时间先于星标**：Bark、Coqui 星标都近 4 万+，但都已停更一年以上；OpenVoice 星标 3.8 万，更新也已放缓。排名里它们都被压后了，原因在此。
3. **引擎 ≠ 成品**：上面一、二、三类都是引擎，要显卡、要部署、要自己拼分章分角流程。只是想把一本书变成能听的成品，先看第四类或 [在线服务收录](online-tts.html)（如 [光年声场](https://aishengchang.com)：粘贴文本自动分角色配音色，浏览器里完成），验证完需求再决定要不要自建。

本页按季度复核。数据有误或项目状态变化，欢迎提 Issue 指正。
