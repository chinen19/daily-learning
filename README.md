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


# 日付: 2026/01/1６

## 学習内容
- <%= render　が連続であると、どこを指しているのかわからないくなる

### つまずいたポイント
- HTML構文。どこの/divか、どこに<%= renderを入れるかなど理解が難しかった

## 明日やること
- つまづいたHTML構文の復習
- カリキュラムの続き


# 日付: 2026/01/17
## 学習内容
- div,endの意識
- <% end %>が必要なのはどんなときは、 Rubyのブロック(do ~ end)を使っているとき。例）form_with、each、ifなど
- <%= render 'form', board: @board %>は_form.html.erbを呼び出している
- _パーシャルを使う理由は、new.html.erbとedit.html.erbで同じフォームを使い回すため

### つまずいたポイント
- 不要なendのエラーが出てきたとき、<%  %>があれば、<% end %>はあるもんだと思い込んでいた
- エラー見ても、構文をちゃんと理解していないと解決できないので、一旦復習する必要があった

### 解決方法
- カリキュラム進めながら、わからない、つまづいているところを復習

## 明日やること
- paramsとは何か
- カリキュラム続き


# 日付: 2026/01/1８
## 学習内容
- t()は翻訳(translation)を行うメソッド
- f.submit nilは、
値がないから何も表示されないのではなく、 Railsが自動的にデフォルトの英語ラベルを表示してくれる
 新規作成なら → "Create Comment"
　更新なら → "Update Comment"

### つまずいたポイント
- １対多、多対多が文章になると理解が難しいので、技術記事を参考にしながら勉強する

## 明日やること
- カリキュラムのER図を書く

## 参考リンク
-  やさしい図解で学ぶ　中間テーブル　多対多　概念編 
 https://qiita.com/ramuneru/items/db43589551dd0c00fef9
- やさしい図解で学ぶ　ER図　表記法一覧
https://qiita.com/ramuneru/items/32fbf3032b625f71b69d



# 日付: 2026/01/２０
## 学習内容
- 用語
- GETメソッド・POSTメソッドとは
・GETメソッドはサーバからさまざまなリソースを取ってくるメソッド。リソースとはhtml/img/jsなどを指す。
・POSTメソッドはサーバへ情報を追加するメソッド
・他にもメソッドにはPUT、DELETEなども存在する
- validatesとは汎用的なバリデーション
:uniqueness重複していないこと
例）validates :email,uniqueness: true
- validates_uniqueness_of(フィールド名..)とは、属性の値が一意であることをバリデーション
※ 一意（ユニーク）とは、重複のないもの
:scopeは、一意性制約を決めるために使用する他のカラム	 
例）validates_uniqueness_of :board_id, scope: :user_id 

## 詳細メモ
- エンティティとは「実体」
E-R図で出てくる箱
- HTTPとはプロトコル（通信のルール）の一種。プロトコルは説明書のイメージ
- バリデーションとはデータを保存する前に、無効なデータでないことを検証する機能のこと

### つまずいたポイント
- 意味を忘れている用語が多く、何のことを言っているかわからなかった
- 似たようなファイルが多く、書くものを間違えていた

### 解決方法
- users,boards,bookmarksのER図書いて相互関係を考えた
- 用語を調べ直した
- 実装フェーズを見直し、ファイルに書く意味を考えた

## 明日やること
- カリキュラム続きする
- ルーティング一覧の見方を理解する

## 参考リンク
- ポート番号/NAT/NAPTの学習メモなどhttps://qiita.com/Kazuyaa/items/5fa259e94098c0d0ca2d
- Railsドキュメント
 https://railsdoc.com/page/validates_uniqueness_of
- validates_uniqueness_ofとは
https://qiita.com/kimino0525/items/109f23eff40bbd4e8b50


# 日付: 2026/01/24

## 学習内容
- 末尾の空白の有無
- ディレクトリ作成するとき、ファイルも一緒に作成しようとしない。個別で作成する。
- ブックマーク機能を作成するにあたってBookmarksControllerとBoardsControllerの違い
- アクションのeditとupdateの違い

