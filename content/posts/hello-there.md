+++
title = 'Hello There'
date = 2024-02-25T21:00:00+09:00
draft = false
+++

去年学んだことをきちんと文章に起こしてみるということをあまりしなかった。
このアウトプットをするかしないかはソフトウェアエンジニアとして成長していくスピードを大きく左右するという確信があるので今更ながら始めたい。

## 今日やったこと
* [レンダーとコミット](https://ja.react.dev/learn/render-and-commit)あたりを読んだ
useStateの挙動を復習で読みテスト問題を解いた。
stateはread onlyである。またスナップショットである。
setStateはqueueで処理され、batch実行される
stateはスナップショットであるのでsetStateで複数回変更しても同じ値で処理される。
次回のレンダーで順に処理されていく。
なおsetState(n=>n+1)みたいに関数を渡すと前回の実行を加味して処理を行うことができる。
よって
1. setState(n=>n+1)
2. setState(n=>n+1)
と繰り返せばインクリメンタルな処理を実現できる。

* [suspense handson by uhyo](https://zenn.dev/uhyo/books/react-concurrent-handson)を読んでsuspenseを調べた。
やはりpendingをthrowして示すというのが違和感を感じて腑に落ちなかった。そういうものなのだろうか。
skeltonの実装1つとっても迷いが生じて止まってしまった。