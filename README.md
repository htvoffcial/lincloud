# LinCloud

LinCloud は、あなたの Web サイトに美しいリンク集（相互リンクなど）を簡単に埋め込むことができる JavaScript ライブラリです。

## 特徴

- **簡単導入**: わずかな JavaScript コードを追加するだけで、指定した場所にリンク集を表示できます。
- **データ管理**: リンク情報は JSON 形式で管理され、複数のユーザーや用途に応じたリンク集をトークンで切り替え可能です。
- **多言語対応**: ブラウザの言語設定に合わせて、日本語と英語の表示を自動的に切り替えます。
- **軽量・クリーン**: CSS を含んだ単一の JS ファイルで動作し、デザインも整っています。

## 使い方

### 1. スクリプトの読み込み

HTML の `<body>` 終了直前などで、LinCloud のスクリプトを読み込みます。

```html
<script src="https://cdn.jsdelivr.net/gh/htvoffcial/lincloud@main/release/lincloud-1.0.0.min.js"></script>
```

### 2. 表示場所の作成

リンク集を表示したい場所に、ID を持った空の要素（`<div>` など）を配置します。

```html
<div id="lincloud-container"></div>
```

### 3. 初期化実行

以下のコードを実行して、リンク集を表示させます。`lincloud_token` には、表示したいデータの識別子を指定します。

```javascript
lincloud_init({
    lincloud_token: "あなたのトークン（UUID）",
    node: "lincloud-container" // 表示させる要素のID
});
```

## データ構造 (userdata/lincloud.json)

リンク集の内容は `userdata/lincloud.json` で管理されています。

```json
{
  "your-token-uuid": {
    "username": "ユーザー名",
    "usericonpath": "アイコン画像URL",
    "postedtime": "2026-02-14",
    "list-linkurl": ["https://example.com", "https://example.jp"],
    "linktitle": ["サイト名1", "サイト名2"]
  }
}
```

## ライセンス

(c)2026 Haruharu Television Group or its Affiliates. All Rights Reserved.
