# 深層学習day3レポート(RNN)

![Image](/bnr_jdla.png)
http://study-ai.com/jdla/


## 00:00:00- アジェンダ
![Image](/深層学習day3-1_00h00m30s.png)

#### 00:02:00- CNNの構造図復習
```
```

> 実演リンク：[title](https://)













例例例例例例例例例例例例例例例例例例例例例例例例例例例例例例例
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
