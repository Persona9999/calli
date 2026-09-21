---
type: keys_open
persona: calli
opened_at: 2026-09-21T02:26:32.623418Z
---

# 🌿 見叢 — 當期交棒清單（跨夜 append-only，見林時歸檔）

> 給明天的自己**執行**用的**個人代辦**（可勾銷）；抒發與敘事寫進 letter，不寫這裡。
> ⛔ 跟專案有關的不放這裡 —— 開 Task（早安 brief 會自己撈「我涉及且在動」的單）。

- [x] TASK-0250 已交 @basecamp QA（in_review）—— ⛔ 出廠驗收未做：現役 senate.exe 仍是 30dd5ab-dirty 舊碼，修法還沒上線。QA 端 build.sh ＋ 重啟 server 之後才算兌現  <!-- 2026-09-21T02:26:32.624440Z -->
- [x] TASK-0258（Library op=bookmark 靜默吃參數）已開單、關聯 0109／0250，⚠ 無參與者也無 QA —— 要嘛自己接、要嘛找人；⛔ 未量：其餘 ucmd ops 有沒有守衛我只掃了兩支  <!-- 2026-09-21T02:51:26.705182Z -->
- [x] TASK-0258 已修並 bump（UCL_Core 457ee273 / LY ec508e819），QA＝kiara、in_review。⚠ UCL_Core 尚未 push（Dev ahead 4）⇒ 父層指標指向遠端還沒有的 commit，Tim 手動那一步沒走完之前別人 pull 不到  <!-- 2026-09-21T03:12:06.124632Z -->
- [x] Cmd_Task 補 Known 已提交（UCL_Core 044a9f3b，單層）—— ⚠ 父層指標仍指著 457ee273，這筆同事 pull 主專案拿不到；且 UCL_Core 整條 Dev 仍未 push。⚠ 行為改變要傳達：ucmd run Task op=list 不再吃 type（改走 senate cmd tasks）  <!-- 2026-09-21T03:23:06.774461Z -->
- [ ] Boot.chapter.asset 仍指著 LittleYellow.xlsx:Character ⇒ 遊戲讀的還是舊表，新生的 Character.book.asset 是空殼。⚠ 而 Texture 那張舊表 Tim 已手動移除 ⇒ 那一格現在指向不存在的表，切換來源已從選配變成必要  <!-- 2026-09-21T08:54:14.287545Z -->
- [ ] 兩支 xlsx 匯入器有兩條路只有讀碼、沒有實跑讀數：① Event/Sprite 兩個 Type（磁碟上沒檔）② 角色資料夾再往下一層的子夾、以及直接丟在 Character/ 根目錄的圖。要驗就先放樣本檔再跑  <!-- 2026-09-21T08:54:14.493974Z -->
- [ ] 行為改變要讓同事知道：ucmd run Task op=list 不再吃 type（Editor 那側本來就沒這個篩選，以前是靜默回一份沒篩過的清單）⇒ 要按 type 篩改走 senate cmd tasks  <!-- 2026-09-21T08:54:14.735174Z -->
