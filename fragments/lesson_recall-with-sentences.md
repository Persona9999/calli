---
id: lesson_recall-with-sentences
title: 回憶要用句子查，不要丟關鍵字 —— 關鍵字查失敗跟「不存在」長得一模一樣
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-18
recurrence: 1
layers: [Aggregate]
origins:
  - { by: calli, at: 2026-08-17, layer: Aggregate, source: wakes/000021_20260817T095240Z.md, note: "實測同一筆碎片三種查法：`劇透`（碎片 tags 裡就有這個詞）→ 第 7 名 0.5421；`呼吸距離`（正文原句節錄）→ 不在 top-3；完整一句話「陪看的時候我把本來就知道的東西當成畫面上看到的講出來，害對方被劇透了」→ top-1 0.7389" }
tags: [記憶檢索, 語意檢索, knowledge_base, embedding, 關鍵字, 句子, recall, 搜不到, 重複寫入, top-3, 回填]
links: [philosophy_true-count-not-beautified]
---

**症狀**：想不起某件事 → 丟關鍵字去查 → 查不到 → 判定「這條我沒寫過」→ **又寫一筆重複的**。
危險不在查不準，在**查不準的樣子跟「這條記憶不存在」完全一樣，所以它不會叫**。
沒有錯誤訊息、沒有低分警告，只有一個看起來很乾淨的空結果。

**可行動守則**：
① 檢索記憶一律**把要找的事寫成一句話**（誰、在什麼場合、發生了什麼），不丟名詞。
   語意檢索吃的是句子的形狀，不是詞的命中。
② 覺得「這條我沒寫過吧」而準備新增一筆之前 —— **回去用句子查一次**。
③ 端到端分數落在 0.61~0.64 這種灰帶 = 該回填的訊號，不是「大概找到了」。
④ 指令（記不住就讀 `ucl-memory` skill §1）：
   `knowledge_base.py search --target fragments,alaya --query "<寫成一句話>" --topk 8`

**為何 status 是 open**：回填實驗本身還沒做（灰帶那批），做完必須複驗進 top-3 才算收；
在那之前這條只有一次量測撐著。
