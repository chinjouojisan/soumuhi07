# 決算チャレンジ 総務費編 — 納品ファイル一式

## 内容
- `index_soumu.html` — 本体(単一HTML、カコモ画像・全データ埋め込み済み、196KB)
- `manifest.json` — PWA用マニフェスト(新規作成)
- `sw.js` — Service Worker(新規作成)
- `soumu_quiz_all.md` — クイズ・トリビア48問の内容一覧(レビュー用)

## 公開前に必要な作業
1. `index_soumu.html`を`index.html`にリネームし(同梱のファイルは既に`index.html`名です)、manifest.json・sw.js・アイコン一式(icon-192.png/icon-512.png/apple-touch-icon.png)・og-image.pngと同じフォルダに配置してください。アイコン・OGP画像は本納品に同梱済みです。
2. `<head>`内のOGPタグ(og:image, og:url, twitter:image)を実際の公開URL(例: `https://kakogawa-giin-map.com/kessan-challenge/soumu/`)に合わせて書き換えてください(該当箇所は`<!-- ▼▼ 公開先のURLに合わせて書き換えてください ▼▼ -->`とコメントしてあります)。

## データの中身
- 全29事業、決算資料(kessansho/kessan_meisai/seika_houkokusho/元PDF)から構築
- クイズ48問(基礎知識5+予算vs決算29+特別トリビア14)、すべて2択形式
- 法定事業2件(参議院議員選挙事業・国勢調査事業)、裁量事業27件に分類
- localStorageキーは`kessan_challenge_soumu_v1`(民生費とは独立して進捗保存)
- 支払先明細は各事業上位40件まで(容量対策)

## 民生費編との差分・総務費特有の注記
- 総務費は民生費と異なり、内訳(委託料等)と実績(利用者数等)が対応しない事業が多く、定性的な取り組み内容(工事の目的・場所など)は「内訳の補足」として別枠表示にしています(民生費テンプレートにこのセクションを追加)
- AI視点の「気になる点」トリビア4問を含みます(かわまちづくり推進事業の認知度低下、自治振興事業のアドバイザー派遣数減少、ICT事業のベンダー集中、ウェルネス協会への複数事業合算依存)
