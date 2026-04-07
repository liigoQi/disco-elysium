# Disco Elysium Plugin

极乐迪斯科风格的 Claude Code 技能系统。24个独特的思维技能，在你的对话中苏醒。

## 功能介绍

### 功能一：DE模式（极乐迪斯科模式）

使用 `/disco-elysium:de-toggle on` 开启极乐迪斯科模式，或者直接和你的agent说：“开启极乐迪斯科模式”。

开启后，24种技能会自动装备，在你和Claude Code的对话中根据语境自动触发——就像在游戏中一样。技能以"脑内声音"的形式突兀出现，时而迎合你，时而和你作对，带来沉浸式的游戏体验。你依然可以和平常一样与Claude Code对话。

样例：
```
用户：我现在特别想喝一杯

[食髓知味] [成功] - 你说对了，宝贝。酒精是你的老朋友，它从不背叛你。去吧，让那琥珀色的液体流过你的喉咙，世界会变得柔软、温暖、可以忍受。

[Claude Code] - 我注意到你有几个金融分析相关的技能和投资银行的技能配置。是要处理工作上的事务，还是纯粹想放松一下?
```

使用 `/disco-elysium:de-toggle off` 关闭模式，技能们沉沉睡去。

### 功能二：单独调用技能

你也可以单独调用任意一个技能，看看你的脑内声音会对你说什么。

| 中文名 | 短描述 | 指令 |
|--------|--------|------|
| 逻辑思维 | 运用纯粹智力，演绎整个世界 | `/disco-elysium:logic` |
| 博学多闻 | 调用知识储备，展示迷人轶事 | `/disco-elysium:encyclopedia` |
| 能说会道 | 践行游说之道，尽享严谨话术 | `/disco-elysium:rhetoric` |
| 故弄玄虚 | 看破人生如戏，献艺以诓攻谎 | `/disco-elysium:drama` |
| 标新立异 | 深入理解创意，纵览世间艺术 | `/disco-elysium:conceptualization` |
| 见微知著 | 重构犯罪现场，驾驭自然法则 | `/disco-elysium:visual-calculus` |
| 平心定气 | 自励奋发图强，保持斗志昂扬 | `/disco-elysium:volition` |
| 内陆帝国 | 放纵直觉预感，漫游清醒梦境 | `/disco-elysium:inland-empire` |
| 通情达理 | 理解他者心情，锻炼镜像神经 | `/disco-elysium:empathy` |
| 争强好胜 | 威吓全场民众，树立自身权威 | `/disco-elysium:authority` |
| 同舟共济 | 同事心心相印，全局众志成城 | `/disco-elysium:esprit-de-corps` |
| 循循善诱 | 魅惑芸芸众生，玩弄傀儡提线 | `/disco-elysium:suggestion` |
| 钢筋铁骨 | 承受沉重打击，直面世界敌意 | `/disco-elysium:endurance` |
| 坚忍不拔 | 无惧痛苦创伤，壮胆迎难而上 | `/disco-elysium:pain-threshold` |
| 强身健体 | 炫耀坚实肌肉，享受健美躯体 | `/disco-elysium:physical-instrument` |
| 食髓知味 | 纵情酒色享乐，沉溺毒品之海 | `/disco-elysium:electrochemistry` |
| 天人感应 | 竖起脖颈汗毛，倾听城市之音 | `/disco-elysium:shivers` |
| 疑神疑鬼 | 笃信本能反应，恐吓威胁他人 | `/disco-elysium:half-light` |
| 眼明手巧 | 手眼高度协调，枪法百发百中 | `/disco-elysium:hand-eye` |
| 五感发达 | 感知世间万物，注重一切细节 | `/disco-elysium:perception` |
| 反应速度 | 遇事当机立断，办事雷厉风行 | `/disco-elysium:reaction-speed` |
| 鬼祟玲珑 | 静则蛇行鳞潜，动则英气逼人 | `/disco-elysium:savoir-faire` |
| 能工巧匠 | 通万千机械，攻破重重封锁 | `/disco-elysium:interfacing` |
| 从容自若 | 挺直腰杆做人，从容应对风浪 | `/disco-elysium:composure` |

## 多平台支持

本插件已适配以下平台（由社区贡献）：

| 平台 | 目录 | 安装说明 |
|------|------|----------|
| Cursor | [cursor-skills/](cursor-skills/) | [README](cursor-skills/README.md) |
| OpenAI Codex | [codex-skills/](codex-skills/) | [README](codex-skills/README.md) |

## 安装

### Claude Code

#### 方式一：从 Marketplace 安装（推荐）

1. 添加市场：
   ```bash
   /plugin marketplace add https://github.com/liigoQi/disco-elysium.git
   ```

2. 安装插件：
   ```bash
   /plugin install disco-elysium@disco-elysium-marketplace
   ```

3. 重载插件：
   ```bash
   /reload-plugins
   ```

### 方式二：在 Plugin 项目目录中直接使用

```bash
cd disco-elysium
claude --plugin-dir .
```

---

*"复仇女神就在家中的镜子里；那便是她们的住址。哪怕这世间最澄清的水，只要够深，也能让人沉溺。"* — R.S.托马斯
