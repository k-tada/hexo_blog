---
title: Vimmerになろう 〜Road to Vimmer〜 第5回
date: 2016-10-05 10:00:04
tags:
- vim
author: "k.tada"
draft: true
---
# 第5回 テキストオブジェクト
前回はVimでの検索、置換の方法について紹介しました。
今回はVimの素晴らしい機能の１つである**テキストオブジェクト**について紹介します。

## テキストオブジェクトとは
Vimでは、特定のルールに基づいてテキストを一かたまりとして扱うことが出来ます。

特定のルールには、例えば、

- 単語
- 括弧で囲われた範囲
- 文字列として`"`や`'`で囲われた範囲
- HTMLのタグ

といったようなものがあります。

例えば、以下のようなコードがあったとします。
```
function ( hoge, fuga ) {
  const piyo = "This is Piyo";
  return hogehoge( hoge, fuga, piyo );
}
```



