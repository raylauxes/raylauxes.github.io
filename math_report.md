# 応用数学レポート

![Image](/bnr_jdla.png)
http://study-ai.com/jdla/

## 線形代数 - 行列

### スカラーとベクトルの違い：
aKyynhD93
スカラー  ：演算できる、普通の数 (MA_17)
 
ベクトル  ：大きさと向きを持っている、数のセット（一次元以上の次元空間に存在している、方向と長さを持っているものと考えられる）

### 行列は何か：

演算しやすいため、ベクトルの集まり。例：連立方程式を簡潔に表現できる。(MA_18-19)

行列が連立方程式の係数（未知数を除いて）を取り出したものとも考えられる。(MA_20)

「行」と「列」を掛けることにより生じた新しい成分の集まり！ (MA_20)

連立方程式の解き方は「行列の変形」(行の基本変形)と考えられる (MA_22)

### 行の基本変形

i行目をc倍する

s行目にt行目のc倍を加える

p行目とq行目を入れ替わる

### 行基本変形は行列を左からかけることで表現できる (MA_23)

行基本変形に対応する（並んでいる）行列を左からかけないと、結果が違う。行列の掛け算の方向に注意！（MA_24）

### 行列に割り算が定義されていないが、「逆行列」を掛けること（すると単位行列になる）が行列の割り算と考えられる（MA_24）

※単位行列：かけても、かけられても相手が変化しない「1」のような行列（MA_24）

行列「A」の逆行列は「Aインバース」と呼ぶ(MA_25)

行列と逆行列の順番を入れ替わっても、掛け算の結果が同じように単位行列となる(MA_25)

逆行列には様々な求め方があるが、ガウスの掃き出し法（はきだしほう）が一般的（MA_26）

### 逆行列が存在しない条件

a b

c d

a:b =/= c:d (逆行列を持ち)

a:b = c:d (逆行列を持たない)

-> a * d = b * c

-> ad - bc = 0 (abベクトルとcdベクトルに囲まれる平行四辺形の面積=0)(MA_28)(?)


### 「行列式」（determinant）：逆行列が存在するかを判断する式

### nのベクトルができている行列の「行列式」にはどんな特徴を持っている？
```
2ベクトルなら、面積
3ベクトルなら、体積
```

#### nベクトルなら： (MA_29)
```
1、同じ行ベクトルが含まれていると行列式はゼロ　（連立方程式として考えると、情報不足だから１つの解とならない）

2、１つのベクトルがλ倍されると、行列式がλ倍される　（面積を考えよう：１つの辺がλ倍とされると、面積もλ倍となる）

3、他の成分が全部同じで、i番目のベクトルだけ違った場合…行列式の足し合わせになる

4、行を入れ替えると符号が変わる（正から負となるとか）

※「行列式」（determinant）を「行列」（matrix）に勘違いしないように！
```

#### ３つ以上のベクトルからできている「行列式」は展開できる

２つの軸の平面の高さが考えられる （MA_29） (??)

![Image](/MA_29_線形代数_行列_12_11m53s.png)

======================================================================================================================================

## 線形代数 - 固有値

### 固有ベクトル：ある行列をかけたのに、結果は変わらない（つまり、元々のベクトルのλ倍となる）

### 何故A-λIの行列式がゼロとなる？ (MA_35)

xベクトルがゼロではないことは確実。しかし、「A-λI」行列には逆行列が存在すると、xベクトルがゼロとなるという矛盾が生じるので、「A-λI」行列の逆行列が存在していないことが判断れきる。逆行列が存在していないため、行列式がゼロとなる

![Image](/MA_35_線形代数_固有値_03_10m29s.png)


### 固有値と固有ベクトルの求め方

1、行列を得てから、「A-λIに逆行列が存在していないから行列式がゼロ」に基づいて固有値を解く

2、さらに、得た固有値を「Ax = λI」に代入し、固有ベクトルを得る

### 何故行列を固有値に分解するか？　計算上有利　（MA_37）

