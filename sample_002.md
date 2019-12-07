---
layout: default
title: Sample 2
---

# Sample 2: CI 連携あり

突然ですが、以下の「ここをクリック」と書かれている箇所をクリックしてみてください。隠されていたコンテンツが表示されるようになるはずです。

{% details ここをクリック %}
これは隠されたコンテンツです。「ここをクリック」を押すことで表示されたはずです。「ここをクリック」をもう一度押すと、再び隠れます。
{% enddetails %}

この機能は Jekyll に備わっている機能ではなく、自分で追加したプラグインによって実現されています。これを使うと Jekyll をどんどん拡張できるようになります。

しかし、セキュリティの観点から GitHub Pages では自分で追加したプラグインをビルドしてくれません。これでは困るので、CI (継続的インテグレーション) を活用してプラグインも使えるようにしてみましょう。

## Travis CI の活用

まず、自分が利用している GitHub アカウントの情報をもとに、[Travis CI](https://travis-ci.com) へアクセスして登録を済ませてください。

