# Naosunefev サイト（骨組み）

ナオスネ語公式サイトのナビゲーション骨組みです。プレーンなHTML/CSSのみで、
ビルドツールなしでそのままGitHub Pagesに置けます。

## 構成

```
naosune-site/
├── index.html        トップページ
├── about.html         言語について（世界観・共和国の紹介）
├── grammar.html        文法
├── dictionary.html     辞書（ZpDICへの導線）
├── translation.html    翻訳作品
├── work.html            創作作品
├── document.html        資料
├── diary.html           製作日記
├── css/style.css        共通スタイル
└── assets/               画像・フォントなど（現状空）
```

`index.html`以外の各ページは、まだ中身が「準備中」のプレースホルダです。
どのページに何を書くべきかは、各ページ内の「準備中：〜」の一文に書いてあります。

## GitHub Pagesでの公開手順

1. GitHubで新しいリポジトリを作成する（例：`naosune-site`）。
2. このフォルダの中身一式をリポジトリのルートに置いてpushする。
   ```
   git init
   git add .
   git commit -m "ナオスネ語サイトの骨組み"
   git branch -M main
   git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
   git push -u origin main
   ```
3. GitHubのリポジトリページで
   `Settings → Pages → Build and deployment → Source` を `Deploy from a branch` にし、
   ブランチを `main` / フォルダを `/ (root)` に設定する。
4. 数分待つと `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される。
   独自ドメインを使いたい場合は同じ設定画面の `Custom domain` で設定できる。

## 今後の拡張候補

- フォント：`naosunefev.ttf` をbase64化して `assets/` 以下に埋め込み、
  ロゴや見出しにこの言語専用の書体を使う
- 辞書ページ：ZpDICのAPIやエクスポートデータを使い、サイト内検索を実装する
- 各ページの共通ヘッダー/フッターをテンプレート化する場合は、
  静的サイトジェネレータ（例：11ty, Jekyll）への移行も検討可能
