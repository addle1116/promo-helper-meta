# promo-helper-meta
Promo helper published metadata.

## 發版 SOP（三步，順序不能反）

1. `npm run build:win` 產出安裝檔（repo：promo-helper 的 app/）。
2. 本 repo 開 GitHub Release，上傳 `promo-helper-<版本>-setup.exe`。
3. 改 `latest.json` 的 `version` 為新版本號後 push——**最後做**：先有檔可下載，才通知舊版用戶。

App 內「檢查更新」讀 `latest.json`（raw URL 燒在 `app/src/shared/updates.ts`）；
「前往下載」開本 repo 的 Releases 最新頁（同檔硬編碼，不吃 latest.json 內容）。

## 序號撤銷（既有）

`revoked.list`＝簽章撤銷清單，由 keygen `publish` 產出後 push 覆蓋（SOP 見主 repo `tools/keygen/README.md`）。
