# 20171013 上課筆記
## 注意事項
* 下週一小考時間提早到 13:00 開始
* 雙教室考試

## 20171006習題檢討
### 1. A permutation of the first $$ n $$ integers is called a derangement if no integer is in its natural position.  Thus, (3, 2, 1) is not a derangement of (1, 2, 3), but (2, 3, 1) is a derangement.  Suppose one of the $$ n! $$ permutations of $$ 1, \cdots , n) $$ is picked at random.  Find $$ P_n $$, the probability that it is a derangement, and show that $$ \lim_{n \to \infty} p_n = e^{-1} $$.
* $$ A_i$$：第 $$ i $$ 個元素位置與自然排列位置一樣
* 求 $$ P(A_1^C A_2^C \cdots A_n^C) $$zz


#### 解決方案 - 排容原理 + 泰勒展開式
* $$ \begin{align*}
P(A_1^C A_2^C \cdots A_n^C) &= P([A_1 \cup A_2 \cup \cdots \cup A_n]^C\\
&= 1-P(A_1 \cup A_2 \cup \cdots \cup A_n)\\
&= (?) \end{align*}$$
* $$ \begin{align*}
P(A_1 \cup A_2 \cup \cdots \cup A_n) &= \sum^n_{i=1} P(A_i) - \sum P(A_i A_j) + \cdots\\
&=n \cdot \frac{1}{n} - \frac{n(n-1)}{2} \cdot \frac{1}{n(n-1)} \\
&= 1 - \frac{1}{2!} + \frac{1}{3!} - \frac{1}{4!} + \cdots + (-1)^n \frac{1}{n!}\\
&= 1 - \frac{1}{2} + \frac{1}{3!} - \frac{1}{4!} + \cdots
\end{align*} $$
	* $$ P(A_1) = \frac{(n-1)!}{n!} = \frac{1}{n} $$
	* $$ P(A_1 A_2) = \frac{(n-2)!}{n!} = \frac{1}{n(n-1)}
	* $$ e^x = \sum^{\infit}{n=0} \frac{x^n}{n!}\\
e^{-1} = \sum^{\infit}{n = 0} \frac{(-1)^n}{n!} = 1-1+\frac{1}{2!} - \frac{1}{3!}+ \frac{1}{4!} + \cdots $$

### 2. An urn contains $$ n $$ red and $$ n $$...
* 令紅球為 $$ R$$ 藍球為 $$B$$

#### (a) What is the sample space?
* 強調順序：$$ {(R, R), (R, B), (B, R), (B, B)} $$ 或不強調順序： $$ {RR, BR, RB} $$都可以

#### (b)
$$ \frac{n}{2n} \cdot \frac{n}{2n-1} + \frac{n}{2n} \cdot \frac{n}{(2n-1)} = \frac{2n^2}{2n(2n-1)} = \frac{n}{2n-1} $$

#### (c)
##### Sol. 餘事件
$$ P_n = 1 - ( \frac{n}{2n-1}) = \frac{n-1}{2n-1} \to (missed 1042) $$

### 3. Two cards are randomly chosen without replacement from the ordinary deck of 52 cards.  Let B be the event that both cards aces; Let $$ A_s $$ be the event that aces of spades is chosen, and A be the event that at least one ace is chosen.

#### (a) Find $$ P(B|A_3) $$
##### Sol. Total probability
$$ \begin{align*}
P(B|A_3) &= \frac{P(A_sB)}{P(A_s)}\\
&= \frac{}{P(A_s|\text{第一次拿到 ace of spades}) \cdot P(\text{第一次拿到 ace of spades}) + P(A_s|\text{第二次拿到 ace of spades}) \cdot P(\text{第二次拿到 ace of spades})}\\
&= \frac{P(A_s B)}{\frac{1}{52} \cdot \frac{51}{51} + \frac{51}{52} \cdot \frac{1}{51}}\\
&= \frac{(3, 1)}{\frac{2}{52}} = \frac{\frac{6}{(-2 \times 5)}}{\frac{2}{52}}
\end{align*} $$

#### (b) Find $$ P(B|A) $$
##### Solution - 餘事件 
$$ P(B|A) = \frac{P(AB)}{P(A)} = \frac{\frac{(4, 1)(3, 1)}{(52, 2)}}{1 -\frac{(48, 2)}{(52, 2)}} = \frac{3}{99} = \frac{1}{33} $$

### 4. English and American spellings are *rigour* and *rigor*, respectively.  A man staying at Grand hotel writes this word, and a letter taken at random from his spelling is found to be vowel.  If 40 percent of English-speaking men at the hotel are English and 60 percent are American, what is the probability that the writer is an Englishman?
#### Solution 貝氏？
* 想求 $$ \begin{align*}
P(E|V) = \frac{P(EV)}{P(V} &= \frac{}{P(V|E) \cdot P(E) + P(V|E^C) \cdot P(E^C)}\\
&= \frac{}{(\frac{3}{6}) \cdot (0.4) + (\frac{2}{5}) (0.6)}
\end{align*} $$

### Ch 2-4 #47. 10 張照片放入六個信封內，問沒信封是空的的機率？
* 樣本空間(?) = $$ 6^{10} $$
* 令 $$ A_1 \cdots A_6 $$：第一～六信封是空的事件

#### Solution - 排容原理
$$ \begin{align*}
A_1^C A_2^C \cdots A_6^C &= (A_1 \cup A_2 \cup \cdots A_6)^C\\
&= ? - n(A_1 \cup A_2 \cup \cdots \cup A_6) \\
&= n(A_1) + n(A_2) + \cdots + n(A_6)\\
&- [n(A_1A_2) + \cdots + ]\\
&+ [ n(A_1 A_2 A_3) + \cdots\\
&- [ n(A_1 A_2 A_3 A_4) + \cdots\\
&- [ n(A_1 A_2 \cdots A_6 ]\\
&= 6^10 - [ C^6_1 \cdot 5^{10} - C^6_2 \cdot 4^{10} + C^6_3 \cdot 3^{10} - (missed 1123)
\end{align*} $$

### Ch 3-1 #21
| type | 數量（隻） |刺激反應時間（秒） | 
| :--: | :--: | :--: |
| $$ I $$ | 15 | 5sec |
| $$ II $$ | 13 | 4.5sec |
| $$ III $$ | 12 | 6.2sec |

* 任取十隻
* 有4隻反應時間是 6.2 sec(III)
* 至少有一隻是 4.5 sec(II)

#### Solution - 餘事件
* $$ \begin{align*}
1 - P(沒有II) - P(有一隻是 II) &= (missed 1141)
\end{align*}$$

### Ch. 3-3 #19 - 一箱子內有 18 網球，8新球（10舊球），取3球打完放回再取三球，求新球機率
#### Solution - Total Probability
$$ \begin{align*}
	P(N) = &P(N | N_3) \cdot P(N_3) + \\
	&P(N | N_2U_1) \cdot P(N_2U_1) + \\
	&P(N | N_1U_2) \cdot P(N_1U_2) + \\
	&P(N|U_3) \cdot P(U_3)
\end{align*} $$

### Ch. 3-4 #14 - 一箱中有？五紅三藍取四片到空箱內，在後箱取出一藍
#### Total Probability
$$ \begin{align*}
P(2B2R | B) &= \frac{AB}{B} \\
&= \frac{}{P(B | 3R1B) + P(B | 2R2B)P(2R2B) + P(B | 1R3B)P(1R3B)}\\
&= (missed 1156)
\end{align*} $$

### P.88 #9 - 在拿到 ace of spades 之前...
#### 提示
在下一節(?)（獨立事件）有速解法

#### Solution
* $$ \begin{align*}
\frac{P(A)}{P(A) + P(B) }
\end{align*} $$
