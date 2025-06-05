# Zmienne losowe ciągłe

<h3>Zmienna losowa ciągła</h3>
W skrócie jest to funkcja, która przypisuje liczby zdarzeniom elementarnym. Zmienna losowa jest określona na przestrzeni zdarzeń elementarnych a jej wartości są ze zbioru liczb rzeczywistych. Zmienna losowa jest ciągła jeśli jej zbiór wartości jest ciągły.

<h3>Rozkład prawdopodobieństwa</h3>
Jest to miara probabilistyczna (nie będę wnikał co to jest) przypisująca prawdopodobieństwa zbiorom wartości danej zmiennej, odpowiadającym zdarzeniom elementarnym.

Dla zmiennej losowej ciągłej wprowadzamy funkcję gęstości prawdopodobieństwa. Jest to funkcja określona na zbiorze liczb rzeczywistych posiadająca następujące własności:

*   jest nieujemna:

    $$f(x) \ge 0,$$

*   prawdopodobieństwo tego, że zmienna losowa przyjmie wartość z przedziału $(a,b]$, to:

    $$P( a< X \le b) = \int\limits_a^b f(x) dx,$$

*   Prawdopodobieństwo tego, że zmienna losowa przyjmie dowolną wartość to:

    $$P(-\infty < X \le +\infty) = \int\limits_{-\infty}^{+\infty} f(x) dx = 1 $$

<h3>Dystrybuanta</h3>
Dystrybuantą zmiennej losowej $X$ nazywamy funkcję $F(x)$ określoną na zbiorze liczb rzeczywistych jako: 

$$F(x) = P(X \le x)$$

Dla zmiennej ciągłej z funkcją gęstości prawdopodobieństwa $f$:

$$F(x) = P(X \le x)= \int\limits_{-\infty}^x f(s) ds $$

<h3>Własności dystrybuanty</h3>
* $0 \le F(x) \le 1,$
* $F(x_1) \le F(x_2) \text{ dla $x_1 \le x_2$},$
* $\lim\limits_{x \to -\infty} F(x) = 0,$
* $\lim\limits_{x \to \infty} F(x) = 1,$
* $F$ jest prawostronnie ciągła.

<h3>Wartość oczekiwana</h3>
Wartość oczekiwana zmiennej losowej $X$ określona jest wzorem:

$$E(X) = \int\limits_{-\infty}^\infty xf(x)dx.$$

Jest to pierwszy moment niecentralny. Momenty niecentralne można zdefiniować następująco:

$$E(X^i) = \int\limits_{-\infty}^\infty x^if(x)dx.$$


<h3>Własności wartości oczekiwanej</h3>
* $E(c) = c,$
* $E(aX+b) = aE(X) + b,$
* $E(X + Y) = E(X) + E(Y),$
* $E(X - Y) = E(X) - E(Y),$
* $E(X_1+X_2+...+X_n)=E(X_1)+E(X_2)+...+E(X_n),$
* Jeżeli zmienne losowe $X$ i $Y$ są niezależne to $E(XY)=E(X)E(Y).$
* Twierdzenie LOTUS:

$$E[g(X)]=\int\limits_{-\infty}^\infty g(x)f_X(x)dx.$$

<h3>Warunkowa wartość oczekiwana</h3>

Jeżeli zmienna $X$ jest ciągła a zmienna $Y$ dyskretna:

$$\mu_{X|Y=y} = E(X|Y=y) = \int\limits_{-\infty}^\infty x f_X(x|Y=y)dx,$$

gdzie:

$$f_X(x|Y=y) = \frac{f_{X,Y}(x, y)}{P(Y=y)},$$

$f_{X,Y}(x, y)$ - jest to rozkład łączny zmiennej $X$ i $Y$.

Jeżeli obie zmienne są ciągłe to:

$$\mu_{X|Y=y} = E(X|Y=y) = \int\limits_{-\infty}^\infty x f_X(x|y)dx,$$

gdzie:

$$f_X(x|y) = \frac{f_{X,Y}(x, y)}{f_Y(y)},$$

$f_Y(y)$ - jest to gęstość zmiennej $Y$.

<h3>Wariancja</h3>
Wariancja zmiennej losowej $X$ określona jest wzorem:

$$Var(X) = \int\limits_{-\infty}^\infty [x - E(X)]^2 f(x)dx,$$

można zapisać również:

$$Var(X) = E\{[X - E(X)]^2\}.$$

Jest to drugi moment centralny. Momenty centralne można zdefiniować następująco:
$$\mu_k = E\{[X - E(X)]^k\}.$$

Definiowane jest odchylenie standardowe jako pierwiastek z wariancji:

$$D(X) = \sqrt{Var(X)}.$$

Odchylenie standardowe to nie pierwszy moment centralny.

