# hirokiarashi.com

Hiroki Arashi の個人サイト。[Academic Pages](https://github.com/academicpages/academicpages.github.io) テンプレート(Jekyll)で構築し、GitHub Pages でホストしています。

公開URL: <https://1984akg.github.io/hirokiarashi.com/>

ページ構成: **About(トップ)/ CV / Research(Publications + Talks)/ Projects**

## 更新の仕方

`main` ブランチに push すると GitHub Pages が自動でビルド・公開します(数分かかります)。ローカルに Ruby や Jekyll をインストールする必要はありません。

### 発表(Talks)を追加する

`_talks/` に `YYYY-MM-DD-短い名前.md` というファイルを1つ作るだけです。Research ページと CV に自動で表示されます。

```markdown
---
title: "発表タイトル"
collection: talks
type: "Conference presentation"   # Talk / Poster / Workshop presentation など
permalink: /talks/YYYY-MM-DD-短い名前
venue: "学会・イベント名"
date: YYYY-MM-DD
location: "開催地"
---

発表者や補足の説明(本文。空でも可)。
```

### 論文(Publications)を追加する

`_publications/` に `YYYY-MM-DD-短い名前.md` を作ります。

```markdown
---
title: "論文タイトル"
collection: publications
category: manuscripts   # manuscripts(雑誌論文)/ conferences(会議論文)/ books / theses
permalink: /publication/YYYY-MM-DD-短い名前
date: YYYY-MM-DD
venue: "掲載誌・学会名"
paperurl: "https://..."   # PDF やページへのリンク(任意)
citation: "Arashi H. (YYYY). &quot;Title.&quot; <i>Venue</i>."
---

論文の説明(本文。空でも可)。
```

カテゴリの種類と見出しは `_config.yml` の `publication_category` で定義しています。

### プロジェクト(Projects)を追加する

`_portfolio/` にファイルを作ります。ファイル名の順(番号順)に表示されるため、`01-`, `02-` … の番号を付けて並び順を管理しています。新しいものを上にしたい場合は番号を振り直してください。

```markdown
---
title: "プロジェクト名(期間)"
excerpt: "一覧ページに表示される短い説明。"
collection: portfolio
---

詳細説明(本文)。
```

### CV を更新する

[_pages/cv.md](_pages/cv.md) を直接編集します(学歴・職歴・Funding・受賞・言語・スキル・資格)。
末尾の Publications / Talks / Projects は各フォルダの内容から自動生成されるので編集不要です。

### その他

- トップページの文章: [_pages/about.md](_pages/about.md)
- 名前・写真・所属・メール・SNSリンク(サイドバー): `_config.yml` の `author:` セクション
- 上部ナビゲーション: `_data/navigation.yml`
- プロフィール写真の差し替え: `images/` に画像を置き、`_config.yml` の `avatar` を変更

`_config.yml` を変更した場合、ローカルプレビュー中はサーバーの再起動が必要です(GitHub Pages 上は push だけでOK)。

## ローカルプレビュー

Docker を使うのが簡単です:

```bash
docker compose up
# http://localhost:4000/hirokiarashi.com/ を開く
```

Markdown や HTML の変更は自動で再ビルドされます(`_config.yml` の変更のみ再起動が必要)。
