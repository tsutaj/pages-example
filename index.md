---
layout: default
---

## GitHub Pages Samples for Competitive Programming Advent Calendar 2019

[![Build Status](https://travis-ci.com/tsutaj/pages-example.svg?token=RTSKP4EqAJvDsfqpp8fy&branch=master)](https://travis-ci.com/tsutaj/pages-example)

**このリポジトリは [Competitive Programming (1) Advent Calendar 2019]({{ site.adc_url }}) の 12 日目の記事「[HCPC のホームページを移行した話]({{ site.adc_article_url }})」の補助資料です。**

## 本リポジトリの目的

GitHub Pages を活用した Markdown ファイルの HTML ビルドを体験していただくことが目的です。ホームページのビルド半自動化に興味を持っていただければ幸いです。

## コンテンツについて

* [Getting Started](./getting_started.html)
    - ホームページをビルドして公開するまでの手順を簡単に紹介します。
* [Sample 1](./sample_001.html)
    - 生の GitHub Pages で生成できるページの一例を紹介します。
* [Sample 2](./sample_002.html)
    - CI と組み合わせて、独自プラグインを使って Jekyll の機能を拡張します。

## ページ生成例

[HCPC 北海道大学競技プログラミングサークル](https://hcpc-hokudai.github.io/) のホームページは、GitHub Pages + Jekyll + Travis CI という構成で動いています。実際のソースコードは [hcpc-hokudai/hcpc-hokudai.github.io](https://github.com/hcpc-hokudai/hcpc-hokudai.github.io/) にて確認できます。

## 謝辞

`details` タグに関するプラグインは、[Adding support for HTML5’s details element to Jekyll](http://movb.de/jekyll-details-support.html) という記事を基に作成されました。また、Jekyll と Travis CI との連携には、[jekyll-travis](https://github.com/mfenner/jekyll-travis) を利用しました。御礼申し上げます。

## 連絡先

tsutaj (Twitter: [@\_TTJR\_](https://twitter.com/_TTJR_))
