# 諸界之衡 / The Scales of Many Realms

> 致敬《逆轉裁判》的奇幻法庭推理視覺小說——設計文件庫。
> A fantasy courtroom visual-novel design bible, in the spirit of *Ace Attorney*.

---

## 中文

### 概述

《諸界之衡》是一款設定在架空奇幻世界「衡律帝國」的視覺小說推理遊戲，共規劃 **14 案、三部曲**。玩家扮演新銳辯護律師**言衡**，憑藉異能「緣命絲」（能看見人與人之間的隱形羈絆）在法庭上調查、質詢證人、揭穿矛盾。

世界觀融合四大元素：多種族社會（七大種族）、有照魔法（術籙制）、靈媒招魂（靈律）、神諭信仰（神諭體系）。故事基調為奇幻史詩，14 案之間由一條貫穿三部曲的主線陰謀串連（神諭的真實來源，在第三部揭示）。

本倉庫只包含**設計文件**（Markdown），不含遊戲程式碼。圖像計畫由 ChatGPT / Gemini / Midjourney 依文件內的 prompt 生成。

### 專案結構

```
.
├── 諸界之衡_故事結構.md          # 總企劃：世界觀地基、核心角色、三部曲主線、14 案場景級設計、開發切片與驗證方法
├── 設定資料/
│   ├── 01_衡律帝國與七大種族.md   # 帝國政治結構與七大種族設定
│   ├── 02_術籙制_魔法系統.md      # 白／灰／黑籙魔法分類、執照制度、犯罪用途與庭審推理
│   ├── 03_靈律_招魂體系.md        # 招魂規則、限制與案件應用
│   ├── 04_神諭體系.md             # 神諭官、神諭院與神諭來源的真相
│   ├── 05_法庭程序與律廷.md       # 律廷組織、庭審流程、玩家可用動作
│   └── AI生圖_Prompt包.md         # 美術風格指南、角色立繪／場景／證物／UI 的 AI 生圖 prompt
├── 角色立繪參考/
│   └── 角色卡_完整集.md           # 11 名核心角色完整卡片（外型、個性、背景、能力、角色弧、對白風格）
├── 第一部_衡律初聲/
│   ├── 案_1-1_初登法庭_完整腳本.md    # 教學案
│   ├── 案_1-2_歌劇院的影子_完整腳本.md # 靈墟登場、招魂機制教學
│   └── 案_1-3_龍裔的證詞_完整腳本.md   # 霜訣明登場、種族議題、神諭院內鬼伏筆
├── 第二部_裂衡之兆/               # 尚未撰寫（僅佔位）
├── 第三部_諸界終律/               # 尚未撰寫（僅佔位）
└── 場景圖參考/                    # 尚未放入圖像（僅佔位）
```

### 三部曲大綱（出自總企劃）

| 部 | 名稱 | 案件 |
|----|------|------|
| 第一部 | 衡律初聲 | 1-1《初登法庭》、1-2《歌劇院的影子》、1-3《龍裔的證詞》、1-4《夏祭夜的煙火》、1-5《神諭官之死》 |
| 第二部 | 裂衡之兆 | 2-1《失蹤的師父》、2-2《精靈長老的審判》、2-3《紋身殺人事件》、2-4《雙生之決》 |
| 第三部 | 諸界終律 | 3-1《自辯之路》、3-2《童年的回響》、3-3《歸源派之首》、3-4《諸神之審》、3-5《最終法庭：龍王與律》 |

### 如何閱讀

純文件庫，用任何 Markdown 閱讀器（或 GitHub 網頁）即可。建議順序：
1. `諸界之衡_故事結構.md`（全貌）
2. `設定資料/` 01 → 05（世界觀與機制）
3. `角色立繪參考/角色卡_完整集.md`
4. `第一部_衡律初聲/` 各案腳本

### 狀態

- 總企劃：14 案的場景級設計已完成。
- 設定資料：5 份世界觀文件 + AI 生圖 Prompt 包已完成。
- 完整腳本：目前只完成第一部前 3 案（1-1 ~ 1-3）；其餘 11 案僅有總企劃中的場景級設計。
- 圖像：尚未生成；`場景圖參考/` 為空。
- 本專案為創作設計文件；未附授權條款，保留所有權利。

---

## English

### Summary

*The Scales of Many Realms* (諸界之衡) is the design bible for a fantasy courtroom-mystery visual novel inspired by *Ace Attorney*. It is planned as a three-part, 14-case game set in the Hengl Empire, a world with seven races, licensed magic, spirit-medium testimony, and an oracle-driven religion. The protagonist is rookie defense attorney Yan Heng, whose "Fate Threads" ability reveals the hidden bonds between people. A single conspiracy runs through all 14 cases and is revealed in Part 3: the oracles do not come from the gods.

This repository contains **design documents only** (Markdown, in Chinese). There is no game code. Art is to be generated with ChatGPT / Gemini / Midjourney using the prompts in the repo.

### Contents

- `諸界之衡_故事結構.md` – master plan: world foundations, core cast, trilogy arc, scene-level design for all 14 cases, development slices.
- `設定資料/` – world-setting files 01-05 (empire and races, magic licensing, spirit-summoning law, oracle system, courtroom procedure) plus an AI image prompt pack.
- `角色立繪參考/` – full character cards for the 11 core characters.
- `第一部_衡律初聲/` – complete scripts for cases 1-1, 1-2, 1-3.
- `第二部_裂衡之兆/`, `第三部_諸界終律/`, `場景圖參考/` – empty placeholders.

### Status

Master plan, world settings, character cards and the first three full case scripts are done. Cases 1-4 through 3-5 exist only as scene-level outlines in the master plan. No artwork has been generated yet. All rights reserved (no license file).
