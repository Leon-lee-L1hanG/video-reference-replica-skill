# video-reference-replica

用于 Codex 的中文技能：根据参考视频制作产品创意宣传片，复刻构图、连续运镜、创意转场、空间文字和声画节奏，再替换为自己的产品。

## 包含什么

- `skills/video-reference-replica/SKILL.md`：技能入口与任务路由。
- `references/workflow.md`：参考拆解、产品转译、试片与全片流程。
- `references/quality-checks.md`：文字、穿模、风格、声音与导出验收。
- `references/hypit.md`：可选的 Hypit 工程对接要点。
- `assets/project-workbook.md`：可复制的需求卡、镜头卡与验收记录。
- `agents/openai.yaml`：Codex 展示与调用信息。

后五项均位于 `skills/video-reference-replica/` 内。

## 安装

把完整的 `skills/video-reference-replica` 文件夹复制到 Codex 用户技能目录：

- 设置了 `CODEX_HOME`：`$CODEX_HOME/skills/video-reference-replica/`
- 未设置：`~/.codex/skills/video-reference-replica/`
- Windows 默认示例：`%USERPROFILE%\.codex\skills\video-reference-replica\`

确认 `SKILL.md` 位于该文件夹第一层。若当前会话未发现新技能，重新打开会话后调用。

## 使用

```text
使用 $video-reference-replica。
风格参考：我的参考视频。
产品参考：产品外形及结构资料。
目标：给客户看的产品宣传片，保留参考的连续转场与展示节奏。
品牌、卖点、画幅、音乐方向和预算：按我的补充资料执行。
```

支持新片制作，也支持基于指定版本移动镜头、修复标题或重配 BGM。技能会把风格参考与产品参考分开处理，不把普通装箱演示当成创意复刻。

## 依赖与边界

这是制作工作流技能，不是自动视频生成服务。实际制作需要可查看参考媒体的能力，以及环境可用的三维／视频渲染与音频工具。可配合已配置的 Hypit，也可使用其他合适引擎；Hypit 不是强制依赖。

本仓库不包含参考视频、商标、字体、音乐、API 密钥或付费模型，也不自动购买服务。没有实际试听能力时必须记录未验证状态。

## 上传 GitHub

将本目录内的 `README.md`、`.gitignore` 和整个 `skills/` 文件夹上传至你的仓库根目录，保持目录结构；不要只上传 `SKILL.md`。也可以把 `skills/video-reference-replica/` 放入已有的技能集合仓库。

## 检查

如环境含 Codex 的 skill-creator，可执行其 `scripts/quick_validate.py` 并传入 `skills/video-reference-replica`。该检查验证技能结构，不代表已经通过真实视频制作或听感验收。
