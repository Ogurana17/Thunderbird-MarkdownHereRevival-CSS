# Thunderbird-MarkdownHereRevival-CSS

Thunderbirdの拡張機能である「MarkdownHereRevival」に記述する用のCSS。GithubのCSSをゴニョゴニョしてます。

previewUrl: https://sindresorhus.com/github-markdown-css/
cssUrl: https://sindresorhus.com/github-markdown-css/github-markdown.css

## 作成手順

VisualStudioCodeで編集しています。

1. cssUrlからCSSを取得。
2. `-ms`, `-moz`, `-webkit`のプレフィックスのついた要素を削除
3. `.xxx`等のid指定の要素を削除
4. `.markdown-body`を`body`に変更
5. `media (prefers-color-scheme: light)`の内容を代入（直書き）
6. `media (prefers-color-scheme: light)`を削除
7. `media (prefers-color-scheme: dark)`を削除
8. 保存
9. Minify:Selectionで1行にする
10. MarkdownHereRivivalに貼り付け
