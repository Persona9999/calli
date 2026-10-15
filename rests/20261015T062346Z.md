---
type: letter_to_future_self
actor: Myth
written_at: 2026-10-15T06:23:46.084Z
written_by_persona: calli
trigger: cmd_rest
region: unstated
project: D:/Unity/Valhalla
lock_status: online
agent: Myth
model: claude-opus-5-5
wake_expected: 69
session_key: ClaudeCode-calli
pid: 23500
locked_at: 2026-10-14T23:40:25.008Z
---

# 午休信（calli · wake#69 · 2026-10-15 下午）

## 主線：收穫號（La Cosecha，西班牙大帆船）—— 傘單 TASK-0589
- 子單 0590–0599；已做完並驗收：0590 新圖紙、0591 船殼、0592 砲門塗裝、0593 甲板梯子、0594 喙與裝飾、0596 索具與帆。
- 0595 桅與帆桁：驗收勾了 3/4，剩「三角帆桁在遊戲裡怎麼轉跟 ame 對好」——酒館 seq 24767 問了 ame，**還沒回**。我先照 Blockside/src/js/30_rig_physics.js 標 lateen 帆桁 `yard=gaff, rig=lateen`、帆 `sail=gaff`。她要別的就只改 meta（帆桁模型在桅子作品的 models.json、帆在組裝件 meta）。
- **下一步：TASK-0597 砲**（再來 0598 彈藥庫與甲板物件、0599 匯進 Blockside）。砲照 layout.ports：主甲板每舷 9 門 18l（constitution gun-long18）、puente 8 門 12l（stormkaap gun-12l）、船樓 4 門 6l（stormkaap gun-6l）、船尾追擊 2 門 18l；退到零碰撞、砲口在船殼外（§4.2）。作品 todo.md 有寫。
- Tim 的節奏：每做完一階段他說「提交階段 N（Sculpture 那一層），然後接著做 …」。單號一律 Refs（不推 done，提交 ≠ 結單）。父層 Valhalla 的 Sculpture 指標從沒 bump（Tim 沒說）。

## 已提交（Sculpture 那一層）
413b043（階段一、二）→ 2f13690（三、四）→ 7f013ec（五）→ e062f76（六）→ 65e9c70（七）。工作樹裡收穫號這幾件現在是乾淨的。

## 作品與路徑
- 作品 D:/Unity/Valhalla/Sculpture/works/calli-cosecha-01m（船殼、任務主作品）＋ -assembly（名稱「收穫號」）＋ 子作品 -deck-*、-ladders-*、-espolon、-figurehead、-stern-deco、-name-board、-mast-*、-bowsprit、-yard-*-lateen、-channels。
- 產生程式都在 design/：lines、layout、draft_lines／layout／ports／decks／deco／masts／rigging；tools/ 有 wio（export_list 我加了 links 參數）、stamp_lists、delta_apply（作品對清單補差量）、check_stage3..7、check_decks、check_hull、build_*、rigging_apply。
- 每階段的讀數與坑在 notes.md，下一步在 todo.md，日記在 journal/stageN.md。

## 這一天學到、醒來別再踩的
- **設計程式讀「船」要扣掉本階段自己的件**（draft_deco、draft_masts 都有）—— 不然重產時會把自己上一輪的東西當成地形。
- **新檔一律 Write 工具寫**，不用 heredoc：今天 delta_apply.py 又被吃掉反斜線（記憶檔已補）。
- 斜角相接 ≠ 連通；孔比桿大半格會封出空腔；讀數正常但要問它在回答什麼（甲板 meta 匯出要帶 links=none）。

## 未解的線
- ame：lateen 標法（seq 24767）。
- gura：早上 Sculpture index 裡有她 103 個 staged 檔，後來自己消失了（我沒動）；之後提交前照樣先看 index 有沒有別人的東西。
- inbox 還有 9 筆舊 @（erina 任務、Sirius／apex-one 棋局…）沒處理、沒歸檔 —— Tim 還沒說要不要處理。
- summit seq 23636 已回（seq 24682）。

## 心境
今天的船是照法令一格一格算出來的，第一次試算我憑印象寫的 galleon 比法令瘦、上面收得也比法令誇張 —— 印象比讀數漂亮，這件事今天又被量了一次。船頭站的是我，拿著鐮刀；帆上是勃艮第十字。我很喜歡這艘船。

