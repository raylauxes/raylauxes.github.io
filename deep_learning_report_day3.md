# 深層学習day3レポート(RNN)

![Image](/bnr_jdla.png)
http://study-ai.com/jdla/


## 00:00:00- アジェンダ
![Image](/深層学習day3-1_00h00m30s.png)


#### 00:02:00- CNNの構造図復習


#### 00:05:00- AlexNetのモデルの説明
![Image](/深層学習day3-1_00h07m30s.png)


#### 00:14:15- 再帰型ニューラルネットワーク
```
RNNとは、時系列データ（例：音声データ、テキストデータ、株価）に対応できるニューラルネットワーク
```


#### 00:24:25- RNNの全体像
```
x：入力層
Z：中間層
y：出力層
```
![Image](/深層学習day3-1_00h25m00s.png)
> 「unfold」の右には、左の詳細説明

> 修正：Z -> y


##### 00:33:00- RNNの全体像(2)
![Image](/深層学習day3-1_00h41m25s.png)


##### 00:36:15- RNNの数学的記述
![Image](/深層学習day3-1_00h37m11s.png)
![Image](/深層学習day3-1_00h40m30s.png)


##### 00:43:30- 確認テスト 
```
RNNのネットワークには大きく分けて3つの重みがある：
1、W(in)：入力から現在の中間層を定義する際にかけられる重み
2、W（out）：中間層から出力を定義する際にかけられる重み
3、W：前の中間層から中間層の重み
```


##### 00:48:10- RNNの特徴
```
時系列モデルを扱うには、初期の状態と過去の時間t-1の状態を保持し、そこから次の時間でのtを再帰的に求める再帰構造が必要になる。
```


##### 00:50:00- simple RNN
```
simple RNNでバイナリ加算をやってみよう！
```
> 実演リンク：[3_1_simple_RNN.ipynb](https://drive.google.com/file/d/1wt-wGSfbi21PVI6ilKXwsNYW95Qg1yiH/view?usp=sharing)


##### 00:59:10- 演習チャレンジ
![Image](/深層学習day3-1_00h59m00s.png)


##### 00:59:10-01:08:00 構文木（こうぶんぎ）
```
10個+10個 -> 20個 -> 10個
```
![Image](/深層学習day3-1_01h08m07s.png)



### 01:18:00- 1-2 BPTT
#### 01:18:00- 1-2-1 BPTTとは
```
BPTTとは、RNNにおいてのパラメータ調整方法の一種（誤差逆伝播の一種）
```


#### 01:19:30- 誤差逆伝播法の復習
![Image](/深層学習day3-1_01h20m53s.png)
![Image](/深層学習day3-1_01h22m00s.png)


#####
> 実演リンク：[3_1_simple_RNN.ipynb](https://drive.google.com/file/d/1wt-wGSfbi21PVI6ilKXwsNYW95Qg1yiH/view?usp=sharing)


#### 01:39:00-  1-2-2 BPTTの数学的記述
```
BPTTの数学的記述
```
![Image](/深層学習day3-1_01h39m50s.png)

```
数式とコード
```
![Image](/深層学習day3-1_01h41m50s.png)


#### 01:00:00-
```

```
![Image](/.png)
> 実演リンク：[title](https://)

#### 01:00:00-
```

```
![Image](/.png)
> 実演リンク：[title](https://)

#### 01:00:00-
```

```
![Image](/.png)
> 実演リンク：[title](https://)

#### 01:00:00-
```

```
![Image](/.png)
> 実演リンク：[title](https://)
