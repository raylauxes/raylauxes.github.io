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


