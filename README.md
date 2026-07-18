# 薅羊毛助手 · WorkBuddy Skill

全网薅羊毛统一入口。电商优惠券搜索(淘宝/京东/拼多多/抖音/快手/1688/苏宁/唯品会全平台比价)+羊毛福利查询+美团本地生活。底层通过 Coze Bot API 聚合多平台数据。

## 特性

- 请参考 SKILL.md 中的详细说明

## 安装

### WorkBuddy 技能市场（推荐）

在 WorkBuddy 中搜索「薅羊毛助手」一键安装。

### 手动安装

```bash
# 安装到 WorkBuddy
git clone https://github.com/guipi888/wool-hunter.git \
  ~/.workbuddy/skills/wool-hunter

# 或安装到 Claude Code / OpenClaw
git clone https://github.com/guipi888/wool-hunter.git \
  ~/.claude/skills/wool-hunter
```

### 环境依赖

- Python ≥ 3.11
- `uv`（跨平台 Python 包管理器）：`curl -LsSf https://astral.sh/uv/install.sh | sh` 或 `pip install uv`
- 配置文件 `~/.coupon_search_config.json`（含 `coze_api_url` 和 `coze_api_token`）

## 使用

```bash
# 搜索商品优惠券
cd wool-hunter && uv run scripts/search.py search --keyword "机械键盘"

# 限定平台搜索
uv run scripts/search.py search --keyword "机械键盘" --platform "京东"

# 羊毛福利查询
python3 scripts/call_bot.py "最近有什么外卖红包"
```

详细用法请参考 [SKILL.md](./SKILL.md)

## 输出

请参考 SKILL.md

## 项目结构

```
.gitignore
LICENSE
SKILL.md
scripts
scripts/call_bot.py
scripts/search.py
```

## 关于作者

**桂皮 Guipi** — AI Agent 开发者 · 超级个体践行者
专注 AI 效率工具与一人公司方法论，帮普通人用 AI 成为超级个体

| 平台 | 账号 |
|------|------|
| 📱 小红书 | [桂皮AI实战](https://www.xiaohongshu.com/user/profile/5a409dda44363b313b9d7e15) |
| 🎬 抖音 | [桂皮AI实战](https://v.douyin.com/QJRjHGAtrvA/) |
| 📺 视频号 | 微信内搜「桂皮AI实战」 |
| 💬 公众号 | 微信搜「桂皮AI实战」 |
| 🌟 知识星球 | [AI超级个体](https://t.zsxq.com/guSUk) — AI工具 · 创作 · 产品 · 流量 · 变现 |
| 🐙 GitHub | [guipi888](https://github.com/guipi888) |
| 💬 微信 | guipi996（注明来意） |

## License

MIT License — 详见 [LICENSE](./LICENSE)
