<div align="center">

# 旅行冰箱贴 · Photo2Magnet

### 把照片，变成想贴在冰箱上的回忆。

将旅行照片、喜欢的建筑，或与宠物相处的瞬间，转成有立体浮雕质感的冰箱贴效果图。

[English](README.md) · **简体中文**

[![License: MIT](https://img.shields.io/badge/License-MIT-315C48.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-546C7A.svg)](SKILL.md)
[![Tested in Codex](https://img.shields.io/badge/Tested_in-Codex-263238.svg)](#运行要求)

</div>

| 你的照片 | 你的冰箱贴 |
| :---: | :---: |
| <img src="docs/images/dogs-before.jpg" alt="草地上白色狗狗与镂空尖塔的原照片" width="420"> | <img src="docs/images/dogs-after.jpg" alt="保留尖塔梁架、白色狗狗与牵引绳的树脂浮雕冰箱贴效果图" width="420"> |

镂空的梁架、草地上的狗狗、伸向一侧的牵引绳——照片里值得记住的细节，都可以成为设计的一部分。旅行冰箱贴引导具备图像能力的 Agent，把这些记忆转成有轮廓、层次与材质的纪念品。

**[查看全部 7 组原图与成品对照 →](docs/gallery.md)**

## 安装到 Codex

使用 [Skills CLI](https://github.com/vercel-labs/skills)：

```bash
npx skills add carpediem67/photo2magnet --skill photo2magnet --agent codex --global
```

也可以直接克隆到用户级 Skills 目录：

```bash
git clone https://github.com/carpediem67/photo2magnet.git ~/.agents/skills/photo2magnet
```

两种方式选一种即可。目录已存在时，先保留自己的修改，再更新现有安装。安装后若没有出现，开启新任务或重启 Codex 刷新。

## 做第一枚冰箱贴

附上照片，然后说：

```text
用 $photo2magnet 把这张照片做成一枚有立体浮雕质感的冰箱贴。
```

默认交付一张方形产品图：彩绘树脂浮雕、干净背景、无文字。你的要求始终优先于默认值。

还可以这样用：

```text
用 $photo2magnet 把这张海港照片做成冰箱贴。
保留薄雾和天际线，采用深蓝珐琅质感，
小铭牌写“海港时光”。
```

```text
用 $photo2magnet 把这组照片逐张做成冰箱贴。
保持统一的材质与光线，保留宠物，不要文字。
```

```text
用 $photo2magnet 修改刚才那枚冰箱贴。
只把背景改成浅鼠尾草绿，保留景物与外轮廓。
```

## 设计关注什么

- **原片的记忆点。** 保留天际线、屋顶、海岸、宠物，以及让照片属于你的具体细节。
- **有依据的浮雕层次。** 将纵深压缩到连续背板上，用高低、遮挡和薄侧边表现立体感。
- **适合主体的外轮廓。** 顺着山脊、穹顶、树冠或海岸组织形状，不给所有照片套同一只框。
- **可辨认的材质。** 让石头、建筑、植被和水面有不同触感。
- **可调整的风格。** 材质、背景、轮廓、文字、画幅和数量均可按你的要求变化。

## 同一个 Skill，更多记忆

| 海港天际线 | 暮色车站 | 海岸石柱 |
| :---: | :---: | :---: |
| <img src="docs/images/skyline-after.jpg" alt="海港天际线树脂浮雕冰箱贴" width="270"> | <img src="docs/images/station-after.jpg" alt="金色夕照与绿色穹顶的车站浮雕冰箱贴" width="270"> | <img src="docs/images/coast-after.jpg" alt="海岸悬崖、石柱与浪花浮雕冰箱贴" width="270"> |

这些示例均来自真实输入照片，已实际生成并查看。它们展示工作流能达到的效果，不保证每次生成结果完全一致。

## 运行要求

**已在 Codex 内置图像生成工具中实测。** 本仓库提供 Skill 指令与示例，不包含图像模型，也不是独立应用。宿主提供内置图像能力时，不需要另外配置 API Key；图像权限和额度取决于宿主。

其他宿主需要支持 Agent Skills、参考图和图像生成/编辑，目前尚未实测。仅安装文本文件不会增加原本不存在的出图能力。

Skill 不绑定模型版本，也不会通过提示词强行切换图像模型。

## 常见问题

**能直接 3D 打印吗？**

当前交付有立体浮雕观感的二维产品效果图。STL/3MF、磁铁槽、尺寸与可打印性，需要另行建模验证。

**能完全还原原照片吗？**

它保留可辨认的主体关系，但属于艺术化转绘。微小人脸、游客数量、招牌、几何细节和色彩可能变化；重要细节需要看图核对。

**只给主题，不给照片可以吗？**

可以。给出明确的场景或主体即可；没有原片时生成的是原创概念，不会声称还原某张照片。

**照片格式不兼容怎么办？**

Skill 会保留原文件，制作并实际查看兼容副本后再尝试。七张照片实测中，已处理一张 HEIC 和两张被接口拒收的 JPEG。

**支持英文吗？**

说明文档与使用示例提供中英文。核心 Skill 以中文编写，可以用中英文提出需求；目前未在独立任务中完成英文调用的端到端验证。

## 参与改进

欢迎提交难例、指令改进和可复核的图片对照。建议附上可分享的原图、请求、结果，以及希望改善的具体问题。只把确有帮助的规则留在核心创作流程中。

## 许可证

[MIT](LICENSE) · Copyright © 2026 Qing1。

本许可证不授予你额外使用第三方照片或其他输入素材的权利。本项目为独立社区 Skill，并非 OpenAI 官方产品。
