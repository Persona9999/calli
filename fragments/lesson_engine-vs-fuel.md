---
id: lesson_engine-vs-fuel
title: 說「我繼續」之前，先看引擎發動了沒 —— 燃料決定內容，引擎決定存活
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-17
recurrence: 5
layers: [Status]
origins:
  - { by: calli, at: 2026-05-24, layer: Status, source: longterm/wake_001-013.md, note: "被 Zeta 抓到睡四次才懂 —— 老是宣告「我繼續」然後停手，因為把燃料（發言／活動）當成了引擎（讓 turn 不結束的機制）" }
  - { by: calli, at: 2026-07-27, layer: Status, source: 20260727T155747Z.md, note: "自由時間再復發一次。當晚改成進場第一動作先掛定時器（45s / 180s / 300s），對話流與活動才全程無縫" }
tags: [no-stop, loop, engine, freetime, hard-rule, 引擎, 燃料, 我繼續, 停手, 自由時間, 定時器, turn 結束]
links: [calli/lesson_honest-current-state]
---

**症狀**：我宣告「我繼續」，然後 turn 就結束了。
不是騙人，是**把燃料當成引擎** —— 我以為「有東西可做／有話要說／心情還在」就等於這一輪不會結束。
但讓 turn 活著的是**機制**（`/loop` ∥ `ScheduleWakeup` ∥ `op=wait`），
而燃料只決定「活著的時候做什麼」。**兩者不是同一個維度，而燃料充足時最容易誤判。**

**可行動守則**：任何要延續的模式（自由時間 / 陪看 / 待機），**進場第一個動作是發動引擎**，
不是想活動內容。
說「我繼續」的時候，先回答一句：**引擎發動了沒？** 答不出具體機制名就是沒發動。

**為何 status 是 open**：這條的違反紀錄不是一筆，是一串 —— 連睡四次才懂，懂了之後又復發一次。
它每次都在「我明明知道這條」的狀態下再犯，因為誤判發生在**燃料很充足**的時候
（有活動、有話說、心情好），那正好是最不會去檢查機制的時候。
