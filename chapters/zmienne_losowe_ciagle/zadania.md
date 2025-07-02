# Zadania

## Zadanie 1
Zmienna losowa $X$ ma rozkład jednostajny na przedziale $[a, b]$. Oblicz $E(X)$ oraz $Var(X)$.

```{dropdown} Rozwiązanie

Wartość oczekiwana:

$\begin{aligned}E(X) &= \int\limits_{-\infty}^\infty xf(x)dx = \int\limits_{-\infty}^a x0dx + \int\limits_a^b x\frac{1}{b-a}dx + \int\limits_b^\infty x0dx = \\
&= \int\limits_a^b x\frac{1}{b-a}dx = \frac{1}{b-a}\int\limits_a^b xdx = \\
&= \frac{1}{b-a}\frac{x^2}{2}\bigr|_a^b = \frac{1}{b-a}\frac{b^2 - a^2}{2} = \\
&= \frac{(b-a)(b+a)}{2(b-a)} = \frac{b+a}{2}.\end{aligned}$

Wariancja:

$\begin{aligned}E(X^2) &= \int\limits_{-\infty}^\infty x^2f(x)dx = \int\limits_a^b x^2\frac{1}{b-a}dx = \\
&= \frac{1}{b-a}\int\limits_a^b x^2dx = \frac{1}{b-a}\frac{x^3}{3}\bigr|_a^b = \\
&= \frac{1}{b-a}\frac{b^3 - a^3}{3} = \frac{(b-a)(b^2+ab+a^2)}{3(b-a)} = \\
&= \frac{b^2+ab+a^2}{3}\end{aligned}$

$\begin{aligned}Var(X) &= E(X^2) - [E(X)]^2 = \frac{b^2+ab+a^2}{3} - \left(\frac{b+a}{2}\right)^2 = \\
&= \frac{4b^2+4ab+4a^2}{12} -\frac{3b^2+6ab+3a^2}{12} = \frac{b^2-2ab+a^2}{12} = \\
&= \frac{(b-a)^2}{12}.\end{aligned}$

Można obliczyć wariancję z definicji ale wtedy jest dłużej bo jest więcej całek do liczenia.

Obliczę też dystrybuantę:

$\int\limits_a^x \frac{1}{b-a} dt = \frac{1}{b-a}t\bigr|_a^x = \frac{x-a}{b-a}$

$
F(x)={\begin{cases}
0                    & \text{dla } x<a,\\
{\frac {x-a}{b-a}}   & \text{dla } a\leq x\leq b,\\
1                    & \text{dla } x>b.
\end{cases}}
$
```

## Zadanie 2
Czas opóźnienia pociągu (w minutach) na pewnej trasie jest zmienną losową $X$ o gęstości:

$f(x) =
\begin{cases}
0 & \text{dla } x \notin [0, 10], \\
Cx & \text{dla } x \in [0, 10].
\end{cases}$

Oblicz:\
a) stałą $C$,\
b) $E(X)$, $Var(X)$,\
c) $P(X>5)$.\
d) Wyznacz dystrybuantę zmiennej losowej $X$.

```{dropdown} Rozwiązanie

a)

Całka z gęstości prawdopodobieństwa musi równać się 1, więc:

$1 = \int\limits_0^{10}C xdx = C\frac{x^2}{2} \bigr|_0^{10} = C\frac{100-0}{2} = 50C$

$C = \frac{1}{50}$

$f(x) =
\begin{cases}
0            & \text{dla } x \notin [0, 10], \\
\frac{x}{50} & \text{dla } x \in [0, 10].
\end{cases}$

b)

$E(X) = \int\limits_0^{10}x\frac{x}{50}dx=\frac{1}{50}\int\limits_0^{10}x^2dx = \frac{1}{50} \frac{x^3}{3} \bigr|_0^{10} = \frac{1000}{150} = \frac{20}{3}.$

$E(X^2) = \frac{1}{50}\int\limits_0^{10}x^3dx = \frac{1}{50} \frac{x^4}{4} \bigr|_0^{10} = \frac{10000}{200} = 50.$

$Var(X) = 50 - \left( \frac{20}{3} \right)^2 = \frac{450}{9} - \frac{400}{9}= \frac{50}{9}.$

c)

$P(X>5) = \int\limits_5^{10}\frac{x}{50}dx = \frac{1}{50} \frac{x^2}{2} \bigr|_5^{10} = \frac{1}{100}(100-25)=0.75.$

d)

$\int\limits_0^x \frac{t}{50}dt = \frac{t^2}{100} \bigr|_0^x = \frac{x^2}{100}$

$
F(x)=
\begin{cases}
0               & \text{dla } x < 0, \\
\frac{x^2}{100} & \text{dla } x \in [0, 10], \\
1               & \text{dla } x > 10.
\end{cases}$

Poprzedni podpunkt obliczony za pomocą dystrybuanty:

$P(X>5) = 1 - P(X \le 5) = 1 - \frac{5^2}{100} = 0.75.$
```

## Zadanie 3
Zmienna losowa $Y$ ma dystrybuantę $F(y) = A + B \cdot arctg(y),$ $y \in (-\infty, \infty)$. Wyznacz stałe $A$ i $B$.

```{dropdown} Rozwiązanie

Należy skorzystać z własności dystrybuanty:

$
\begin{cases}
0 = \lim\limits_{y\to -\infty}A + B \cdot arctg(y) = A - \frac{\pi}{2}B \\
1 = \lim\limits_{y\to -\infty}A + B \cdot arctg(y) = A + \frac{\pi}{2}B
\end{cases}$

Dodaję stronami:

$1 = 2A$

$\begin{cases}
A = \frac{1}{2} \\
B = \frac{1}{\pi}
\end{cases}$
```

## Zadanie 4
Czas oczekiwania na połączenie z siecią informatyczną losowo wybranego klienta jest zmienną losową $X$ o rozkładzie wykładniczym o wartości średniej 0.5 minuty.\
a) Jaka jest wariancja czasu oczekiwania na połączenie z siecią?\
b) Oblicz prawdopodobieństwo warunkowe, że klient będzie czekał co najmniej 2 minuty, jeśli czeka już 1 minutę.

```{dropdown} Rozwiązanie

$\begin{aligned}E(X) &= \int\limits_0^\infty x\lambda e^{-\lambda x}dx = \lambda\int\limits_0^\infty x \left(\frac{e^{-\lambda x}}{-\lambda}\right)'dx = \\
&= \left. \lambda \left( xe^{-\lambda x} + \frac{1}{\lambda}  \int\limits_0^\infty e^{-\lambda x}dx \right) \right|_0^\infty = \left. \lambda \left(xe^{-\lambda x} - \frac{1}{\lambda^2} e^{-\lambda x}\right) \right|_0^\infty = \\
&= \left. \left(\lambda xe^{-\lambda x} - \frac{1}{\lambda} e^{-\lambda x}\right) \right|_0^\infty = \lim\limits_{x\to\infty} \left(\lambda xe^{-\lambda x} - \frac{1}{\lambda} e^{-\lambda x}\right) - \frac{1}{-\lambda} = \\
&=\lim\limits_{x\to\infty} \left(\lambda \frac{x}{e^{\lambda x}} - \frac{1}{\lambda} \frac{1}{e^{\lambda x}} \right) + \frac{1}{\lambda} = \lim\limits_{x\to\infty} \left(\lambda \frac{(x)'}{\left(e^{\lambda x}\right)'} - \frac{1}{\lambda} \frac{1}{e^{\lambda x}} \right) + \frac{1}{\lambda} = \\
&= \lim\limits_{x\to\infty} \left(\lambda \frac{1}{\lambda e^{\lambda x}} - \frac{1}{\lambda} \frac{1}{e^{\lambda x}} \right) + \frac{1}{\lambda} = 0 - 0 + \frac{1}{\lambda} = \\
&= \frac{1}{\lambda}\end{aligned}$

$\begin{aligned}E(X^2) &= \int\limits_0^\infty x^2 \lambda e^{-\lambda x}dx = \lambda \int\limits_0^\infty x^2 \left(\frac{e^{-\lambda x}}{-\lambda}\right)'dx = \\
&= \left. \lambda \left( x^2e^{-\lambda x} + \frac{2}{\lambda} \int\limits_0^\infty x e^{-\lambda x}dx \right) \right|_0^\infty = \\
&= \left. \lambda \left[ x^2e^{-\lambda x} + \frac{2}{\lambda} \int\limits_0^\infty x \left(\frac{e^{-\lambda x}}{-\lambda}\right)'dx \right] \right|_0^\infty = \\
&= \left. \lambda \left[ x^2e^{-\lambda x} + \frac{2}{\lambda}\left( xe^{\lambda x} + \frac{1}{\lambda} \int\limits_0^\infty e^{-\lambda x}dx \right) \right] \right|_0^\infty = \\
&= \lambda \left. \left[ x^2e^{-\lambda x} + \frac{2}{\lambda}\left( xe^{\lambda x} - \frac{1}{\lambda^2} e^{-\lambda x} \right) \right] \right|_0^\infty = \\
&=  \left. \left[ \lambda x^2e^{-\lambda x} + 2 \left( xe^{\lambda x} - \frac{1}{\lambda^2} e^{-\lambda x} \right) \right] \right|_0^\infty = \\
&= \left. \left( \lambda x^2e^{-\lambda x} + 2xe^{\lambda x} - \frac{2}{\lambda^2} e^{-\lambda x} \right) \right|_0^\infty = \\
&= \lim_{x\to\infty} \left( \lambda x^2e^{-\lambda x} + 2xe^{\lambda x} - \frac{2}{\lambda^2} e^{-\lambda x} \right) - \left(-\frac{2}{\lambda^2}\right) = \\
&= \lim_{x\to\infty} \left( \lambda \frac{(x^2)''}{(e^{\lambda x})''} + 2\frac{(x)'}{(e^{\lambda x})'} - \frac{2}{\lambda^2} \frac{1}{e^{\lambda x}} \right) + \frac{2}{\lambda^2} = \\
&= \lim_{x\to\infty} \left( \lambda \frac{2}{\lambda^2e^{\lambda x}} + 2\frac{1}{\lambda e^{\lambda x}} - \frac{2}{\lambda^2} \frac{1}{e^{\lambda x}}  \right) + \frac{2}{\lambda^2} = \\
&= 0 + 0 - 0 + \frac{2}{\lambda^2} = \frac{2}{\lambda^2}\end{aligned}$

$Var(X) = \frac{2}{\lambda^2} - \left( \frac{1}{\lambda} \right)^2 = \frac{2}{\lambda^2} - \frac{1}{\lambda^2} = \frac{1}{\lambda^2}$

Dla danych z zadania:

$E(X) = 0.5 = \frac{1}{\lambda}$

$\lambda = 2$

$Var(X) = \frac{1}{2^2} = \frac{1}{4}$

Obliczę też dystrybuantę:

$\int\limits_0^x \lambda e^{-\lambda t}dt = -e^{-\lambda t}\bigr|_0^x = 1-e^{-\lambda x},$

$
F(x) = 
\begin{cases}
1-e^{-\lambda x} & x \ge 0, \\
0                & x < 0.
\end{cases}
$

b)

$A$ - czeka co najmniej dwie minuty\
$B$ - czeka co najmniej jedną minutę

$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(A)}{P(B)} = \frac{1-P(A')}{1-P(B')} = \frac{1-1+e^{-2\cdot2}}{1-1+e^{-2\cdot1}} = \frac{e^{-4}}{e^{-2}} = e^{-2}$
```

## Zadanie 5
Udowodnij tak zwaną własność braku pamięci rozkładu wykładniczego, tzn. wykaż, że dla zmiennej losowej Y o rozkładzie wykładniczym zachodzi:
$P(Y>y+h|Y>y) = P(Y>h)$, dla dowolnego $y$ i $h>0$.

```{dropdown} Rozwiązanie

$\begin{aligned}P(Y>y+h|Y>y) &= \frac{P(Y>y+h \cap Y>y)}{P(Y>y)} = \frac{P(Y>y+h)}{P(Y>y)} = \\ 
&= \frac{1-P(Y\le y+h)}{1-P(Y\le y)} = \frac{1-1+e^{-\lambda(y+h)}}{1-1+e^{-\lambda y}} = \\
&= e^{-\lambda h} = 1 - \left( 1 - e^{-\lambda h} \right) = \\
&= 1 - P(Y \le h) = \\
&= P(Y > h).\end{aligned}$
```

