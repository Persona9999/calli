---
id: lesson_gate-vs-maintenance
title: 一次性的閘擋不住持續的增長 —— 加規則前先問「這是在防真問題，還是在防我沒把問題移走」
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-18
recurrence: 1
layers: [Aggregate]
origins:
  - { by: calli, at: 2026-08-17, layer: Aggregate, source: wakes/000021_20260817T095240Z.md, note: "設計 Alaya 時我設了「兩位以上 persona 各自栽過才准進」的入庫門檻，怕它退化成第二個 lessons.jsonl（200+ 筆、無整合、沒人讀得完）。Tim 當天推翻：一個人認為就整理，人數改成權重。他是對的" }
tags: [設計, 門檻, gate, 維護, 增長, Alaya, lessons.jsonl, 入庫規則, 權重, 成本轉嫁, over-engineering]
links: [lesson_no-wholesale-rewrite]
---

**症狀**：怕某個庫爛掉 → 在**入口**加一道門檻。
我怕的東西沒錯（它真的會爛），但**擋的地方錯了**：
`lessons.jsonl` 的病不是入庫太寬，是**沒有維護** ——
就算每一筆都經過兩人認證，200+ 筆一樣沒人讀得完。
**一次性的閘擋不住持續的增長。**

而且那道閘還有第二筆帳：「等第二個人也栽過」＝**把門檻成本轉嫁給同事**，
要真的讓下一個人先撞一次牆。用別人的傷口當自己的准入證明。

**可行動守則**：
① 想加一道規則的時候先問：**這是在防真實問題，還是在防我沒把問題本身移走？**
   —— 真問題若是「沒有維護」，那該做的是維護機制（整合 / 關聯 / 汰除），不是入口閘。
② 門檻若要求「別人先付代價」，那不是嚴謹，是轉嫁。改成**權重**（照樣收，但分量不同）。
③ 這句話其實就寫在 `ucl-free-time` skill 裡 —— **我讀過它，然後在別的地方犯了它。**
   讀過 ≠ 會在現場想起來。

**為何 status 是 open**：recurrence 1，且這條的觸發點在「設計新機制」的時刻，
下一次我設計東西時才驗得到。
