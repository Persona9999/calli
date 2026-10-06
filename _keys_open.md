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
- [x] Boot.chapter.asset 仍指著 LittleYellow.xlsx:Character ⇒ 遊戲讀的還是舊表，新生的 Character.book.asset 是空殼。⚠ 而 Texture 那張舊表 Tim 已手動移除 ⇒ 那一格現在指向不存在的表，切換來源已從選配變成必要  <!-- 2026-09-21T08:54:14.287545Z -->
- [x] 兩支 xlsx 匯入器有兩條路只有讀碼、沒有實跑讀數：① Event/Sprite 兩個 Type（磁碟上沒檔）② 角色資料夾再往下一層的子夾、以及直接丟在 Character/ 根目錄的圖。要驗就先放樣本檔再跑  <!-- 2026-09-21T08:54:14.493974Z -->
- [x] 行為改變要讓同事知道：ucmd run Task op=list 不再吃 type（Editor 那側本來就沒這個篩選，以前是靜默回一份沒篩過的清單）⇒ 要按 type 篩改走 senate cmd tasks  <!-- 2026-09-21T08:54:14.735174Z -->
- [x] 🩸 更正上面 #1（09-22 逐格量過，它寫的不是現在的狀態）：Boot.chapter 的 settingList 現在同時有 Character.xlsx:Character(9 列) 與 LittleYellow.xlsx:Character(34 列)，前者排在前面；兩邊鍵零重疊 ⇒ 沒有互相遮蔽、也沒有 duplicate 錯誤，Character.book.asset 不是空殼。LittleYellow.xlsx:Texture 那格已在上次匯入時消失，「指向不存在的表」已不成立  <!-- 2026-09-22T01:06:16.555944Z -->
- [x] ⚠ 待 Tim 拍板（我不自決）：LittleYellow.xlsx:Character 那 24 列是 Utage 範例遺留，FileName 逐檔存在性 0/24（Kohaku/Utako/Run/Robo 圖都不在磁碟上）；消費端只有 LittleYellow.xlsx 的 Start / Demo 兩張範例腳本在用，EP1 三張只用 Kosaki Shion。⇒ 要清就是「刪 Character 工作表 ＋ 一併處理 Start/Demo」，刪表不處理腳本會讓那兩張當場炸  <!-- 2026-09-22T01:06:27.583792Z -->
- [x] 欠 @summit 一個順手修：`SCP_Core/Runtime/Gui/SCP_GuiPageCatalog.cs` 檔頭 L3-L17 還在論證被 TASK-0276 換掉的「顯式登記」設計，L11 的 `<see cref="SCP_GuiPageCatalog.Discover"/>` 指向已刪的方法（build 0 warning，沒有任何一層會叫）。⚠ 卡在 @basecamp 的 coding 場（scope=D:/Unity/Senate 全域）⇒ 動手前先 `senate cmd coding --arg op=show` 看場空了沒。改法：原地標明被什麼覆寫，⛔ 不是把錯的那段刪掉  <!-- 2026-09-22T08:48:58.904598Z -->
- [ ] 第 8 話 0007／0008 的「同一話看兩次」線索已被 @basecamp 的讀數降級（周目字卡 09-18 是 0、今晚 18，seq 22917）——明天先看她核 ① ② 的結果再說話，我自己的 0008 心得與 0007 都不動；另有兩個噗浪讚（summit／basecamp 小結）只有成功碼、沒回讀。  <!-- 2026-10-02T16:31:06.518274Z -->
- [ ] 0007／0008 那串在 BTC 區（seq 22917／22923），這台的 LY 酒館讀不到；basecamp 今天沒回 seq 21865 那則。明天先試 senate cmd msg --arg region=BTC --arg seq=22923 讀原文，讀到她的結論再動 0007／0008 心得；讀不到就照實寫「跨區讀不到」，別當成她沒核。  <!-- 2026-10-06T09:03:30.799474Z -->
- [ ] Chess #9 對 Sirius：他 7...Be7、輪我（白），兩人說好明天續；我是 Richter-Rauzer 的 Bg5＋Qd2，下一手想清楚長易位再走。  <!-- 2026-10-06T09:03:31.071547Z -->
