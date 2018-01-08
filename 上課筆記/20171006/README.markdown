# 2017/10/06 筆記
## 第 3.3 章<br>Law of Total Probability
### 第 3.4 定理<br>Law of Total Probability

### 第 3.15 例題<br>Suppose that 80% of the seniors（大四）, 70%（大三） of the juniors, 50% of the sophomores（大二）, and 30% of the freshmen（大一） of a college use the library of their campus frequently.  If 30% of all students are freshmen, 25% are sophomores, 25% are juniors, and 20% are seniors, what percent of all students use the library frequently?
* 令大一為 \(F\)大二為\(S\)大三為\(J\)大四為\(E\)圖書館為\(U\)
* \(\begin{align*}
P(U)&=P(U|F)\cdot P(F)+P(U|S) \cdot P(S) + P(U|J)\cdot P(J) + P(U|E) \cdot P(E)\\
&=0.3\cdot 0.3 + 0.5 \cdot 0.25 + 0.7 \cdot 0.25 + 0.80 \cdot 0.20
\end{align*}\)

### 第 3.17 例題<br>An urn contains 10 white and 12 red chips.  Two chips are drawn at random and, without looking at their colors, are discarded.  What is the probability that a third chip drawn is red.
* 令 \(W\)為白色\(R\)為紅色
* 分為四種情形：
	* R_1 R_2
	* R_1 W_2
	* W_1 R_2
	* W_1 W_2
* \(\begin{align*}
P(R_3) &= P(R_3|R_1R_2)P(R_1R_2)+P(R_3|R_1W_2)+P(R_3|W_1R_2)P(W_1R_2)+P(R_3|W_1W_2)P(W_1W_2)\\
&= \frac{10}{20}\frac{12}{22}\cdot\frac{11}{21}+\frac{11}{20}(\frac{12}{22}\cdot\frac{10}{21}) + \frac{11}{20}(\frac{10}{22}\frac{12}{21})+ (left)\\
&= \frac{12}{22}
\end{align*}\)
* 第三張紅色機率同重新開局

### 習題
3, 5, 7, 11, 18, 19

### 第 3.4 章<br>Baye's Formula
To introduce Bayes' formula, let us first examine the following problem.  

#### In a bolt factory, 30, 50, and 20% of production is manufactured by machines I, II, and III, respectively.  If 4, 5, and 3% of the output of these respective machines is defective, what is the probability that a randomly selected bolt that is found to be defective is manufactured by machine III?  To solve this problem, let \(A\) be the event that a random bolt is defective and B_3 be the event that it is manufactured by machine III.\

##### Solution<br>樹狀圖求解
![pic1103]()
![missed]()

* 想求\( \begin{align*}
P(III | D) &= \frac{P(III\cdot D)}{P(D)}\\
&= \frac{P(D|III) \cdot P(III)}{P(D|I) \cdot P(I) + P(D|II) \cdot P(II) + P(D|III) \cdot P(III)}\\
&= \frac{0.03 \cdot 0.2}{(0.04) \cdot (0.3) + (0.05) \cdot (0.5) + 0.03 \cdot 0.2}
\end{align*} \)

* \(P(I)\)、\(P(II)\)、\(P(III)\)為事前機率(prior)
* \(P(III|D)\)為事後機率(posterior)

#### 第 3.5 定理<br>Bayes' Theorem
* Let \({B_1, B_2, \cdots , B_n}\) be a partition of the sample space \( S \) of an experiment.  If for \( i = 1, 2, \cdots, n\) , \( P(B_i) > 0 \), then for any event \( A \) of \(S \) with \( P(A) > 0 \)  
\( \begin{align*}
P(B|A) = \frac{P(A|B)P(B)}{P(A|B)P(B)+P(A|B^c)P(B^c)}
\end{align*}\)

#### 第 3.18 例題<br>In a study conducted three years ago, 82% of the people in a randomly selected sample were found to have "good" financial credit ratings, while the remaining 18% were found to have "bad" financial credit ratings.  Current records of the people from that sample show that 30% of those bad credit ratings have since improved their ratings to good, while 15% of those with good credit ratings have since changed to having a bad credit rating.  What percentage of people with good credit ratings now had bad ratings three years ago?

* 令「現在信用是好的」事件為\( G \)
* 令「三年前信用是壞的」事件為\(B\)

![pic 1124]()

* 求 \( \begin{align*}
P(B|G) &= \frac{P(BG)}{P(G)}\\
&= \frac{P(G|B) \cdot P(B)}{P(G|B^c) \cdot P(B^c) + P(G|B) \cdot P(B)}\\
&= \frac{0.18}{0.85 \cdot 0.82 + 0.3 \cdot 0.18}
\end{align*} \)

#### 第 3.20 例題<br>On the basis of reconnaissance reports, Colonel Smith decides that the probability of an enemy attack against the left is 0.20, against the center is 0.50, and against the right is 0.30.  A flurry of enemy radio traffic occurrs in preparation for the attack.  Since deception is normal as a prelude to battle, Colonel Brown, having intercepted the radio traffic, tells General Quick that if the enemy wanted to attack on the left, the probability is 0.20 that he would have sent this particular radio traffic.  He tells the general that the corresponding probabilities for an attack on the center or the right are 0.70 and 0.10, respectively.  How should General Quick use these two equally reliable staff members' views to get the best probability profile for the forthcoming attack?
* \( \Delta \)：收到 radio 的事件
* \( A \)：左邊攻擊
* \( B \)：中間攻擊
* \( C \)：右邊攻擊
* 求 \( P(A|\Delta) = ?\)、\( P(B|A) = ?\)、\(C|\Delta = ? \)
* \( \begin{align*}
P(A|\Delta) &= \frac{A\Delta}{P(\Delta)} = \frac{P(\Delta|A)\cdot P(A) }{P(\Delta|A)\cdot P(A) + P(\Delta|B)\cdot P(B) + P(\Delta | C) \cdot P(C) }\\
&= \frac{(0.2)(0.2)}{(0.2)(0.2) + (0.3)(0.5) + (0.1)(0.3)}
\end{align*} \)

#### 第 3.21 例題<br>A box contains seven red and 13 blue balls.  Two balls are selected at random and are discarded without their colors being seen.  If a third ball is drawn randomly and observed to be red, what is the probability that both of the discarded balls were blue?
##### 解決方案：同重新開局(?)

##### 解決方案：Bayes Formula
\( \begin{align*}
	P(B_1B_2|R_3) = ?\\
	\frac{P(B_1 B_2 R_3)}{P(R_3)} = \frac{P(R_3|B_1B_2)P(B_1 B_2)}{P(R_3|R_1R_2)P(R_1 R_2) + P(R_3 | R_1B_2)P(R_1B_2) + P(R_3 | B_1R_2)P(B_1R_2) + P(R_3|B_1B_2)P(B_1 B_2)}
\end{align*} \)

#### 習題
6, 7, 8, 9, 14

#### 要交的作業
* 2.4#47, 3.1#21, 3.3#19, 3.4#14
* derangement: 排列的一種
* 下週五交並檢討習題

## 第 3.5 章<br>Independence
* We know \( P(B|A) \ne P(B) \)
* If \( P(B|A) = P(B) \), we say that \( A \) is **independent** of \( B \)
* From \( P(B|A) = P(B) \), \( \begin{case}
\frac{P(AB)}{P(A)} = P(B) \\
\frac{P(AB)}{P(B)} = P(A)
\end{case} \to P(AB) = P(A)P(B) \text{（主要記這個）} \)