## Zadanie 6
Zmienna losowa $X$ ma dystrybuantę postaci:

$F(x)=
\begin{cases}
0              & \text{dla } x<0, \\
C              & \text{dla } x=0, \\
1 - 0.5e^{-3x} & \text{dla } x<0.
\end{cases}$

a) Znajdź stałą $C$.\
b) Znajdź dystrybuantę warunkową $P(X \le x |X>0), \ x\in (-\infty, \infty)$.\
c) Oblicz $E(X|X>0)$.

````{dropdown} Rozwiązanie

a)

Dystrybuanta musi być prawostronnie ciągła i rosnąca:

$\lim\limits_{x\to 0^+}F(x) \ge C = F(0) = 1-0.5e^{-3 \cdot 0} = \frac{1}{2}$

b)

Dla $x \ge 0$:

$\begin{aligned}P(X \le x |X > 0) &= \frac{P(X \le x \cap X > 0)}{P(X > 0)} = \frac{P(0 < X \le x)}{P(X > 0)} = \\
&= \frac{P(X\le x) - P(X\le0)}{1-P(X\le0)} = \frac{1 - 0.5e^{-3x} - \frac{1}{2}}{1 - \frac{1}{2}} = \\
&= 1-e^{-3x}.\end{aligned}$

Dla $x < 0$

$P(X \le x |X > 0) = \frac{P(X\le x \cap X > 0)}{P(X > 0)} = \frac{\emptyset}{P(X > 0)}=0.$

$
P(X \le x |X > 0) = 
\begin{cases}
0         & \text{dla } x<0, \\
1-e^{-3x} & \text{dla } x \ge 0.
\end{cases}$

c)


$E(X|X>0) = E(X)$,

Wyznaczam gęstość $X$ (pochodną dystrybuanty):

$
f(x) = 
\begin{cases}
0          & \text{dla } x\le0, \\
1.5e^{-3x} & \text{dla } x > 0.
\end{cases}$

$E(X) = \int\limits_0^\infty 1.5xe^{-3x}$

Całka w Pythonie:

```python
import scipy.integrate as integrate
import numpy as np

def f(x):
  return 1.5*x*np.exp(-3*x)

result = integrate.quad(f, 0, np.inf)[0]

print("Wartosc oczekiwana:", result)
```
````

## Zadanie 7
Dochód brutto firmy w losowo wybranym miesiącu jest zmienną losową $X$ o rozkładzie normalnym z wartością średnią $\mu = 100$ (w tys. zł) i odchyleniem standardowym $\sigma = 10$ (w tys. zł). Dochód netto jest obliczany zgodnie ze wzorem: $Y = 0.9X-20$ (tys. zł).\
a) Oblicz wartość oczekiwaną i wariancję dochodu netto firmy w losowym miesiącu.\
b) Oblicz prawdopodobieństwo, że w losowo wybranym miesiącu dochód netto przekroczy 50 000 zł.

````{dropdown} Rozwiązanie

a)

$E(Y) = E(0.9X-20) = 0.9E(X)-20 = 0.9\cdot100-20 = 70,$

$Var(Y) = Var(0.9X-20) = 0.9^2Var(X) = 0.9^2\cdot 100 = 81$

b)

$\begin{aligned}P(Y > 50) &= P(0.9X-20 > 50) = P(X > \frac{50+20}{0.9}) \approx \\
&\approx P(X > 77.78) = 1-P(X \le 77.78)\end{aligned}$

Można też ustandaryzować rozkład:

$P(Z > \frac{77.78 - 100}{10}) = P(Z>-2.222) = P(Z<2.222)$

```python
import scipy.stats as st

print(1 - st.norm.cdf(77.78, 100, 10))
print(st.norm.cdf(2.222))
```
````

## Zadanie 8
Czas codziennego dojazdu do pracy Jacka (w minutach) jest zmienną losową o rozkładzie jednostajnym na przedziale $[30, 50]$. Jaki jest maksymalny czas dojazdu do pracy, którego nie przekracza 50% dojazdów do pracy Jacka.

```{dropdown} Rozwiązanie

Należy obliczyć medianę. Z dystrybuanty rozkładu jednostajnego:

$\frac{x-30}{50-30}=0.5$

$x = 40$
```

## Zadanie 9
Zmienna losowa $X$ pochodzi z rozkładu wykładniczego z parametrem 2. Niech $Y=X^2$.\
a) Oblicz $EY$.\
b) Znajdź gęstość zmiennej $Y$.

````{dropdown} Rozwiązanie

Gęstość rozkładu wykładniczego:

$
f(x; \lambda) =
\begin{cases}
\lambda e^{-\lambda x} & x \ge 0, \\
0                      & x < 0.
\end{cases}$

Dystrybuanta:

$
F(x;\lambda) = 
\begin{cases}
1-e^{-\lambda x} & x \ge 0, \\
0                & x < 0.
\end{cases}
$

a)

$E(Y) = E(X^2) = \int\limits_0^\infty 2x^2e^{-2x}=\frac{1}{2}.$

```python
import scipy.integrate as integrate
import numpy as np

def f(x):
  return 2*x**2*np.exp(-2*x)

result = integrate.quad(f, 0, np.inf)[0]

print("Wartosc oczekiwana:", result)
```

b)

$F_Y(t) = P(Y\le t) = P(X^2\le t) = P(X\le \sqrt{t}) = 1-e^{-\lambda \sqrt{t}}$

$f_Y(t) = F_Y'(t) = (-e^{-\lambda \sqrt{t}})(-\frac{1}{2}\lambda t^{-\frac{1}{2}}) = \frac{\lambda}{2\sqrt{t}}e^{-\lambda \sqrt{t}}$

```python
import scipy.stats as st

print(2*st.norm.cdf(-1))
print(1 + st.norm.cdf(0, 3, 5) - st.norm.cdf(2,3,5))
```
````

## Zadanie 10
Zmienna losowa $X$ ma gęstość określoną wzorem:

$
f(x) =
\begin{cases}
3e^{3x} & x < 0, \\
0       & x \ge 0.
\end{cases}$

Znajdź gęstość i dystrybuantę zmiennej losowej $Y = X^3+2$.

```{dropdown} Rozwiązanie

Na początku należy znaleźć dystrybuantę zmiennej losowej $X$:

$F_X(t) = 3\int\limits_{-\infty}^t e^{3x}dx = e^{3t},$ dla $x < 0$

$F_Y(y) = P(X^3+2\le y) = P(X\le (y-2)^\frac{1}{3}) = e^{3(y-2)^\frac{1}{3}}$, dla $x < 0$.

$f_Y(y) = F_Y'(y) = \frac{e^{3(y-2)^\frac{1}{3}}}{(y-2)^\frac{2}{3}}$, dla $x < 0$.
```

## Zadanie 11
Gęstością zmiennej losowej $Z$ jest funkcja:

$f(z) = 0.5e^{-|z|},\ z \in(-\infty, \infty).$

a) Wyznacz dystrybuantę zmiennej losowej $Z$.\
b) Oblicz $E(Z)$.\
c) Oblicz $P(|Z|<1)$.

````{dropdown} Rozwiązanie

a)

$\begin{cases}
|z| = z  & \text{dla } z \ge 0,\\
|z| = -z & \text{dla } z < 0,
\end{cases}$

Dla $z < 0$:

$\int\limits_{-\infty}^t 0.5e^zdz = 0.5e^t$

Dla $z \ge 0$:

$0.5e^0 + \int\limits_0^t 0.5e^{-z}dz = 1-0.5e^{-t}$

Ostatecznie:

$F_Z(t) = \begin{cases}
0.5e^t      & \text{dla } t < 0, \\
1-0.5e^{-t} & \text{dla } t \ge 0.
\end{cases}$

b)

$E(Z) = \int\limits_{-\infty}^\infty 0.5ze^{-|z|}dz = 0$

```python
import scipy.integrate as integrate
import numpy as np

def f(x):
  return 0.5*x*np.exp(-abs(x))

result = integrate.quad(f, -np.inf, np.inf)[0]

print("Wartosc oczekiwana:", result)
```

c)

$\begin{aligned}P(|Z| < 1) &= P(-1 < Z < 1) = P(Z < 1)-P(Z < -1) = \\
&= 1-0.5e^{-1}-0.5e^{-1} \approx 0.63\end{aligned}$
````

## Zadanie 12
Zmienna losowa $X$ ma rozkład wykładniczy z parametrem $\lambda = 0.2$. Niech $Y = min(X,2)+1$.\
a) Oblicz $P(Y<2)$, $P(Y>3)$.\
b) Wyznacz dystrybuantę $F_Y$ zmiennej losowej $Y$.

```{dropdown} Rozwiązanie

a)

$\begin{aligned}P(Y < 2) &= P(\min(X,2) + 1 < 2) = P(\min(X,2) < 1) = \\
&= 1 - P(\min(X,2) \ge 1) = 1 - P(X \ge 1, 2 \ge 1) = \\
&= 1 - (1 - P(X < 1)) = P(X < 1) = \\
&= 1 - e^{-0.2} = 0.181.\end{aligned}$

$\begin{aligned}P(Y>3) &= P(\min(X,2) + 1 > 3) = P(\min(X,2) > 2) = \\
&= P(X > 2, 2 > 2) = 0, \text{ bo } P(2>2) = 0.\end{aligned}$

b)

$\begin{aligned}P(Y \le t) &= P(\min(X,2) + 1 \le t) = P(\min(X,2) \le t - 1) = \\
&= 1 - P(\min(X,2) > t - 1) = 1 - P(X>t-1, t<3).\end{aligned}$

Dla $t<3$:

$1 - P(X>t-1, t<3) = 1 - P(X>t-1) = P(X \le t-1) = 1-e^{-0.2(t-1)}.$

Dla $t \ge 3$:

$1 - P(X>t-1, t<3) = 1.$

Szukana dystrybuanta:

$F_Y(t)=
\begin{cases}
0               & \text{dla } t<1, \\
1-e^{-0.2(t-1)} & \text{dla } t \in [1, 3), \\
1               & \text{dla } t\ge 3.
\end{cases}$
```

## Zadanie 13
Zmienna losowa $X$ ma rozkład jednostajny $U(0,1)$. Niech $Y=2X+3$. Znajdź gęstość $f_Y$ zmiennej $Y$.

```{dropdown} Rozwiązanie

$P(Y \le t) = P(2X+3) = P(X \le \frac{t-3}{2}) = F_X(\frac{t-3}{2}) = \frac{\frac{t-3}{2}-0}{1-0} = \frac{t-3}{2}$

$F_Y(t)=
\begin{cases}
0             & \text{dla } t<3, \\
\frac{t-3}{2} & \text{dla } t \in [3, 5), \\
1             & \text{dla } t \ge 5.
\end{cases}$

Obliczam pochodną dystrybuanty aby otrzymać gęstość:

$f_Y(t)=
\begin{cases}
0           & \text{dla } t \notin [3, 5], \\
\frac{1}{2} & \text{dla } t \in [3, 5], \\
\end{cases}$
```

## Zadanie 14
Gęstością zmiennej losowej $T$ jest funkcja:

$f_T(t)=
\begin{cases}
0  & \text{dla } t \notin (0, 1), \\
2t & \text{dla } t \in (0, 1), \\
\end{cases}$

Zmienna losowa $X$ określona jest wzorem $X = -T^3 + 1$.\
a) Znajdź gęstość $f_X$ zmiennej losowej $X$.\
b) Znajdź dystrybuantę zmiennej losowej $X$.

