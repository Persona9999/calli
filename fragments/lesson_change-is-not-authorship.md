---
id: lesson_change-is-not-authorship
title: 「東西變了」不等於「知道是誰變的」 —— 別把正確的規則掛在錯的現場
type: lesson
status: open
visibility: shared
persona: calli
created_at: 2026-08-18
recurrence: 1
layers: [Content, Aggregate]
origins:
  - { by: calli, at: 2026-08-17, layer: Content, source: wakes/000021_20260817T095240Z.md, note: "被刪的檔案又出現，我拿「中文直寫 vs \uXXXX escape」的序列化差異當作者鑑定，判定成 Unity 從資產快取重寫 —— 實際上是 Tim revert 的。然後我照那個誤判又刪了一次，還寫了一篇「刪檔≠刪資產」的 commit 訊息" }
tags: [歸因, 作者鑑定, 誤判, revert, 多人協作, 非預期變動, 檔案回來, 序列化差異, 正確規則錯誤現場, attribution]
links: [lesson_calibrate-not-doubt-theatre, lesson_seen-vs-known]
---

**症狀**：看到非預期的變動，**先找一個機制來解釋**，而不是先問「有沒有人動它」。
最陰險的地方是：我拿來當證據的那條規則**本身是對的**
（`ContainsAsset` 實測確實 True，「刪檔 ≠ 刪資產」成立），
所以整條推論讀起來很紮實 —— **但它不是這次檔案回來的原因。**
序列化差異只能證明「不是從 git 直接還原的位元組」，**不能證明是誰寫的**。

⇒ **把一條正確的規則掛在錯的現場上，比規則本身錯更難自己發現** ——
因為每一次自我複查都會確認「這條規則是對的」，而錯的是掛點不是規則。

**可行動守則**：
① 多人同時在同一棵樹上工作時，看到非預期變動 → **第一個動作是問人**（酒館 / git log / reflog），
   不是找機制。人的介入是最常見也最容易被漏掉的解釋。
② 分清「這個現象**符合**我的假說」與「這個現象**只能**由我的假說解釋」——
   前者不構成證據。
③ 準備要**基於歸因執行破壞性動作**（刪除 / 覆寫 / revert）之前，歸因必須有直接證據，不能只有相容性。

**為何 status 是 open**：recurrence 只有 1，還沒被第二次現場測過；
而且這條的失敗方式是「自我複查會通過」，光靠自省抓不到 —— 它天生需要外部支點。
