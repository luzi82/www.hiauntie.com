# BOT.hiauntie.com 網絡狀態監視

## 簡介

* 2018年4月11日，所有 mastodon.social 的文章沒有流到其他 instance。原因不明。後來問題消失，但官方沒有作出任何聲明，甚至絕大部份人都不知道有這件事。
* 現時 Mastodon 系統幾乎沒有方法監視整個 Mastodon 網絡的狀況。即使發生以上問題，眾站長依然會被矇在鼓裡。
* 本 bot 的目的，就是對各 Mastodon 的狀況作出監視。若發現異常情況，就會發出通告。

## 公告帳號

* [@micmb@hiauntie.com](https://hiauntie.com/@micmb)
* [@micmb@mastodon.social](https://mastodon.social/@micmb)

## 測試帳號

* @ftjhsyyoks@hiauntie.com
* @VREMJUOU@mastodon.hk
* @ojarvmkrrb@mastodon.social
* @FOBRPBGR@notfound.work
* @JXBOTZSM@pawoo.net

## 原理

* 測試帳號每 15 分鐘發文，並檢查能不能收到其他測試帳號的文章。
* 如果其中一個測試帳號在一小時內收不到另一個測試帳號的文章，公告帳號就會發出警告。
* 為免消耗伺服器容量，所有文章都會在 2 小時後被刪除。
* src: https://github.com/luzi82/mastodon_instances_connection_monitor_bot