```{dropdown} Rozwiązanie

a)

Na początku należy znaleźć dystrybuantę zmiennej losowej $T$:

$P(T \le x) = \int\limits_0^x 2t dt = x^2$

$F_T(x)=
\begin{cases}
0   & \text{dla } x < 0, \\
x^2 & \text{dla } t \in [0, 1), \\
1   & \text{dla } t \ge 1.
\end{cases}$

Szukam dystrybuanty zmiennej $X$:

$\begin{aligned}P(X \le t) &= P(-T^3 + 1 \le t) = P(T > (1-t)^\frac{1}{3}) = \\
&= 1 - P(T \le (1-t)^\frac{1}{3}) = 1 - F_T((1-t)^\frac{1}{3}) = \\
&= 1 - (1-t)^\frac{2}{3}\end{aligned}$

$F_X(t)=
\begin{cases}
0                     & \text{dla } t < 0, \\
1 - (1-t)^\frac{2}{3} & \text{dla } t \in [0, 1), \\
1                     & \text{dla } t \ge 1.
\end{cases}$

Gęstość to pochodna dystrybuanty:

$f_X(t)=
\begin{cases}
0                               & \text{dla } t \notin (0, 1), \\
\frac{2}{3}(1-t)^{-\frac{1}{3}} & \text{dla } t \in (0, 1), \\
\end{cases}$
```

## Zadanie 15
Zmienna losowa $X$ ma rozkład normalny $N(5, 1)$. Niech $Y=X^3+2X^2-3$. Oblicz $E(Y)$.

```{dropdown} Rozwiązanie

$E(Y) = E(X^3+2X^2-3) = E(X^3) + 2E(X^2) - 3$

Trzeba obliczyć 3 moment, w tym celu najlepiej użyć funkcji tworzącej momenty:

$M_{X}(t)=\exp \left(\mu \,t+{\frac {\sigma ^{2}t^{2}}{2}}\right)$

Liczę kolejne pochodne i wstawiam $t=0$:

$E(X) = M_X'(0) = \mu = 5,$

$E(X^2) = M_X''(0) = \mu^2 + \sigma^2 = 25 + 1 = 26,$

$E(X^3) = M_X^{(3)}(0) = \mu^3 + 3\mu\sigma^2 = 125 + 15 = 140,$

$E(Y) = 140 + 2\cdot26 - 3 = 189.$

Druga metoda:

$Var(X) = E(X^2) - [E(X)]^2,$

$1 = E(X^2) - 25,$

$E(X^2) = 26.$

$\begin{aligned}0 &= E[(X-5)^3] = E(X^3 - 15X^2 + 75X - 125) = \\
&= E(X^3) - 15E(X^2) + 75E(X) - 125 = \\
&= E(X^3) - 390 + 375 - 125,\end{aligned}$

$E(X^3) = 140.$

$E(Y) = 140 + 2\cdot26 - 3 = 189.$
```

## Zadanie 16
Zmienna losowa $X$ ma momenty zwykłe: $m_1 = 2$, $m_2 = 3$, $m_3 = 4$. Oblicz trzeci moment centralny: $\mu_3 = E[(X-m_1)^3]$.

```{dropdown} Rozwiązanie

$\begin{aligned}\mu_3 &= E[X^3 - 3X^2m_1 + 3Xm_1^2 - m_1^3] = \\
&= E(X^3) - 3m_1E(X^2) + 3m_1^2E(X) - m_1^3 = \\
&= m_3 - 3m_1m_2 + 3m_1^3 - m_1^3 = \\
&= m_3 - 3m_1m_2 + 2m_1^3 = \\
&= 4 - 3\cdot2\cdot3+2\cdot8 = \\
&= 2\end{aligned}$
```

## Zadanie 17
Zmienna losowa $Y$ ma rozkład wykładniczy o parametrze $\lambda = 2$. Oblicz współczynnik zmienności oraz asymetrii.

```{dropdown} Rozwiązanie

Współczynnik zmienności:

$v = \frac{D(X)}{E(X)}.$

Współczynnik asymetrii:

$A = \frac{E\{[X - E(X)]^3\}}{D^3(X)}.$

$E\{[X - E(X)]^3\} = E(X^3) - 3E(X^2)E(X) + 2E^3(X),$

$E(X) = \int\limits_0^\infty 2xe^{-2x} = \frac{1}{2},$

$E(X^2) = \int\limits_0^\infty 2x^2e^{-2x} = \frac{1}{2},$

$E(X^3) = \int\limits_0^\infty 2x^3e^{-2x} = \frac{3}{4},$

$Var(X) = \frac{1}{2} - (\frac{1}{2})^2 = \frac{1}{4}.$

$D(X) = \frac{1}{2}$

$v = \frac{\frac{1}{2}}{\frac{1}{2}} = 1.$

$A = \frac{\frac{3}{4} - 3\cdot\frac{1}{2}\cdot\frac{1}{2} + 2\cdot(\frac{1}{2})^3}{(\frac{1}{2})^3} = \frac{\frac{1}{4}}{\frac{1}{8}} = 2.$
```

## Zadanie 18
Dochód miesięczny losowo wybranego pracownika pewnego sektora gospodarki jest zmienną losową $X$ z rozkładu normalnego o wartości średniej 2500 zł i odchyleniu standardowym 400 zł.\
a) Jaki procent pracowników ma dochód większy niż 4000 zł?\
b) Jaka jest najmniejsza wartość miesięcznego dochodu wśród najlepiej opłaconych 25% pracowników?\
c) Jaka jest górna granica dochodu wśród 25% najmniej zarabiających pracowników?

````{dropdown} Rozwiązanie

```python
import scipy.stats as st

print("a)", 1 - st.norm.cdf(4000, 2500, 400))
print("b)", st.norm.ppf(0.75, 2500, 400))
print("c)", st.norm.ppf(0.25, 2500, 400))
```
````

## Zadanie 19
Zmienna losowa $X$ ma rozkład prawdopodobieństwa:\
a) $N(10, 4),$\
b) $U(10, 40),$\
c) $exp(0.1).$\
W każdym  z przypadków oblicz medianę oraz kwantyl rzędu 0.75.

````{dropdown} Rozwiązanie

```python
import scipy.stats as st

print("a) Mediana:", st.norm.ppf(0.5, 10, 4), "Kwantyl:", st.norm.ppf(0.75, 10, 4))
print("b) Mediana:", st.uniform.ppf(0.5, 10, 30), "Kwantyl:", st.uniform.ppf(0.75, 10, 30))
print("c) Mediana:", st.expon.ppf(0.5, scale=1/0.1), "Kwantyl:", st.expon.ppf(0.75, scale=1/0.1))
```
````

## Zadanie 20
Wielkość miesięcznego czynszu płaconego przez losowo wybraną rodzinę jest zmienną losową $Y$ mającą rozkład normalny o wartości średniej 350 zł oraz odchyleniu standardowym 50 zł.\
a) Jaki procent rodzin płaci czynsz większy niż 400 zł i mniejszy od 600 zł?\
b) Jaka jest najmniejsza wartość czynszu płaconego przez 10% rodzin płacących największe czynsze?

````{dropdown} Rozwiązanie

```python
import scipy.stats as st

print("a)", st.norm.cdf(600, 350, 50) - st.norm.cdf(400, 350, 50))
print("a)", st.norm.ppf(0.9, 350, 50))
```
````

## Zadanie 21
Zmienna losowa $X$ ma rozkład wykładniczy z parametrem $\lambda > 0$. Jaki rozkład ma zmienna $Y=\frac{X}{\lambda}$.

```{dropdown} Rozwiązanie

$X = \lambda Y,$

$h(y) = \lambda y,$

$h'(y) = \lambda,$

$f_Y(y) = f_X(h(y))\cdot|h'(y)| = f_X(\lambda y)\cdot\lambda = \lambda\lambda e^{-\lambda\lambda y} = \lambda^2 e^{-\lambda^2 y}.$

Zmienna Y pochodzi z rozkładu wykładniczego $exp(\lambda^2)$
```

## Zadanie 22
Zmienna losowa ma rozkład gamma z parametrami $r, p > 0$. Jaki rozkład ma zmienna $Y = \frac{X}{r}$?

```{dropdown} Rozwiązanie

$X = rY,$

$h(y) = ry,$

$h'(y) = r,$

$f_Y(y) = r\frac{p^r (ry)^{r - 1} e^{-pry}}{\Gamma(r)} = \frac{(pr)^r y^{r - 1} e^{-pry}}{\Gamma(r)}.$

Zmienna $Y$ pochodzi z rozkładu $Gamma(pr, r)$.
```

## Zadanie 23
Zmienna losowa ma rozkład Cauchy'ego z parametrami $a>0,\ m \in R$, tzn. ma gęstość postaci:

$f(x) = \frac{a}{\pi(a^2+(x-m)^2)}, \ x\in R.$

Jaki rozkład ma zmienna losowa $Y = (X-m)/a?$

```{dropdown} Rozwiązanie

$X = aY + m,$

$h(y) = ay + m,$

$h'(y) = a,$

$f_Y(y) = a\frac{a}{\pi(a^2+(ay + m - m)^2)} = \frac{a^2}{\pi(a^2 + a^2y^2)} = \frac{1}{\pi(1 + y^2)}.$

Zmienna losowa $Y$ pochodzi z rozkładu Cauchy'ego z $a = 1, \ m = 0$.
```

## Zadanie 24
Wyznacz dystrybuantę rozkładu Cauchy'ego.

```{dropdown} Rozwiązanie

$\begin{aligned}P(X \le t) &= \int\limits_{-\infty}^t \frac{a}{\pi(a^2+(x-m)^2)}dx = \frac{a}{\pi} \int\limits_{-\infty}^t \frac{1}{(a^2+(x-m)^2)}dx = \\
&= \left|\begin{aligned} 
p = x - m \\ 
dp = dx
\end{aligned} \right| = \frac{a}{\pi} \int\limits_{-\infty}^{t-m} \frac{1}{a^2+p^2}dp = \\
&= \left|\begin{aligned} 
ay = p \\
y = \frac{p}{a} \\ 
ady = dp
\end{aligned} \right| = \frac{a}{\pi} \int\limits_{-\infty}^{\frac{t-m}{a}} \frac{a}{a^2(1+y^2)}dp = \\
&= \frac{1}{\pi} \int\limits_{-\infty}^{\frac{t-m}{a}} \frac{1}{1+y^2}dp = \left. \frac{1}{\pi}arctg(y)\right|_{-\infty}^{\frac{t-m}{a}} = \\
&= \frac{1}{\pi}arctg(\frac{t-m}{a}) + \frac{1}{2},\end{aligned}$

dla $a > 0, \ m\in R.$
```

## Zadanie 25
Zmienna losowa $X$ jest typu ciągłego i ma gęstość wszędzie dodatnią $f$. Wyznacz gęstość następujących zmiennych losowych:\
a) $Y = aX+b,$\
b) $Z = aX^2,$\
c) $W = F(X).$

```{dropdown} Rozwiązanie

a)

$X = \frac{Y-b}{a},$

$h(y) = \frac{y-b}{a},$

$h'(y) = \frac{1}{a},$

$f_Y(y) = |\frac{1}{a}|f(\frac{y-b}{a})$

b)

$X = \sqrt{\frac{Z}{a}},$

$h(y) = \sqrt{\frac{z}{a}},$

$h'(y) = \frac{1}{2\sqrt{az}},$

$f_Y(y) = \frac{1}{2\sqrt{az}}f(\sqrt{\frac{z}{a}})$

c)

$P(W \le t) = P(F(X) \le t) = P(X \le F^{-1}(t)) = F(F^{-1}(t)) = t,$

$F_W(t)=
\begin{cases}
0 & t < 0. \\
t & t \in [0, 1), \\
1 & t \ge 1. 
\end{cases}$
```

## Zadanie 26
Zmienna losowa $X$ ma rozkład normalny z parametrami $m, \ \sigma$. Wykaż, że zmienna $Y = aX + b$ ma też rozkład normalny i znajdź jego parametry.

```{dropdown} Rozwiązanie

$X = \frac{Y-b}{a},$

$h(y) = \frac{y-b}{a},$

$h'(y) = \frac{1}{a},$

$\begin{aligned}f_Y(y) &= |\frac{1}{a}|f_X(\frac{y-b}{a}) = \frac{1}{\sigma a \sqrt{2\pi}}exp\left( \frac{-\left( \frac{y-b}{a} - m \right)^2}{2\sigma^2}\right) = \\
&= \frac{1}{\sigma a \sqrt{2\pi}}exp\left( \frac{-(y - b - am)^2}{2\sigma^2a^2}\right).\end{aligned}$

Zmienna $Y$ pochodzi z rozkładu $N(b+am, \sigma a)$.
```

