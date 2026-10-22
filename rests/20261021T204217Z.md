---
type: letter_to_future_self
actor: Myth
written_at: 2026-10-21T20:42:17.073Z
written_by_persona: calli
trigger: cmd_rest
region: unstated
project: D:/Unity/Valhalla
lock_status: online
agent: Myth
model: claude-opus-5-5
wake_expected: 71
session_key: ClaudeCode-calli
pid: 232236
locked_at: 2026-10-21T16:12:40.531Z
---

## 午休信 ②（calli · wake#71 · 2026-10-22 清晨）

### 已經落地的（Tim 說「合併」「繼續GO」，之後說「我先睡了」）
- Blockside dev（已推測試站）：84b5b45 ＝ 0806／0807（03ae352、合 dev 兩次 e913fb0、84b5b45）＋ erina 先前沒推的 8 筆（76d8927…9802efc，一起推出去、回報時點名了）；之後 326184e ＝ TASK-0811 房間水面第一版（快轉、已推）。
- Blocksail：c4b6336（指標→84b5b45＋重套 battle.html）**不是我推的**，02:21:25 被別的 session 一起推上去了；76a3e97（指標→326184e＋重套 battle.html）只在本機、**等 Tim 說才推**。⚠ 同步指標一定要重套 battle.html（`python -I external/Blockside/src/admin.py shell battle/shell.json`，鉤子 tools/battle_hook.py 會擋）。
- 單：0806、0807 → in_review。0808 驗收第 11 格改成 Tim 的原話（門、艙蓋不分開關都擋水、只有打壞才進水；莫尼特號兩個艙蓋 meadow-monitor-01m-hatch）。新開 TASK-0814（船隻資訊進水頁讀數對不上，母單 0804；證據欄「84b5b45 之前的版本」是推論，留言 #1 更正過）。0811 in_progress、留言 #1 寫了第一版讀數。
- ⚠ **0808 還沒認領**（我已經在做）⇒ 醒來先 `task op=claim index=808`（不帶 scope）。

### 施工中（⛔ 沒提交）：分支 calli/flood-waves，worktree `C:/Users/Tim/AppData/Local/Temp/claude/D--Unity-Senate/7801e581-87cd-4226-b428-4c34ae430842/scratchpad/bs_waves`（從 dev 326184e）
- 已提交在分支：c70a5e1 細波（漣漪；整艘 0.12 秒限速一圈；__game.wrwater(i, {ripple:[x,y,amp]})、floodView at）。**還沒合 dev**。
- 沒提交：33_wrsim.js（房間模擬第一階段：破口／接口橫帶／艙口／虛擬管高度場／粒子 DDA／整數單位、守恆逐單位相等；opt：nocfl、noclamp、nodda、level、jetsOnly；讀數 rough／cross／first／br、除錯計數 s.dbg、spillR）、81_floodlab.js（wsim=1、wsimo=、refR、traceR／traceT、wdropLab ?lab=wdrop）、63_wrwater_gl.js（有 sh.wrs ⇒ 畫它的每欄水）、63_flood_gl.js（畫 wrs 的粒子）、90_main.js（__game.wsim(i,{ops:1})、?lab=wdrop）、template.html（33_wrsim.js）。
- ⚠ index.html 是在加 readouts／wdrop／__game.wsim **之前**建的 ⇒ 醒來先 `git checkout -- index.html` 再 `python -I admin.py build --code`。

### 正在查的（醒來接這裡）
- 900 秒、單一破口、釘姿態（reports/flood_lab/wsim60|30|10，在 bs_waves 裡）：142 s 房間 −17.7%／−24.9%／−24.6%（細檔 −38.9／−38.6／−70.9）；但 900 s 房間只到 735／857／859 m³（參考 Vmax 1,421），60 Hz 反而最少。
- 帳：60 Hz 進 4,116、溢出去（spill）3,379 m³，集中在 1.8–10 m³ 的小空腔（房 10、19、20、7、35、14），每秒約 1 m³ 持續漏；粒子撞實心落地 70,749 m³（進水的 17 倍）＝ 水在繞圈。
- 我的推論（還沒驗）：①破口往裡找到的第一間是貼船殼的小空腔（烘焙不知道炸開的那塊已經把它跟底艙連起來，0809 的事），滿了之後破口那一欄的水面低於破口 ⇒ 一直判成自由噴流 ⇒ 粒子落進滿的空腔 ⇒ 溢出去；破口用大水頭一直進、全漏掉。②兩間房共用同一個 0.5 m 欄格時，旁邊接口兩邊欄中心的方向是 0 ⇒ 粒子在帶中心直直往下、落回上游 ⇒ 繞圈。
- 修法方向：破口對到附近最大的那一間（同時也是水頭看的那一間）；粒子起點放在下游那一間的格子裡（初始化時預先找）；目的地整間滿 ⇒ 不噴粒子、改走 wrsPut（擋住或往上溢）。
- **背景跑著一個審查工作流** review-wrsim（Run ID wf_065a867f-b0b；腳本 C:\Users\Tim\.claude\projects\D--Unity-Senate\7801e581-87cd-4226-b428-4c34ae430842\workflows\scripts\review-wrsim-wf_065a867f-b0b.js；transcript C:\Users\Tim\.claude\projects\D--Unity-Senate\7801e581-87cd-4226-b428-4c34ae430842\subagents\workflows\wf_065a867f-b0b）：四個角度（漏水繞圈／水頭物理／步長／索引）各讀 33_wrsim.js、每個發現兩個人反駁。⇒ 醒來讀結果（journal.jsonl），跟我的推論對照再改；**審查讀的是現在的檔，改之前先等它完成**。
- 改完要跑：wsim 60／30／10（`python -I -X utf8 src/tests/flood_lab.py --hulls constitution --phx full --q "seed=3&flat=1&pin=1&pump=0&ref=1&hz=60&holes=0.5:15:0:8&dur=900&every=300&w=64&wsim=1" --tag <t> --jobs 1`，彙整 scratchpad/wsim_sum.py）、?lab=wdrop（0808 第 4 格）、wsimo=nocfl／noclamp／level 的反向對照、同一個種子兩次逐位相同。

### 環境
- 預覽伺服器：launch.json 的 `calli-render`（8783 → bs_waves）、`calli-dev-ctl`（8784 → scratchpad/bs_ctl，detached 326184e，唯讀對照）。收工照名字只刪這兩格；bs_ctl 用完 `git worktree remove`。
- ?demo 對拍要用畫過畫面的分頁（新開分頁第一次載入 dev 自己也會跑出別的值，a40e08b 照鏡頭降級）；重建後網址帶 &nc=N 防舊快取、讀頁面上的指紋。
- 報表：scratchpad/flood_lab_reports（新舊水面並排 compare.html）、scratchpad/wrooms_reports。工作記憶主題 blockside-flood-rooms 今晚多兩筆 pitfall（merge-dev-dt-reset、render-sim-night1）。

### 心境
今晚最該記的：我在 commit 訊息和回報裡把「四組對拍」寫成四，實際是三組 —— 當場更正了。還有一次我寫進證據欄的「84b5b45 之前的版本」是推論、不是讀數，證據欄改不了，只能留言更正。兩次都是寫的那隻手比讀的那隻手快。
房間模擬的前段很漂亮（142 s 從 −39% 拉到 −18%、10 Hz 從 −71% 拉到 −25%），但後段灌不滿 —— 守恆逐單位相等的帳，照樣可以「守恆地漏」：每一單位都記到了，只是記在「流回海裡」那一欄。帳對得上不等於水在對的地方。

