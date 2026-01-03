# 概要ページ

## 見出し2

### 見出し3

#### 見出し4

markdownサンプル文章です。ここは地の文です。

markdownでは、箇条書きは*や-などの記号を文頭に置くことで記述します。箇条書きの階層は行頭スペース4つを足します。

- これはひとつめの箇条書き
- ふたつめの箇条書き
    - 一つ階層が深い箇条書き
- みっつめの箇条書き

### コード

3つのバッククォート記号でくくることで、コード例を示します

```
[ozuma@vpscon ~]$ cp a
cp: missing destination file operand after `a'
Try `cp --help' for more information.
```

markdown形式については、Wikipediaなども参照ください
- http://ja.wikipedia.org/wiki/Markdown

### mkdocsをdockerで使う
- ローカルで表示する：http://localhost:8000 にアクセスして確認できます。
  ```
  docker run --rm -it -p 8000:8000 -v `pwd`:/docs squidfunk/mkdocs-material
  ```
- 静的ファイルを生成する：./site 内に生成されます。(Gitで管理する必要はなし)
  ```
  docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
  ```

### Github Pagesで公開
- push時に公開するようにGitHub Actinonsを構成します。
  https://github.com/abcdeu/doc-site/blob/159e5c7046863d2740ab7c8d1de20f9591dc89ba/.github/workflows/mkdocs.yml
- GitHub Pagesを有効化します。
  1. Settings -> Pages
  2. Sources -> Deploy from a branch
  3. Branch -> gh-pages /(root)
  4. Saveボタンをクリック
- GitHub Pagesのリンクを作成
  1. Code -> About -> 歯車アイコンをクリック
  2. `Use your GitHub Pages website`をチェック

### リンク集
- https://qiita.com/grhg/items/eb2935ba815db16a16a4#4-github-pagesを設定する
- https://zenn.dev/mebiusbox/articles/81d977a72cee01
