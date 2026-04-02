# 週報自動滾動生成 Skill

Claude Code 的週報助手 Skill。貼上上週週報，自動滾動生成本週版本，你只需回報差異。

> **[線上安裝與使用指南](https://badbadted.github.io/weekly-report-skill/guide.html)**

## 功能

- 自動從上週週報滾動生成本週初始版本
- 差異更新模式 — 只說變動的部分，其餘自動沿用
- 工時自動加總與驗算
- 待辦項目自動進出管理
- 異常偵測（工時過高/過低、完成度異常等）
- 民國年日期格式

## 安裝

1. 在你的專案目錄下建立 Skill 資料夾：

```bash
mkdir -p .claude/skills/weekly-report
```

2. 把 `SKILL.md` 複製進去：

```bash
cp SKILL.md .claude/skills/weekly-report/SKILL.md
```

或者直接 clone 本 repo 後複製：

```bash
git clone https://github.com/<your-org>/weekly-report-skill.git
cp weekly-report-skill/SKILL.md <你的專案>/.claude/skills/weekly-report/SKILL.md
```

3. 在 Claude Code 中輸入 `/weekly-report` 即可啟用。

## 使用方式

1. 啟動後貼上上週週報
2. AI 自動滾動生成本週初始版本
3. 一次告知所有變動（例如「C1 第 1 項完成度改 80%，工時 6hr」）
4. 產出完整週報，複製貼上即可

### 指令

| 指令 | 說明 |
|------|------|
| `/新週報` | 開始新一週的週報 |
| `/修改` | 局部修改已產出的週報 |
| `/驗算` | 重新加總驗算所有工時 |
| `/格式` | 顯示格式參照範例 |
| `/指令` | 列出所有可用指令 |

## 自訂格式

如果你的週報格式與預設不同，修改 `SKILL.md` 中的 `[格式參照範例]` 區段，替換成你自己的格式即可。

## 需求

- [Claude Code](https://claude.ai/code) CLI 或桌面版
