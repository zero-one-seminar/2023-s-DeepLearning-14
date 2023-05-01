---
marp: true
header: ""
footer: "2023/04/30 ゼロイチゼミ <a href=\"https://twitter.com/nu_zero_one\" style=\"color:white\">@nu_zero_one</a>"
theme: 01dracula
paginate: true
---

<!--
headingDivider: 2
_class: title
_paginate: false
-->
# 3次元畳み込み / プーリング層
<a style="color:#eeeeee; text-decoration: none;" href="https://github.com/kentakom1213">ぱうえる（けんた）:link:</a>

## 3次元の画像とは？

![h:480](images/color_separastion.drawio.png)


## 3次元の畳み込み
3次元に拡張するとどうなる？

![h:400](images/convolution3d_1.drawio.png)

## 3次元の畳み込み
計算方法
1. **レイヤーごとに畳み込み**を行う
2. **それらの和**を求める

## 手順1
![bg contain](images/convolution3d_2.drawio.png)

<!--
_footer: ""
-->

## 手順2
- 畳み込みを行ったもの同士を足し合わせる

![bg contain](images/convolution3d_3.drawio.png)

<!--
_footer: ""
-->

## 3次元畳み込みの注意！
入力データとフィルターの**チャンネル数**が同じである必要がある
<hr>

$$
(C,H,W) \ast (C,FH,FW) \to (1,OH,OW)
$$

## 3次元畳み込みの注意！（図）
![bg](images/batch.drawio.png)

<!--
_footer: ""
-->

## 複数のフィルターによる畳み込み
![h:480](images/multi_filter.drawio.png)

## バイアス・バッチ処理
![bg contain](images/dimension.drawio.png)

<!--
_footer: ""
-->

## プーリング層


