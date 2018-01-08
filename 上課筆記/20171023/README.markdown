# 20171023 筆記
## 第 3.5 章<br>Independence
### 第 3.33 例題 - Adam tosses a fair coin  \( n + 1 \) times, Andrew tosses the same coin \( n \) times.  What is the probability that Adam gets more heads than Andrew?
* 設
	* \( H_1, H_2 \) 分別是 Adam 與 Andrew 得到正面的次數
	* \( T_1, T_2 \) 分別是 Adam 與 Andrew 得到反面的次數
* 本來想求：\( P(H_1 > H_2) = P( T_1 > T_2) \)
* \( \begin{align*}
 \因為 P(H_1 > H_2) = P(n+1-T_1 > n-T_2) &= P(T_2 > T_1 -1)\\
&= P(T_2 \ge T_1 )
\end{align*}\)
* 利用（？）\( \to P(T_1 > T_2) = P(T_2 \ge T_1) \)
* 又 \( P( T_1 > T_2) + P(T_2 \ge T_1) = 1 \)
* \( \所以 P(T_1 > T_2) = \frac{1}{2} \)
* 推論：多一次機率一樣

## 第 4.1 章<br>Random Variables
* 很多事件的發生含有不確定性
* 令這些不確定量的為**隨機函數**或**隨機變數**的結果

	> "In probability, quantities introduced in these diverse examples are called random variables(r.v.)."

* 範例：If in rolling two fair dice, \( X \) is the sum then \( X \) can only assume the values \( 2, 3, 4, \cdots , 12 \) with the following probabilities:

	\( 
	P(X=2) = P({(1, 1)}) = 1/36\\
	P(X=3) = P({(1, 2), (2, 1)}) = 2/36\\
	P(X=4) = P({(1, 3), (2, 2), (3, 1)}) = 3/36
	\)

### 定義 - 
* Let \( S \) be the sample space of an experiment.  A real-valued function \( X:S\toR \) is called a **random variable** of the experiment if, for each interval \( 1 \被包含於等於 R \),  \( { s: X(s) \屬於 1} \) is an event.
* In probability, the set \( {s: \) ...

### 4.1 例題 - 
#### 命題
Suppose that three cards are drawn from an ordinary deck of 52 cards, one by one, at random and with replacement.  Let \( X \) be the number of spades drawn; then \( X \) is a random variable.  If an outcome of spades is denoted by \( s \), and other outcomes are represented by \( t \), then \( X \) is a real-valued function defined on the sample space

\( S = {(s, s, s), (t, s, s), (s, t, s), (s, s, t), (s, t, t), (t, s, t), (t, t, s), (t, t, t) } \)

by \( X(s, s, s) = 3 \), \(X(s, t, s) = 2 \), \(X(s, s, t) = 2 \),  \( X(s, t, t) = 1 \), and so on.  Now we must determine the values that \( X \) means ...

#### Solutions

### 4.2 例題
#### 命題
A bus stops at a station every day at some random time between 11:00 A.M. and 11:30 A.M..  If \( X \) is the actual arrival time of the bus, \( X \) is a random variable.  It is a function defined on the sample space \( S  = {t: 11 < t < 11 \frac{1}{2} } \) by \( X(t) = t \).  As we know from Section 1.7, \( P(X = t) = 0 \) for any \( t \屬於 \)...

### 4.3 例題
#### 命題
In the United States, the number of twin births is approximately \( 1\) in \( 90 \).  Let \( X \) be the number of births in a certain hospital until the first twins are born.  \( X \) is a random variable.  Denote twin births by \( T \) and single births by \( N \).  Then \( X \) is a real-valued function defined on the sample space...

### 4.5 例題
#### 命題
The diameter（直徑） of a flat meta disk manufactured by a factory...

#### Solution
* 求 \( \begin{align*}
P(A > 4.41 \pi) &= P(\pi (\frac{P}{2})^2 > 4.41 \pi)\\
&= P(\frac{\pi P^2}{4} > 4.41 \pi) ...
\end{align*}\)

## 第 4.2 章<br>Distribution Functions<br>分佈函數
* 分佈函數可以用來描述（刻劃）隨機變數 \( r.v.x \)
* 應用例子
	1. If a bus arrives at a random time between 10:00A.M. and 10:30 A.M. at a station, and \( X \) is the arrival time, then \( X < 10 \frac{1}{6} \) is the event that the bus arrives before 10:10 A.M.
	2. If \( X \) is the price of gold per troy ounce on a random day, then \( X \le 400 \) is the event that the price of gold remains at or below \$400 per troy ounce.
	3. If \(X \) is the number of votes that the next Democratic presidential candidate will get, then \( X \ge 5 \times 10^7 \) is the event that he or she will get at least 50 million votes
	4. If \( X \) is the number of heads in 100 tosses of a coin, then \( 40 \lt X \le 60 \) is the event that the number of heads is at least 41 and at most 60.

