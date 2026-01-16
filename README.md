# Today I Learned

## 2026年01月13日
- Gitの基本操作について学習
- RUNTEQのカリキュラムでRails基礎を学習中



# 日付: 2024/01/1４

## 学習内容
- <% %>　：変数の定義などに使用する
- <%= %>　：変数の値など処理するために使用する
どちらも画面には表示されない
- <%= render 、、、で_board.html.erbを呼び出している

## 詳細メモ

### つまずいたポイント
- それぞれのファイルがどの役割をしているか曖昧だった
- docker compose exec web rails sとdocker compose exec web bin/devの違いがわからなかった


## 明日やること
- 「タイトルを動的に出力する」一問一答で自分の理解力を確認する
- t('.title')と@board.titleの違いを理解する
-docker compose exec web rails sとdocker compose exec web bin/devの違いをまとめる

## 参考リンク
https://qiita.com/natsumi_23/items/42f4b075e417aaf925df


# 日付: 2024/01/15

## 学習内容
-　前回の復習
- t('.title') は、ログイン、一覧など、ページの種類ごとに固定のタイトル 
@board.title は、詳細ページなど、表示する対象によってタイトルが変わる （Aさんの、、、）
-  CRUD機能
create：データを新規作成し、データベースへ保存
Index：データ一覧を表示
show：データの読み込み
new：データを新規作成するためのフォームを表示する
edit ：データを編集
update：データの更新
destroy：データの削除

### つまずいたポイント
- CRUD機能のそれぞれの意味を理解していなかったので、繋がりがわからなかった
- 編集機能のCRUD機能のコマンドの意味
- <% end %> の閉じタグの位置

### 解決方法
- 調べてまとめた
- HTML構文を復習

## 明日やること
- カリキュラムの続きをする

## 参考リンク
- https://qiita.com/TK1422/items/5b6e25cf1d0a16163337
-  https://qiita.com/okamoto_ryo/items/6bcc49cc0cbcb55f93da
- https://zenn.dev/iranorih/articles/753c7d14d9c4b3
- https://www.youtube.com/watch?v=1BufFqTbhyU
-https://school.learning-next.app/docs/rails/rails_basic/edit-update


# 日付: 2024/01/1６

## 学習内容
- <%= render　が連続であると、どこを指しているのかわからないくなる

### つまずいたポイント
- HTML構文。どこの/divか、どこに<%= renderを入れるかなど理解が難しかった

## 明日やること
- つまづいたHTML構文の復習
- カリキュラムの続き

