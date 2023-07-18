# README

## 環境構築
```
$ bundle install --without=production
$ bin/rails db:setup
$ yarn install
$ bin/webpack
$ bin/rails s
```

## 事業をエンジニアリングしよう提案編の回答は以下に記述してください
選択した事業側の課題
サービス登録者数の内、男性60%に対して、女性は40%。一方で、サービス内のもくもく会に参加した人の比率は、男性90%：女性10%と大きな差が出ています。もっと女性が使いやすいようなサービス設計にする必要があるのではないか？
提案内容
女性専用のもくもく会の開催をできるようにする
→ 現状どのような方が主催であるかが不透明のため、女性が参加しにくいもくもく会になっているとこが考えられる。
実装方針
・ユーザー登録時、gender項目を追加。（入力方式ではなく、選択式）
・もくもく会の作成時に、性別制限をかけることができる様にする。（誰でもOK、男性専用、女性専用の３択を選択式）
・イベント詳細に女性又は男性専用のもくもく会であることの表示を作成。
・男性ユーザーのもくもく会一覧画面に女性専用は表示されないよう設定。
・女性ユーザーのもくもく会一覧画面に男性専用は表示されないよう設定。
・検索フォームで女性専用又は男性専用も検索できるよう、条件を追加。