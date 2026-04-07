# Disco Elysium Skills for Codex

极乐迪斯科风格的 Codex skill 集合。24 个独特的思维技能，在需要时作为“脑内声音”被点名唤醒。

> 复仇女神就在家中的镜子里；那便是她们的住址。
> 哪怕这世间最澄清的水，只要够深，也能让人沉溺。

---

## 适配说明

### DE 模式

Codex 没有 Cursor/Claude 插件式的全局开关状态，所以这里的 DE 模式被设计成一种当前会话中的角色扮演约定：

- 你可以明确说“开启 DE 模式”或“关闭 DE 模式”
- 开启后，AI 应优先把极乐迪斯科的技能理解成一种可选的内心独白层
- 为了避免误触发，单个技能更推荐点名调用，而不是期待它们自动介入所有对话

示例：
```
用户：我今天想喝一杯酒

[食髓知味] [成功] - 对。就是它。琥珀色的液体，你的老朋友。今天它不会背叛你的。

[Codex] - 想喝什么？红酒、威士忌还是啤酒？
```

开启 DE 模式：告诉 AI "开启DE模式" 或 "开启极乐迪斯科模式"

关闭 DE 模式：告诉 AI "关闭DE模式"

### 单独调用技能

也可以直接点名某个技能，让它对你说话。例如：

- "用 de-logic 分析一下这段代码"
- "食髓知味，我今天很累"
- "内陆帝国，这个函数名起得怎么样"

为了减少 Codex 中的误匹配，这个分支给技能目录统一加了 `de-` 前缀，比如：

- `de-logic`
- `de-empathy`
- `de-shivers`
- `de-skillbook`
- `de-toggle`

---

## 安装

### 方式一：clone 后软链接到 `~/.codex/skills/`（推荐，可随时同步更新）

```bash
git clone -b codex https://github.com/shoushouo/disco-elysium-plugin-for-cursor.git ~/disco-elysium-plugin-for-codex

for d in ~/disco-elysium-plugin-for-codex/*/; do
  ln -s "$d" ~/.codex/skills/
done
```

以后更新：

```bash
cd ~/disco-elysium-plugin-for-codex && git pull
```

### 方式二：直接复制

```bash
git clone -b codex https://github.com/shoushouo/disco-elysium-plugin-for-cursor.git
cp -r disco-elysium-plugin-for-cursor/*/ ~/.codex/skills/
```

---

## 24个技能

### 智力系

| 技能 | 描述 |
|------|------|
| 逻辑思维 (`de-logic`) | 运用纯粹智力，演绎整个世界 |
| 博学多闻 (`de-encyclopedia`) | 调用知识储备，展示迷人轶事 |
| 能说会道 (`de-rhetoric`) | 践行游说之道，尽享严谨话术 |
| 故弄玄虚 (`de-drama`) | 看破人生如戏，献艺以诓攻谎 |
| 标新立异 (`de-conceptualization`) | 深入理解创意，纵览世间艺术 |
| 见微知著 (`de-visual-calculus`) | 重构犯罪现场，驾驭自然法则 |

### 精神系

| 技能 | 描述 |
|------|------|
| 平心定气 (`de-volition`) | 自励奋发图强，保持斗志昂扬 |
| 内陆帝国 (`de-inland-empire`) | 放纵直觉预感，漫游清醒梦境 |
| 通情达理 (`de-empathy`) | 理解他者心情，锻炼镜像神经 |
| 争强好胜 (`de-authority`) | 威吓全场民众，树立自身权威 |
| 同舟共济 (`de-esprit-de-corps`) | 同事心心相印，全局众志成城 |
| 循循善诱 (`de-suggestion`) | 魅惑芸芸众生，玩弄傀儡提线 |

### 体质系

| 技能 | 描述 |
|------|------|
| 钢筋铁骨 (`de-endurance`) | 承受沉重打击，直面世界敌意 |
| 坚忍不拔 (`de-pain-threshold`) | 无惧痛苦创伤，壮胆迎难而上 |
| 强身健体 (`de-physical-instrument`) | 炫耀坚实肌肉，享受健美躯体 |
| 食髓知味 (`de-electrochemistry`) | 纵情酒色享乐，沉溺毒品之海 |
| 天人感应 (`de-shivers`) | 竖起脖颈汗毛，倾听城市之音 |
| 疑神疑鬼 (`de-half-light`) | 笃信本能反应，恐吓威胁他人 |

### 运动系

| 技能 | 描述 |
|------|------|
| 眼明手巧 (`de-hand-eye`) | 手眼高度协调，枪法百发百中 |
| 五感发达 (`de-perception`) | 感知世间万物，注重一切细节 |
| 反应速度 (`de-reaction-speed`) | 遇事当机立断，办事雷厉风行 |
| 鬼祟玲珑 (`de-savoir-faire`) | 静则蛇行鳞潜，动则英气逼人 |
| 能工巧匠 (`de-interfacing`) | 精通万千机械，攻破重重封锁 |
| 从容自若 (`de-composure`) | 挺直腰杆做人，从容应对风浪 |

---

## 说明

本项目改编自 [liigoQi/disco-elysium](https://github.com/liigoQi/disco-elysium)。

- `main` 分支保留 Cursor 版
- `codex` 分支为 Codex 适配版

Codex 适配的重点是：

- 所有技能目录统一加 `de-` 前缀，降低误触发
- `de-toggle` 改为会话约定，而不是插件状态开关
- 安装目标目录改为 `~/.codex/skills/`