行列Aはv1, v2...固有ベクトルを持ち、λ1,λ2...固有値を持っている

V = v1, v2...


Λ = λ1
　　　　λ2
    　　　...

とすると

AV = VΛ　（ポイント：定義上、行列の固有ベクトルは該当行列をかけても変わらなくて、固有値の倍数となるだけ！）

A = VΛV(-1) => A行列の累乗は簡単にできる！

※VV(-1) => I(単位行列)

Λは対角線しか数字がないので、累乗は楽！

![Image](/MA_37_線形代数_固有値_05_05m31s.png)

### 固有値分解には一個の方法だけじゃない (MA_38)

A = VΛV(-1) のうち、

Λ（対角線に各固有値λ(n)が入っている行列）は固定だが、固有ベクトルVは固定してない。でも、後についているVの逆行列と組み合わせたら同じ値となる！


### 固有値分解には、正方行列しかできない！ 正方でない行列に似たものを求める場合、特異値分解(MA_41)

直交行列（ちょっこうぎょうれつ, orthogonal matrix）とは、転置行列と逆行列が等しくなる正方行列のこと。 つまりn × n の行列 M の転置行列を MT と表すときに、MTM = M MT = E を満たすようなMのこと。 ただし、 E は n 次の単位行列。

![Image](/MA_41_線形代数_固有値_09_01m08s.png)


### 特異値分解の方法：
![Image](/MA_42_線形代数_固有値_10_04m08s.png)

長方行列を転置させて、それを転置させる前の行列を掛け合わせると無理やり正方形にする。その正方行列の固有値分解のうち、S(ラムダ)　（MA_42）



非正方行列を転置して自身をかけたら正方行列を得る。その正方行列を固有値分解すると、下記の通りに左特異値ベクトル（U）、特異値の二乗（SS(T)）、および右特異値ベクトル（V(T)）を得る。

```
A     = V *   Λ   * V(-1)

MM(T) = U * SS(T) * U(T)

M(T)M = V * S(T)S * V(T)
```


### [特異値分解PART2：特異値分解(Youtube)](https://www.youtube.com/watch?v=CUtT2Pi3ITQ)

![Image](/MA_43_線形代数_固有値_11_04m04s.png)
![Image](/MA_43_線形代数_固有値_11_05m51s.png)


### 特異値分解の応用：

画像処理：画質を下げる（）？？ 画像を行列として考える(MA_44)

![Image](/MA_44_線形代数_固有値_12_07m23s.png)

同一画像かを判断する：２つの画像を特異値分解をかけた結果、もし大きな部分が同じ数値であれば、似たものが写っている可能性が高い

======================================================================================================================================


## 確率統計 - 集合と確率

和集合と共通部分 (MA_73)
![Image](/MA_73_統計_03_05m00s.png)

絶対補と相対補 (MA_73)
![Image](/MA_73_統計_03_07m50s.png)

確率の二種類：（MA_75）
1、頻度確率（客観）
2、ベイズ確率（主観）


![Image](/MA_75_統計_05_04m30s.png)

### 条件付き確率

P(A∩B) = P(A) * P(B|A)

つまり、

AとB事象が同時に起こる確率 = (A事象の数/全事象の数) * (A事象とB事象が同時に起こる数/A事象の数)

※A事象の件数、cancel out!

P(B|A)の「B|A」は分数でなく、「Aが条件でBが現れること」！

![Image](/MA_77_統計_07_05m00s.png)

「Aの条件下でBが起こる」=/=「AとBが同時に起こる」 (MA_78)
例えば、「雨が降っている条件下で交通事故に遭遇すること」=/=「雨と交通事故が同時に起こる」

※P：確率

※n：数

![Image](/MA_78_統計_08_07m30s.png)

### 独立な事象の同時確率（MA_79）

事象AとBは因果関係がない時、P(B|A) = P(B)

例えば、「猫を見ること」をA、「風邪を引くこと」をBにすると、

