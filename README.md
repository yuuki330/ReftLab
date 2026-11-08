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

## 今後の拡張候補

- 対面相性表（レーン・試合全体・時間帯別の評価）
- JG対面メモの拡充
- 座学・試合ごとの練習記録と振り返り

## 注意事項

非公式の個人学習用ツールであり、Riot Games・CommunityDragon・Memorize LoLとは提携していません。対面メモは一般的なスキル特性からの学習用要約で、実際のパッチ・ゲーム内仕様を優先してください。

参考：[Riot Data Dragon](https://developer.riotgames.com/docs/lol) / [CommunityDragon](https://communitydragon.org/docs/assets) / [Memorize LoL](https://www.memlol.com/)