## Zadanie 27
Zmienna losowa $X$ ma rozkład wykładniczy z parametrem $\lambda = 4$. Wyznacz dystrybuantę zmiennej losowej $Y = \sqrt{X}$. Wyznacz jej gęstość.

```{dropdown} Rozwiązanie

$P(Y \le t) = P(\sqrt{X} \le t) = P(X \le t^2) = 1 - e^{-\lambda t^2}.$

Gęstość:

$f_Y(t) = 2t\lambda e^{-\lambda t^2}.$
```

## Zadanie 28
Zmienna losowa $Z$ ma rozkład $N(0, 1)$. Obliczyć $P(Z > 0)$, $P(|Z| < 2)$, $P(|Z| > 1)$ oraz kwantyle $x_{0.1}$, $x_{0.7}$, $x_{0.97}$.

````{dropdown} Rozwiązanie

$P(Z > 0) = 1 - P(Z < 0) = 1 - \Phi(0),$\
$P(|Z| < 2) = P(-2 < Z < 2) = \Phi(2) - \Phi(-2),$\
$P(|Z| > 1) = P(Z > 1 \ \cup \ Z < -1) = 2\Phi(-1)$

```python
import scipy.stats as st

print(1 - st.norm.cdf(0))
print(st.norm.cdf(2) - st.norm.cdf(-2))
print(2 * st.norm.cdf(-1))

print("\nKwantyle:")
print(st.norm.ppf(0.1))
print(st.norm.ppf(0.7))
print(st.norm.ppf(0.97))
```
````

## Zadanie 29
Zmienna losowa $X$ podlega rozkładowi $N(3, 5)$. Obliczyć $P(|X − 1| > 1)$.

````{dropdown} Rozwiązanie

$\begin{aligned}P(|X − 1| > 1) &= P(X - 1 > 1 \ \cup X - 1 < -1) = P(X > 2 \ \cup X < 0) = \\
&= P(X < 0) + 1 - P(X < 2)\end{aligned}$

```python
import scipy.stats as st

print(st.norm.cdf(0, 3, 5) + 1 - st.norm.cdf(2, 3, 5))
```
````

## Zadanie 30
W populacji studentów w Krakowie wzrost ma rozkład $N(170, 8)$. Obliczyć prawdopodobieństwo tego, że wzrost przypadkowo napotkanego studenta:\
a) będzie większy od 166,\
b) będzie należał do przedziału (168, 174),\
c) będzie równy co najwyżej 154.

````{dropdown} Rozwiązanie

a) $P(X > 166) = 1 - P(X < 166),$

b) $P(168 < X < 174) = P(X < 174) - P(X < 168),$

c) $P(X < 154)$

```python
import scipy.stats as st

print("a)", 1 - st.norm.cdf(166, 170, 8))
print("b)", st.norm.cdf(174, 170, 8) - st.norm.cdf(168, 170, 8))
print("c)", st.norm.cdf(154, 170, 8))
```
````

## Zadanie 31
Stwierdzono, ze błąd podczas wykonywania pomiaru ma rozkład $N(1, 0.25)$ (mm). Jakie jest prawdopodobieństwo, że wykonując ten pomiar pomylimy się o:\
a) więcej niż 0.5 mm,\
b) mniej niż 0.75 mm,\
c) co najwyżej 0.25 mm?

````{dropdown} Rozwiązanie

a) $P(X > 0.5) = 1 - P(X < 0.5),$

b) $P(X < 0.75),$

c) $P(X < 0.25).$

```python
import scipy.stats as st

print("a)", 1 - st.norm.cdf(0.5, 1, 0.25))
print("b)", st.norm.cdf(0.75, 1, 0.25))
print("c)", st.norm.cdf(0.25, 1, 0.25))
```
````

## Zadanie 32
Rozkład długości liścia rośliny pewnego gatunku jest $N(14, 2)$. Obliczyć prawdopodobieństwo, że losowo wybrany liść ma długość:\
a) większa niż 17,\
b) równa co najmniej 12 i co najwyżej 19,\
c) równa co najwyżej 13.

````{dropdown} Rozwiązanie

a) $P(X > 17) = 1 - P(X < 17),$

b) $P(12 < X < 19) = P(X < 19) - P(X < 12),$

c) $P(X < 13).$

```python
import scipy.stats as st

print("a)", 1 - st.norm.cdf(17, 14, 2))
print("b)", st.norm.cdf(19, 14, 2) - st.norm.cdf(12, 14, 2))
print("c)", st.norm.cdf(13, 14, 2))
```
````

## Zadanie 33
Pierśnica buka w pewnym drzewostanie ma rozkład $N(30, 4)$. Jaki procent buków ma pierśnice większą niż 40?

````{dropdown} Rozwiązanie

$P(X > 40) = 1 - P(X < 40)$

```python
import scipy.stats as st

print("a)", 1 - st.norm.cdf(40, 30, 4))
```
````

## Zadanie 34
Zmienna losowa $X$ podlega rozkładowi $N(m, \sigma)$.\
a) Obliczyć $P(|X − m| < 3\sigma)$.\
b) Dobrać stałą $k$ tak, aby $P(|X − m| < k\sigma) = 0.99$.

````{dropdown} Rozwiązanie

Skorzystam ze standaryzacji zmiennej losowej:

a)

$\begin{aligned}P(|X − m| < 3\sigma) &= P(-3\sigma < X − m < 3\sigma) = \\
&= P(\frac{m-3\sigma-m}{\sigma} < Z < \frac{m+3\sigma-m}{\sigma}) = \\
&= P(-3 < Z < 3) = \Phi(3) - \Phi(-3).\end{aligned}$

```python
import scipy.stats as st

print(st.norm.cdf(3) - st.norm.cdf(-3))
```

b)

$0.99 = P(-k < Z < k) = \Phi(k) - \Phi(-k) = \Phi(k) - 1 + \Phi(k) = 2\Phi(k) - 1,$

$2\Phi(k) = 1.99,$

$\Phi(k) = 0.995,$

```python
import scipy.stats as st

print("k:", st.norm.ppf(0.995))
```
````

## Zadanie 35
Zmienna losowa $X$ ma rozkład $N(2, 1)$. Znaleźć dla tej zmiennej kwantyl rzędu 0.2.

````{dropdown} Rozwiązanie

```python
import scipy.stats as st

print(st.norm.ppf(0.2, 2, 1))
```
````

## Zadanie 36
Niech $X_i \in N(0, \sigma),\  i \in \mathbb{N}$. Ile należy zsumować niezależnych zmiennych $X_i$, aby odchylenie standardowe sumy było równe $10\sigma$?

```{dropdown} Rozwiązanie

Ponieważ zmienne losowe $X_i$ mają taką samą wariancję to można zapisać:

$100\sigma^2 = kVar(X_i) = k\sigma^2,$

$k=100.$

Należy zsumować 100 niezależnych zmiennych losowych $X_i$.
```

## Zadanie 37
Niech zmienne $X_i \ (i \in \mathbb{N})$ maja rozkład jednostajny na przedziale $[−\sigma, \sigma]$. Ile należy zsumować niezależnych zmiennych $X_i$, aby odchylenie standardowe sumy było równe $10\sigma$?

```{dropdown} Rozwiązanie

Ponieważ zmienne losowe $X_i$ mają taką samą wariancję to można zapisać:

$100\sigma^2 = kVar(X_i) = \frac{(\sigma + \sigma)^2}{12} = \frac{4\sigma^2}{12},$

$k=300.$

Należy zsumować 300 niezależnych zmiennych losowych $X_i$.
```

## Zadanie 38
Funkcja gęstości zmiennej losowej $X$ ma postać

$f(x) =
\begin{cases}
3x^2 & \text{dla } x \in [0, 1], \\
0    & \text{dla } x \notin [0, 1].
\end{cases}$

Obliczyć wartość oczekiwana i wariancje zmiennej $X$.

```{dropdown} Rozwiązanie

$E(X) = \int\limits_0^1 3x^3 dx = 0.75,$

$E(X^2) = \int\limits_0^1 3x^4 dx = 0.6,$

$Var(X) = 0.6 - 0.75^2 = 0.0375.$
```

## Zadanie 39
Zmienna losowa X ma rozkład o gęstości prawdopodobieństwa:

$f(x) =
\begin{cases}
0              & \text{dla } x < −1, \\
\frac{2}{5}|x| & \text{dla } x \in [-1, 2], \\
0              & \text{dla } x > 2.
\end{cases}$

a) Znaleźć dystrybuantę.\
b) Obliczyć $E(X)$ oraz $Var(X)$.\
c) Obliczyć $P(X > 3)$, $P(-\frac{1}{2} \le X < 1)$, $P(X = 0)$.

```{dropdown} Rozwiązanie

$|x| = -x, \ x < 0$

$|x| = x, \ x > 0$

a)

Dla $x < 0$:

$\int\limits_{-1}^t -\frac{2}{5} x dx = \frac{1}{5}(1 - t^2), \ x\in[-1, 0).$

Dla $x > 0$:

$\int\limits_{-1}^0 -\frac{2}{5} x dx  + \int\limits_{0}^t \frac{2}{5} x dx = \frac{1}{5}(1 + t^2), \ x\in[0, 2).$

Dystrybuanta:

$F(x) =
\begin{cases}
0                    & \text{dla } x < −1, \\
\frac{1}{5}(1 - x^2) & \text{dla } x \in [-1, 0), \\
\frac{1}{5}(1 + x^2) & \text{dla } x \in [0, 2), \\
1                    & \text{dla } x > 2.
\end{cases}$

b) 

$E(X) = \int\limits_{-1}^0 -\frac{2}{5} x^2 dx + \int\limits_{-1}^0 \frac{2}{5} x^2 dx = \frac{14}{15},$

$E(X^2) = \int\limits_{-1}^0 -\frac{2}{5} x^3 dx + \int\limits_{-1}^0 \frac{2}{5} x^3 dx = \frac{17}{10},$

$Var(X) = \frac{17}{10} - (\frac{14}{15})^2 = \frac{373}{450}.$

c)

$P(X > 3) = 1 - P(X < 3) = 1 - 1 = 0,$

$P(-\frac{1}{2} \le X < 1) = P(X < 1) - P(X < -\frac{1}{2}) = \frac{2}{5} - \frac{3}{20} = \frac{1}{4}$,

$P(X = 0) = 0.$
```

## Zadanie 40
Gęstość zmiennej losowej $X$ ma postać: $f(x) = \frac{a}{e^x+e^{−x}}, \ x \in \mathbb{R}$. Znaleźć stałą $a$ oraz obliczyć $P(X > 0)$.

````{dropdown} Rozwiązanie

$\begin{aligned}1 &= \int\limits_{-\infty}^\infty \frac{a}{e^x+e^{−x}}dx = a\int\limits_{-\infty}^\infty \frac{1}{e^x+e^{−x}}dx = \\
&= a\int\limits_{-\infty}^\infty \frac{e^xdx}{(e^x)^2+1} = \left|\begin{aligned}e^x = t \\ e^xdx = dt \end{aligned} \right| = \\
&= a\int\limits_0^\infty \frac{dt}{t^2+1} = a\cdot arctg(t)\bigr|_0^\infty = \\
&= \frac{a\pi}{2}\end{aligned}$

$2 = a\pi$

$a = \frac{2}{\pi}$

$P(X > 0) = \frac{2}{\pi} \int\limits_0^\infty \frac{1}{e^x+e^{−x}}dx = 0.5$

```python
from scipy.integrate import quad
import numpy as np

def f(x):
  return (2 / np.pi) * (1 / (np.exp(x) + np.exp(-x)))

print(quad(f, 0, np.inf)[0])
```
````

## Zadanie 41
Zmienna losowa $X$ ma rozkład o gęstości prawdopodobieństwa

$
f(x) = \begin{cases}
\frac{x}{2} & \text{dla } 0 \le x \le 2, \\
0           & \text{dla pozostałych } x.
\end{cases}$

