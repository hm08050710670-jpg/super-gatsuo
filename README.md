# スーパーガツオ（SUPER GATSUO）

エビスゴルフガッツのブラウザゲーム。1ファイル（`index.html`）だけで動く横スクロールアクションです。
スマホ（タッチ操作）とPC（キーボード）の両方に対応しています。

## 遊び方

| 操作 | PC | スマホ |
|---|---|---|
| 移動 | ← → | ◀ ▶ |
| ジャンプ | Z / Space | A |
| ダッシュ・ファイアボール | X / Shift | B |
| スタート・ポーズ | Enter | START |
| 音のオン／オフ | M | おと |

- Gブロックを下から叩くとコイン・おにぎり・トマトが出ます
- おにぎりで大きくなり、トマトで炎をまとってファイアボールが撃てるようになります
- 全9ステージ（3ワールド×3）、各ワールドの最後はボス戦

## 裏技（タイトル画面で）

| 操作 | 効果 |
|---|---|
| ◀ を押しながら A | 全ステージを選べるようになる（3-3 を選ぶと最終決戦のオオイノシシ戦から炎の状態でスタート） |
| B を押しながら ▶ を7回 | 3-3 の最終決戦（オオイノシシ）から炎の状態でスタート |
| B を押しながら ◀ を7回 | エンディングを見る |
| B を押しながら START | エンディングを見る |

PCでは A = Z、B = X、START = Enter です。

## GitHub Pages で公開する手順

1. GitHub で新しいリポジトリを作る（例：`super-gatsuo`、Public）
2. このフォルダの中身（`index.html`、`README.md`、`.nojekyll`）をリポジトリにアップロードする
   - ブラウザから：リポジトリの「Add file → Upload files」でドラッグ＆ドロップ → 「Commit changes」
   - コマンドから：下の「git で上げる場合」を参照
3. リポジトリの **Settings → Pages** を開く
4. 「Build and deployment」の Source を **Deploy from a branch** にし、Branch を **main / (root)** にして Save
5. 1〜2分待つと `https://<ユーザー名>.github.io/super-gatsuo/` で遊べます

### git で上げる場合

```bash
cd super-gatsuo
git init
git add .
git commit -m "スーパーガツオ 初回"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/super-gatsuo.git
git push -u origin main
```

## 更新するとき

`index.html` を差し替えて再アップロード（またはcommit & push）するだけです。
GitHub Pages は数分で自動的に新しい版に切り替わります。

## ファイル構成

```
super-gatsuo/
├── index.html   ゲーム本体（画像・音・ロゴもすべてこの中に入っています）
├── README.md    この説明
└── .nojekyll    GitHub Pages 用の設定ファイル（中身は空でOK）
```

## メモ

- ハイスコアと進行状況はブラウザに保存されます（別の端末・ブラウザには引き継がれません）
- フォントは Google Fonts（DotGothic16 / Press Start 2P）を読み込みます。オフラインでも動きますが、文字の見た目が変わります