## 詳細メモ
- ファイル末尾の改行は必要。Gitなどのバージョン管理システムが正しく動作するため
- BookmarksControllerはブックマーク情報の操作（ブックマーク作成、削除）、BoardsControllerは、掲示板の表示（全掲示板一覧、ブックマーク済み掲示板一覧）で役割で分ける。
全てBookmarksControllerに入れると、URLが /bookmarks になり、「掲示板の一覧」という意味が伝わりにくい
- editは、編集画面を表示する。データベースは変更しない。
updateは、データを更新する。

### つまずいたポイント
- 何回もLinkエラーが出ていたが空白の有無をわかっていなかった
- ファイルの違いがわかっていなかった。アクションの違いもわかっていなかったため、editとupdateを混同して考えていた

## 明日やること
- 違いを意識しながらカリキュラムを進めていく。


# 日付: 2026/01/25

## 学習内容
- Railsコンソール

## 詳細メモ
- Railsコンソールが必要な理由は、データベースを確認したい、コードが正しく動くか試したい、データの作成・更新・削除

## 明日やること
- カリキュラム継続

## 参考リンク
- [掲示板にコメント機能を実装する③](https://study-diary.hatenadiary.jp/entry/2020/08/11/231101)


# 日付: 2026/01/２８

## 学習内容
- oder
- Turbo Streams
- redirect_toを使用したい時
-　「基本的にはハイフンでつなげることが HTML の ID属性の命名規則」- flashメッセージ

## 詳細メモ
-　Turbo Streams は、HTMLの断片をリアルタイムに更新できる
代表的なアクションには、 append、prepend、replace、update、remove、before、after 
- * replace は、指定した 要素全体を置き換え
    * 例: <div id="comment-123">...</div> という要素全体を新しいものに置き換える
* update は、指定した 要素の中身だけを更新
    * 例: <div id="comment-123">ここの中身だけ</div> を更新する
- redirect_toを使用したい時
データの更新が成功したときは、HTTPリクエストを走らせて別のページに遷移する。
- renderを使用したい時
保存に失敗したときは、エラーメッセージを添えてviewを表示してやるだけでOK。無駄にリクエストを増やさないようにする。データの登録は行われていないので、リロードされても問題ない。
- orderメソッドは、並び順を変更するメソッド
並び替えの基準にはASC(昇順)とDESC(降順)の2種類があり、ASCは値が古いものから新しいのものになり、DESCはその逆で新しいものから古いものになる

app/controllers/tweets_controller.rb
〜省略〜
  def index
    @tweets = Tweet.includes(:user).order("created_at DESC")
  end
- flashメッセージとは、Webサービスにて何かの処理を行なった際に、それが正しく行われたかをユーザー側で確認できるよう、メッセージで表示させるための機能。
flash[:notice] = "ユーザーの新規登録に成功しました"
flash[:success] = "ログインに成功しました"
flash[:danger] = "コメント投稿に失敗しました"

### つまずいたポイント
- 忘れているものや、根本的にわかっていないものが多いためつまづいた

### 解決方法
- 調べたり、ロボランてくんに聞いた

## 明日やること
- コメント投稿、削除機能のajax化の復習

## 参考リンク
- [redirect_toとrenderの使い分け](https://qiita.com/s3710/items/7162c66a8b4a875d2696#:~:text=%E6%A6%82%E8%A6%81.%20Rails%E3%81%A7%20scaffold%20%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%9F%E3%82%89create%E3%82%A2%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AF%E4%BB%A5%E4%B8%8B%E3%81%AE%E3%82%88%E3%81%86%E3%81%AB%E3%81%AA%E3%82%8B%E3%80%82%20%E4%BF%9D%E5%AD%98%E3%81%AB%E6%88%90%E5%8A%9F%E3%81%97%E3%81%9F%E6%99%82%E3%81%AF%20redirect_to%20%E3%81%A7%E3%83%9A%E3%83%BC%E3%82%B8%E9%81%B7%E7%A7%BB%E3%81%99%E3%82%8B%E3%81%AE%E3%81%AB%E5%A4%B1%E6%95%97%E3%81%97%E3%81%9F%E3%81%A8%E3%81%8D%E3%81%AF,User.new(user_params)%20respond_to%20do%20%7Cformat%7C%20if%20@user.save%20format.html)
- カリキュラムの説明文
- 【初心者向けまとめ】flashメッセージの理解と実装
https://qiita.com/A__Matsuda/items/008be17d5d0659ea9dc0