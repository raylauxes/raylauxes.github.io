# 応用数学レポート

## 線形代数 - 行列

### スカラーとベクトルの違い：

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

#### 2ベクトルなら、面積

#### 3ベクトルなら、体積

#### nベクトルなら：

1、同じ行ベクトルが含まれていると行列式はゼロ　（連立方程式として考えると、情報不足だから１つの解とならない）

2、１つのベクトルがλ倍されると、行列式がλ倍される　（面積を考えよう：１つの辺がλ倍とされると、面積もλ倍となる）

3、他の成分が全部同じで、i番目のベクトルだけ違った場合…行列式の足し合わせになる






You can use the [editor on GitHub](https://github.com/raylauxes/raylauxes.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/raylauxes/raylauxes.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
