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

## MY CHAMPION — ヨネの練習（試作）

画面上部の **「ヨネの練習」** タブから利用できます。対面検索とは独立した画面で、YouTube公式埋め込みプレイヤーの時間指定再生を使用します。動画ファイルをリポジトリへ転載・保存しません。

- **基本コンボ 6区間**：通常攻撃とQのつなぎ、Q3からのトレード、Q3 → R、E → Q3 → R、Eの立ち位置、Q3フラッシュ
- **ヨネ vs ジャックス 2区間**：高レート試合の序盤を見ながらCS位置やJaxのQ/E使用状況を観察
- **ヨネ vs ヨリック 2区間**：同様にEの射線、召喚物、Wの檻、ヨネの帰還位置を観察
- 各区間に「何を見る？」「どう使う・練習する？」の説明、元のYouTubeへのリンクがあります。
- メニューを切り替えると前の動画を止め、次の区間を選択できます。

### 動画ソースと内容検証の範囲

| 収録範囲 | 動画・公開年 | 動画区間 |
|---|---|---|
| コンボ | [Flügerl / ULTIMATE Yone Guide](https://www.youtube.com/watch?v=f_M6faixOsU)（2020年） | 投稿者によるチャプター情報に基づく6区間（00:04〜01:46の一部） |
| vs ジャックス | [domisumReplay: Yone / KR Grandmaster](https://www.youtube.com/watch?v=-sjPdpgGwOU)（2025年、パッチ25.19） | 00:30〜03:40、03:40〜07:10 |
| vs ヨリック | [domisumReplay: Yone / KR Master](https://www.youtube.com/watch?v=kRHdLq4RJ7A)（2025年、パッチ25.8） | 00:30〜03:40、03:40〜07:10 |

**重要**：対面の4区間は、フルマッチから時間で切り出した「観察用の抜粋」です。該当区間に具体的なスキル使用・成功した駆け引きが含まれるか、プレイヤーがなぜ判断したかは未確認です。解説は動画の事実認定ではなく、観察してほしい観点と練習仮説です。

コンボ動画は2020年のもので、現在のパッチと細かな仕様が異なる可能性があります。最新のゲーム内情報を優先し、練習ツールでも再現を確認してください。

YouTube側で埋め込みを無効にしている場合やブラウザで再生できない場合は「YouTubeで元動画を見る」を使用してください。YouTube APIキーやサーバーは不要です。

## 今後の拡張候補

- ヨネ練習動画の高品質な対面シーンの確認・追加、ムンドなど他の持ちチャンピオンへの拡張
- 対面相性表（レーン・試合全体・時間帯別の評価）
- JG対面メモの拡充
- 座学・試合ごとの練習記録と振り返り

## 注意事項

非公式の個人学習用ツールであり、Riot Games・CommunityDragon・Memorize LoLとは提携していません。対面メモは一般的なスキル特性からの学習用要約で、実際のパッチ・ゲーム内仕様を優先してください。

参考：[Riot Data Dragon](https://developer.riotgames.com/docs/lol) / [CommunityDragon](https://communitydragon.org/docs/assets) / [Memorize LoL](https://www.memlol.com/)
