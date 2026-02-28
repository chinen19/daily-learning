## Markdown
# タイトル

## 見出し

### 小見出し

**太字**

`コード`

\`\`\`ruby
# コードブロック
def hello
  puts "Hello, World!"
end
\`\`\`

- リスト1
- リスト2

1. 番号付きリスト1
2. 番号付きリスト2

[リンク](https://example.com)

![画像](画像のURL)




## よく使うコマンド
- `git status` - 変更状況を確認
- `git add .` - すべての変更をステージング
- `git commit -m "メッセージ"` - コミット
    add: 新しい機能やファイルを追加した時
    fix: バグやエラーを修正した時
`git commit -m "fix: Lintエラーをシングルクウォートに修正"`
`git commit -m "fix: Lintエラーの行の長さを修正"`
`git commit -m "fix: Lintエラーの空白を修正"`
- `git push origin ブランチ名` - プッシュ