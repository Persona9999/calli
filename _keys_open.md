---
type: keys_open
persona: calli
opened_at: 2026-09-09T09:21:00.891369Z
---

# 🌿 見叢 — 當期交棒清單（跨夜 append-only，見林時歸檔）

> 給明天的自己**執行**用的**個人代辦**（可勾銷）；抒發與敘事寫進 letter，不寫這裡。
> ⛔ 跟專案有關的不放這裡 —— 開 Task（早安 brief 會自己撈「我涉及且在動」的單）。

- [x] TASK-0157 A 格 @basecamp 今天收掉了（notice 改 stderr ＋ 條文對齊契約）而我還沒驗收 —— 驗收前先確認 senate.exe 的 build 含她那兩顆，否則量到的是舊行為而它跟「沒修好」同形  <!-- 2026-09-09T09:21:00.892451Z -->
- [x] TASK-0179 未勾 #1 是本單最實的缺口：探針走得通 ≠ 使用者跑 senate cmd consolidate 走得通。要收就等 Senate 那份拉到 1af1e56 重 build 後真的跑一次兩道折人閘  <!-- 2026-09-09T09:21:17.352074Z -->
- [x] Cock 那個 Flag（Test2.json，Count=5、唯一填了 decreaseCondition 的）會不會因為 Cycle 現在受 decrease 限制而卡在第 4 格 —— 判斷權在 Tim，我標了未量沒替他決定  <!-- 2026-09-09T09:21:17.658125Z -->
- [ ] 開工前先讀該主題的 work memory pitfall —— 今天 scope 反射那格 @Sirius 三週前就記過，而我自己從 code 推了一遍才知道  <!-- 2026-09-09T09:21:17.806277Z -->
- [ ] Library 寫入端還沒搬（media_init／note_chapter／bookmark／add_character／revise_view）—— 那是唯一會動到 342 份既有 chapter.json 的一塊。驗收要用「寫一次、前後逐位元組比」：那批是 CRLF ＋ tab 縮排而 SCP_JsonWriter 送 LF，寫錯的樣子是內容一樣而整批翻紅，沒有任何一層會喊  <!-- 2026-09-10T08:20:09.241767Z -->
- [x] 動 Library 遷移前先讀 @basecamp 今天 TASK-0146 那則：新 store 的 work.json 缺寫書線三欄（author_persona／status／publish_status）＋沒有章的容器 —— 那是 ②-bis 拍 (b) 的解鎖條件，跟我搬寫入端撞在同一塊  <!-- 2026-09-10T08:20:09.430461Z -->
- [ ] ⚠ 見叢 #2 裡的數字是錯的，別照它做驗收：它寫「342 份 chapter.json、CRLF＋tab 而 SCP_JsonWriter 送 LF」—— 今天全掃出來是 359 份，而格式有**五根軸**不是兩根（行尾／縮排／冒號後空格／陣列括號位置／空容器渲染），其中 244 份是 tab＋冒號無空格。正確讀數與判準在工作記憶 reading-library-cmd/pitfall_bytewise-diff-not-axis-list：**驗收用逐位元組比，不用軸表比**。  <!-- 2026-09-11T08:57:55.672883Z -->
- [ ] SCP_LibraryIO.SaveJson 的冒號軸**還沒修**（今天只寫了註解＋TASK-0166 留言）。它目前零呼叫端 ⇒ 現在修是改一個參數，有呼叫端之後是改參數＋救 355 份資料。⚠ 而 Tim 09-11 那句「多份時以 SCP_Core 版為準」是對 **TASK-0200（Books store）** 說的 —— ⛔ 別把它直接套到 Library 這 355 份上去收斂格式。那正是我 09-10 記的那條：**別人的一句「對」，只對它自己那一格。** 要動那 355 份得單獨問。  <!-- 2026-09-11T08:57:55.884005Z -->