<h3>Własności wariancji</h3>
* $Var(X)=E(X^2)-[E(X)]^2,$
* $Var(c)=0,$
* $Var(a\cdot X)=a^2\cdot Var(X),$
* $D^{2}(X+b)=D^{2}(X),$
* $ D^{2}(X\pm Y)=D^{2}(X)+D^{2}(Y)\pm 2 Cov(X,Y)$
* jeżeli zmienne losowe $X$ i $Y$ są niezależne to $D^{2}(X\pm Y)=D^{2}(X)+D^{2}(Y).$

<h3>Warunkowa wariancja</h3>

$$Var(X|Y) = E(X^2|Y)-[E(X|Y)]^2 = E[(X-\mu_{X|Y})^2|Y]$$

<h3>Mediana</h3>
Kwantylem rzędu $p$, gdzie $0\le p\le 1$, w rozkładzie empirycznym $P_{X}$ zmiennej losowej $X$ nazywamy taką wartość $x_{p}$ zmiennej losowej $X$  dla której spełnione są nierówności:

$P_{X}((-\infty, x_{p}]) \ge p$

oraz

$P_{X}([x_{p}, \infty)) \ge 1 - p.$

Kwantyl rzędu $\frac{1}{2}$ to inaczej mediana.

<h3>Dominanta</h3>
Dominanta to statystyka dla zmiennych o rozkładzie dyskretnym, wskazująca na wartość o największym prawdopodobieństwie wystąpienia.

<h3>Współczynnik zmienności</h3>

$$v = \frac{D(X)}{E(X)}.$$

<h3>Współczynnik asymetrii</h3>

$$A = \frac{\mu_3}{D^3(X)}.$$

<h3>Twierdzenie 1</h3>
Jeżeli $X = h(Y)$ to zmienna losowa $Y$ ma gęstość:

$$f_Y(y) = f_X(h(y))\cdot |h'(y)|.$$

<h3>Rozkład jednostajny</h3>
Ciągły rozkład prawdopodobieństwa, dla którego gęstość prawdopodobieństwa w przedziale od $a$ do $b$ jest stała i różna od zera, a poza nim równa zeru.

Funkcja rozkładu prawdopodobieństwa:

$$
f(x)=
\begin{cases}
\frac{1}{b-a} & \text{dla } a\leq x\leq b,            \\
0             & \text{dla } x < a \text{ lub } x > b. \\
\end{cases}
$$

Dystrybuanta:

$$
F(x)={\begin{cases}
0                    & {\text{dla }} x<a,\\
{\frac {x-a}{b-a}}   & {\text{dla }} a\leq x\leq b,\\
1                    & {\text{dla }} x>b.
\end{cases}}
$$

Wartość oczekiwana:

$$E(X) = \frac{a+b}{2}.$$

Wariancja:

$$Var(X) = \frac{(a-b)^2}{12}.$$

<h3>Rozkład wykładniczy</h3>
Funkcja rozkładu prawdopodobieństwa:

$$
f(x; \lambda) =
\begin{cases}
\lambda e^{-\lambda x} & x \ge 0, \\
0                      & x < 0.
\end{cases}$$

Dystrybuanta:

$$
F(x;\lambda) = 
\begin{cases}
1-e^{-\lambda x} & x \ge 0, \\
0                & x < 0.
\end{cases}
$$

Wartość oczekiwana:

$$E(X) = \frac{1}{\lambda}.$$

Wariancja:

$$Var(X) = \frac{1}{\lambda^2}.$$

<h3>Rozkład normalny</h3>
Funkcja rozkładu prawdopodobieństwa:

$$f_{\mu ,\sigma }(x)={\frac {1}{\sigma {\sqrt {2\pi }}}}\,\exp \left({\frac {-(x-\mu )^{2}}{2\sigma ^{2}}}\right).$$

Wartość oczekiwana:

$$E(X) = \mu.$$

Wariancja:

$$Var(X) = \sigma^2.$$

Funkcja tworząca momenty:

$$M_{X}(t)=\exp \left(\mu \,t+{\frac {\sigma ^{2}t^{2}}{2}}\right)$$

<h3>Rozkład gamma</h3>
Funkcja rozkładu prawdopodobieństwa:

$${\begin{aligned}f(x;\alpha ,\beta )&={\frac {\beta ^{\alpha }x^{\alpha -1}e^{-\beta x}}{\Gamma (\alpha )}}\quad {\text{ dla }}x>0\quad \alpha ,\beta >0, \end{aligned}}$$

gdzie $\Gamma(\alpha)$ jest funkcją gamma. Dla dodatnich liczb całkowitych $\Gamma(\alpha )=(\alpha -1)!$.

Wartość oczekiwana:

$$E(X) = \frac{\alpha}{\beta}.$$

Wariancja:

$$Var(X) = \frac{\alpha}{\beta^2}.$$