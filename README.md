# Toughness Baldwin Legal Pages

GitHub Pages で公開する Toughness Baldwin の法務・サポートページ。

## 公開URL(セットアップ後)

- トップ: https://hikakinhouse3.github.io/toughnessbaldwin-legal/
- 利用規約: https://hikakinhouse3.github.io/toughnessbaldwin-legal/terms/
- プライバシーポリシー: https://hikakinhouse3.github.io/toughnessbaldwin-legal/privacy/
- 特定商取引法表記: https://hikakinhouse3.github.io/toughnessbaldwin-legal/tokushoho/
- サポート: https://hikakinhouse3.github.io/toughnessbaldwin-legal/support/

## ファイル構成

```
toughnessbaldwin-legal/
├── index.html              ← トップ
├── style.css               ← 共通スタイル(ライト/ダーク対応)
├── terms/index.html        ← 利用規約
├── privacy/index.html      ← プライバシーポリシー
├── tokushoho/index.html    ← 特定商取引法表記
└── support/index.html      ← サポート + FAQ
```

各ページは独立しており、ページ間のリンクはありません(過去アプリと同じ方針)。

## GitHub Pages での公開手順

### 1. リポジトリ作成
1. GitHub にログイン
2. 右上の「+」→「New repository」
3. Repository name: `toughnessbaldwin-legal`
4. Public を選択
5. README は追加しない(後でアップロードするため)
6. Create repository

### 2. ファイルのアップロード
1. 「uploading an existing file」リンクをクリック
2. このフォルダ内の全ファイル・フォルダをドラッグ&ドロップ
   - `index.html`
   - `style.css`
   - `terms/index.html`
   - `privacy/index.html`
   - `tokushoho/index.html`
   - `support/index.html`
   - `README.md`
3. Commit changes をクリック

### 3. GitHub Pages を有効化
1. リポジトリの **Settings** タブを開く
2. 左メニュー **Pages** をクリック
3. **Source** で **Deploy from a branch** を選択
4. **Branch** で **main** / **/ (root)** を選択
5. **Save** をクリック
6. 数分待つと、ページが公開されます

### 4. 公開確認
ブラウザで以下にアクセスし、表示されることを確認:
- https://hikakinhouse3.github.io/toughnessbaldwin-legal/
- https://hikakinhouse3.github.io/toughnessbaldwin-legal/terms/
- https://hikakinhouse3.github.io/toughnessbaldwin-legal/privacy/
- https://hikakinhouse3.github.io/toughnessbaldwin-legal/tokushoho/
- https://hikakinhouse3.github.io/toughnessbaldwin-legal/support/

## App Store Connect での設定

App Store にアプリを登録する際、以下のフィールドにURLを設定:

| フィールド | URL |
|---|---|
| プライバシーポリシー URL | `https://hikakinhouse3.github.io/toughnessbaldwin-legal/privacy/` |
| サポート URL | `https://hikakinhouse3.github.io/toughnessbaldwin-legal/support/` |
| 利用規約 URL | `https://hikakinhouse3.github.io/toughnessbaldwin-legal/terms/` |
| マーケティング URL(任意) | `https://hikakinhouse3.github.io/toughnessbaldwin-legal/` |

特商法のURLは App Store Connect の必須項目ではありませんが、アプリ内のPaywall・設定画面から参照できるように、アプリ内のリンクからアクセス可能にすると審査がスムーズです。

## アプリ内からのリンク先設定

すでに `PaywallView.swift` および `SettingsView.swift` に以下のURLを記載済みです:

```swift
Link("利用規約", destination: URL(string: "https://hikakinhouse3.github.io/toughnessbaldwin-legal/terms")!)
Link("プライバシーポリシー", destination: URL(string: "https://hikakinhouse3.github.io/toughnessbaldwin-legal/privacy")!)
```

GitHub Pages の URL パターンと一致しているので、特に修正は不要です。

## 公開後の確認チェックリスト

- [ ] 5ページすべてがブラウザで正しく表示される
- [ ] ライト/ダークモードの切り替えで自動的に色が変わる(macOS の Safari でも確認可能)
- [ ] スマートフォンで表示が崩れない
- [ ] アプリ内のリンク(設定画面 → 利用規約など)が正しく開く

## 修正が必要になった場合

GitHub のWeb UIで該当ファイルを編集 → Commit changes で即座に反映されます(数分かかる場合あり)。

## 注意点

### 特商法の住所・電話番号
特定商取引法上、本来は住所・電話番号の表記が必要ですが、「請求があったら遅滞なく開示します」と記載することで省略可能という運用が一般化しています。本テンプレートもこの方式を採用しています。

ユーザーから情報開示の請求があった場合は、メールで本名・住所・電話番号を通知できる準備をしておいてください。

### 著作権
本ページは Toughness Baldwin 専用のテンプレートです。他アプリで流用する際は、アプリ名・サブスクリプション内容等を必ず書き換えてください。
