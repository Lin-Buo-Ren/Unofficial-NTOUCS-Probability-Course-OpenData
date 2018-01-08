# 2017/09/29 筆記
## 第 2.4 章<br>組合
### Ex. 2.21 - What is the probability that a poker hand is a full house?
* full house = 三張同一面牌、餘兩張也同一面牌
* $$ \frac{(13, 1) (4, 3) (12, 1) (4, 2)}{52 取 5} $$

### Ex. 2.24 - An absentminded professor wrote *$$ n $$ letters* and sealed them in envelopes before writing the addresses on the envelopes.  Then he wrote the $$ n $$ addresses on the envelopes at random.  What is the probability that *at least* one letter was addressed correctly?
* 看到「至少」可用(rec 1029)餘事件來解（ $$ 1 - P({E_1}^c{E_2}^c \cdots {E_n}^c $$），不過第三章之後才有方法解此類型問題
* $$
E_i：第i封信地址是正確的\\
求 P(E_1 OR E_2 OR ... OR E_n) （課本作法）
$$

#### Solution - 排容原理(1037)
令 $$ E_i $$ 表示第 $$ i $$ 封信地址正確的事件 $$ i = 1, 2, 3, \cdots, n $$，所求為 $$ \begin{align*}
P(E_1 OR E_2 OR \cdots OR E_n) \\
&= P(E_1) + P(E_2) + \cdots + P(E_n)\\
&- [ P(E_i E_j) + \cdots ] \\
&+ [ P(E_i E_j E_k) + \cdots ] \\
&\vdots \\
&+(-1)^nP(E_1 E_2 \cdots E_n)(missed 1030)
\end{align*} $$

### 第 2.5 定理 - 二項式展開<br>Binomial Expansion - For any integer $$ n \gt 0 $$, $$ (x+y)^n = \sum^{n}_{i = 0} (n, i) x^{n-i}\cdot y^i $$

#### 第 2.26 例題 - Evaluate the sum $$ (n, 0) + (n, 1) + (n, 2) + (n, 3) + \cdots + (n, n) $$

##### Solution - 類比二項式展開

#### 第 2.27 例題 - Evaluate the sum $$ (n, 1) + 2(n, 2) + 3(n, 3) + \cdots n(n, n) $$
##### Solution - Binomial Expansion, $$ (n-i)! = [(n-1) - (i=1)]! $$
原式等同為 $$ 1(n, 1) + 2(n, 2) + 3(n, 3) + \cdots n(n, n) $$

每一項的一般式：$$ i \cdot (n, i) , i = 1, 2, 3, \cdots, n $$

#### 第 2.28 例題 - Prove that $$ (2n, n) = \sum^n_{i=0} (n, i)^2 $$

### 第 2.6 定理 - 多項式展開<br>Multinomial Expansion
* 多項式展開為二項式展開的推廣

### 習題
7, 8, 12, 17, 18, 19, 42, 43, 47（信解）

## 第 2.5 章 - Stirling's Formula
### 第 2.7 定理 - Stirling's Formula - $$ n! ~ \sqrt{2\pi n} n^n e^{-n} $$
#### 第 2.31 例題 - Approximate the value of $$ 2^n (n!)^2 \ / (2n)! $$ for large $$ n $$
$$ \begin{align*}
原式 &= \frac{2^n \cdot 2\pi n \cdot n^{2n} \cdot e^{-2n}}{\sqrt{2\pi2n} \cdot(2n)^{2n}} (missed 1100)
\end{align*} $$

## 第 3 章 - 條件機率<br>Conditional Probability
### 例題 - All the freshmen of an engineering college took * discrete math* and *calculus* $$ 70% passed calculus\\55% passed discrete math \\45% passed both  $$.  Ask: (missed 1126)
$$\begin{align*}
P(A|B) &= (missed 1132)
\end{align*}$$


### 例題 - Suppose that a bus arrives at a station every day at a random time between 1:00PM and 1:30PM.  Suppose that at 1:10 the bus has not arrived and we want to calculate the probability that it arrive in not more than 10 minutes from now.
#### Solution
Let $$ A $$ be the event that the bus will arrive between 1:10~1:20, and $$B$$ be the event that it will arrive between 1:10~1:30.

$$ 
P(A | B) = \frac{P(A)}{P(B)}
$$

### 第 3.1 例題 - In a certain region of Russia, the probability that a person lives at least 80 years is 0.75, and the probability that he or she lives at least 90 years is 0.63.  What is the probability that a randomly selected 80-year-old person from this region will survive to become 90?

#### Solution
Let A and B be the events that the person selected survives to become 90 and $$ P(A|B) = \frac{P(AB}{P(B)} (missed 1135) $$

### 第 3.2 例題 - From the set of all families with two children, *a family* is selected at random and is found to have a girl.  What is the probability that the other child of the family is a girl?  Assume that in a two-child family all sex distribution are equally probable
#### Solution
Let $$ B $$ and $$ A $$ be the events that the family has a girl and the family has two.

$$
\{(B,B), (B,G), (G,B), (G,G)\}
$$

$$
P(A|B) = \frac{P(AB)}{P(B)} = \frac{\frac{1}{4}}{\frac{3}{4}} = \frac{1}{3}
$$

### 第 3.4 例題 - An English class consists of 10 Koreans, 5 Italians, and 15 Hispanics.  A paper is found belonging to one of the students of this class.  If the name on the paper is not Korean, what is the probability that it is Italian?  Assume that names completely identify ethnic groups

#### Solution
Let A be the event that the name on the paper is Italian, and let B be the event(missed 1143)

$$ P(A | B) = (missed 1144) $$

### 第 3.1 定理 - Let $$ S $$ be the sample space of an experiment, and let B be an event of $$ S $$ with $$ P(B) \gt 0 $$.  Then (a) $$ P(A | B) \ge 0 $$ for any event $$ A $$ of $$  S $$ (b) $$ P(S|B) = 1$$ (c) If $$ A_1, A_2, \cdots $$ is a sequence of mutually exclusive events, then $$ P(U^{\inf}_{i = 1} A_i | B) = \sum^{\inf}_{i = 1} P(A_i | B) (missed 1146)

### 習題
3, 5, 9, 13, 16, 19, 21

## 第 3.2 章 - Law of Multiplication

