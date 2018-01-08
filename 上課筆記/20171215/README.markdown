# 20171215上課筆記

## 習題討論

### 6-1 \#7: r.v. $$ x $$ 對稱 $$ \alpha $$，表示 $$ P(x \ge \alpha + x ) = P(x \le \alpha - x) $$
* $$ P(x \ge \alpha + x ) $$ 等價 $$ f(\alpha - x) = f(\alpha + x) $$
* 弄成分佈函數的關係：  
  $$ 1 - P(x \lt \alpha + x) = F(\alpha - x)\\
  \to 1 - F(\alpha + x) = F(\alpha - x) $$  
  兩邊對 $$ x $$ 微分： $$ - \frac{d}{dx} F(\alpha + x) = \frac{d}{dx} F(\alpha - x)\\
  -f(\alpha + x) \cdot 1 = f(\alpha -x)(-1)\\
  \to f(\alpha + x) = f(\alpha - x) \\
  \int^f_{-\infty} f(\alpha - x) dx = \int^f_{-\infty} f( \alpha + x)dx \\
  \vdots\\
  f(x) = \frac{1}{\sqrt{2\pi}} e ^{-\frac{(x + 3)^2}{v} }$$

### 5-2 #15: 
* 先求一月份中*一天*（31 天）沒有事故的機率
* $$ N(t) ~ Poi(\lambda t) = Poi(3t) $$
* $$ \begin{align*}
\lambda &= E(N(1))\\
&= 3 ( ^次/_天 )
\end{align*} $$
* $$ \to N(1) ~ Poi(3) $$
* $$ P(N(1) = 0) = \frac{e^{-3} \cdot 3^0}{0!} = e^{-3} + p $$

### ?
* $$ \lambda = 35 $$
* r.v.x. 空房間的(?
* $$ Poi(35) = P( X \ge 30) = 1 - \sum^{29}_{n = 0}P(X = n) $$
* $$ P(x=n)... $$

### 5-1 #14
![image 1042]()

* 取100個數字，四捨五入到小數點第三位

![image 1043]()

* 100個組合中，*至少*有一個是 $$ 0.345 \cdots $$ $$ \to $$ 用餘事件來作
* $$ 1 - 沒有 0.345（不是 0.345） $$
* $$ 1 - \frac{1}{1000} = \frac{999}{1000} $$
* 用餘事件來解
* $$ 1 - (\frac{999}{1000}^{100} $$

### 5-3 #3:
* $$ r.v.x.: $$ 識別把門打開的鑰匙個數$$
* $$ r.v.x ~ (\pi e_0 (P = \frac{1}{1^2}))?$$
* ...

### 6.2 #3
* $$ f(x) = \begin{cases} e^{-x}, x \gt 0\\
e, ??? \end{cases} $$
* 用 transformation 方法
* $$ \begin{align*}
Y &= x \sqrt{x} 的 p.d.f.\\
&= e^{-x}\\
Y^{\frac{2}{3}} &= h(x) = x^{\frac{3}{2}}^{\frac{2}{3}} 
\end{align*} $$
* $$ Y^{\frac{2}{3} = x = h^{-1}(y)\\
(h^{-1})^1 y^2 = \frac{2}{3}- \frac{1}{3} $$
* f_y(y) = f_x(h^{-1}(y)) \cdot \mid (h^{-1}^1(y))

