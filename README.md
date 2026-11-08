# my-lol-app

個人用 League of Legends 学習ツール集。現在は **RIFT SCOUT（日本語対応・対面スキル検索）** を公開準備中です。

## RIFT SCOUT

- 日本語・ひらがな・英語・一部通称でチャンピオン検索
- 173体の名前データと、主要TOP対面の警戒スキル／反撃の条件／ヨネ・ムンド視点のメモ
- Riot Data Dragon による日本語スキル説明・射程・クールダウンの取得（ネット接続が必要）
- Memorize LoL へのスキル動画リンク
- TOP / JG の絞り込み、お気に入り、スマートフォン対応

アプリ本体はリポジトリ直下の `index.html`。サーバー、ビルド、APIキーは不要です。

## GitHub Pages の公開設定

1. GitHub の **Settings → Pages** に移動。
2. **Build and deployment → Source** で **Deploy from a branch** を選択。
3. Branch を **main**、フォルダーを **/(root)** とし、**Save**。
4. 公開が完了したら `https://yuuki330.github.io/my-lol-app/` にアクセス。

公開状況は GitHub Pages の設定画面でも確認できます。

## 今後の拡張案

- 対面相性マトリクス（レーン指標／試合勝率／時間帯別の戦い方）
- チャンピオン別のピック判断とアイテム学習
- TOP・JG の座学、練習メニュー、試合振り返り

今後の機能追加に合わせてページ構成を拡張する想定です。

## 注意事項

- 動画は外部サイト Memorize LoL で再生します。動画の埋め込みや転載はしません。
- スキル説明・射程などは元データの仕様や取得状況により不完全なことがあります。
- 試合中の判断は実際のゲーム内説明および最新パッチ情報を優先してください。
- Riot Games／Memorize LoL の公式アプリではありません。

参考：[League of Legends 公式チャンピオン一覧](https://www.leagueoflegends.com/ja-jp/champions/) ・ [Riot Data Dragon](https://developer.riotgames.com/docs/lol) ・ [Memorize LoL](https://www.memlol.com/)
