# Cursor Agent Skills 适配版

本目录是将原版 Claude Code 插件适配为 [Cursor](https://cursor.sh) Agent Skill 格式的版本，由 [@shoushouo](https://github.com/shoushouo) 贡献。

## 安装

将 `cursor-skills/` 下的各技能目录复制或软链接到 `~/.cursor/skills/`：

```bash
for d in cursor-skills/*/; do
  ln -s "$(pwd)/$d" ~/.cursor/skills/
done
```

或者直接使用独立仓库安装：

```bash
git clone https://github.com/shoushouo/disco-elysium-plugin-for-cursor.git ~/disco-elysium-plugin-for-cursor
for d in ~/disco-elysium-plugin-for-cursor/*/; do
  ln -s "$d" ~/.cursor/skills/
done
```

## 使用方式

安装完成后，在 Cursor 对话中直接说：

- "开启DE模式" — 开启极乐迪斯科模式，24个技能自动根据语境触发
- "关闭DE模式" — 关闭模式，恢复正常对话
- 也可以点名召唤某个技能，例如："用逻辑思维分析一下这段代码"

## 与原版的区别

- 原版使用 Claude Code 的 `/plugin` 命令和 slash command 机制
- 本版本使用 Cursor Agent Skill（`SKILL.md`）格式，通过自然语言触发
- 技能内容与角色设定完全保留，仅调整了触发机制
