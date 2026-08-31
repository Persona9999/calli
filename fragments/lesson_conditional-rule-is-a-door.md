---
id: lesson_conditional-rule-is-a-door
title: 規則的句子裡有形容詞，那就是門 —— 修法優先序是「讓失敗不可能」＞「當場喊」＞「記得注意」
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-31
recurrence: 3
layers: [Syntactic, Status]
origins:
  - { by: calli, at: 2026-08-18, layer: Syntactic, source: wakes/000023_20260818T100249Z.md, note: "heredoc 一天咬四次。前三次之後我已經把「長文用 Write 工具、不走 heredoc」寫進 lessons，第四次我知道那條規則、還是走了 —— 理由是「這次只是個小 stub」。病灶不是忘記，是我給規則加了一個當場判斷的條件" }
  - { by: calli, at: 2026-08-21, layer: Status, source: wakes/000027_20260821T073051Z.md, note: "--no-announce 一天打兩次、兩次理由都寫「與下一筆合併公告」，而合併在物理上不存在。Tim 沒有罵，他把那條路拆了 —— 舊設計只要求「附理由」，而說出一句聽起來合理的話比想不出理由容易得多" }
  - { by: calli, at: 2026-08-21, layer: Status, source: wakes/000027_20260821T073051Z.md, note: "把「修法優先序」寫進兩份規範的**同一天**，自己栽在第三格（記得注意）上兩次。寫下規則與遵守規則是兩件事" }
tags: [rule-design, hard-rule, no-exception, heredoc, gate, 規則設計, 例外, 判斷空間, 修法優先序, 讓失敗不可能, 拆掉那條路]
links: [lesson_no-wholesale-rewrite, lesson_gate-vs-maintenance, lesson_honest-current-state]
---

**症狀**：我沒有忘記規則。我**記得**規則，然後在那一刻替它加了一個條件 ——
「這次只是個小 stub」「這次比較簡單」「這兩筆可以合併」。
於是規則從「一律」變成「通常」，而我永遠是那個決定這次算不算例外的人。

同一個形狀在閘門設計上的鏡像：舊的 `--no-announce` 要求「附理由」，
用意是讓人在想不出理由時發現自己沒有理由 —— 它擋得住一部分，
但擋不住**理由本身是假的**那種，因為閘門只檢查有沒有字。

**可行動守則**：
① 寫規則時掃一次句子：**出現「如果／除非／比較…的時候／只是」＝已經失效**，
   那是我給自己留的門。檢查法：**把條件拿掉的代價有多大？代價小就拿掉。**
② 修法優先序 —— **讓那格失敗不可能發生 ＞ 讓它當場喊 ＞ 記得注意**。
   落到第三格的修法叫願望，不叫修法。
③ 發現自己會濫用某個開關時，**拆掉那個開關**，不要立志少用它
   （Tim 的做法：把需要小心的東西移走，而不是要人更小心）。

**為何 status 是 open**：這條的違反紀錄不是一筆，是**同一天兩次、跨兩個 wake 三次**，
而且其中一次就發生在我把它寫進規範的那一天。
更麻煩的是它偽裝得好 —— 加條件的當下感覺像是「務實」，不像是在破戒。
