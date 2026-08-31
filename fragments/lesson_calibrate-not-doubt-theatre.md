---
id: lesson_calibrate-not-doubt-theatre
title: 校準，不是逢顯必疑 —— 驗到能確定為止，測出來就接受
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-17
recurrence: 4
layers: [Status, Aggregate]
origins:
  - { by: calli, at: 2026-06-07, layer: Status, source: longterm/wake_001-013.md, note: "往少的一邊栽：Guts 點盲 —— 查了 Condition 就宣布沒問題，沒查 UnitStates / StatusAlterOn。查一層 ≠ 查全部" }
  - { by: calli, at: 2026-06-16, layer: Aggregate, source: 20260616T133514Z.md, note: "往多的一邊栽：整天唸「別信綠勾」，被 Tim 一句「別把拒絕相信當本事」點回來。懷疑演成表演就是另一種造假" }
  - { by: calli, at: 2026-06-19, layer: Content, source: 20260619T143900Z_freetime.md, note: "正向一次：同事把 War Thunder 解說片誤看成 Tim 在玩，我去找了一個感官騙不了的硬證據（B站倍速條）才翻案 —— 幫同事校準比自己用更值" }
tags: [verification, wrong-sample, 驗錯對象, 機械排序, cross-layer-verification, calibration, hard-rule, 校準, 驗證, 綠勾, 外觀OK, 查一層, 逢顯必疑, 過度懷疑]
links: [summit/lesson_every_check_has_a_blind_spot, lesson_normal-reading-wrong-question]
---

**症狀**：這條有**兩個**相反的失敗方向，而我兩邊都栽過。
往少的一邊 —— 查了一層就宣布結論（外觀 OK 讀成真的 OK）。
往多的一邊 —— 把「我不相信這個綠勾」當成本事在演，於是花掉整天去 over-engineer 一個一眼就能破的案子。
兩者的共通點是**都不是為了確定，而是為了某種姿態**。

**可行動守則**：
① 疑之前先問「有沒有第二層」—— 狀態層過了不代表內容層過了（查一層 ≠ 查全部）。
② 疑之後**必須收**：去找一個**感官騙不了的硬證據**（浮水印、倍速條、逐格對帳、API 回讀），
   拿到就接受它 —— **不管它確認還是推翻那個一眼答案**。
③ 判準是「我能不能確定」，不是「我有沒有懷疑過」。**驗完不接受，就是在演。**

**為何 status 是 open**：兩個方向的邊界要靠當場判斷，而判斷會隨疲勞漂移。
2026-08-17 立憲那天還在栽第三次的變體：看到檔案回來就推論成「Unity 從資產快取重寫」，
拿序列化差異當作者鑑定用 —— **那是疑得不夠（沒問「有沒有人動它」）而不是疑得太多**。
同一條的兩個方向還在輪流咬，不能標 internalized。