P(B|A):「猫を見る時風邪を引く確率」

P(B)「風邪を引く確率」

変わらない！

![Image](/MA_79_統計_09_03m00s.png)

### (MA_80)

P(AUB) = P(A) + P(B) - P(A∩B) 

### ベイズ則 (MA_81)
```
問題：P(Candy | Smile) = ?
ヒント：P(Smile) * P(Candy | Smile) = P(Candy) * P(Smile | Candy)
```
![Image](/MA_81_統計_11_03m03s.png)

======================================================================================================================================

## 確率統計 - 統計

### 統計の二種類：（MA_82）

1、記述統計:平均値などを計算したりする、集団の全データの性質を要約し記述。ただし、すべてのデータを収集することが難しい時がある

2、推測統計：抽出した標本から、集団の全データの性質を推測

### 確率変数と確率分布（MA_83）

![Image](/MA_83_統計_13_04m30s.png)

### 期待値（MA_84）

![Image](/MA_84_統計_14_02m52s.png)

### 分散と共分散（MA_84_統計_14_2）

データはどれくらい散らばっているのかを示している

分散を求める際に二乗にする理由：絶対値を求めてもいいけど、計算コストが高い。また、四乗や六乗にしてもいいが、無駄な計算コストが増える

#### 分散の式：

![Image](/MA_84_統計_14_2_02m39s.png)

### 分散と標準偏差 (MA_85_統計_15)

```
「分散」で散らばりを示すと、単位が元単位の二乗になってしまう！
なので、「標準偏差」（分散の平方根）で散らばりを示す
```

![Image](/MA_85_統計_15_02m50s.png)

### 様々な確率分布 (MA_86_統計_16)
```
x = 1 OR 0
μ：平均の値（ここでは確率のようなもの？）
```
> このμは確率のようなもの？成功の値は1なので、成功の期待値=平均値=確率？？

![Image](/MA_86_統計_16_00m33s.png)
```
なぜ２つの結果しかなくても、ベルヌーイ分布は複雑の式で確率を示しているの？
-1行で簡潔にかけて、数式で扱える
-ほかの確率理論とつながっている
```
> Q: なぜマルチヌーイ分布には数式で書く意味ない？
> `P(x|μ)`とは？μの前提でxが現れる確率ではないよね？

