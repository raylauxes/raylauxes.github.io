# 深層学習day2レポート(CNN)

![Image](/bnr_jdla.png)
http://study-ai.com/jdla/

## 00:00:00- アジェンダ
![Image](/深層学習day2_00h00m03s.png)

## 00:00:16- 深層学習全体層の復習　学習概念
```
学習の流れ
1、入力層に値を入力
2、重み、バイアス、活性化関数で計算しながら値が伝わる
3、出力層から値が伝わる
4、出力層から出た値と正解値から、誤差関数を使って誤差を求める
5、誤差を小さくするために重みやバイアスを更新する
6、1~5を繰り返すことにより、出力値を正解値に近づけていく
```


## 00:03:30- 深層モデルのための学習テクニック
### Section1) 勾配消失問題について
#### 全体像（前回の流れと課題全体像のビジョン）
```
元々一個だけの中間層をどんどん増やしていこう！
```

```
誤差逆伝播法の復習：あるW成分であるwjiの求め方
```
![Image](/深層学習day2_00h18m51s.png)
![Image](/深層学習day2_00h19m20s.png)
> 実演リンク：[1_3_stochastic_gradient_descent.ipynb](https://drive.google.com/file/d/1kk-V9IHIyR4rNG-Li-Ih5aqeiYDekAhN/view?usp=sharing)

> 1_3_stochastic_gradient_descent.ipynbの「backward」関数を参照


####  00:25:10- なぜ勾配消失問題が起きるのか
```
微分した結果が0~1ので、乗算したらどんどん小さくなる。
※シグモイド関数の結果は最大でも0.25である。
```
![Image](/深層学習day2_00h26m09s.png)

```
勾配消失の解決法
1、活性化関数の選択
2、重みの初期値設定
3、バッチ正規化
```

#### 00:34:40- 1-1 活性化関数
```
ReLU関数（今最も使われている活性化関数）：0以下の入力を0にする
※勾配消失問題を回避できる
※スパース化：必要な場所だけ抽出する
```

#### 00:40:05- 1-2 初期値の設定方法
```
重みの初期値の設定により勾配消失問題を解消
設定手法の１つ：Xavier
```
```
Xavier初期化の効果を見てみよう！
```
![Image](/深層学習day2_00h52m21s.png)
![Image](/深層学習day2_00h53m27s.png)
![Image](/深層学習day2_00h53m45s.png)


##### 00:56:00- He初期化
```
He初期化（活性化関数：Relu関数）
```
![Image](/深層学習day2_00h58m48s.png)


##### 01:05:00 確認テスト
```
Q:重みの初期値に0を設定すると、どのような問題が発生するか。
A:重みを0で初期化すると正しい学習が行えない。すべての重みの値が均一に更新されるため、多数の重みを持つ意味がなくなる
```


#### 01:11:39　1-3 バッチ正規化
```
バッチ正規化とは、ミニバッチ単位で、入力値のデータの偏りを抑制する手法
```
![Image](/深層学習day2_01h19m55s.png)
![Image](/深層学習day2_01h25m18s.png)


##### 01:26:00- コード：2_2_2_vanishing_gradient_modified.ipynb
```
sigmoid - gauss
```
![Image](/2_2_2_vanishing_gradient_modified.ipynb_sigmoid - gauss.png)

```
ReLU - gauss
```
![Image](/2_2_2_vanishing_gradient_modified.ipynb_ReLU - gauss.png)

```
sigmoid - Xavier
```
![Image](/2_2_2_vanishing_gradient_modified.ipynb_sigmoid - Xavier.png)

```
ReLU - He
```
![Image](/2_2_2_vanishing_gradient_modified.ipynb_ReLU - He.png)
> 実演リンク：[2_2_2_vanishing_gradient_modified.ipynb](https://drive.google.com/file/d/1kYiddadTG1V9KxiCRTBpFbn7mPvEEm1J/view?usp=sharing)


##### 外部資料
> 外部資料リンク：[To understand LSTM architecture, code a forward pass with just NumPy](https://towardsdatascience.com/the-lstm-reference-card-6163ca98ae87)


##### 01:29:00- コード：2_3_batch_normalization.ipynb 
```
```
![Image](/.png)
> 実演リンク：[title](https://)



#### 
```
```
![Image](/.png)
> 実演リンク：[title](https://)


#### 
```
```
![Image](/.png)
> 実演リンク：[title](https://)
