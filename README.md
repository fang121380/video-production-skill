# Video Production Skill · 视频制作助手

从音乐、歌词、需求与可选参考视频出发，辅助 AI agent 规划、制作、审查和交付视频或 MV。工作流吸收了实际动画 MV 项目的经验，强调持续完成用户指定的范围、画面叙事、人物一致性和诚实报告验证情况。

## 能做什么

- 读取音频、歌词和可选参考视频，梳理故事、情绪、节奏和画风。
- 根据已安装能力选择 HyperFrames、Remotion 或其他合适的工具；现有视频剪辑服务与生成动画的工具能力不同，按任务选择。
- 优先查找用户配置的素材库，复用指定角色或在没有指定时设计角色；为镜头整理可复用的生成提示词。
- 编写分镜，准备素材、制作视频、合成音乐与字幕，并检查人物动作、转场和道具接触。
- 自审实际输出，记录未能听校的字幕和未能验证的动态效果，避免把截图或自动检查当作最终验收。

这是工作流程指引，不包含视频生成模型、音乐、角色素材或付费服务；实际制作能力取决于 agent 的工具、权限和运行环境。

## 开始使用

将仓库下载到本机后，把 `video-production` 整个文件夹复制到 agent 支持的 Skills 目录。请依据你使用的产品和环境调整路径。

- Codex 用户目录：`~/.codex/skills/video-production/`（如果设置了 `CODEX_HOME`，使用 `$CODEX_HOME/skills/`）。
- 其他支持 Agent Skills 格式的 agent：参照其官方文档安装到对应的 Skill 目录。
- 不支持自动发现但可以读文件的 agent：明确要求其读取 `video-production/SKILL.md` 及其中按需引用的文档。是否执行以及可访问哪些工具，取决于该 agent。

例如，下载仓库后在 Windows PowerShell 中安装到当前用户 Codex：

```powershell
# 在本仓库根目录执行；若目标已存在，先检查已有内容
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse .\video-production "$env:USERPROFILE\.codex\skills\video-production"
```

在新对话中使用：

> 使用 video-production Skill，根据附件音乐和歌词制作一支二维卡通 MV。可以参考附件视频的画风，使用我指定的角色素材，完成分镜、制作、自审和成片导出。

也可以不提供参考视频、人物或歌词，说明哪些部分希望 agent 根据素材设计或转写。复制 [视频需求模板](video-production/assets/video-brief.md) 可更容易整理需求。

长项目可以使用 [项目交接模板](video-production/assets/project-handoff.md) 记录分镜进度、实际检查结果和下一步，让其他 agent 根据文件继续。

## 目录

```text
video-production/
├── SKILL.md                        # 入口及全流程
├── assets/
│   ├── video-brief.md               # 用户需求模板
│   └── project-handoff.md           # 跨会话与跨 agent 项目交接
└── references/
    ├── tool-routing.md             # 按能力选择工具
    ├── prompts-and-assets.md       # 提示词与素材管理
    ├── production.md               # 制作与动画经验
    └── review.md                   # 自审和验证边界
```

## 隐私、版权与能力

项目不附带私人音乐、歌词、人物图或生成服务凭据。素材复用及发布应由使用者确认权利范围；上传外部服务和付费使用遵循用户授权。不同 agent 的 Skill 自动发现、视频播放、音频聆听与外部服务访问能力可能不同；未能完成的检查应明确报告。

## 许可

[MIT License](LICENSE)。