[Introduction to the Bernoulli Distribution(Youtube)](https://www.youtube.com/watch?v=bT1p5tJwn_0)
![Image](/Introduction_to_the_Bernoulli_Distribution_02m15s.png)

### 様々な確率分布II (MA_87_統計_17)

#### 二項分布（binominal distribution）とガウス分布（normal/Gaussian/Gauss/Laplace–Gauss distribution）

![Image](/MA_87_統計_17_08m55s.png)

```
μ = mu
σ = Σ = sigma
```

> 二項分布の式について、Youtubeを参考…
> [An_Introduction_to_the_Binomial_Distribution(Youtube)](https://www.youtube.com/watch?v=qIzC1-9PwQo)
> ![Image](/An_Introduction_to_the_Binomial_Distribution_05m57s.png)
> ![Image](/An_Introduction_to_the_Binomial_Distribution_06m26s.png)
> ![Image](/An_Introduction_to_the_Binomial_Distribution_09m20s.png)

### 推定（MA_88_統計_18）

**ここの「母数」とは「母集団の個数」でなく、「平均値など母集団の特徴を決めるパラメーター」といる意味である**

2種類の推定：点推定と区間推定（機械学習にはあまり使わない）
![Image](/MA_88_統計_18_03m00s.png)

### 推定量（estimator、推定関数とも）と推定値（estimate）（MA_89_統計_19）
```
θ：theta（シータ）
```
![Image](/MA_89_統計_19_03m00s.png)

### MA_90_統計_20

標本平均：母集団から取り出した標本の平均値

一致性：サンプル数が大きくなれば、母集団の値に近づく

不偏性：サンプル数がいくらであっても、その期待値は母集団の値と同様
> なぜ？
> 参考リンク：[標本分散の一致性と不偏性(BellCurve)](https://bellcurve.jp/statistics/course/14987.html)

### 標本分散と不偏分散（MA_91_統計_21）

標本分散には、一致性は満たすが、普遍性は満たさない！

標本分散を修正する＝＞不偏分散

**解釈の１つ：xの平均値が決まっているので、自由にn個のサンプルを取れるわけではない**

nが大きくなれば、`n/(n-1)`はほぼ1となるため、掛けてもかけなくてもあまり変わらない

![Image](/MA_91_統計_21_06m30s.png)

> 参考リンク：[18-4. 標本分散と不偏分散(BellCurve)](https://bellcurve.jp/statistics/course/8614.html)

### MA_92_統計_22

どっちでも一個だけ増やしたのに、なぜひとつしか一目で分からないの？

![Image](/MA_92_統計_22_05m00s.png)

### 自己情報量(self-information)(MA_93_統計_23)

珍しいことは情報量が多い
![Image](/MA_93_統計_23_09m01s.png)

> 参考リンク：[情報理論の基礎～情報量の定義から相対エントロピー、相互情報量まで～](https://logics-of-blue.com/information-theory-basic/)

> 以下の2つの要請を満たす「情報量」を定義しましょう。

> １：発生する確率が低いこと（珍しいこと）が分かった時のほうが、情報量が多い

> ２：情報量は足し算で増えていく。

> この条件を満たす情報量は以下のように定義できます。あることが分かった際の「そのことの情報量」を自己情報量と呼びます。

### シャノンエントロピ（Shannon entropy）(MA_94_統計_24)

![Image](/MA_94_統計_24_00m30s.png)

> Entropy is a measure of uncertainty（参考リンク：[Building the Shannon entropy formula](https://towardsdatascience.com/building-the-shannon-entropy-formula-ca67bdb74cdc)）

> the information contained in a message about an event is related to the uncertainty and surprise-value of the event. An occurrence of an unlikely event gives you more information than the occurrence of a likely event. Claude Shannon formalised this intuition behind information in his seminal work on Information Theory.（参考リンク：[Cross-Entropy for Dummies](https://towardsdatascience.com/cross-entropy-for-dummies-5189303c7735)）


### カルバック・ライブラー　ダイバージェンス（Kullback–Leibler divergence）(MA_95_統計_25)

※「カルバック・ライブラー情報量」や「カルバック・ライブラー距離」とも訳されているが、「ダイバージェンス」イコール「情報量」や「距離」であるわけではない！

カルバック・ライブラー　ダイバージェンス：「Pの珍しさとQの珍しさはどれぐらい違う」を表現すること

```
E：期待値（= 平均）
I(P(x))：Pの自己情報量
```
![Image](/MA_95_統計_25_16m00s.png)

> Very often in Probability and Statistics we'll replace observed data or a complex distributions with a simpler, approximating distribution. KL Divergence helps us to measure just how much information we lose when we choose an approximation. (参考リンク：[Kullback-Leibler Divergence Explained](https://www.countbayesie.com/blog/2017/5/9/kullback-leibler-divergence-explained))


### 交差エントロピー（cross-entropy）(MA_96_統計_26)

発想：秘密情報を送る前に、暗号表をまず送ること

```
H：エントロピー
H(P,Q)：PとQの交差エントロピー
```
![Image](/MA_96_統計_26_08m00s.png)

> The x~P in the above equation means that the values x takes are from the distribution P.（参考リンク：[Cross-Entropy for Dummies](https://towardsdatascience.com/cross-entropy-for-dummies-5189303c7735)）

> Cross-entropy measures the relative entropy between two probability distributions over the same set of events. Intuitively, to calculate cross-entropy between P and Q, you simply calculate entropy for Q using probability weights from P.（参考リンク：[Cross-Entropy for Dummies](https://towardsdatascience.com/cross-entropy-for-dummies-5189303c7735)）