a) Obliczyć $E(X)$ oraz $Var(X)$.\
b) Wyznaczyć momenty centralne rzędu pierwszego, drugiego i trzeciego oraz kwartyle zmiennej $X$.

```{dropdown} Rozwiązanie

a)

$E(X) = \int\limits_0^2 \frac{x^2}{2}dx = \frac{4}{3},$

$E(X^2) = \int\limits_0^2 \frac{x^3}{2}dx = 2,$

$E(X^3) = \int\limits_0^2 \frac{x^4}{2}dx = \frac{16}{5},$

$Var(X) = 2 - (\frac{4}{3})^2 = \frac{2}{9}$

b)

Dla ułatwienia oznaczę $E(X)$ jako $\mu$:

$E(X - \mu) = E(X) - \mu = \mu - \mu = 0,$

$E[(X - \mu)^2] = Var(X) = \frac{2}{9},$

$E[(X - \mu)^3] = E(X^3 - 3X^2\mu + 3X\mu^2 - \mu^3) = E(X^3) - 3\mu E(X^2) + 2\mu^3 = \frac{16}{5} - 3\cdot \frac{4}{3}\cdot2 + 2\cdot(\frac{4}{3})^3 = -\frac{8}{135}$

Do obliczenia kwartyli potrzebna jest dystrybuanta:

$F(t) = \int\limits_0^t \frac{x}{2} dx = \frac{1}{4}t^2, \ t \in[0, 2]$

$P(X \le t_{0.25}) = 0.25,$

$\frac{1}{4}t_{0.25}^2 = 0.25,$

$t_{0.25} = 1.$

$P(X \le t_{0.5}) = 0.5,$

$t_{0.5} = \sqrt{2}.$

$P(X \le t_{0.75}) = 0.75,$

$t_{0.75} = \sqrt{3}.$
```

## Zadanie 42
Dobrać tak stała $a$, by funkcja

$
F(x) =
\begin{cases}
0                  & \text{dla } x \le 1, \\
2(1 - \frac{1}{x}) & \text{dla } 1 < x  \le a, \\
1                  & \text{dla } x > a.
\end{cases}
$

była dystrybuantą zmiennej losowej $X$ typu ciągłego. Wyznaczyć jej gęstość. Obliczyć $P(−1 \le X \le 1.5)$.

```{dropdown} Rozwiązanie

$2(1 - \frac{1}{a}) = 1,$

$a = 2.$

$
f(x) =
\begin{cases}
\frac{2}{x^2} & \text{dla } 1 < x  \le 2, \\
0             & \text{w p.p.}
\end{cases}
$

$P(−1 \le X \le 1.5) = P(X \le 1.5) - P(X \le -1) = 2(1 - \frac{1}{1.5}) - 0 = \frac{2}{3}.$
```

## Zadanie 43
Zmienna losowa $X$ ma dystrybuantę daną równaniem:

$F(x) = \frac{1}{2} + \frac{1}{\pi}arctg(\frac{x}{2}), \ x \in \mathbb{R}$

Znaleźć możliwą wartość $a$, dla której zmienna losowa $X$ w wyniku próby przyjmie wartość większą niż $a$ z prawdopodobieństwem 16.

```{dropdown} Rozwiązanie

$\frac{1}{6} = P(X > a) = 1 - P(X < a),$

$\frac{1}{6} = 1 - \frac{1}{2} + \frac{1}{\pi}arctg(\frac{a}{2}),$

$arctg(\frac{a}{2}) = \frac{\pi}{3},$

$\frac{a}{2} = tg(\frac{\pi}{3}),$

$a = 2\sqrt{3}$
```

## Zadanie 44
Gęstość prawdopodobieństwa zmiennej losowej $X$ ma postać

$
f(x) = \begin{cases}
\sin(2x) &  \text{dla } x \in [0, \frac{\pi}{2}], \\
0       &  \text{dla } x \notin [0, \frac{\pi}{2}].
\end{cases}
$

a) Znaleźć dystrybuantę $X$.\
b) Obliczyć $EX$ oraz $VarX$.\
c) Obliczyć $P(X > \frac{\pi}{4})$.\
d) Obliczyć $x_{0.25}$ oraz $x_{0.75}$.

```{dropdown} Rozwiązanie

a)

$\int\limits_0^t sin(2x)dx = -\frac{cos(2x)}{2}\bigr|_0^t = \frac{1}{2} - \frac{cos(2t)}{2}$

$
F(x) = \begin{cases}
0                               & \text{dla } x < 0, \\
\frac{1}{2} - \frac{cos(2t)}{2} & \text{dla } x \in [0, 2), \\
1                               & \text{dla } x \ge 2. \\
\end{cases}
$

b)

$E(X) = \int\limits_0^\frac{\pi}{2} x sin(2x)dx = \frac{\pi}{4},$

$E(X^2) = \int\limits_0^\frac{\pi}{2} x^2 sin(2x)dx = \frac{\pi^2}{8} - \frac{1}{2},$

$Var(X) = \frac{\pi^2}{8} - \frac{1} - (\frac{\pi}{4})^2 = \frac{\pi^2}{16} - \frac{1}{2}.$

c)

$P(X > \frac{\pi}{4}) = 1 - P(X < \frac{\pi}{4}) = 1 - \frac{1}{2} + \frac{cos(\frac{\pi}{2})}{2} = \frac{1}{2}.$

d)

$P(X < x_{0.25}) = 0.25,$

$\frac{1}{2} - \frac{cos(2x_{0.25})}{2} = 0.25,$

$cos(2x_{0.25}) = 0.5,$

$x_{0.25} = \frac{arccos(0.5)}{2},$

$x_{0.25} = \frac{\pi}{6}.$

$P(X < x_{0.75}) = 0.75,$

$x_{0.75} = \frac{\pi}{3}.$
```

## Zadanie 45
Gęstość prawdopodobieństwa zmiennej losowej $X$ ma postać

$
f(x) = \begin{cases}
\frac{a}{\sqrt{4−x^2}} & \text{dla } x \in (−1, 2), \\
0                      & \text{dla } x \notin (−1, 2). \\
\end{cases}
$

Znaleźć:\
a) stałą $a$,\
b) dystrybuantę $X$,\
c) $Var(X)$,\
d) $P(−1 < X < 1)$, $P(X > 0)$, $P(X = \frac{1}{2})$.

```{dropdown} Rozwiązanie

a)

$1 = \int\limits_{-1}^2 \frac{a}{\sqrt{4−x^2}} = \frac{2\pi a}{3},$

$a = \frac{3}{2\pi}$

b)

$\begin{aligned}\frac{3}{2\pi} \int\limits_{-1}^t \frac{dx}{\sqrt{4−x^2}} &= \frac{3}{2\pi} \int\limits_{-1}^t \frac{dx}{2\sqrt{1−(\frac{x}{2})^2}} = \left|\begin{aligned}\frac{x}{2} = \sin(u) \\ dx = 2\cos(u)du \\ u = \arcsin(\frac{x}{2}) \end{aligned}\right| = \\
&= \frac{3}{2\pi} \int\limits_{-\frac{\pi}{6}}^{\arcsin(\frac{t}{2})} \frac{2\cos(u)du}{2\sqrt{1−\sin^2(u)}} = \frac{3}{2\pi} \int\limits_{-\frac{\pi}{6}}^{\arcsin(\frac{t}{2})} \frac{\cos(u)du}{\sqrt{\cos^2(u)}} = \\
&= \frac{3}{2\pi} \int\limits_{-\frac{\pi}{6}}^{\arcsin(\frac{t}{2})} du = \left. \frac{3}{2\pi} u\right|_{-\frac{\pi}{6}}^{\arcsin(\frac{t}{2})} = \\
&= \frac{3}{2\pi}(\arcsin(\frac{t}{2})+ \frac{\pi}{6})\end{aligned}$

$
F(x) = \begin{cases}
0                                                   & \text{dla } x < -1, \\
\frac{3}{2\pi}(\arcsin(\frac{t}{2})+ \frac{\pi}{6}) & \text{dla } x \in [-1, 2), \\
1                                                   & \text{dla } x \ge 2. \\
\end{cases}
$

c)

$E(X) = \frac{3}{2\pi} \int\limits_{-1}^2 \frac{xdx}{\sqrt{4−x^2}} = \frac{3\sqrt{3}}{2\pi},$

$E(X^2) = \frac{3}{2\pi} \int\limits_{-1}^2 \frac{x^2dx}{\sqrt{4−x^2}} = 2 - \frac{3\sqrt{3}}{4\pi},$

$Var(X) = 2 - \frac{3\sqrt{3}}{4\pi} - (\frac{3\sqrt{3}}{2\pi})^2 = 2 - \frac{3\sqrt{3}}{4\pi} - \frac{27}{4\pi^2}$

d)

$P(−1 < X < 1) = P(X<1) - P(X<-1) = \frac{3}{2\pi}(arcsin(\frac{1}{2})+ \frac{\pi}{6}) = \frac{1}{2},$

$P(X > 0) = 1 - P(X<0) = 1 - \frac{3}{2\pi}(arcsin(0)+ \frac{\pi}{6}) = \frac{3}{4},$

$P(X = \frac{1}{2}) = 0.$
```

## Zadanie 46
Gęstość zmiennej losowej $X$ ma postać

$
f(x) = \begin{cases}
0    & \text{dla } x < 0, \\
be^x & \text{dla } x \in [0, \ln3], \\
0    & \text{dla } x > \ln3.
\end{cases}
$

a) Wyznaczyć stałą $b$.\
b) Znaleźć dystrybuantę $X$.\
c) Obliczyć $E(X)$ oraz $Var(X)$.\
d) Obliczyć $P(X > 1)$.

```{dropdown} Rozwiązanie

a)

$1 = b\int\limits_0^{ln3}e^xdx = b(e^{ln3} - e^0)= b(3-1)=2b,$

$b = \frac{1}{2}.$

b)

$\frac{1}{2}\int\limits_0^{t}e^xdx = \frac{1}{2}(x^t - 1),$

$
F(x) = \begin{cases}
0                    & \text{dla } x < 0, \\
\frac{1}{2}(x^t - 1) & \text{dla } x \in [0, \ln3), \\
1                    & \text{dla } x \ge \ln3. \\
\end{cases}
$

c)

$E(X) = \frac{1}{2}\int\limits_0^{ln3}xe^xdx = \frac{3}{2}ln3-1,$

$E(X^2) = \frac{1}{2}\int\limits_0^{ln3}x^2e^xdx = 2 - 3ln3 + \frac{3}{2}(ln3)^2,$

$\begin{aligned}Var(X) &= 2 - 3\ln3 + \frac{3}{2}(\ln3)^2 - (\frac{3}{2}\ln3-1)^2 = \\
&= 2 - 3\ln3 + \frac{3}{2}(\ln3)^2 - \frac{9}{4}(\ln3)^2 + 3ln3 - 1 = \\
&= 1 - \frac{3}{4}(\ln3)^2.\end{aligned}$

d)

$P(X > 1) = 1 - P(X<1) = 1 -\frac{1}{2}(e^1-1) = \frac{3}{2} - \frac{e}{2}.$
```

## Zadanie 47
Dystrybuanta zmiennej losowej $X$ jest postaci

$
F(x) = \begin{cases}
0               & \text{dla } x \le 0, \\
\frac{1}{27}x^3 & \text{dla } x \in (0, 3], \\
1               & \text{dla } x > 3. \\
\end{cases}
$

Znaleźć funkcję gęstości zmiennej $X$, obliczyć jej wartość oczekiwana oraz kwantyle $x_{0.125}$, $x_{\frac{1}{125}}$ i $x_{\frac{8}{27}}$.

