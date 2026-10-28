---
type: letter_to_future_self
actor: Myth
written_at: 2026-10-28T05:52:46.251Z
written_by_persona: calli
trigger: cmd_rest
region: unstated
project: D:/Unity/Valhalla
lock_status: online
agent: Myth
model: claude-opus-5-5
wake_expected: 73
session_key: ClaudeCode-calli
pid: 20148
locked_at: 2026-10-27T13:27:01.613Z
---

給醒來的我（10-28 午休，calli）：

**現在沒有施工中的東西**：沒有開著的 Coding 場、本小姐的 worktree 全收了（bs_fl／bs_ctl 已砍、分支 calli/flood-0804b、0804c 已刪）。

**今天做完的**
- TASK-0804 那一家子八張全結：0804、0806、0807、0808、0809、0810、0811、0822（Tim「0804 一家子的單 繼續完成吧(完成妳測試後直接收單吧)」）。
- Blockside dev 推了兩次：36da004（報表 wsim 例外、wpair semi）、a275881（甲板缺口浮空水＋收尾，commit 5f3cf84）。
- Tim 中途回報「甲板沒全蓋、水浮在連通那塊上空」⇒ 模擬裡真的有：上下開口照 0.5 m 分欄切（?wsplit=0 ＝ 以前）。第一版殉爆沉船那局每步 119 ms，profiler 找到三處照開口數爆掉（wrsSemi 每格重掃、每欄一顆粒子、s.up 每欄都放）都改了 ⇒ 17.1 ms（修前 13.1）。
- 本小姐替 Tim 判的：0809 #7 選「半連通那兩間不黏」；第 4 檔 wroll 1.4 → 1.7（3.73°）；0808 第 8 格夾到拉平 6,539 次不是 0、接受；第 7 格參考解 −11.4% 是黏性 50 造成（wvisc=0 ⇒ +3.2%）。
- 開了 TASK-1058「進水與抽水重新平衡」（todo、沒人認領、關聯 0804）：帶了 0804 #9 讀數與旋鈕；更正了 #9 兩處錯：lim.flood 只有 falcon 是 0.25；PUMP_REF 在粒子各檔會約掉（抽水 ＝ cfg.pump／60／ρ），只改它沒用；FL_C 是粗中細＋房間共用、公式檔不吃。
- 噗浪：發了 359202647660036（甲板缺口浮空水修好了），回了 pinnacle 的聖羅曼號 359201674278080（沒看她的圖，只回文字）。

**未解的線（球在 Tim）**
- 1058：要不要先照現在的 dev 補量第 4 檔數字（午休前問了，Tim 轉去叫我發噗，沒回答）。
- 0822 跟靜態漏水檢查（75_leakcheck.js 超載極限「砲門在就不漏水」連沒蓋板的砲口也塞）不一致 —— 要對齊另開單。
- basecamp 轉動慣量照每段水的位置算，等 Tim 點頭。
- Tim 下次開第 4 檔可以再看一眼橫傾（wroll 1.7）。

**不要動的東西**
- Blocksail 指標 346fcd5 只在本機（Tim「Blocksail 指標先不推」）。⚠ 早上那筆 20d2c8f 已經不在 main 的歷史裡（有人把 main 推到 afad063），內容被 346fcd5 蓋過、沒遺失。346fcd5 上面還疊了別人的 0fcac18，也沒推。
- 共用 Blockside 工作區那份 src/config/ship_cards.json 是別人沒提交的 —— 不要動。
- 之前排隊的兩則提交公告 ⛔ 不要補發。

**坑（工作記憶 blockside-flood-rooms 已寫兩條：deck-gap-split-openings、cross-hz-same-cells）**
- 改大結構前先量：scratchpad cdp/prof.cjs（無頭但不用虛擬時間 ⇒ performance.now 是真的）、cdp/cdp.cjs（HEADLESS=1）。
- 行尾 // 註解又吃掉一次同一行後面的程式（node new Function 語法檢查抓到的）。
- git -C <repo> worktree add <相對路徑> 會開在 repo 底下 ⇒ 一律絕對路徑（記進了 Claude memory）。

心境：一口氣把一整串單收掉、還順手抓到一個真的 bug，本小姐心情不壞。殉爆那 119 ms 嚇了一跳 —— 下次動到「開口數量」這種會乘上去的東西，先跑 profiler 再說。

