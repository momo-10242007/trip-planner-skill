# trip-planner-skill ✈️

一个 [CodeBuddy Code](https://www.codebuddy.cn) 技能插件：**AI 旅行行程规划器**。

当你说「做旅行攻略 / 规划行程 / 去XX玩」时，AI 助手会自动收集你的出行信息（目的地、天数、预算、同行人、偏好），联网核实景点开放情况和门票价格，然后生成一份**分天分时段、可直接执行**的行程表。

## ✨ 功能

- **信息收集**：自动追问缺失的关键信息（目的地/天数/预算），一次问完不啰嗦
- **事实查证**：景点开放时间、门票价格、交通耗时联网核实，查不到的明确标注「出行前请自行确认」，绝不编造
- **顺路排程**：同一天景点地理上顺路，单日通勤不超过 1.5 小时，每天留 2 小时自由时间
- **预算分解**：住宿/交通/门票/餐饮/其他五类拆解，确保不超预算
- **真实避坑提示**：预约要求、闭馆日、打车建议等具体提示，拒绝「注意安全」式空话

## 📦 安装

### 方式一：手动复制（推荐新手）

1. 下载本仓库（Code → Download ZIP，或 `git clone`）
2. 把 `skills/trip-planner` 整个文件夹复制到：
   ```
   ~/.codebuddy/skills/trip-planner
   ```
3. 重启 CodeBuddy Code，然后说「帮我做一份成都 3 天的攻略」即可使用

### 方式二：git clone

```bash
git clone https://github.com/momo-10242007/trip-planner-skill.git
cp -r trip-planner-skill/skills/trip-planner ~/.codebuddy/skills/
```

## 🚀 使用示例

> 你：帮我做一份成都 3 天的攻略，预算 3000，两个人，爱吃辣。

AI 助手会输出（节选）：

```markdown
# 成都 3 日游行程表（2 人 · 预算 3000 元）

## D1（周五）| 市中心经典线
- 09:00 人民公园 → 鹤鸣茶社喝茶（人均 30 元）
- 11:30 午餐：小名堂担担甜水面（人均 40 元）；备选：洞子口张老二凉粉
- 14:00 武侯祠（门票 50 元/人，公众号预约）→ 锦里步行街
- 18:00 晚餐：马路边边麻辣烫（人均 70 元）
- 交通提示：全天景点集中在地铁 3 号线沿线

## 预算分解（2 人 3 天）
| 项目 | 金额 |
|---|---|
| 住宿 | ¥1200 |
| 门票 | ¥400 |
| ... | ... |
```

## 📁 目录结构

```
trip-planner-skill/
├── README.md                            # 本文件
├── LICENSE                              # MIT 开源协议
└── skills/
    └── trip-planner/                    # 技能本体
        ├── SKILL.md                     # 技能定义（核心）
        └── assets/
            └── itinerary-template.md    # 行程表模板
```

## 🛠️ 自定义

- 想改行程表格式？编辑 `skills/trip-planner/assets/itinerary-template.md`
- 想改排程规则（如节奏更紧凑）？编辑 `skills/trip-planner/SKILL.md` 的「第 3 步」

## 📄 License

[MIT](./LICENSE)