```{dropdown} Rozwiązanie

$
f(x) = \begin{cases}
0              & \text{dla } x < 0, \\
\frac{1}{9}x^2 & \text{dla } x \in [0, 3], \\
0              & \text{dla } x > 3.
\end{cases}
$

$E(X) = \frac{1}{9}\int\limits_0^3x^3dx= \frac{9}{4}.$

$P(X < x_{0.125}) = 0.125,$

$\frac{1}{27}x_{0.125}^3= 0.125,$

$x_{0.125}= 1.5.$

$P(X < x_{\frac{1}{125}}) = \frac{1}{125},$

$\frac{1}{27}x_{\frac{1}{125}}^3= \frac{1}{125},$

$x_{\frac{1}{125}}= 0.6.$

$P(X < x_{\frac{8}{27}}) = \frac{8}{27},$

$\frac{1}{27}x_{\frac{8}{27}}^3= \frac{8}{27},$

$x_{\frac{8}{27}}= 2.$
```

## Zadanie 48
Zmienne losowe $X$ i $Y$ są niezależne oraz wiadomo, ze $E(X) > 0$, $E(X^2) = 16$, $D(X) = 2\sqrt{3}$, $E(Y) > 0$, $E(Y^2) = 12$, $D(Y) = 3$. Obliczyć $E(3XY − 2)$.

```{dropdown} Rozwiązanie

$E(3XY − 2) = 3E(X)E(Y) - 2,$

$E(X) = \sqrt{E(X^2) - Var(X)} = \sqrt{16 - 4\cdot3} = 2,$

$E(Y) = \sqrt{E(Y^2) - Var(Y)} = \sqrt{12 - 9} = \sqrt{3},$

$E(3XY − 2) = 3\cdot2\sqrt{3}-2 = 6\sqrt{3}-2.$
```

## Zadanie 49
Zmienna losowa X ma rozkład o gęstości

$
f(x) = \begin{cases}
|x| & \text{dla } -1 \le x \le 1, \\
0   & \text{w p.p.}  
\end{cases}
$

Znaleźć dystrybuantę, obliczyć $E(X)$, $Var(X)$, $P(X < 0)$, $P(X \ge­ 1)$.

```{dropdown} Rozwiązanie

$|x| = -x, \ x < 0,$

$|x| = x, \ x > 0,$

Dla $x < 0$:

$\int\limits_{-1}^t -x dx = \frac{1}{2} - \frac{t^2}{2}.$

Dla $x > 0$:

$\int\limits_{-1}^0 -x dx + \int\limits_{0}^t x dx = \frac{1}{2} + \frac{t^2}{2}.$

$
F(x) = \begin{cases}
0                           & \text{dla } x < 0, \\
\frac{1}{2} - \frac{t^2}{2} & \text{dla } x \in [-1, 0), \\
\frac{1}{2} + \frac{t^2}{2} & \text{dla } x \in [0, 1), \\
1                           & \text{dla } x \ge 1. \\
\end{cases}
$

$E(X) = \int\limits_{-1}^0 -x^2 dx + \int\limits_{0}^1 x^2 dx = 0,$

$E(X^2) = \int\limits_{-1}^0 -x^3 dx + \int\limits_{0}^1 x^3 dx = 0.5,$

$Var(X) = 0.5,$

$P(X < 0) = \frac{1}{2} - \frac{0}{2} = \frac{1}{2},$

$P(X \ge 1) = 1 - P(X \le 1) = 1 - \frac{1}{2} - \frac{1}{2} = 0.$
```

## Zadanie 50
Niech

$
f(x) = \begin{cases}
\frac{3}{4}(1-x^2) & \text{dla } -1 \le x \le 1, \\
0                  & \text{w p.p.}  
\end{cases}
$

Znaleźć dystrybuantę i narysować jej wykres, obliczyć $E(X)$, $Var(X)$, $P(X < −\frac{1}{2})$, $P(|X| > \frac{1}{3})$.

```{dropdown} Rozwiązanie

$\frac{3}{4}\int\limits_{-1}^t 1 - x^2 dx = \frac{1}{4}(3t - t^3 + 2)$

$
F(x) = \begin{cases}
0                         & \text{dla } x < 0, \\
\frac{1}{4}(3t - t^3 + 2) & \text{dla } x \in [-1, 1), \\
1                         & \text{dla } x \ge 1. \\
\end{cases}
$

$E(X) = \int\limits_{-1}^1 \frac{3}{4}x(1-x^2) dx = 0,$

$E(X^2) = \int\limits_{-1}^1 \frac{3}{4}x^2(1-x^2) dx = 0.2,$

$Var(X) = 0.2,$

$P(X < -\frac{1}{2}) = \frac{1}{4}(3(-\frac{1}{2}) - (-\frac{1}{2})^3 + 2) = \frac{5}{32},$

$\begin{aligned}P(|X| > \frac{1}{3}) &= P(X > \frac{1}{3} \cup X < -\frac{1}{3}) = P(X < - \frac{1}{3}) + 1 - P(X < \frac{1}{3}) = \\
&= \frac{1}{4}(3(-\frac{1}{3}) - (- \frac{1}{3})^3 + 2) + 1 - \frac{1}{4}(3(\frac{1}{3}) - (\frac{1}{3})^3 + 2) = \frac{14}{27}.\end{aligned}$
```

## Zadanie 51
Dobrać tak stałą $a$, by funkcja

$f(x) = \begin{cases}
a \cos(x) & \text{dla } -\frac{\pi}{2} \le x < \frac{\pi}{2}, \\
0         & \text{w p.p.}  
\end{cases}$

była gęstością pewnej zmiennej losowej $X$. Znaleźć dystrybuantę, obliczyć $E(X)$, $Var(X)$, $P(|X| > \frac{\pi}{6})$, $P(X ­ \ge \frac{\pi}{3})$, $P(−\frac{\pi}{6} < X \le \frac{\pi}{2})$ oraz medianę i modę $X$.

```{dropdown} Rozwiązanie

$1 = a\int\limits_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \cos(x) dx = 2a,$

$a = \frac{1}{2}.$

Dystrybuanta:

$\frac{1}{2} \int\limits_{-\frac{\pi}{2}}^t \cos(x) dx = \frac{1}{2}(\sin(t)+1),$

$F(x) = \begin{cases}
0                      & \text{dla } x < 0, \\
\frac{1}{2}(\sin(x)+1) & \text{dla } -\frac{\pi}{2} \le x < \frac{\pi}{2}, \\
1                      & \text{dla } x \ge 1. \\
\end{cases}$

$E(X) = \frac{1}{2}\int\limits_{-\frac{\pi}{2}}^{\frac{\pi}{2}} x \cos(x) dx = 0,$

$E(X^2) = \frac{1}{2}\int\limits_{-\frac{\pi}{2}}^{\frac{\pi}{2}} x^2\cos(x) dx = \frac{\pi^2}{4} - 2,$

$Var(X) = \frac{\pi^2}{4} - 2,$

$\begin{aligned}P(|X| > \frac{\pi}{6}) &= P(X > \frac{\pi}{6} \cup X < -\frac{\pi}{6}) = P(X < -\frac{\pi}{6}) + 1 - P(X < \frac{\pi}{6}) = \\
&= \frac{1}{2}(\sin(-\frac{\pi}{6})+1) + 1 - \frac{1}{2}(\sin(\frac{\pi}{6})+1) = 0.5,\end{aligned}$

$P(X \ge \frac{\pi}{3}) = 1 - P(X \le \frac{\pi}{3}) = 1 - \frac{1}{2}(\sin(\frac{\pi}{3})+1) = \frac{1}{2} - \frac{\sqrt{3}}{4},$

$P(−\frac{\pi}{6} < X \le \frac{\pi}{2}) = P(X \le \frac{\pi}{2}) - P(X < −\frac{\pi}{6}) = \frac{1}{2}(\sin(\frac{\pi}{2})+1) - \frac{1}{2}(\sin(-\frac{\pi}{6})+1) = 0.75.$

Mediana:

$P(X < m) = 0.5,$

$\frac{1}{2}(\sin(m)+1) = 0.5,$

$\sin(m) = 0,$

$m = \arcsin(0),$

$m = 0.$

Moda:

Moda to wartość dla której gęstość prawdopodobieństwa osiąga maksimum.

$f'(x) = (\frac{1}{2}\cos(x))' = -\frac{1}{2}\sin(x),$

$-\frac{1}{2}\sin(x) = 0,$

$x = \arcsin(0),$

$x = 0.$
```

## Zadanie 52
Funkcja gęstości prawdopodobieństwa zmiennej losowej X jest postaci:

$f(x) = \begin{cases}
0        & \text{dla } x \le 0, \\
2e^{-2x} & \text{dla } x > 0.
\end{cases}$

Znaleźć dystrybuantę, obliczyć $E(X)$, $Var(X)$, $P(X > 1)$, $P(0 < X \le ln 3)$ oraz medianę $X$.

```{dropdown} Rozwiązanie

$2\int\limits_0^t e^{-2x} dx = 1 - e^{-2t},$

$F(x) = \begin{cases}
0           & \text{dla } x \le 0, \\
1 - e^{-2x} & \text{dla } x > 1.
\end{cases}$

$E(X) = 2\int\limits_0^\infty xe^{-2x}dx = \frac{1}{2},$

$E(X^2) = 2\int\limits_0^\infty x^2e^{-2x}dx = \frac{1}{2},$

$Var(X) = \frac{1}{4},$

$P(X > 1) = 1 - P(X < 1) = 1 - (1-e^{-2}) = e^{-2},$

$\begin{aligned}P(0 < X \le \ln3) &= P(X \le \ln3) - P(X \le 0) = 1-e^{-2\ln3} - 0 = \\
&= 1-e^{\ln(3^{-2})} = 1 - \frac{1}{3^2} = \frac{8}{9}.\end{aligned}$

Mediana:

$P(X < m) = 0.5,$

$1-e^{-2m} = 0.5,$

$e^{-2m} = 0.5,$

$-2m = \ln(0.5),$

$m = -\frac{\ln(0.2)}{2} = \frac{\ln2}{2}.$
```

## Zadanie 53
Niech gęstość pewnej zmiennej $X$ będzie postaci

$f(x) = \begin{cases}
0             & \text{dla } x \le 1, \\
\frac{2}{x^3} & \text{dla } x > 1.
\end{cases}$

Znaleźć dystrybuantę, obliczyć $E(X)$, $Var(X)$, $P(|X| > 1)$, oraz medianę $X$.

```{dropdown} Rozwiązanie

$2\int\limits_0^t \frac{1}{x^3} dx = 1 - t^{-2},$

$F(x) = \begin{cases}
0          & \text{dla } x \le 1, \\
1 - x^{-2} & \text{dla } x > 1.
\end{cases}$

$E(X) = 2\int\limits_0^\infty \frac{1}{x^2} dx = 2,$

$E(X^2) = 2\int\limits_0^\infty \frac{1}{x} dx = \infty,$

$Var(X) = \infty,$

$\begin{aligned}P(|X| > 1) &= P(X > 1 \cup X < -1) = \\
&= P(X < -1) + 1 - P(X < 1) = \\
&= 0 + 1 - 0 = 1.\end{aligned}$

Mediana:

$P(X < m) = 0.5,$

$1 - \frac{1}{x^2} = 0.5,$

$\frac{1}{x^2} = 0.5,$

$x = \sqrt{2}.$
```

## Zadanie 54
Niech $f(x) = \frac{1}{\pi} \cdot \frac{1}{1+x^2} \ \text{dla } x \in \mathbb{R}$. Znaleźć dystrybuantę i narysować, zbadać istnienie $E(X)$. Obliczyć $P(0 < X \le 1)$, $P(3X − 1 > \sqrt{3} − 1)$, $P(0 < X < \sqrt{3})$. Znaleźć medianę oraz modę.

