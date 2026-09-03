# ツカイキリ — 検証用LP

[[30_Resources/プロダクト開発〜販売 手順書]] ステージ2「検証」用の1枚LP。
需要が確認できてから（ステージ3）Next.js フル構成に作り直す。ここは使い捨て前提。

## 構成（新規登録・課金・OAuthなし）
- `index.html` … 1枚完結（Tailwind CDN）。
- ウェイトリスト保存先: **Google フォーム**「ツカイキリ ウェイトリスト」
  - 編集: https://docs.google.com/forms/d/1_Eh9lLREhFj_zpcrucHU32sggOos5liqppBFhlpH0Es/edit
  - 回答: フォームの「回答」タブ（新規回答のメール通知ON）
  - `種別` entry.1045432751 = `visit`（ページ表示）/ `signup`（メール登録）
  - `メールアドレス` entry.1373306927
- ホスティング: **GitHub Pages**（リポジトリ `shin0510katayama-boop/tsukaikiri-lp`）

## 計測の見かた
- 回答スプレッドシートで `種別` 列を数える
- 訪問数 = `visit` 行数、登録数 = `signup` 行数
- **登録率 = 登録数 ÷ 訪問数**（訪問は sessionStorage で1セッション1回）

## ゲート判定（手順書より）
- 定量: 登録率 10%以上 かつ 登録 5件以上
- 定性: SNS で「欲しい/使いたい」等の意欲コメント・DM 3件以上
- どちらか一方で「進む」。※1個目なので数値は様子見
- 期間: 1〜2週間（実行日は Google カレンダー）

## 更新のしかた
- `index.html` を編集 → `git commit` → `git push` で GitHub Pages に自動反映（数十秒〜数分）
