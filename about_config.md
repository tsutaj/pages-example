---
layout: page
title: About `_config.yml`
---

GitHub Pages の設定変更方法を簡単に解説しています。ここで説明しているものはほんの一部分ですので、もっと見たい方は [構成・設定 \| Jekyll](http://jekyllrb-ja.github.io/docs/configuration/) を参照してください。

## TL;DR

GitHub Pages のために、テーマを設定し絵文字を表示できるようにします。また、ホームページのビルドに必要ないファイルはビルド対象から除外します。

これを達成するには `_config.yml` に以下を書けば良いです。

```yml
# テーマの選択
theme: minima

# 絵文字表示のためのプラグイン
plugins:
  - jemoji

# ビルドの対象から除外するファイル
exclude:
  - README.md
```

## 解説

### テーマの変更

GitHub Pages において標準で用意されているテーマがいくつか存在します。一覧は [Supported themes \| GitHub Pages](https://pages.github.com/themes/) を参照してください。

ここでは `minima` テーマを設定します。以下のように書けば終わりです。

```yml
theme: minima
```

標準で用意されていないテーマを使用することもできます。詳しくは [Jekyll を使用して GitHub Pages サイトにテーマを追加する - GitHub ヘルプ](https://help.github.com/ja/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll) を参照してください。

### 絵文字の表示

Jekyll には絵文字を表示する機能を持つプラグイン ([jemoji](https://github.com/jekyll/jemoji)) があります。これを import することで絵文字を表示できます :tada:

```yml
plugins:
  - jemoji
```

### 特定ファイルをビルド対象から除外

本リポジトリには `README.md` ファイルが含まれていますが、これは HTML 化される必要がなく、ビルド対象にしたくありません。このような場合、`exclude` でビルド対象から除外したいファイルを指定することができます。

```yml
exclude:
  - README.md
```
