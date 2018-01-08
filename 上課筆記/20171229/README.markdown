# 20171229
## 第11.3章 - Markov and Chebyshev Inequalities
### 第 11.8 定理 - Markov's Inequality
![](graph1020.png)

* $$ P(X \ge t) \le \frac{E{X}}{t} $$

(missing)

### 第 11.12 例題：An post office, on average, handles 10,000 letters per day.  ...probablility that t will handle (a) at least 15,000 letters tomorrow; (b) less than 15,000 letters tomorrow
* $$ E(x) = 10,000 $$
* $$ r.v. x $$：一天信件數

#### (a) 
$$ P( X \le 15,000) \le \frac{10,000}{15,000} = \frac{2}{3} $$

### (b)
$$ P( X < 15,000) = 1 - P( X \ge 15,000) \ge \frac{1}{3} $$

### 第 11.3 章 - Chebyshev Inequalities
* 基於 Markov
* ……如果兩個都給你就用 Chebyshev
* $$ P( \mid X - \mu \mid \ge t) \le \frac{a^2}{r^2} $$

#### 證明
![](graph1037.png)

* 因 $$ X - \mu)^2 \ge 0 $$，基於 Markov's Inequality 我們可得到 $$ P((X - \mu)^2 \ge t^2) \le \frac{E [ (}{}... $$

* $$ P(X \ge t) \le \frac{E(X)}{t} $$

#### Thus, for example, $$ P( \mid X - \mu \mid\ge 2 \sigma ) \le 1/4\\  P( \mid X - \mu \mid ...)\\  P(...)$$

### 第 11.13 例題 - Suppose that, on average, a post office handles 10,000 letters a day with a variance of 2,000.  ...the probability that this post office will handle between 8,000 and 12,000 letters tomorrow?
* $$ r.v. x$$：一天能處理的信件數 $$

![](graph1048.png)

* $$ P( \mid X - \mu \mid \ge t) \le \frac{\sigma^2}{t^2} $$
* $$ P(8000 \lt X \lt 12,000) $$
* $$ P( \mid X - 10000 \mid \le 2000) = 1-P( \mid X - 10000 \mid \lt 2000)\\
\ge \frac{1999}{2000} ...$$

### 第 11.14 例題：（百葉窗）A blind will fit Myra's bedroom's window if its width is between 41.5 and 42.5 inches.
![](graph1054.png)

* 利用 Chebyshev 定律，$$ \begin{align}
P( 41.5 \lt x \lt 42.5) &= P( \mid x - 42 \mid \le 0.5)\\ &= 1-P( \mid x-42\mid \gt 0.5) \le \frac{(0.25)^2}{(0.5)^2} = (\frac{1}{2})^2 = \frac{1}{4} 
\end{align} $$

### 第 11.15 例題：（骰子）Roll a die and let $$X$$ be the outcome.  Clearly, $$ E(X) = \frac{1}{6}(1+2+3+4+5+6) = \frac{21}{6}$$ $$ E(X^2) = \frac{1}{6}(1^2+2^2+3^2+4^2+5^2+6^2) = \frac{91}{6} $$
![](graph1103)

* Thus $$ Var(X) = 91/6 - 441/36 = 35/12 $$.  By Markov's inequality, $$ P(X \ge 6) \le \frac{21/6}{6} \approx 0.583 $$

* 用 Chebyshev 不等式結果會太大

### Chebyshev's 不等式與樣本平均值(sample mean)
![](graph1123)

* Let $$ X_1 , X_2, \cdots, X_n $$ be a random sample of size $$ n $$ from a (continuous or discrete) distribution function $$ F $$ with mean $$ \mu $$ and variance $$ \sigma^2 $$.  Let $$ \bar{X} $$ be the mean of the sample.  Then, by Lemma 10.1, $$ E( \bar{X}) = E( \frac{X_1 + X_2 + \cdots + X_n}{n}) = \mu $$,
* 依賴：期望值的線性特性

### 第 11.17 例題 - For the scores on an achievement test given to a certain population of students, the expected value is 500 and the standard deviation is 100.  Let $$ \bar{X} $$ be the mean of the scores of a random sample of 10 students.  Find a lower bound for $$ P(460 \lt \bar{X} \lt 540) $$.
* ![](graph1128)
* $$ P( \mid \bar{X} - 500 \mid \lt 40) = 1 - P( \mid \bar{X} - 500 \mid \gt 40 \le \frac{(100)^2}{(40)^2 \cdot 10} = \frac{10000}{16000} = \frac{5}{8} $$

### 第 11.18 例題：A biologist wants to estimate $$ l $$, the life expectancy of a certain type of insect.  To do so, he takes a sample of $$ n $$ and measures the lifetime from birth to death of each insect.
* $$ \begin{align}
P( \mid \bar{X} - l \mid \le 0.2) &\ge 0.98\\
= 1-P(\mid \bar{X} - l \mid \gt 0.2) &\ge 0.98 \\
\le \frac{105}{n \cdot (0.2)^2}
\end{align} $$
...

### 習題
3, 6, 7, 9

### 雜項
下下週五期末考

## 第 11.4 章<br>Laws of Large Numbers<br>大數法則
### independent and identically distributed(i.i.d.)
* 表示 $$ X_1, X_2, X_3, \cdots $$為**獨立**且**具有相同的分布函數、機率函數、期望值與變異數**
* $$ f_n \to f \雙箭頭 lim_{n \to \infnty} f_n = f $$
	* 微積分中的收斂
* 任意 $$ \epsilon > 0 $$，當 $$ n \ge N $$（當 $$n$$ 夠大）則$$ \mid f_n - f \mid \lt \epsilon $$

### 大數法則

### 第 11.4 例題 - Let $$ {X_1, X_2, \cdots $$ be a sequence of nonnegative independent random variables and, for all $$ i $$, suppose that the probability density function of $$ X_i $$ is $$f(x) =  \begin{cases} 4x(1-x)	if 0 \le x \le 1\\ 0	otherwise \end{cases}$$.  Find $$ lim_{n \to \infnty} \frac{X_1 + X_2 + \cdots ...}{}...$$

### 大數法則的應用

