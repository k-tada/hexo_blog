---
title: Vimmerになろう 〜Road to Vimmer〜 第3回
date: 2016-10-05 10:00:02
tags:
  - vim
categories:
  - editor
author: "k.tada"
---
# 第3回 Vimでのコピー、カット、ペースト
前回はVimでのテキスト編集方法について紹介しました。
今回はコピー、カット、ペーストの方法について紹介します。

## コピー
Vimでのコピーは、基本的にノーマルモード、ヴィジュアルモードから行います。

- ノーマルモード：単語、行のコピー
- ヴィジュアルモード：範囲を選択してコピー

のようなイメージです。

### ノーマルモードでのコピー

| キー | 移動方法 |
|---|---|
| yw | カーソル位置から単語の末尾までをコピー |
| yy | 現在の行をコピー |
| Y | 現在の行をコピー(yyと同じ) |

前回説明したテキスト編集時の`c`と似たようなイメージですね。`c`を`y`に変えるとコピーになります。
なぜ`y`なのか。Vimではコピーのことをヤンク（Yank）と呼ぶからです。
Vimではコピーは`y`。これ、頭に叩き込んでおいて下さい。

### ヴィジュアルモードへの遷移方法
次はヴィジュアルモードでのコピー方法。といきたかったのですが、まだヴィジュアルモードになる方法を紹介していませんでしたね。
ヴィジュアルモードへの遷移方法は以下のような感じです。

| キー | 移動方法 |
|---|---|
| v | 通常選択モード |
| V | 行選択モード |
| Ctrl + v | 矩形選択モード |

上述の通り、ヴィジュアルモードには3つのタイプがあります。
まずは`v`で通常選択モード。これは普通にカーソル移動で選択範囲を操作するモードです。
続いて`V (Shift + v)`で行選択モード。これは行単位の選択を行うモードです。○行目〜×行目までみたいな範囲選択に使います。
最後に`Ctrl + v`で矩形選択モード。使ってみてもらうと分かると思いますが、四角形の形で範囲選択するモードです。
基本的には上記3つのいずれかでヴィジュアルモードに遷移します。ノーマルモードに戻るにはお察しの通り`ESC`キーです。

### ヴィジュアルモードでのコピー
ヴィジュアルモードで範囲を選択して`y`を押すことで、その範囲をコピーすることが出来ます。

## カット
ノーマルモード、ヴィジュアルモードともにyのかわりにdを使うことでカットが行えます。

## ペースト
何かしらコピーした状態で`p`を押すとカーソル位置の後ろにペーストされます。`P`だとカーソル位置の前にペーストとなります。
また、行をコピーしている状態では、`p`で現在の行の次に、`P`で前の行にペーストされます。
更に、ヴィジュアルモードで範囲選択した状態で`p`を押すと選択範囲を置き換える形でペーストされます。

## まとめ
さっくりまとめてみます。

| キー | 移動方法 |
|---|---|
| yw | カーソル位置から単語の末尾までをコピー |
| yy | 現在の行をコピー |
| Y | 現在の行をコピー(yyと同じ) |
| dw | カーソル位置から単語の末尾までをカット |
| dd | 現在の行をカット |
| D | 現在の行をカット(ddと同じ) |
| p | カーソル位置の後ろにペースト（行コピーの場合は後ろの行にペースト） |
| P | カーソル位置の前にペースト（行コピーの場合は前の行にペースト） |

## 結
今回も短いですがこの辺で。
次回は検索、置換について紹介していこうと思ってます。
