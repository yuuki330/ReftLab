# ReftLab

個人用 League of Legends 学習ツール集。公開先：**https://yuuki330.github.io/ReftLab/**

## RIFT SCOUT — 対面チャンピオンのスキル検索

- 日本語・ひらがな・英語・一部通称で173体のチャンピオン名を検索
- TOP候補47体の警戒スキル・反撃条件などの対面メモ
- 使用チャンピオンの選択（ヨネ／ムンド）と個別対策の表示切り替え
- Data Dragonの日本語スキル説明・射程・クールダウン
- **全173体を対象として、Q/W/E/Rのスキルプレビュー動画をページ内で再生**
- 動画未提供・取得エラー・再生不可の場合はMemorize LoLへのリンクで確認
- TOP/JG絞り込み、お気に入り、スマートフォン対応

GitHub Pagesで `main` / `/(root)` を公開しています。アプリ本体は `index.html`（静的HTML/CSS/JavaScript）です。

### 動画の仕組み

CommunityDragonが提供する [champion-summary.json](https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champion-summary.json) からチャンピオンの数値IDを特定し、各チャンピオンJSONに収録された `spells[].abilityVideoPath` を読み取ります。そのパスをRiot配信CDN（`d28xe8vt774jo5.cloudfront.net`）に接続して、ページ内のHTML5動画プレイヤーで再生します。

- **対象は全173体**ですが、動画の提供状況はスキル・チャンピオンごとに異なります。
- 動画ファイルの転載・GitHubリポジトリへの保存はしません。再生時に外部CDNへ接続します。
- 以前ブラウザで再生確認したジャックス・ヨリック・ザーヘンは、動画パス取得に失敗しても従来のプレビューURLを使います。
- データ取得にはブラウザからCommunityDragonへアクセスできることが必要です（CORS・通信環境の影響を受けます）。
- ブラウザ側での全173体の再生テストは未実施です。データに動画パスがないスキルは外部リンクを利用してください。

## MY CHAMPION — ヨネの練習（2026年教材へ更新）

画面上部の **「ヨネの練習」** タブから利用できます。動画ファイルのダウンロード・保存は行いません。

### 収録内容

| 教材 | 件数 | 情報源・公開時期 | 再生方法 |
|---|---:|---|---|
| 基本コンボ・操作練習 | 3 | [Mobalytics Yone Combos](https://mobalytics.gg/lol/champions/yone/combos)、Season 26の掲載内容 | **Mobalyticsで動画を開く**（個別動画の埋め込みURL未確認） |
| 2026年版ヨネ総合ガイド | 1 | [Raksi / Guide to Yone 2026](https://www.youtube.com/watch?v=g1ge0c2umPs)、2026-02-20公開 | YouTubeをサイト内埋め込み（動画全編・コンボの該当秒数は未確認） |
| ヨネ vs ジャックス | 2 | [Yone Challenger Replays / KR Master Patch 26.17](https://www.youtube.com/watch?v=r-V6jzDhlfg)、2026-08-28公開 | **00:51 First Blood、02:01 catches Jax** の投稿者タイムラインに合わせて再生 |
| ヨネ vs ヨリック | 2 | [Challenger Replays / KR Master Patch 26.03](https://www.youtube.com/watch?v=8WMdro8aCTk)、2026-02-13公開 | **01:37 Gameplay、15:16 SOLO KILL** の投稿者タイムラインに合わせて再生 |

**合計8教材**。以前使っていた2020年のコンボ動画・2025年の対面動画はメニューから除外しました。

### 確認できた事実と未確認事項

- 各2026年YouTube動画のタイトル・公開日・投稿者が指定したイベント時刻は外部情報で確認しています。
- **指定イベントの前後で何が起こるかを学ぶための観察区間**です。ジャックスEの使用秒数や、相手の行動を見て判断した理由までは映像で個別検証していません。
- Mobalyticsの「Season 26」はページの掲載内容であり、**個々の動画が2026年に撮影された証拠ではありません**。現時点で個別動画をReftLab内に埋め込む方法は確認できないため、公式ページへ案内します。
- YouTubeの2026年総合ガイドは全編再生です。コンボが登場する個別の時刻は未特定です。
- 2026年に公開された動画でも現在のパッチ26.22とは差があるため、練習ツールとゲーム内説明で操作を確認してください。
- YouTube側が埋め込み再生を許可しない場合は「元の動画・教材を開く」を使ってください。

## 今後の拡張候補

- ヨネのコンボ個別動画をページ内再生できるソースの確保、対面シーンの映像検証、ムンドなど他の持ちチャンピオンへの拡張
- 対面相性表（レーン・試合全体・時間帯別の評価）
- JG対面メモの拡充
- 座学・試合ごとの練習記録と振り返り

## 注意事項

非公式の個人学習用ツールであり、Riot Games・CommunityDragon・Memorize LoLとは提携していません。対面メモは一般的なスキル特性からの学習用要約で、実際のパッチ・ゲーム内仕様を優先してください。

参考：[Riot Data Dragon](https://developer.riotgames.com/docs/lol) / [CommunityDragon](https://communitydragon.org/docs/assets) / [Memorize LoL](https://www.memlol.com/)
