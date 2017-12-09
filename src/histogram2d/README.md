# 概要

2つの入力画像から2次元のヒストグラムを作成する処理をHalide で実装しました。

# 主な仕様

- 入力0: 768 x 1280 pixel, 2次元グレースケール画像 (unit8 or unit16)
- 入力1: 768 x 1280 pixel, 2次元グレースケール画像 (unit8 or unit16)
- 出力0: 768 x 1280 pixel, 2次元グレースケール画像 (uint 32 であり、縦横のサイズが同じ)
- 処理内容:
  - 出力0 のサイズになるように正規化された、入力0 と入力1 のヒストグラムを返す
  - 出力0 のx座標は、入力0(i, j) x (出力0の幅 / UINT[8 or 16]\_MAX)で計算する。
  – 出力0 のy座標は、入力1(i, j) x (出力0の幅 / UINT[8 or 16]\_MAX)で計算する。
---
Project Name: ヒストグラム(2次元), Category: Library