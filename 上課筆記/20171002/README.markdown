# 2017/10/02 筆記
## 第 3.2 章<br>Law of Multiplication
### (missed to 1323)

### 第 3.11 例題

#### Solution
* $$ \begin{align*}
P(G_1D_2D_3 OR D_1 G_2 D_3)\\
&= P(G_1 D_2 D_3) + P(D_1 G_2 D_3)\\
&= P(G_1) \cdot P(D_2 | G_1) \cdot P(D_3 | G_1 D_2) + P(D_1)\cdot P(G_2 | D_1)\cdot P(D_3 | P_1 G_2)\\
&= \frac{5}{7} \cdot \frac{2}{6} \cdot {1}{5} + \frac{2}{7} \frac{5}{6} \frac{1}{5}
\end{align*}$$

### 習題
1, 3, 5, 9

## 第 3.3 章<br>Law of Total Probability
### 第 3.3 定理<br>Law of Total Probability
* ex. $$ A = AS = A(B OR B^C) = AB OR AB^C \to P(A) = P(AB) + P(AB^C) = P(B)\cdot P(A|B) $$

### 第 3.12 例題 - An insurance company rents 35% of the cars for its customers from agency I and 65% from agency II.  If 8% of the cars of agency I and 5% of the cars of agency II break down during the rental periods, what is the probability that a car rented by this insurance company breaks down?

#### Solution
令 B 事件為租到車子事故障車  
I：車子來自 I 代理商  
II: 車子來自 II 代理商

$$\begin{align*}
P(B) &= P(I) \cdot P(B|I) + P(II) \cdot P(B|II) \\
&= (0.35)(0.08) + (0.65)\cdot(0.05)
\end{align*}$$

### 第 3.13 例題 - In a trial, the judge is 65% sure that Susan has committed a crime.  Julie and Robert are two witnesses who know whether Susan is innocent or guilty.  However, Robet is Susan's friend and will lie with probability 0.25 if Susan is guilty.  He will tell the truth if she is innocent.  Julie is Susan's enemy and will lie with probability 0.30 if Susan is innocent.  She will tell the truth if Susan is guilty.  What is the probability that, in the course of the trial, Robert and Julie will give conflicting testimony?

#### Solution
* 令 Robert and Julie will give conflicting testimony 事件為 $$ C $$
* I: 有罪之下作偽證
* G: 無罪之下作偽證
* $$\begin{align*}
P(C) &= P(I) \cdot P(C|I) + P(I^C) \cdot P(c|I^C)
&= 0.35 \cdot (0.3)^2 (missed 1346)
\end{align*}$$

### 第 3.14 例題 - Gambler's Ruin Problem - Two gamblers play a game of "heads or tails", in which each time a fair coin lands heads up player A wins $1 from B, and each time it lands tails up, player B wins $1 from A.  Suppose that player A initially has $$a$$ dollars and player B has $$b$$ dollars.  If they continue to play this game successively, what is the probability that (a) A will be ruined; (b) the game goes forever with nobody winning.

#### Solution
* 令 $$ E $$ 為開始有 $$i$$ dollars 而最終破產的事件，且 $$p_i = P(E) $$，想求 $$p_a$$

### 注意事項
* 10/6 給習題（10/13要交且檢討）
* 10/16 小考