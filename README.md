# Thunderbird-MarkdownHereRevival-CSS

![S9l20zFQQFj4lBmRjBnS1671007994-1671008019](https://user-images.githubusercontent.com/36149909/207550537-d10e16a6-9a32-440c-8947-f1d49a2a5f78.gif)


Thunderbirdの拡張機能である「MarkdownHereRevival」に記述する用のCSS。GithubのCSSをゴニョゴニョしてます。

previewUrl: https://sindresorhus.com/github-markdown-css/  
cssUrl: https://sindresorhus.com/github-markdown-css/github-markdown.css

## 導入手順

1. `GFM_Light_Thunderbird_MarkdownHereRevival.css`をダウンロード
2. Minify:Selectionで1行にする
3. MarkdownHereRivivalに貼り付け

## 作成手順

VisualStudioCodeで編集しています。

1. cssUrlからCSSを取得。
2. `-ms`, `-moz`, `-webkit`のプレフィックスのついた要素を削除
3. `.xxx`等のid指定の要素を削除
4. `.markdown-body`を`body`に変更
5. `media (prefers-color-scheme: light)`の内容を代入（直書き）
6. `media (prefers-color-scheme: light)`を削除
7. `media (prefers-color-scheme: dark)`を削除
8. `body table`, `body code`に`color: #24292f;`を追加
9. 保存

## 失敗談（そのままCSSを利用できない理由）

- @mediaが機能しないメーラーが多い→テーマによる切り替え不可能
- DarkThemeは受けが悪いので標準にはできない→LightThemeを標準に
- `id`, `class`, `VendorPrefix`は使用しない→削除
- `markdown-body`という名前で使用されない→`body`に変更
- `body table`と`body code`内の文字がテーマによって見えなくなる→`color: #24292f;`を追加
- markdownHereRivival上で記述できる文字数制限がある(7,543文字は保存されなかったが7,073文字は保存された)→Minify
