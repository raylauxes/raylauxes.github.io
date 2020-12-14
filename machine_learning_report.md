# 機械学習レポート

![Image](/bnr_jdla.png)
http://study-ai.com/jdla/

## 機械学習前半

### ML_01_01_プロローグ

E資格の試験には応用数学と機械学習が40-50%出題されている！
```
機械学習モデリングプロセス：
1、問題設定
2、データ選定
3、データの前処理
4、機械学習モデルの選定
5、モデルの学習（パラメータ推定）
6、モデルの評価
```
![Image](/ML_01_01_プロローグ_06m30s.png)

この講義で扱う学習モデルとパラメータの推定問題
![Image](/ML_01_01_プロローグ_11m00s.png)


### ML_02_01_機械学習とは

![Image](/ML_02_01_機械学習とは_03m01s.png)

> A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E. (参考リンク：[What is machine learning and types of machine learning — Part-1](https://towardsdatascience.com/what-is-machine-learning-and-types-of-machine-learning-andrews-machine-learning-part-1-9cd9755bc647#:~:text=Tom%20Mitchell%20provides%20a%20more,Example%20%3A&text=To%20find%20that%20logic%20is%20called%20%E2%80%9Cmachine%20learning%E2%80%9D.))


### ML_03_01_線形回帰モデル
```
線形回帰　：直線で予測回帰問題
非線形回帰：曲線で予測回帰問題
```
T:転置（transpose）

![Image](/ML_03_01_線形回帰モデル_01m40s.png)


### ML_03_02_線形回帰モデル

通常の表記には、予測値にハット（hat）を付ける
![Image](/ML_03_02_線形回帰モデル_00m00s.png)


### ML_03_03_線形回帰モデル

線形結合で、多次元のベクトルが入力されても、1次元の出力となる

重み（w）は未知のパラメータで、機械学習で最適な重みを探す！

![Image](/ML_03_03_線形回帰モデル_00m45s.png)


### ML_03_04_線形回帰モデル
```
ε：イプシロン（epsilon）
```
![Image](/ML_03_04_線形回帰モデル_00m55s.png)
![Image](/ML_03_04_線形回帰モデル_02m03s.png)


### ML_04_01_データ分割・学習

モデルの汎化性能を測るため、データを学習データ（train）と検証データ（test）に分割する


### ML_04_02_データ分割・学習

平均二乗誤差（MSE/Mean Squared Error）で実際の値と予測した値の誤差を測る

最小二乗法：学習データのMSEを最小化とするパラメータを探す

![Image](/ML_04_02_データ分割・学習_02m22s.png)


### ML_04_03_データ分割・学習

MSEの最小値を求めるのは、MSEを微分したものが0となるwを求めるのと同じ

![Image](/ML_04_03_データ分割・学習_00m22s.png)
![Image](/ML_04_03_データ分割・学習_01m33s.png)


### ML_05_02_ハンズオン（住宅価格予測）

> A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E. (参考リンク：[skl_regression.ipynb](https://colab.research.google.com/drive/1bH9NltODOPXnOiuHinsf4ozRZkG6TBSC#scrollTo=mUMLJMTIMsNQ))


### ML_06_01_非線形回帰モデル

![Image](/ML_06_01_非線形回帰モデル_00m53s.png)


### ML_06_02_非線形回帰モデル

![Image](/ML_06_02_非線形回帰モデル_01m06s.png)
![Image](/ML_06_02_非線形回帰モデル_02m23s.png)

### ML_06_03_非線形回帰モデル
```
過学習を防ぐ方法：
1、データ数を増やす
2、不要な変数（基底関数）を削除
3、正則化（罰則化）
```

### ML_07_02_正則化法

![Image](/ML_07_02_正則化法_00m00s.png)


### ML_07_03_正則化法
![Image](/ML_07_03_正則化法00m03s.png)


### ML_08_01_モデル選択
```
データを学習データと検証データに分割する際に、２つの方法がある：
1、ホールドアウト法：多くのデータがある際に一回しか分割する
2、交差検証法：データが少ない時、数回分割する
```

## 機械学習前半

### ML_09_01_ロジスティック回帰モデル

ロジスティック回帰モデルには「回帰」という文字が付いているが、回帰問題ではなく、分類問題に使う


### ML_09_02_ロジスティック回帰モデル

```
単調増加関数：xが大きくなると、yも大きくなる
バイアス変化は段差の位置？
```
![Image](/ML_09_02_ロジスティック回帰モデル_01m00s.png)


### ML_09_03_ロジスティック回帰モデル

![Image](/ML_09_03_ロジスティック回帰モデル_01m00s.png)

> 尤度関数（ゆうどかんすう、英: likelihood function）とは統計学において、ある前提条件に従って結果が出現する場合に、逆に観察結果からみて前提条件が「何々であった」と推測する尤もらしさ（もっともらしさ）を表す数値を、「何々」を変数とする関数として捉えたものである。また単に尤度ともいう。

### ML_09_04_ロジスティック回帰モデル

![Image](/ML_09_03_ロジスティック回帰モデル_01m00s.png)
