---
layout: default
title: Sample 1
---

# Sample 1: CI 連携なし

自分で Jekyll の機能を拡張しない場合、CI との連携は特に必要ありません。GitHub Pages 側で勝手にビルドして HTML 化してくれるためです。

では、実際に Sample 1 までをビルドしてみましょう。

## ビルド方法

`homepage` リポジトリにおいてまだ `gh-pages` ブランチを作成していない場合は作成し、ブランチをうつしてください。

```sh
$ git checkout -b gh-pages
```

Sample 2 は CI と連携しなければビルドできないため、README に加えて Sample 2 もビルド対象から除外します。`_config.yml` の `exclude` を以下のように変更してください。

```yml
exclude:
  - README.md
  - sample_002.md
```

あとは、本リポジトリの中身を全て `gh-pages` ブランチに push しましょう。

```sh
$ git add [files]
$ git commit -m "add contents until Sample 1"
$ git push -u origin HEAD
```

うまくいけば、`https://[username].github.io/homepage/` にビルドされるはずです。Sample 2 はまだビルドしていないため、リンクを踏んでも 404 になります。

## おまけ: Markdown 記法テスト

以下は Markdown 記法テストです。主な記法を知りたい方は、[Markdown 記法 チートシート](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa) などを参考にしてください。

# 見出し 1
## 見出し 2
### 見出し 3
#### 見出し 4
##### 見出し 5
###### 見出し 6

|左揃えのサンプル|中央揃えのサンプル|右揃えのサンプル|
|:---|:---:|---:|
|テキスト|テキスト|テキスト|

* 箇条書き 1
    - 箇条書き 2
        + 箇条書き 3

1. ナンバリング 1
1. ナンバリング 2
1. ナンバリング 3

**太字** *斜体* ~~取り消し線~~

<span style="color:red;">HTML タグなどを直に書いても良いです</span>
