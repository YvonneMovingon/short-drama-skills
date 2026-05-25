# 🎬 Short Drama Skills — LuxReal

**经工业化生产验证的 AI 短剧 Skill 合集**  
AI Short Drama Skills, battle-tested in real production pipelines.

[![Stars](https://img.shields.io/github/stars/YOUR_USERNAME/short-drama-skills?style=flat-square)](https://github.com/YOUR_USERNAME/short-drama-skills)
[![Skills](https://img.shields.io/badge/Skills-10-blue?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](./LICENSE)

---

<!-- 放一段 GIF：左边输入提示词 / 右边生成的短剧分镜画面，建议时长 4-6 秒，循环播放 -->
<!-- ![Demo](./assets/hero-demo.gif) -->

> 这里的每一条 Skill，都在真实短剧生产流水线中被数以万计的用户跑过验证。  
> 直接复制使用，或在 LuxReal 中直接开始生产。

---

## Skill 列表

### 📽️ 镜头提示词

| # | Skill | 用途 | 适合场景 |
|---|-------|------|---------|
| 01 | [通用叙事拆解](#01-通用叙事拆解) | 将叙事内容转化为可执行的连续镜头序列 | 日常剧情、场景切换、对话段落 |
| 02 | [深度情绪刻画](#02-深度情绪刻画) | 用镜头语言放大人物情绪张力 | 冲突戏、高情绪密度段落、告白 |
| 03 | [详细动态描述](#03-详细动态描述) | 精确控制画面内的动作与运动细节 | 动作戏、追逐、肢体表演 |
| 04 | *(即将上线)* | — | — |
| 05 | *(即将上线)* | — | — |

### 📝 剧本工作流

| # | Skill | 用途 | 适合场景 |
|---|-------|------|---------|
| 06 | [按剧情连贯拆分副本](#06-按剧情连贯拆分副本) | 保持叙事连贯性地拆分剧本段落 | 长剧本分集、多集制作 |
| 07 | [单视频提示词润色](#07-单视频提示词润色) | 优化单条视频的生成提示词质量 | 提升单条出片效果、精细化调整 |
| 08 | *(即将上线)* | — | — |
| 09 | *(即将上线)* | — | — |
| 10 | *(即将上线)* | — | — |

---

## 快速上手

**方式一：直接复制**  
点击任意 Skill → 打开 `prompt.md` → 复制 → 粘贴到你使用的 AI 工具中。

**方式二：一键导入 LuxReal**  
点击每条 Skill 末尾的「在 LuxReal 中使用 →」，注册后自动加载，直接开始生产。

---

## Skill 详情

### 01 · 通用叙事拆解

**含生成逻辑 + 预期镜头格式**

将剧本叙事内容自动拆解为可执行的镜头序列，适用于大多数剧情场景的连续镜头生成。

**适合场景：** 日常剧情推进 / 对话段落 / 场景切换

<!-- 放一张对比图：左边输入的剧本文字，右边生成的镜头序列截图 -->

**[查看完整 Skill →](./skills/01-通用叙事拆解/prompt.md)**　　**[在 LuxReal 中使用 →](https://luxreal.com?skill=01)**

---

### 02 · 深度情绪刻画

**含生成逻辑 + 预期镜头格式**

通过镜头语言强化人物情绪表达，让 AI 生成的画面具备情绪张力，而不是表情平淡的动作复现。

**适合场景：** 告白 / 争吵 / 分离 / 高潮冲突段落

<!-- 放一张对比图：普通提示词 vs 深度情绪刻画 Skill 的生成效果对比 -->

**[查看完整 Skill →](./skills/02-深度情绪刻画/prompt.md)**　　**[在 LuxReal 中使用 →](https://luxreal.com?skill=02)**

---

### 03 · 详细动态描述

**含生成逻辑 + 预期镜头格式**

精确描述画面内的动作细节与运动轨迹，解决 AI 视频中动作模糊、肢体失真的问题。

**适合场景：** 动作戏 / 追逐场景 / 武打 / 肢体表演

<!-- 放一张对比图：有无此 Skill 的动作场景生成效果对比 -->

**[查看完整 Skill →](./skills/03-详细动态描述/prompt.md)**　　**[在 LuxReal 中使用 →](https://luxreal.com?skill=03)**

---

### 06 · 按剧情连贯拆分副本

保持叙事连贯性地将长剧本拆分为多个段落，确保分集后故事逻辑不断裂、情绪节奏不丢失。

**适合场景：** 长剧本分集制作 / 多集连续短剧

<!-- 放一张截图：拆分前后的对比，展示连贯性保留效果 -->

**[查看完整 Skill →](./skills/06-按剧情连贯拆分副本/prompt.md)**　　**[在 LuxReal 中使用 →](https://luxreal.com?skill=06)**

---

### 07 · 单视频提示词润色

对已有的视频生成提示词进行质量优化，提升单条出片的画面表现力和生成稳定性。

**适合场景：** 精细化调整单条视频 / 提升出片质量

<!-- 放一张对比图：润色前后的提示词，以及对应的生成效果变化 -->

**[查看完整 Skill →](./skills/07-单视频提示词润色/prompt.md)**　　**[在 LuxReal 中使用 →](https://luxreal.com?skill=07)**

---

## 目录结构

```
short-drama-skills/
├── README.md
├── README_EN.md
├── skills/
│   ├── 01-通用叙事拆解/
│   │   ├── prompt.md        # 完整提示词 + 使用说明
│   │   └── example/         # 输入示例 & 输出截图
│   ├── 02-深度情绪刻画/
│   ├── 03-详细动态描述/
│   ├── 06-按剧情连贯拆分副本/
│   ├── 07-单视频提示词润色/
│   └── ...
├── assets/
│   └── hero-demo.gif
└── CONTRIBUTING.md
```

---

## 贡献

欢迎提交在真实短剧生产中验证过的 Skill。

1. Fork 本仓库
2. 在 `skills/` 下新建文件夹，参考现有格式
3. 提交 Pull Request，注明使用场景和效果

---

## 关于 LuxReal

这些 Skill 来自 [LuxReal](https://luxreal.com) 的内部生产流水线。  
LuxReal 是专为短剧工作室和创作者设计的 AI 工业化制作平台。

[🚀 免费体验 LuxReal，注册即得 200 积分 →](https://luxreal.com)
