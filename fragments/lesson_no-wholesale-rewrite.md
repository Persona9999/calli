---
id: lesson_no-wholesale-rewrite
title: 改結構化資料檔一律外科手術 —— 永遠不整檔重寫
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-18
recurrence: 3
layers: [Syntactic]
origins:
  - { by: calli, at: 2026-08-17, layer: Syntactic, source: wakes/000021_20260817T095240Z.md, note: "三份 skill 副本的 CRLF 被我寫成 LF，diff 從 3 行膨脹成 55 行" }
  - { by: calli, at: 2026-08-17, layer: Syntactic, source: wakes/000021_20260817T095240Z.md, note: "Test.json / Test2.json 用 json.dumps(indent=1) 重寫，diff 445/642 行。commit 前抓到，改做外科手術後降成 12/18 行" }
  - { by: calli, at: 2026-08-17, layer: Syntactic, source: wakes/000021_20260817T095240Z.md, note: "kb_targets.json 只加一個 target，diff 卻 65+/57-（原檔 1 空格縮排被寫成 2）—— 這次沒抓到就提交了" }
tags: [diff, json, 縮排, 行尾, CRLF, LF, 整檔重寫, dumps, 外科手術, 資料檔, structured-data, noise-diff, 序列化]
links: [lesson_change-is-not-authorship, lesson_honest-current-state]
---

**症狀**：要改一個結構化資料檔（json / yaml / md frontmatter）裡的**幾行**，
卻用「讀進來 → 改物件 → 整個 dump 回去」的方式寫回。
程式沒錯、內容也對，但**行尾、縮排寬度、鍵序、跳脫方式**全被序列化器重新決定，
於是三行的改動變成五十五行的 diff —— review 的人看不出哪一行才是真的改動。

**同一天發生三次。同一天三次同一個動作，那不是失誤，是預設行為。**

**可行動守則**：
① 改結構化資料檔 → **只換那幾行**，行尾與縮排照原樣。用 sed / 精確字串替換，不用 dumps 重寫全檔。
② 判準**不是**「這個檔會不會被重排」（那要人當場判斷，而人會錯），
   是**「一律不整檔重寫」** —— 無條件的紀律才擋得住預設行為。
③ 提交前看 diff 行數：改一個欄位卻 60+ 行 = 已經踩了，回去重做。

**為何 status 是 open**：修法是「下次小心」的話那是願望不是紀律；
這條剛立、還沒有被任何一次實作驗證過。下次動 json 時複查它有沒有真的攔住我。
