# 日记封面 Skill

把一个月的日记，整理成一个书名和几张可供挑选的封面。

Agent 会读取你指定范围的日记，建议书名，再寻找有来源的艺术作品或摄影图片，制作封面对比。支持朝花夕拾 / Obsidian，也可以只选图、做预览。

## 安装

### 把链接交给 Agent

复制下面这句话，发给你使用的 Codex、Claude Code 等支持 Skill 安装的 Agent：

> 帮我安装这个 Skill：https://github.com/Tangerine-Cat888/tangerine-cat-diary-cover

Agent 需要有联网和本地文件操作能力，并能按当前工具的技能目录完成安装。安装后开启新会话使用。

### 或者，一条命令安装

已安装 Node.js 22.20 或更新版本，可以在终端运行：

```bash
npx skills add Tangerine-Cat888/tangerine-cat-diary-cover -g
```

按提示选择你使用的 Agent。`-g` 表示安装到用户级目录，各项目均可使用；只想在当前项目使用，去掉 `-g`。

只安装到 Codex：

```bash
npx skills add Tangerine-Cat888/tangerine-cat-diary-cover -g -a codex
```

安装由开源工具 [Skills CLI](https://github.com/vercel-labs/skills) 完成，不需要手动下载 ZIP、改文件夹名称。

## 怎么用

在新会话里告诉 Agent 日记位置和月份：

> 用日记封面 Skill，读取我指定目录里 2026 年 8 月的日记，先建议几个书名。这次只做预览，不修改日记本。

选好书名后，继续说：

> 就用这个书名，找几张适合的艺术作品或摄影图片，做成封面对比给我看看。

你会得到：

- **书名候选**：结合日记主题，说明各个标题的侧重。
- **配图候选**：提供作品、作者、来源和许可信息；涉及获奖摄影时核对奖项。
- **封面对比**：比较标题与图片的搭配、裁切和缩小后的可读性，指出不足。

确定喜欢的方案后，再让 Agent 应用到日记本。明确只预览时不会应用；应用需要软件访问能力和你的授权。

Codex 也可以通过 `$tangerine-cat-diary-cover` 调用。

## 使用前需要什么

- 支持 Skill 的 Agent，以及文件读取、网页检索和图片处理能力。
- 日记所在目录和需要处理的月份。
- 要在朝花夕拾中预览或应用时，还需要访问 Obsidian。

这是一套供 Agent 执行的工作流程，不是 Obsidian 插件安装包。

## 隐私与图片来源

本仓库不包含日记、个人配置、账号凭据或画作图片。外部检索使用通用主题词和公开作品信息，不发送日记原文。Agent 服务如何处理提供的日记，取决于你使用的服务和设置。

图片使用权按单件作品核验；获奖不代表可以自由使用。仓库的 MIT 许可证只覆盖 Skill 文本及配置，不包含第三方图片的使用权。

## 仓库内容

- [SKILL.md](SKILL.md)：完整工作流程。
- [图片来源](references/sources.md)：来源选择与核验。
- [Obsidian 适配](references/obsidian.md)：朝花夕拾预览与应用。
- [Codex 配置](agents/openai.yaml)：界面元数据。

欢迎通过 [Issues](https://github.com/Tangerine-Cat888/tangerine-cat-diary-cover/issues) 反馈，或提交 Pull Request。提交示例前，请移除私人日记、个人路径和账号信息。

## 许可证

[MIT](LICENSE)
