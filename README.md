# 陈士铎 · 四书思维技能

> ⚠️ **仅供中医文献与学术方法研究，不构成诊疗建议，不提供处方与剂量。**

[![Version](https://img.shields.io/badge/版本-V0.1.1-blue)](CHANGELOG.md)
[![Corpus](https://img.shields.io/badge/语料-四书%2066万字-orange)]()
[![Coverage](https://img.shields.io/badge/15维度-11%2F15-yellow)]()

把清初医家**陈士铎（陈远公）**的《石室秘录》《辨证录》《本草新编》《外经微言》，蒸馏成可被 AI 调用的人物技能。

## 三条必须先知道的

1. **托名仙授**：全书以「岐天师曰」立论，序署岐伯、张仲景、吕洞宾。这是著述体例，不是史实。
2. **病案是虚构的**：《辨证录》「人有……人以为……谁知……」是为辨证设的教学范型，非真实病历。
3. **与《傅青主女科》重合**：学界公案，同源说／传授说／互掺说并存，本技能不判定。

## 语料来源

| 书 | 来源 |
|---|---|
| 石室秘录 | cmedalib `oldTCMBooksA/022.htm` |
| 辨证录 | cmedalib `oldTCMBooks/744.htm` |
| 本草新编 | cmedalib `oldTCMBooks/733.htm` |
| 外经微言 | cmedalib `oldTCMBooksA/068.htm` |

四书均为公版古籍；电子文本来自上述站点（该站标注"只作自学研究"）。本仓库保存目的是文本校勘与引文校验，如权利人异议即移除 `modules/`。

## 安装

```bash
git clone https://github.com/idavailable/chenshiduo.git ~/.workbuddy/skills/chenshiduo
# 或
cp -r chenshiduo ~/.workbuddy/skills/chenshiduo
```

装完自检：

```bash
cd ~/.workbuddy/skills/chenshiduo
python3 scripts/health_check.py
python3 scripts/check_quotes.py
```

## 目录

```
chenshiduo/
├── SKILL.md                     # 主文件
├── modules/                     # 四书语料 + 索引
├── cases/                       # 6 则范型病案（四段链）
├── references/                  # 心智模型 / 启发式 / 表达DNA / 反模式 / FAQ
└── scripts/                     # 8 个校验脚本（仅标准库）
```

## 覆盖率 11/15

缺：7 饮食、8 条辨、9 生平（生卒无确考）、12 谱系（傅青主公案未定）；15 功法不适用。

## 校验

```bash
python3 scripts/health_check.py
python3 scripts/check_quotes.py
python3 scripts/validate_keyword_refs.py --skill SKILL.md
```

## 许可

代码与方法 MIT；`modules/` 古籍原文属公有领域，不适用 MIT。
