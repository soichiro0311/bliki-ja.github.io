---
layout: pofeaa
title: レコードセット
---

原文: <https://www.martinfowler.com/eaaCatalog/recordSet.html>

*テーブルデータのメモリ上での表現*

解説の全文は『PofEAA』 **508** ページを参照。

![](https://www.martinfowler.com/eaaCatalog/recordSetSketch.gif)

過去20年、データベースにおけるデータを表現するための支配的な方法は、リレーショナルなテーブル形式だった。大小のデータベースベンダや標準の問い合わせ言語に指示されたことで、新しい開発は全てリレーショナルデータを用いているように見える。

この上位層には、UIを素早く構築するためのツールが豊富にある。このデータを強く意識したUIフレームワークは、ベースとなるデータがリレーショナルであるという事実に依存し、また様々な種類のUIウィジェットを提供することでプログラミングをしないでも簡単にこのデータを表示したり操作できるようになる。

こうした状況の悪い面は、データの表示や単純なデータ更新を驚くほど容易にしている一方で、ビジネスロジックを配置するインフラが用意されていない、ということだ。"正しい日付"以上のバリデーションやビジネスルール、計算処理を実行する隙間が用意されていないのだ。そのため、ストアドプロシージャとしてデータベースに埋め込まれるか、あるいはUIコードとごっちゃになってしまうのだ。

このRecord Setというアイデアは、SQL問い合わせ結果のように正確に見え、システム上の他の部分から生成したり操作したりが可能なメモリ上のデータ構造を提供することでケーキを与え食べてもらおうということなのである。

(translated by money@andore.com)
