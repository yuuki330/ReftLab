# ReftLab

個人用 League of Legends 学習ツール集。公開URL：**https://yuuki330.github.io/ReftLab/**

現在の機能は **RIFT SCOUT（日本語対応・対面スキル検索）** です。

## RIFT SCOUT

- 日本語・ひらがな・英語・一部通称で173チャンピオンを検索
- TOP候補47体の警戒スキル・反撃条件などの対面メモ
- 自分のチャンピオン（ヨネ／ムンド）に応じた対策を切り替え、ブラウザに選択状態を保存
- Riot Data Dragonによる日本語スキル説明・射程・クールダウンの取得（インターネット接続が必要）
- **ジャックス／ヨリック／ザーヘンのQ/W/E/R動画をサイト内で試験再生**
- それ以外はMemorize LoLへのスキル動画リンク。試験再生失敗時も外部リンクへ切り替え可能
- TOP/JG絞り込み、お気に入り、スマートフォン対応

アプリ本体はルートの `index.html`。GitHub Pagesの `main` / `/(root)` から公開する静的ページです。

### 試験再生について

3チャンピオンの動画はCommunityDragonのチャンピオンデータに記載された `abilityVideoPath` の形式を元に、Riot配信CDNから再生します。**動画ファイルはリポジトリに保存しません**。

動作には通信環境・配信元のアクセス可否・ブラウザのWebM対応が必要です。配信元の仕様変更などで再生できない場合は、元動画リンクまたはMemorize LoLを使用してください。動画がブラウザ上で再生できるかは利用環境での確認が必要です。

## 今後の拡張案

- 再生テストの結果を確認して動画対象チャンピオンを拡大
- 対面相性マトリクス（レーン戦／試合全体／時間帯別）
- TOP・JGの練習メニューと振り返り
- アイテムやピック判断の学習

## 免責

非公式の個人学習用ツール。Riot GamesおよびMemorize LoLとの提携はありません。スキルの効果や数値は実際のゲーム内説明と最新パッチを優先してください。

参照：[Riot Data Dragon](https://developer.riotgames.com/docs/lol) / [CommunityDragon](https://communitydragon.org/docs/assets) / [Memorize LoL](https://www.memlol.com/)