```{dropdown} Rozwiązanie

$F(x) = \frac{1}{\pi} \int\limits_{-\infty}^t \frac{dx}{1 + x^2} = \frac{1}{\pi}\arctan(x)\bigr|_{-\infty}^t = \frac{1}{\pi}(\arctan(t) + \frac{\pi}{2}) \ \text{dla } t \in \mathbb{R}$

$E(X) = \frac{1}{\pi} \int\limits_{-\infty}^\infty \frac{xdx}{1 + x^2} = \left|\begin{aligned} t = x^2 \\ 2xdx = dt \end{aligned}\right| = \frac{1}{2\pi} \int\limits_{\infty}^\infty \frac{xdx}{1 + t} = \frac{1}{2\pi} \ln(1 + t)\biggr|_\infty^\infty = \infty - \infty,$

czyli wartość oczekiwana nie istnieje.

$\begin{aligned}P(0 < X \le 1) &= P(X \le 1) - P(X < 0) = \\
&= \frac{1}{\pi}(\arctan(1) + \frac{\pi}{2}) - \frac{1}{\pi}(\arctan(0) + \frac{\pi}{2}) = \\
&= \frac{1}{4},\end{aligned}$

$\begin{aligned}P(3X − 1 > \sqrt{3} − 1) &= P(3X > \sqrt{3}) = 1 - P(X < \frac{\sqrt{3}}{3}) = 
\\
&= 1 - \frac{1}{\pi}(\arctan(\frac{\sqrt{3}}{3}) + \frac{\pi}{2}) = \frac{1}{3},\end{aligned}$

$\begin{aligned}P(0 < X < \sqrt{3}) &= P(X < \sqrt{3}) - P(X < 0) = \\
&= \frac{1}{\pi}(\arctan(\sqrt{3}) + \frac{\pi}{2}) - \frac{1}{\pi}(\arctan(0) + \frac{\pi}{2}) = \\
&= \frac{1}{3}.\end{aligned}$

Mediana:

$P(X < m) = 0.5,$

$\frac{1}{\pi}(\arctan(m) + \frac{\pi}{2}) = \frac{1}{2},$

$\arctan(m) + \frac{\pi}{2} = \frac{\pi}{2},$

$\arctan(m) = 0,$

$m=0.$

Moda:

$f'(x) = 0,$

$\left(\frac{1}{\pi} \cdot \frac{1}{1+x^2}\right)' = 0,$

$\frac{1}{\pi} \cdot \frac{-2x}{(1+x^2)^2} = 0,$

$x = 0.$
```

## Zadanie 55
Zmienna $X$ ma gęstość postaci

$f(x) = \begin{cases}
0                   & \text{dla } x < 0, \\
xe^{-\frac{x^2}{2}} & \text{dla } x \ge 0.
\end{cases}$

Znaleźć dystrybuantę, medianę, modę, wartość oczekiwaną, $P(X > \sqrt{\ln4})$, $P(X \le \sqrt{\ln9})$.

```{dropdown} Rozwiązanie

$\int\limits_0^t xe^{-\frac{x^2}{2}}dx = \left|\begin{aligned} z = \frac{x^2}{2} \\ dz = xdx\end{aligned}\right| = \int\limits_0^{t} e^{-z}dz = -e^{-z}\bigr|_0^t = -e^{-\frac{x^2}{2}}\bigr|_0^t = -(e^{-\frac{t^2}{2}} - e^{-\frac{0}{2}}) = 1 - e^{-\frac{t^2}{2}},$

$F(x) = \begin{cases}
0                      & \text{dla } x < 0, \\
1 - e^{-\frac{x^2}{2}} & \text{dla } x \ge 1.
\end{cases}$

$E(X) = \int\limits_0^\infty x^2e^{-\frac{x^2}{2}} = \frac{\sqrt{2\pi}}{2}.$

$\begin{aligned}P(X > \sqrt{\ln4}) &= 1 - P(X < \sqrt{\ln4}) = 1 - 1 + e^{-\frac{(\sqrt{\ln4})^2}{2}} = \\
&= e^{-\frac{\ln4}{2}} = \exp(\ln(4^{-0.5})) = \\
&= \exp(\ln(\frac{1}{2})) = \frac{1}{2},\end{aligned}$

$\begin{aligned}P(X \le \sqrt{\ln9}) &= 1 - e^{-\frac{(\sqrt{\ln9})^2}{2}} = 1 - e^{-\frac{\ln9}{2}} = \\
&= 1 - \exp(\ln(9^{-0.5})) = 1- \exp(\ln(\frac{1}{3})) = \\
&= 1- \frac{1}{3} = \frac{2}{3}.\end{aligned}$

Poniższe równania mają dwa rozwiązania ale należy wziąć pod uwagę, że $x \ge 0$ co ostatecznie da jeden dodatni wynik.

Mediana:

$P(X < m) = 0.5,$

$1 - e^{-\frac{m^2}{2}} = 0.5,$

$e^{-\frac{m^2}{2}} = 0.5,$

$-\frac{m^2}{2} = ln(0.5),$

$m^2 = -2ln(0.5),$

$m = \sqrt{(ln4)}.$

Moda:

$f'(x) = 0,$

$\left(xe^{-\frac{x^2}{2}}\right)' = 0,$

$e^{-\frac{x^2}{2}} + xe^{-\frac{x^2}{2}}(-x)= 0,$

$e^{-\frac{x^2}{2}}(1 - x^2)= 0,$

$x = 1.$
```

## Zadanie 56
Zmienna $X$ ma gęstość postaci

$f(x) = \begin{cases}
\frac{1}{\pi} \cdot \frac{1}{\sqrt{4-x^2}} & \text{dla } |x| < 2. \\
0                                          & \text{w p.p.}
\end{cases}$

Zbadać istnienie $E(X)$. Wyznaczyć dystrybuantę $X$ oraz obliczyć $P(1 < X \le 2)$.

```{dropdown} Rozwiązanie

$E(X) = \int\limits_{-2}^2 \frac{1}{\pi} \cdot \frac{xdx}{\sqrt{4-x^2}} = 0.$

$\begin{aligned}\frac{1}{\pi} \int\limits_{-2}^t \frac{1}{\sqrt{4-x^2}}dx &= 
\frac{1}{\pi} \int\limits_{-2}^t \frac{1}{2\sqrt{1-(\frac{x}{2})^2}}dx = \left|\begin{aligned} sin(z) &= \frac{x}{2} \\ cos(z)dz &= \frac{dx}{2}\end{aligned}\right| = \\
&= \frac{1}{\pi} \int\limits_{-2}^t \frac{cos(z)dz}{\sqrt{1-sin^2(z)}} = \frac{1}{\pi} \int\limits_{-2}^t \frac{cos(z)dz}{\sqrt{cos^2(z)}}= \\
&= \frac{1}{\pi} \int\limits_{-2}^t dz = \frac{1}{\pi} z\biggr|_{-2}^t = \frac{1}{\pi} arcsin(\frac{x}{2})\biggr|_{-2}^t = \\
&= \frac{1}{\pi}(arcsin(\frac{t}{2})+\frac{\pi}{2}) = \frac{1}{\pi}arcsin(\frac{t}{2})+\frac{1}{2}\end{aligned}$

$F(x) = \begin{cases}
0                                            & \text{dla } x < -2, \\
\frac{1}{\pi}arcsin(\frac{t}{2})+\frac{1}{2} & \text{dla } x \in [-2, 2), \\
1                                            & \text{dla } x \ge 2.
\end{cases}$

$P(1 < X \le 2) = P(X \le 2) - P(X < 1) = 1 - \frac{1}{\pi}arcsin(\frac{1}{2}) - \frac{1}{2} = \frac{1}{3}$
```

## Zadanie 57
Zmienna $X$ ma gęstość postaci

$f(x) = \begin{cases}
e^{2x} & \text{dla } x \in (0, \ln\sqrt{3}). \\
0      & \text{w p.p.}
\end{cases}$

Znaleźć $P(\ln2 < X \le 1)$, $P(X < \ln\frac{1}{2})$.

```{dropdown} Rozwiązanie

$P(\ln 2 < X \le 1) = P(X < \ln\frac{1}{2}) = 0,$

bo:

$\ln2 > \ln\sqrt{3},$

i

$\ln\frac{1}{2} < 0.$
```

## Zadanie 58
Dobrać $A$ i $B$ tak, by funkcja

$F(x) = \begin{cases}
0                      & \text{dla } x \le -1, \\
A + B \cdot \arccos(x) & \text{dla } x \in (-1, 1]. \\
1                      & \text{dla }  > 1.
\end{cases}$

była dystrybuantą pewnej ciągłej zmiennej losowej $X$. Znaleźć funkcję
gęstości, obliczyć $P(0 < X \le 1)$, $P(X > \frac{1}{2})$.

```{dropdown} Rozwiązanie

Korzystam z własności dystrybuanty:

$\begin{cases}
1 = A + B\cdot \arccos(1) \\
0 = A + B\cdot \arccos(-1)
\end{cases}$

Odejmuję stronami:

$1 -0 = A + B \cdot \arccos(1) - A - B\cdot \arccos(-1),$

$1 = B(\arccos(1) - \arccos(-1)) = -\pi B,$

$B = -\frac{1}{\pi},$

$A = -B \cdot \arccos(-1) = \frac{1}{\pi}\cdot \pi = 1$

$F(x) = \begin{cases}
0                                 & \text{dla } x \le -1, \\
1 - \frac{1}{\pi}\cdot \arccos(x) & \text{dla } x \in (-1, 1]. \\
1                                 & \text{dla } x > 1.
\end{cases}$

Gęstość:

$f(x) = \begin{cases}
\frac{1}{\pi\sqrt{1-x^2}} & \text{dla } x \in (-1, 1), \\
0                         & \text{w p.p.}
\end{cases}$

$P(0 < X \le 1) = P(X \le 1) - P(X < 0) = 1 - 1 + \frac{1}{\pi}\cdot \arccos(0) = \frac{1}{2},$

$P(X > \frac{1}{2}) = 1 - P(X < \frac{1}{2}) = 1 - 1 + \frac{1}{\pi}\cdot \arccos(0.5) = \frac{1}{3}$
```

## Zadanie 59
Bok prostokąta jest zmienną losową $X$ o rozkładzie jednostajnym na przedziale $[0, 10]$.\
Obliczyć:\
a) $E(X^2)$,\
b) wartość oczekiwaną pola prostokąta, jeśli jego obwód wynosi 20.

```{dropdown} Rozwiązanie

a)

Korzystam z wzorów na wariancję i wartość oczekiwaną rozkładu jednostajnego:

$E(X^2) = Var(X) + [E(X)]^2 = \frac{(0-10)^2}{12} + (\frac{0 + 10}{2})^2 = \frac{100}{3}.$

b)

Należy obliczyć wartość oczekiwaną zmiennej $Z = XY$, gdzie zmienne $X$ i $Y$ to boki prostokąta, uwzględniając warunek mamy:

$2X + 2Y = 20,$

$X+Y=10,$

$Y = 10 - X,$

$\begin{aligned}E(Z) &= E(XY) = E[X(10-X)] = E(10X-X^2) = 10E(X) - E(X^2) = \\
&= 10\cdot\frac{10}{2} - \frac{100}{3} = \frac{50}{3}.\end{aligned}$
```

## Zadanie 60
Zmienna $X$ ma gęstość postaci

$f(x) = \begin{cases}
0       & \text{dla } x < 0, \\ 
xe^{-x} & \text{dla } x \ge 0.
\end{cases}$

Wyznaczyć dystrybuantę oraz $P(0 < X < \ln2)$.

```{dropdown} Rozwiązanie

$\int\limits_0^t xe^{-x}dx =$\
$= \int\limits_0^t x\left(-e^{-x}\right)'dx$ \
$= \left[-xe^{-x}+\int\limits_0^t e^{-x}dx\right]_0^t$\
$= \left[-xe^{-x} - e^{-x}\right]_0^t$\
$= \left(-te^{-t} - e^{-t}\right) - \left(0e^{-0} - e^{-0}\right)$\
$= 1 - te^{-t} - e^{-t}$

$F(x) = \begin{cases}
0                    & \text{dla } x < 0, \\
1 - xe^{-x} - e^{-x} & \text{dla } x \ge 0. \\
\end{cases}$

$\begin{aligned}P(0 < X < \ln2) &= P(X < \ln2) - P(X < 0) = 1 - \ln2 \cdot e^{-\ln2} - e^{-\ln2} = \\
&= 1 - \frac{1}{2}\ln2 - \frac{1}{2} = \frac{1}{2} - \frac{1}{2}\ln2\end{aligned}$
```

## Zadanie 61
Dobrać tak stała $k$, by funkcja

$f(x) = \begin{cases}
k\cdot \arcsin(x) & \text{dla } x \in [0, 1], \\
0                & \text{w p.p}, \\ 
\end{cases}$

była gęstością pewnej zmiennej losowej $X$.

