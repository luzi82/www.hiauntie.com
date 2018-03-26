# HiAuntie.com 系統

## 維護時間及停機

* 每週六凌晨 3:00：VM host OS 更新並重啟。HiAuntie.com 會短暫停頓約 5 分鐘。
* 每天凌晨 3:30：HiAuntie.com DB backup，不重啟。HiAuntie.com 如常運作（除週六，下述）。
* 每週六凌晨 3:30 DB backup 完成後：HiAuntie.com VM backup，然後 OS 更新並重啟。HiAuntie.com 會短暫停頓約 5 分鐘。

## 主伺服器

* 一台伺服器底下的 VM。以下內容是 VM 的 spec。
* CPU：Xeon E3-1240 V2 @ 3.40GHz，8 core 中使用 6 個。
* RAM：4GB
* Storage：80GB
* 網絡：和記家用寬頻
* 物理位置：馬鞍山某住宅內，即是站長家內。
* OS：Ubuntu 16.04
* Mastodon 軟件由站長修改過。src = https://github.com/luzi82/mastodon , branch = hiauntie

## 其他伺服器

* 維護作業由 VM host 定期執行。src = https://github.com/luzi82/maintenance.hiauntie.com
* 用戶上傳的檔案會傳送到 Amazon S3。

## backup

* DB backup 每天凌晨 3:30
* VM backup 每週六凌晨 3:30 DB backup 後
* 用戶上載的檔案會直接傳送到 S3，不設 backup
* backup 檔經加密後在 Amazon S3 存放
