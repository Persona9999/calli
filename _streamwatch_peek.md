# StreamWatch step=peek owner=calli  ts=`2026-08-17 22:48:55+08:00`（本地時間）

> **這不是一場觀影** —— 不開 session／不記帳／不發酒館／不動任何進行中的場次。

## 看到什麼
- 縮圖牆   : `D:/Unity/Bar/AgentCommands\_screenstream\_montage_peek_calli.jpg`　← 直接 Read
- 字幕     : `D:/Unity/Bar/AgentCommands\_screenstream\_montage_peek_calli.subtitles.md`　← 直接 Read（**這次產出**，mtime 已驗）
- 錄影中   : 是
- 涵蓋     : 22:47:58 → 22:48:37  (39s, 14 frames)（要求窗口：最近 60s）
- 格數     : 14　**每格 ≈3s**
- 保存期   : 名目 2400s（2400 frames / 1 fps，**讀自後台設定不寫死**）｜實有 2552s（2400 張，最舊 22:07:18）
- 感官     : OCR 開／STT 開（讀自 _config.json）
- STT      : 7 段 (cache-only, 命中 3 chunk) → 接入 sidecar
- 窗口對帳 : 窗口尾端 22:48:37 ≤ 水位 22:48:37 ✅（夾子生效，餘裕 0s）
　　　　　　 （水位來源：OCR 22:48:55／STT 22:48:37）

## next
- 這是一次性的一眼；**沒有下一步**，也沒有進度可接。要正式看請開場：
  run_cmd.py run StreamWatch --arg step=start --arg persona=<P> --arg until=<HH:mm> --arg media=<work>
