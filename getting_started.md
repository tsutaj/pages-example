---
layout: default
title: Getting Started
---

# Getting Started

[GitHub Pages](https://help.github.com/ja/github/working-with-github-pages/about-github-pages) と、それに組み込まれている静的サイトジェネレータである [Jekyll](https://jekyllrb.com/) を利用して、Markdown を HTML 化してホームページを作成してみましょう。

* this unordered seed list will be replaced by toc as unordered list
{:toc}

## 準備

GitHub アカウントを持っていない人は [GitHub に登録](https://github.com/join) してください。以降、`username` というアカウントを持っているものとして説明を続けます。

### リポジトリの作成

ホームページ用のリポジトリを作ります。リポジトリ名は割と重要で、大きく分けて以下の二種類のいずれかで命名することになります。詳しくは [GitHub Pages について](https://help.github.com/ja/github/working-with-github-pages/about-github-pages) などを参考にしてください。

- `[username].github.io` (ユーザサイト)
    - この名前でリポジトリを作ると、各ページは `https://[username].github.io/` 直下にビルドされます。
    - サイトの公開元は **master ブランチしか選べない** ので注意してください。
- 上記以外 (プロジェクトサイト)
    - 例えば `repo` という名前のリポジトリを作ると、各ページは `https://[username].github.io/[repo]/` 直下にビルドされます。
    - サイトの公開元が `master` や `gh-pages` などから選べます (`gh-pages` というブランチが存在する場合、それがデフォルトで選択されます)

ここでは `homepage` というリポジトリを作成し、`gh-pages` に push することを考えます (つまり後者の方法です)

### `_config.yml` の追加

GitHub Pages で使用している静的サイトジェネレーター Jekyll の設定をするために `_config.yml` というファイルを作成します。ここで解説されている設定事項はほんの一部分ですので、もっと見たい方は [構成・設定 \| Jekyll](http://jekyllrb-ja.github.io/docs/configuration/) などを参照してください。

また、ここに書かれている内容をすべてまとめたものは [tsutaj/pages-example/\_config.yml](https://github.com/tsutaj/pages-example/blob/master/_config.yml) にあります。

#### テーマの設定

GitHub Pages において標準で用意されているテーマがいくつか存在します。一覧は [Supported themes \| GitHub Pages](https://pages.github.com/themes/) を参照してください。

ここでは `minimal` テーマを設定します。以下のように書けば終わりです。

```yml
theme: jekyll-theme-minimal
```

標準で用意されていないテーマを使用することもできます。詳しくは [Jekyll を使用して GitHub Pages サイトにテーマを追加する - GitHub ヘルプ](https://help.github.com/ja/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll) を参照してください。

#### 絵文字の表示

Jekyll には絵文字を表示する機能を持つプラグイン ([jemoji](https://github.com/jekyll/jemoji)) があります。これを import することで絵文字を表示できます :tada:

```yml
plugins:
  - jemoji
```

#### 特定ファイルをビルド対象から除外

本リポジトリには `README.md` ファイルが含まれていますが、これは HTML 化される必要がなく、ビルド対象にしたくありません。このような場合、`exclude` でビルド対象から除外したいファイルを指定することができます。

```yml
exclude:
  - README.md
```

### コンテンツの追加

試しに、本リポジトリをコンテンツとして `homepage` リポジトリの `gh-pages` ブランチに追加してビルドしてみましょう。CI と連携させるかさせないかで手順の量が少し違います。

* [Sample 1 までを追加する方法 (CI 連携なし)](./sample_001.html)
* [Sample 2 までを追加する方法 (CI 連携あり)](./sample_002.html)