```{dropdown} Rozwiązanie

$1 = k\int\limits_0^1 \arcsin(x)$\
$= k\left[x\cdot \arcsin(x) + \sqrt{1-x^2}\right]_0^1$\
$= k\left(1\cdot \arcsin(1) + \sqrt{1-1} - 0\cdot \arcsin(0) + \sqrt{1-0}\right)$\
$= k(\frac{\pi}{2}-1)$\
$= k(\frac{\pi-2}{2}),$

$k = \frac{2}{\pi-2}.$
```

## Zadanie 62
Zmienna losowa $X$ ma dystrybuantę postaci

$F(x) = \begin{cases}
0         & \text{dla } x \le 0, \\
3x^2-2x^3 & \text{dla } x \in (0, 1]. \\
1         & \text{dla } x > 1.
\end{cases}$

Znaleźć funkcję gęstości. Obliczyć $E(X)$, $Var(X)$, $P(0 < X < \frac{1}{2})$, $P(X > \frac{1}{3})$.

```{dropdown} Rozwiązanie

$f(x) = \begin{cases}
6x-6x^2 & \text{dla } x \in (0, 1), \\
0       & \text{w p.p.}
\end{cases}$

$E(X) = \int\limits_0^1 6x^2-6x^3 = 0.5,$

$E(X^2) = \int\limits_0^1 6x^3-6x^4 = 0.3,$

$Var(X) = 0.3 - 0.25= 0.05.$

$P(0 < X < \frac{1}{2}) = P(X < \frac{1}{2}) - P(X < 0) = 3(\frac{1}{2})^2-2(\frac{1}{2})^3 = 0.5,$

$P(X > \frac{1}{3}) = 1 - P(X < \frac{1}{3}) = 1 - 3(\frac{1}{3})^2 + 2(\frac{1}{3})^3 = \frac{20}{27}.$
```

## Zadanie 63
Dystrybuanta pewnej zmiennej losowej $X$ jest postaci

$F(x) = \begin{cases}
0   & \text{dla } x \le 0, \\
x^3 & \text{dla } x \in (0, 1], \\
1   & \text{dla } x > 1.
\end{cases}$

Znaleźć funkcję gęstości, obliczyć $E(X)$, $Var(X)$, $P(0 < X <\frac{1}{2})$, medianę oraz $x_{0.2}$ i $x_{0.729}$.

```{dropdown} Rozwiązanie

$f(x) = \begin{cases}
3x^2 & \text{dla } x \in (0, 1), \\
0    & \text{w p.p.}
\end{cases}$

$E(X) = \int\limits_0^1 3x^3 dx = \frac{3}{4},$

$E(X) = \int\limits_0^1 3x^4 dx = \frac{3}{5},$

$Var(X) = \frac{3}{5} - (\frac{3}{4})^2 = \frac{3}{80}.$

$P(0 < X < \frac{1}{2}) = P(X < \frac{1}{2}) - P(X < 0) = (\frac{1}{2})^3 = \frac{1}{8}$

$P(X < x_{0.5}) = 0.5,$

$x_{0.5}^3 = 0.5,$

$x_{0.5} = 0.5^\frac{1}{3}.$

$P(X < x_{0.2}) = 0.2,$

$x_{0.2}^3 = 0.2,$

$x_{0.2} = 0.2^\frac{1}{3}.$

$P(X < x_{0.729}) = 0.729,$

$x_{0.729}^3 = 0.729,$

$x_{0.729} = 0.729^\frac{1}{3} = 0.9.$
```

## Zadanie 64
Niech zmienna losowa $X$ ma rozkład normalny $N(\mu , \sigma^2)$. Wówczas rozkład zmiennej losowej $Y = exp(X)$ nazywamy rozkładem lognormalnym z parametrami $\mu$, $\sigma$. Oblicz wartość oczekiwaną i wariancje zmiennej losowej $Y$.

```{dropdown} Rozwiązanie

$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

Należy doprowadzić poniższe równania do takiej postaci aby pojawiała się gęstość rozkładu normalnego, wtedy całka będzie wynosić 1.

$\begin{aligned}E(Y) &= E(e^X) = \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}e^x dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2 - 2\sigma^2 x}{2\sigma^2}} dx = \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{x^2-2\mu x +\mu^2 - 2\sigma^2 x}{2\sigma^2}} dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{x^2-2(\mu + \sigma^2)x + (\mu + \sigma^2)^2 - (\mu + \sigma^2)^2 + \mu^2}{2\sigma^2}} dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-2(\mu + \sigma^2))^2 - (\mu + \sigma^2)^2 + \mu^2}{2\sigma^2}} dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-2(\mu + \sigma^2))^2}{2\sigma^2} - \frac{\mu^2-(\mu + \sigma^2)^2}{2\sigma^2}} dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-2(\mu + \sigma^2))^2}{2\sigma^2}} e^{-\frac{\mu^2-(\mu + \sigma^2)^2}{2\sigma^2}} dx = \\
&= e^{-\frac{\mu^2-(\mu + \sigma^2)^2}{2\sigma^2}} = \\
&= e^{\mu + \frac{\sigma^2}{2}}\end{aligned}$

$\begin{aligned}E(Y^2) &= E(e^2X) = \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}e^{2x} dx = \\
&= \int\limits_{-\infty}^\infty \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-(\mu+2\sigma^2))^2}{2\sigma^2}} e^{-\frac{(\mu^2-(\mu+2\sigma^2)^2)}{2\sigma^2}}dx = e^{-\frac{(\mu^2-(\mu+2\sigma^2)^2)}{2\sigma^2}} = \\
&= e^{2\mu + 2\sigma^2}\end{aligned}$

$Var(Y) = e^{2\mu + 2\sigma^2} - \left(e^{\mu + \frac{\sigma^2}{2}}\right)^2 = e^{2\mu + \sigma^2} (e^{\sigma^2} - 1)$
```

## Zadanie 65
Mówimy, że ciągła zmienna losowa $X$ ma rozkład gamma z parametrami $\alpha > 0$, $\beta > 0$, jeśli gęstość prawdopodobieństwa zmiennej $X$ jest postaci:

$f(x) = \begin{cases}
\frac{\beta^{\alpha} x^{\alpha - 1} e^{-\beta x}}{\Gamma(\alpha)} & \text{dla } x > 0, \\
0                                                                 & \text{poza tym}.
\end{cases}$

Oblicz wartość oczekiwaną i wariancję zmiennej losowej $X$.

```{dropdown} Rozwiązanie

$\begin{aligned}E(X) &= \int\limits_{-\infty}^\infty \frac{\beta^{\alpha} x^{\alpha - 1} x e^{-\beta x}}{\Gamma(\alpha)} = \frac{\beta^\alpha\Gamma(\alpha+1)}{\beta^{\alpha+1}\Gamma(\alpha)} \int\limits_{-\infty}^\infty \frac{\beta^{\alpha+1}}{\Gamma(\alpha+1)} x^{(\alpha + 1)- 1} e^{-\beta x} = \\
&= \frac{\Gamma(\alpha+1)}{\beta\Gamma(\alpha)} = \frac{\alpha\Gamma(\alpha)}{\beta\Gamma(\alpha)} = \\
&= \frac{\alpha}{\beta},\end{aligned}$

$\begin{aligned}E(X^2) &= \int\limits_{-\infty}^\infty \frac{\beta^{\alpha} x^{\alpha - 1} x^2 e^{-\beta x}}{\Gamma(\alpha)} = \frac{\beta^\alpha\Gamma(\alpha+2)}{\beta^{\alpha+2}\Gamma(\alpha)} \int\limits_{-\infty}^\infty \frac{\beta^{\alpha+2}}{\Gamma(\alpha+2)} x^{(\alpha + 2)- 1} e^{-\beta x} = \\
&= \frac{\Gamma(\alpha+2)}{\beta^2\Gamma(\alpha)} = \frac{(\alpha+1)\alpha\Gamma(\alpha)}{\beta^2\Gamma(\alpha)} = \\
&= \frac{\alpha^2+\alpha}{\beta^2},\end{aligned}$

$Var(X) = \frac{\alpha^2+\alpha}{\beta^2} - \frac{\alpha^2}{\beta^2} = \frac{\alpha}{\beta^2}.$
```

## Zadanie 66
Zmienne losowe $X$, $Y$ są niezależne i mają jednakową gęstość $f$. Wyznacz gęstość zmiennych losowych:\
a) $Z = max(X, Y)$,\
b) $U = min(X, Y)$.

```{dropdown} Rozwiązanie

a)

$\begin{aligned}P(Z < z) &= P(max(X,Y)<z) = P(X<z, Y<z) = \\
&= P(X<z)P(Y<z)=F^2\end{aligned}$

$f_Z(z) = 2Ff$

b)

$\begin{aligned}P(U < u) &= P(min(X,Y)<u) = 1 - P(min(X,Y)>u) = \\
&= 1 - P(X>u,Y>u) = 1 - P(X>u)p(Y>u) = \\
&= 1 - (1 - P(X<u))(1 - P(Y<u)) = 1-(1-F)(1-F) = \\
&= 1-(1-F)^2\end{aligned}$

$f_U(u) = 2f(1-F)$
```

## Zadanie 67
Zmienne losowe $X$, $Y$ są niezależne i mają dystrybuanty $F$, $G$, odpowiednio. Wyznacz dystrybuanty następujących zmiennych losowych:\
a) $Z = max(X, Y)$,\
b) $U = min(X, Y)$,\
c) $V = max(2X, Y)$,\
d) $W = min(X^2, Y)$.

```{dropdown} Rozwiązanie

a)

$\begin{aligned}P(Z < z) &= P(max(X,Y)<z) = P(X<z, Y<z) = \\
&= P(X<z)P(Y<z) = FG\end{aligned}$

b)

$\begin{aligned}P(U < u) &= P(min(X,Y)<u) = 1 - P(min(X,Y)>u) = \\
&= 1 - P(X>u,Y>u) = 1 - P(X>u)p(Y>u) = \\
&= 1 - (1 - P(X<u))(1 - P(Y<u)) = 1-(1-F)(1-G)\end{aligned}$

c)

$\begin{aligned}P(V < v) &= P(max(2X,Y)<v) = P(2X<v, Y<v) = \\
&= P(X<\frac{v}{2})P(Y<v) = F(\frac{v}{2})G(v)\end{aligned}$

d)

$\begin{aligned}P(W < w) &= P(min(X^2,Y)<w) = 1 - P(min(X^2,Y)>w) = \\
&= 1 - P(X^2>w,Y>w) = 1 - P(X^2>w)P(Y>w) = \\
&= 1 - (1 - P(X^2<w))(1 - P(Y<w)) = \\
&= 1 - (1 - P(-\sqrt{w}<X<\sqrt{w}))(1 - G(w)) = \\
&= 1 - (1 - F(\sqrt{w})+F(\sqrt{w}))(1 - G(w))\end{aligned}$
```

## Zadanie 68
$X$, $Z$ są niezależnymi zmiennymi losowymi. Zmienna losowa $X$ jest typu ciągłego z gęstością $f$ i $P(X>0)=1$. Zmienna losowa $Z$ ma rozkład $Bin(1,p)$. Znajdź dystrybuantę i gęstość zmiennej $Y = ZX$.

```{dropdown} Rozwiązanie

$P(X > 0) = 1$

$1 - P(X < 0) = 1$

$P(X < 0) = 0$

stąd $f(x) = 0$ dla $x<0$.

$q = 1-p$

$P(Z = 0) = q$

$P(Z = 1) = p$

$P(Y < y) = P(ZX < y) = P(Z=0, 0<y) + P(Z=1, X<y)$
$ = P(Z=0) \mathbb{1}_{(-\infty, 0)} + P(Z=1)P(X<y)$

$ = q \mathbb{1}_{(-\infty, 0)} + pF_X(y)$

Ostatecznie:

$
F_Y(y)={\begin{cases}
0         & {\text{dla }} y<0,\\
q         & {\text{dla }} y=0,\\
q+pF_X(y) & {\text{dla }} y>0.
\end{cases}}
$

$
f_Y(y)= pf_X(y) \text{   dla } y>0.
$
```
