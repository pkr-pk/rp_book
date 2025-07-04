# Zadania

## Zadanie 1

Wyznaczyć funkcję charakterystyczną rozkładu: \
a) zero-jedynkowego, \
b) geometrycznego, \
c) dwumianowego, \
d) liczby wyrzuconych orłów przy rzucie trzema monetami, \
e) wykładniczego o gęstości

$f(x) = \begin{cases}
\frac{1}{\lambda}exp(-\frac{x-a}{\lambda}) & \text{dla } x > a,   \\
0                                          & \text{dla } x \le a, \\
\end{cases}$

f) Laplace'a o gęstości 

$f(x) = \frac{1}{2}e^{-|x|}.$

```{dropdown} Rozwiązanie

a) 

Gęstość rozkładu zero-jedynkowego to:

$p_k = P(X = k) = \begin{cases}
1-p & \text{dla } k=0, \\
p   & \text{dla } k=1, \\
\end{cases}$

$\phi(t) = \sum\limits_{k} p_k e^{itk} = (1-p)e^{it\cdot0} + pe^{it\cdot 1} = 1-p+pe^{it}.$

b) 

Gęstość rozkładu geometrycznego to:

$p_k = P(X = k) = p(1-p)^{k-1} \text{ dla } k=1, 2, 3,...$

$\begin{aligned}\phi(t) &= \sum\limits_{k} p_k e^{itk} = \sum\limits_{k=1}^\infty p(1-p)^{k-1} e^{itk} = \\
&= \sum\limits_{k=1}^\infty pe^{it}(1-p)^{k-1} (e^{it})^{k-1} = pe^{it} \sum\limits_{k=1}^\infty [(1-p)e^{it}]^{k-1}.\end{aligned}$

Powyżej jest suma szeregu geometrycznego, gdzie $q = (1-p)e^{it}$ co daje:

$\phi(t) = \frac{pe^{it}}{1-(1-p)e^{it}}.$

c)

Gęstość rozkładu dwumianowego to:

$p_k = P(X = k) = {n\choose k}p^kq^{n-k} \text{ dla } k=0, 1, 2,...,n; q= 1-p.$

$\phi(t) = \sum\limits_{k} p_k e^{itk} = \sum\limits_{k=0}^n {n\choose k}p^kq^{n-k}e^{itk} = \sum\limits_{k=0}^n {n\choose k}(pe^{it})^kq^{n-k} = (pe^{it} + q)^n.$

Powyżej skorzystałem z wzoru dwumianowego.

d)

Liczby wyrzuconych orłów przy rzucie trzema monetami to zdarzenia z rozkładu dwumianowego, gdzie $p = q = \frac{1}{2}$. Korzystając z poprzedniego przykadu:

$\phi(t) =  (\frac{1}{2}e^{it} + \frac{1}{2})^3 = \frac{1}{8}(e^{it} + 1)^3.$

e)

$\begin{aligned}\phi(t) &= \int\limits_{-\infty}^{\infty}e^{itx}f(x) dx = \int\limits_{a}^{\infty} e^{itx} \frac{1}{\lambda} \exp(-\frac{x-a}{\lambda}) dx = \\
&= \int\limits_{a}^{\infty} \frac{1}{\lambda} \exp\left(itx-\frac{x-a}{\lambda}\right)dx = \int\limits_{a}^{\infty} \frac{1}{\lambda} \exp\left[\frac{x(\lambda it-1) + a}{\lambda}\right]dx = \\
&= \int\limits_{a}^{\infty} \frac{1}{\lambda} \exp(\frac{a}{\lambda})\exp\left[\frac{x(\lambda it-1) + a}{\lambda}\right]dx = \\
&= \frac{1}{\lambda} \exp(\frac{a}{\lambda}) \int\limits_{a}^{\infty} \exp\left[\frac{x(\lambda it-1)}{\lambda}\right]dx\end{aligned}$

Zbadam istnienie granicy:

$\lim\limits_{N\to\infty} \int\limits_{a}^{\infty} \exp\left[\frac{x(\lambda it-1)}{\lambda}\right]dx = \lim\limits_{N\to\infty}\left[ \frac{\exp\left[\frac{x(\lambda it-1)}{\lambda}\right]}{\frac{\lambda it-1}{\lambda}}\right]_a^N = $

$= \frac{\lambda}{\lambda it - 1} \lim\limits_{N\to\infty}\left[ \exp\left[\frac{x(\lambda it-1)}{\lambda}\right]\right]_a^N = $

$= \frac{\lambda}{\lambda it - 1} \lim\limits_{N\to\infty} \exp\left[\frac{N\lambda it-N}{\lambda}\right] - \frac{\lambda}{\lambda it - 1} \exp\left[\frac{a\lambda it-a}{\lambda}\right] = $

$= \frac{\lambda}{\lambda it - 1} \lim\limits_{N\to\infty} \exp[-\frac{N}{\lambda}] \exp[N it] - \frac{\lambda}{\lambda it - 1} \exp\left[\frac{a\lambda it-a}{\lambda}\right] = $

$= \frac{\lambda}{\lambda it - 1} \lim\limits_{N\to\infty} \exp[-\frac{N}{\lambda}][\cos(Nt)+i\sin(Nt)] - \frac{\lambda}{\lambda it - 1} \exp\left[\frac{a\lambda it-a}{\lambda}\right]$

Pierwszy składnik jest zerem, ponieważ jest to granica iloczynu funkcji, w którym pierwszy czynnik dąży do zera a drugi jest funkcją ograniczoną. Otrzymuję więc:

$\begin{aligned}\phi(t) &= - \frac{1}{\lambda} \exp\left[\frac{a}{\lambda}\right] \frac{\lambda}{\lambda it - 1} \exp\left[\frac{a\lambda it-a}{\lambda}\right] = \\
&= \frac{\lambda}{1- \lambda it} \exp\left[\frac{a\lambda it-a}{\lambda}\right] \exp\left[\frac{a}{\lambda}\right] = \\
&= \frac{\lambda}{1- \lambda it} \exp\left[\frac{a\lambda it-a}{\lambda}+\frac{a}{\lambda}\right] = \\
&= \frac{e^{ait}}{1- \lambda it}.\end{aligned}$

f)

$|x| = \begin{cases}
-x  & \text{dla } x < 0,   \\
x   & \text{dla } x \ge 0, \\
\end{cases}$

$\begin{aligned}\phi(t) &= \int\limits_{-\infty}^{\infty}e^{itx}f(x) dx = \\
&= \int\limits_{-\infty}^{0}e^{itx}\frac{1}{2}e^{x} dx + \int\limits_{0}^{\infty}e^{itx}\frac{1}{2}e^{-x} dx = \\
&= \int\limits_{-\infty}^{0} \frac{1}{2}e^{itx+x}dx + \int\limits_{0}^{\infty}\frac{1}{2}e^{itx-x}dx = \\
&= \frac{1}{2}\left[ \int\limits_{-\infty}^{0} e^{itx+x}dx + \int\limits_{0}^{\infty}e^{itx-x}dx \right].\end{aligned}$

Zbadam istnienie granic:

$\lim\limits_{N\to\infty}\int\limits_{-N}^{0} e^{itx+x}dx + \lim\limits_{M\to\infty}\int\limits_{0}^{M}e^{itx-x}dx =$

$= \lim\limits_{N\to\infty} \left[\frac{e^{itx+x}}{it+1}\right]_{-N}^0 + \lim\limits_{M\to\infty} \left[\frac{e^{itx-x}}{it-1}\right]_0^M$

$= \frac{1}{it+1} - \lim\limits_{N\to\infty} \frac{e^{-itN-N}}{it+1} + \frac{1}{it-1} - \lim\limits_{M\to\infty} \frac{e^{itM-M}}{it-1}$

$=\frac{1}{it+1} - \lim\limits_{N\to\infty} e^{-N}\frac{\cos(Nt) - i\sin(Nt)}{it+1} + \lim\limits_{M\to\infty} e^{-M}\frac{\cos(Mt) + i\sin(Mt)}{it-1} - \frac{1}{it-1}.$

Drugi i czwarty składnik jest zerem, ponieważ są to granice iloczynu funkcji, w których pierwszy czynnik dąży do zera a drugi jest funkcją ograniczoną. Otrzymuję więc:

$\begin{aligned}\phi(t) &= \frac{1}{2}\left[\frac{1}{it+1} - \frac{1}{it-1}  \right] = \\
&= \frac{1}{2}\left[\frac{it-1}{i^2t^2-1} - \frac{it+1}{i^2t^2-1}  \right] = \\
&= \frac{1}{2}\left[\frac{it-1-it-1}{-t^2-1}\right] = \\
&= \frac{1}{2}\left[\frac{2}{t^2+1}\right] = \\
&= \frac{1}{t^2+1}\end{aligned}$
```

## Zadanie 2

Zmienna losowa $X$ ma rozkład prawdopodobieństwa o funkcji charakterystycznej $\phi$. Wyznaczyć funkcję charakterystyczną zmiennej: $Y = aX+b$, gdzie $a$, $b$ są dowolnymi liczbami rzeczywistymi $(a \ne 0)$.

```{dropdown} Rozwiązanie

$Y = aX + b,$

$\begin{aligned}\phi_Y(t) &= E[e^{it(aX+b)}] = \int\limits_{-\infty}^\infty e^{it(ax+b)} f(x) dx = \\
&= \int\limits_{-\infty}^\infty e^{itax+itb} f(x) dx = e^{itb} \int\limits_{-\infty}^\infty e^{itax} f(x) dx = \\
&= e^{itb}\phi(at)\end{aligned}$
```

## Zadanie 3

Zmienna losowa $X$ ma rozkład $N(0,1)$, wyznaczyć rozkład zmiennej losowej $Y = X^2$.

```{dropdown} Rozwiązanie

$f(x)=\frac{1}{\sqrt{2\pi}}\exp(-\frac{x^2}{2}),$

$\begin{aligned}
\phi(t) &= E[\exp(itX^2)] = 
\int\limits_{-\infty}^\infty \exp(itx^2) \frac{1}{\sqrt{2\pi}}\exp(-\frac{x^2}{2})dx = \\
&= \frac{1}{\sqrt{2\pi}}\int\limits_{-\infty}^\infty \exp(itx^2-\frac{x^2}{2})dx=
\frac{1}{\sqrt{2\pi}}\int\limits_{-\infty}^\infty \exp(-\frac{(x\sqrt{1-2it})^2}{2})dx= \\
&= \left|\begin{aligned} y = x\sqrt{1-2it} \\ dy = \sqrt{1-2it}dx \end{aligned}\right|=
\frac{1}{\sqrt{2\pi} \sqrt{1-2it}}\int\limits_{-\infty}^\infty \exp(-\frac{y^2}{2})dy = \\
&= \frac{1}{\sqrt{2\pi} \sqrt{1-2it}} \sqrt{2\pi} = \\
&= \left(\frac{1}{1-2it}\right)^{\frac{1}{2}}
\end{aligned}$

Powyżej skorzystałem z informacji, że całka oznaczona z funkcji Gaussa wynosi $\sqrt{2\pi}$.

Wynik to funkcja charakterystyczna rozkładu gamma o parametrach $\lambda=2$, $p=\frac{1}{2}$, a rozkład gamma z takimi parametrami to rozkład $\chi^2$ z 1 stopniem swobody. Gęstość takiego rozkładu to:

$f(x) = \frac{1}{\sqrt{2}\Gamma(\frac{1}{2})}x^{-\frac{1}{2}}e^{-\frac{x}{2}},$ dla $x>0$.
```

## Zadanie 4

Wyznaczyć gęstość prawdopodobieństwa zmiennej losowej $X$, o funkcji charakterystycznej postaci:\
a) $\phi(t) = \exp(\frac{t^2}{2}),$ \
b) $\phi(t) = \begin{cases}
1-|t| & \text{dla } |t| \le 1,   \\
0     & \text{dla } |t| > 0, \\
\end{cases}$ \
c) $\phi(t) = e^{2it-3|t|},$ \
d) $\phi(t) = e^{2it},$ \
e) $\phi(t) = \cos(t),$ \
f) $\sum\limits_{k=1}(\frac{1}{2})^k\cos(kt).$

```{dropdown} Rozwiązanie

a)

Sprawdzam warunek czy mogę skorzystać z wzoru nr I:

$\int\limits_{-\infty}^\infty \left|\exp(-\frac{t^2}{2})\right|dt = \sqrt{2\pi} < \infty.$

Warunek jest spełniony więc korzystam z wzoru nr I:

$\begin{aligned}f(x) &= \frac{1}{2\pi}\int\limits_{-\infty}^\infty \exp(-itx)\exp(-\frac{t^2}{2})dt =
\frac{1}{2\pi}\int\limits_{-\infty}^\infty exp(-itx - \frac{t^2}{2})dt = \\
&= \frac{1}{2\pi}\int\limits_{-\infty}^\infty exp[-\frac{1}{2}t(ix + ix + t)]dt =
\left|\begin{aligned} u = t + ix \\ du = dt \end{aligned}\right| = \\
&=\frac{1}{2\pi}\int\limits_{-\infty}^\infty exp[-\frac{1}{2}(u - ix)(u + ix)]du =
\frac{1}{2\pi}\int\limits_{-\infty}^\infty exp[-\frac{1}{2}(u^2 +x^2)]du = \\
&=\frac{1}{2\pi}\exp(-\frac{x^2}{2}) \int\limits_{-\infty}^\infty exp(-\frac{u^2}{2})du =
\frac{1}{2\pi}\exp(-\frac{x^2}{2}) \sqrt{2\pi} = \\
&= \frac{1}{\sqrt{2\pi}}\exp(-\frac{x^2}{2})\end{aligned}$

b)

Sprawdzam warunek czy mogę skorzystać z wzoru nr I:

$|1-|t|| = \begin{cases}
1-|t| & \text{dla } -1 < t < 1, \\
|t|-1 & \text{w p.p.},          \\
\end{cases}$

$|t| = \begin{cases}
-t & \text{dla } t < 0,   \\
t  & \text{dla } t\ge0, \\
\end{cases}$

$\int\limits_{-1}^1 |1-|t||dt = \int\limits_{-1}^1 1-|t|dt = $

$= \int\limits_{-1}^0 (1+t)dt + \int\limits_0^1 (1-t)dt = (t+\frac{t^2}{2})\bigr|_{-1}^0 + (t-\frac{t^2}{2})\bigr|_0^1 = $

$= 0+0+1-\frac{1}{2}+1-\frac{1}{2}-0+0=1<\infty.$

Warunek jest spełniony więc korzystam z wzoru nr I:

$\begin{aligned}f(x) &= \frac{1}{2\pi}\int\limits_{-1}^1 \exp(-itx) (1-|t|) dt = \\
&= \frac{1}{2\pi}\left[\int\limits_{-1}^0 \exp(-itx) (1+t) dt  + \int\limits_{0}^1 \exp(-itx) (1-t) dt\right] = \\
&= \frac{1}{2\pi}\left[\frac{ix - e^{ix} + 1}{x^2} - \frac{ix + e^{ix} -1}{x^2}\right] = \\
&= \frac{1}{2\pi}\left[\frac{-e^{ix} + 1 -  e^{ix} +1}{x^2} \right] = \\
&= \frac{1}{2\pi}\left[\frac{2 - 2 \frac{e^{ix} + e^{ix}}{2}}{x^2} \right] = \\
&= \frac{1}{2\pi}\left[\frac{2 - 2\cos(x)}{x^2} \right] = \\
&= \frac{1 - \cos(x)}{\pi x^2}\end{aligned}$

c)

Sprawdzam warunek na zastosowanie wzoru nr I:

$|\phi(t)|=|e^{2it-3|t|}| = e^{-3|t|}|\cos(2t) + i\sin(2t)| = e^{-3|t|},$

$\int\limits_{-\infty}^\infty e^{-3|t|} dt = 2\int\limits_0^\infty e^{-3t} dt=\frac{2}{3} <\infty.$

Warunek jest spełniony więc można użyć wzoru nr I:

$f(x) = \frac{1}{2\pi}\int\limits_{-\infty}^\infty e^{-itx+2it-3|t|}dt.$

W całce pojawiają się nieskończoności więc należy zbadać istnienie granic:

$\lim\limits_{N\to\infty} \int\limits_{-N}^0 e^{-itx + 2it + 3t} dt + \lim\limits_{M\to\infty} \int\limits_0^M e^{-itx + 2it - 3t} dt =$

$= \lim\limits_{N\to\infty} \left[\frac{e^{3t + 2it + itx}}{3+2i-ix} \right]_{-N}^0 + \lim\limits_{M\to\infty} \left[\frac{e^{-3t + 2it - itx}}{-3+2i-ix} \right]_0^M =$

$= \frac{1}{3+2i-ix} - \lim\limits_{N\to\infty} \frac{e^{-3N - 2iN - iNx}}{3+2i-ix} + \lim\limits_{M\to\infty} \frac{e^{-3M + 2iM - iMx}}{-3+2i-ix} - \frac{1}{-3+2i-ix} =$

$= \frac{1}{3+2i-ix} - \lim\limits_{N\to\infty} e^{-3N} \frac{e^{-2iN - iNx}}{3+2i-ix} + \lim\limits_{M\to\infty} e^{-3M}\frac{e^{2iM - iMx}}{-3+2i-ix} - \frac{1}{-3+2i-ix} =$

$= \frac{1}{3+2i-ix} - \lim\limits_{N\to\infty} e^{-3N} \frac{\cos(-2N - Nx) + i\sin(-2N - Nx)}{3+2i-ix} +$

$+ \lim\limits_{M\to\infty} e^{-3M}\frac{\cos(2M-Mx) + i\sin(2M-Mx)}{-3+2i-ix} - \frac{1}{-3+2i-ix}$

Drugi i trzeci składnik jest zerem, ponieważ są to granice iloczynu funkcji, w których pierwszy czynnik dąży do zera a drugi jest funkcją ograniczoną. Otrzymuję więc:

$\begin{aligned}f(x) &= \frac{1}{2\pi}\left(\frac{1}{3+2i-ix} - \frac{1}{-3+2i-ix}\right) = \\
&= \frac{1}{2\pi}\left[\frac{1}{i(2-x)+3} - \frac{1}{i(2-x)-3}\right] = \\
&= \frac{1}{2\pi}\left[\frac{i(2-x)-3}{i^2(2-x)^2-9} - \frac{i(2-x)+3}{i^2(2-x)^2-9}\right] = \\
&= \frac{1}{2\pi}\left[\frac{i(2-x) - 3 - i(2-x) - 3}{-(2-x)^2-9}\right] = \\
&= \frac{1}{\pi}\frac{3}{(2-x)^2+9}\end{aligned}.$

Jest to gęstość rozkładu Cauchy'ego o parametrach $\mu = 2$, $\lambda=3$.

d)

Ponieważ $|\phi(t)| = 1$, więc nie istnieje całka skończona $\int\limits_{-\infty}^\infty|\phi(t)|dt$ i nie można skorzystać z wzoru nr I. Ponieważ $e^{2it}$ jest funkcją okresową, więc zmienna losowa jest typu skokowego. Korzystam więc z definicji funkcji charakterystycznej:

$\sum\limits_k p_ke^{itx_k} \equiv e^{2it},$ 

gdzie $p_k = P(X = x_k).$ 

Ponieważ funkcja charakterystyczna zmiennej losowej wyznacza rozkład jednoznacznie, to lewa strona powyższej tożsamości musi być równa prawej stronie. Jest to prawdą gdy:

$p_k = 1,$ 

$x_k = 2.$

Szukany rozkład to rozkład jednopunktowy:

$P(X = 2) = 1.$

e)

Nie istnieje całka skończona $\int\limits_{-\infty}^\infty|\phi(t)|dt$ i nie można skorzystać z wzoru nr I. Ponieważ $\cos(t)$ jest funkcją okresową, więc zmienna losowa jest typu skokowego. Korzystam więc z definicji funkcji charakterystycznej oraz z informacji o wzorze nr II: $x_k = 0, \pm 1, \pm 2, ...$ i $\sum_k p_k = 1$. Mam:

$\sum\limits_k p_ke^{itx_k} \equiv \cos(t),$ gdzie $p_k = P(X = x_k).$

$p_k(e^{itx_k} + e^{-itx_k}) \equiv \cos(t)$

$2p_k \cos(tx_k) \equiv \cos(t)$

Wynika z tego, że:

$x_k = 1 \vee x_k = -1,$

$p_k = \frac{1}{2}.$

Szukany rozkład prawdopodobieństwa to:

$P(X = -1) = \frac{1}{2},$ $P(X = 1) = \frac{1}{2}.$

f)

Nie istnieje całka skończona $\int\limits_{-\infty}^\infty|\phi(t)|dt$ i nie można skorzystać z wzoru nr I. Ponieważ $\cos(t)$ jest funkcją okresową, więc zmienna losowa jest typu skokowego. Korzystam więc z definicji funkcji charakterystycznej oraz z informacji o wzorze nr II: $x_k = 0, \pm 1, \pm 2, ...$ i $\sum_k p_k = 1$. Mam:

$\sum\limits_k p_ke^{itx_k} \equiv \sum\limits_{k=1}(\frac{1}{2})^k\cos(kt),$ gdzie $p_k = P(X = x_k).$

$p_k(e^{itx_k} + e^{-itx_k}) \equiv (\frac{1}{2})^k\cos(kt)$

$2p_k \cos(tx_k) \equiv (\frac{1}{2})^k\cos(kt)$

Wynika z tego, że:

$x_k = k \vee x_k = -k,$

$p_k = \frac{1}{2}(\frac{1}{2})^k.$

Szukany rozkład prawdopodobieństwa to:

$P(X = k) = \frac{1}{2}(\frac{1}{2})^{|k|},$ dla $k\in\mathbb{Z}-\{0\}.$
```

## Zadanie 5

Wyznaczyć za pomocą funkcji charakterystycznych:\
a) drugi moment zwykły rozkładu Poissona,\
b) trzeci moment zwykły rozkładu dwumianowego, \
c) czwarty moment zwykły rozkładu $N(0, 1)$, \
d) k-ty moment zwykły rozkładu wykładniczego, o gęstości 

$f(x) = \frac{1}{\lambda}\exp(-\frac{x}{\lambda})$ dla $x>0$, $\lambda>0$,

e) k-ty moment zwykły dwuparametrowego rozkładu gamma o gęstości 

$f(x) = \frac{a^p}{\Gamma(p)}x^{p-1}e^{-ax}$ dla $x>0$, $a, p >0$.

```{dropdown} Rozwiązanie

W rozwiązaniach skorzystam z twierdzenia nr I.

a)

$\phi(t) = e^{\lambda(e^{it}-1)},$

$\phi'(t) = \lambda i e^{it} e^{\lambda(e^{it}-1)},$

$\phi''(t) = -\lambda^2 e^{2it} e^{\lambda(e^{it}-1)} -\lambda e^{it} e^{\lambda(e^{it}-1)},$

$\phi''(0) = -\lambda^2-\lambda$

$EX^2 = \frac{1}{i^2}(-\lambda^2 - \lambda) = \lambda^2 + \lambda$

b)

$\phi(t) = (pe^{it}+q)^n,$

$\phi'(t) = inpe^{it}(e^{i t}p + q)^{n-1},$

$\phi''(t) = -npe^{it}(e^{it}p + q)^{n-1} - (n-1)np^2e^{2it}(e^{it}p + q)^{n-2},$

$\begin{aligned}\phi'''(t) &= -inpe^{it}(e^{it}p + q)^{n-1}-3in(n-1)p^2e^{2it}(e^{it}p + q)^{n-2} - \\
&- in(n-1)(n-2)p^3e^{3it}(e^{it}p + q)^{n-3},\end{aligned}$

$\begin{aligned}\phi'''(0) &= -inp(p + q)^{n-1}-3in(n-1)p^2(p + q)^{n-2} - \\
&- in(n-1)(n-2)p^3(p + q)^{n-3},\end{aligned}$

ponieważ $q = 1 - p$ to:

$\begin{aligned}\phi'''(0) &= -inp - 3in(n-1)p^2 - in(n-1)(n-2)p^3 = \\
&= -inp[1 + 3(n-1)p + (n-1)(n-2)p^2].\end{aligned}$

$\begin{aligned}EX^3 &= -\frac{1}{i^3}inp[1 + 3(n-1)p + (n-1)(n-2)p^2] = \\
&= np[1 + 3(n-1)p + (n-1)(n-2)p^2].\end{aligned}$

c)

$\phi(t) = \exp(-\frac{t^2}{2}),$

$\phi'(t) = -t\exp(-\frac{t^2}{2}),$

$\phi''(t) = (t^2 - 1) \exp(-\frac{t^2}{2}),$

$\phi'''(t) = (-t^3 + 3t) \exp(-\frac{t^2}{2}),$

$\phi^{(4)}(t) = (t^4 - 6t^2 + 3) \exp(-\frac{t^2}{2}),$

$\phi^{(4)}(0) = 3,$

$EX^4 = \frac{1}{i^4}3 = 3.$

Druga metoda:

Jeżeli znamy rozwinięcie funkcji eksponent w szereg Maclaurina to możemy w szybki sposób wyznaczyć k-ty moment zwykły danego rozkładu.

$\exp(t) = \sum\limits_{k=0}^\infty \frac{t^k}{k!} \text{ dla } r\in\mathbb{R},$

$\exp(-\frac{t^2}{2}) = \sum\limits_{k=0}^\infty \frac{\left(-\frac{t^2}{2}\right)^k}{k!} = \sum\limits_{k=0}^\infty \frac{\left(-1\right)^k t^{2k}}{2^k k!} \text{ dla } r\in\mathbb{R},$

Zgadnie z twierdzeniem I:

$a_{2k} = \frac{\left(-1\right)^k}{2^k k!}$ dla $k\in\mathbb{N_0},$ 

$EX^{2k} = \frac{\left(-1\right)^k (2k)!}{2^k k! i^{2k}} = \frac{(2k)!}{2^k k!}$ dla $k\in\mathbb{N}.$

Dla $k=2$ mamy $EX^4 = 3.$

d)

Wyznaczę $\phi^{(k)}(t)$:

$\phi(t) = (1-\lambda it)^{-1}$

$\phi'(t) = \lambda i(1-\lambda it)^{-2},$

$\phi''(t) = 2 \lambda^2 i^2 (1-\lambda it)^{-3},$

$\phi'''(t) = 6 \lambda^3 i^3 (1-\lambda it)^{-4},$

wynika stąd:

$\phi^{(k)}(t) = k! \lambda^k i^k (1-\lambda it)^{-k-1},$

$\phi^{(k)}(0) = k! \lambda^k i^k,$

$EX^k = \frac{k! \lambda^k i^k}{i^k} = \lambda^k k!,$ $k\in\mathbb{N}.$

e)

Wyznaczę $\phi^{(k)}(t)$:

$\phi(t) = (1-\frac{it}{a})^{-p},$

$\phi'(t) = p\frac{i}{a}(1-\frac{it}{a})^{-p-1},$

$\phi''(t) = p(p+1)\left(\frac{i}{a}\right)^2(1-\frac{it}{a})^{-p-2},$

$\phi'''(t) = p(p+1)(p+2)\left(\frac{i}{a}\right)^3(1-\frac{it}{a})^{-p-3},$

wynika stąd:

$\phi^{(k)}(t) = p(p+1)(p+2) \dots (p+k-1)\left(\frac{i}{a}\right)^k(1-\frac{it}{a})^{-p-k},$

$\phi^{(k)}(0) = p(p+1)(p+2) \dots (p+k-1)\left(\frac{i}{a}\right)^k,$

$EX^k = \frac{1}{i^k} \frac{p(p+1)(p+2) \dots (p+k-1)i^k}{a^k} = \frac{p(p+1)(p+2) \dots (p+k-1)}{a^k},$ $k\in\mathbb{N}.$
```

## Zadanie 6

Niech $X$ i $Y$ będą niezależnymi zmiennymi losowymi. Dla których spośród poniższych rozkładów zachodzi twierdzenie o dodawaniu? Wyznaczyć rozkład zmiennej losowej $Z = X + Y$.\
a) Poissona z parametrami $\lambda_1$ i $\lambda_2$, \
b) wykładniczych z tym samym parametrem $\lambda$, \
c) gamma o gęstościach odpowiednio równych:

$f(x) = \frac{a^{p_1}}{\Gamma(p_1)}x^{p_1-1}e^{-ax},$ $x>0,$

$g(y) = \frac{a^{p_2}}{\Gamma(p_2)}y^{p_2-1}e^{-ay},$ $y>0,$

d) Cauchy'ego o gęstościach:

$f(x) = \frac{\lambda_1}{\pi\left[\lambda_1^2 + (x - \mu_1)^2\right]},$

$g(y) = \frac{\lambda_2}{\pi\left[\lambda_2^2 + (y - \mu_2)^2\right]}.$

```{dropdown} Rozwiązanie

Skorzystam z twierdzenia nr I podpunkt 2: funkcja charakterystyczna sumy dowolnej skończonej liczby niezależnych zmiennych losowych równa się iloczynowi funkcji charakterystycznych tych zmiennych.

a)

$\phi(t) = \exp[\lambda_1(e^{it}-1)]\exp[\lambda_2(e^{it}-1)]= \exp[(\lambda_1+\lambda_2)(e^{it}-1)]$

Zachodzi twierdzenie o dodawaniu dla parametru $\lambda$. Zmienna losowa $Z$ pochodzi z rozkładu Poissona z parametrem $\lambda = \lambda_1 + \lambda_2$.

b)

$\phi(t) = \frac{1}{1-\lambda it}\frac{1}{1-\lambda it} = \frac{1}{(1-\lambda it)^2}$

Nie zachodzi twierdzenie o dodawaniu. Zmienna losowa $Z$ pochodzi z rozkładu gamma z parametrem $p=2$.

c)

$\phi(t) = \frac{1}{\left(1-\frac{it}{a}\right)^{p_1}}\frac{1}{\left(1-\frac{it}{a}\right)^{p_2}} = \frac{1}{\left(1-\frac{it}{a}\right)^{p_1+p_2}}$

Zachodzi twierdzenie o dodawaniu dla parametru $p$. Zmienna losowa $Z$ pochodzi z rozkładu Gamma z parametrami $\lambda = \frac{1}{a},$ $p = p_1+p_2$.

d)

$\phi(t) = \exp(i\mu_1t-\lambda_1|t|)\exp(i\mu_2t-\lambda_2|t|) = \exp[i(\mu_1+\mu_2)t-(\lambda_1+\lambda_2)|t|]$

Zachodzi twierdzenie o dodawaniu dla parametrów $\mu$ i $\lambda$. Zmienna losowa $Z$ pochodzi z rozkładu Cauchy'ego z parametrami $\mu = \mu_1+\mu_2$, $\lambda = \lambda_1+\lambda_2$.
```

## Zadanie 7

Zmienna losowa ma rozkład geometryczny. Wyznaczyć rozkład sumy $r$ niezależnych zmiennych losowych o tym samym rozkładzie geometrycznym.

```{dropdown} Rozwiązanie

$\phi(t) = \left(\frac{pe^{it}}{1-qe^{it}}\right)^r,$

jest to funkcja charakterystyczna ujemnego rozkładu dwumianowego.
```

## Zadanie 8

$X_1,...,X_n$ są niezależnymi zmiennymi losowymi o tym samym rozkładzie $N(\mu, \sigma)$. Wyznaczyć rozkład zmiennej losowej $X = \frac{1}{n}\sum\limits_{i=1}^n X_i$.

```{dropdown} Rozwiązanie

Skorzystam z zadania nr 2 gdzie wyznaczyłem funkcję charakterystyczną zmiennej $Y = aX + b$:

$\phi_Y(t) = e^{itb}\phi_X(at)$,

gdy $b=0$, to:

$\phi_Y(t) = \phi_X(at)$.

Dalej będą oznaczenia zgodne z treścią tego zadania. Wyznaczę najpierw funkcję charakterystyczną zmiennej $Y = \sum\limits_{i=1}^n X_i$:

$\phi_Y(t) = \left[\exp(i\mu t - \frac{\sigma^2t^2}{2})\right]^n = \exp(ni\mu t - \frac{n\sigma^2t^2}{2})$

Zmienna losowa $X$ jest więc postaci:

$X = \frac{1}{n} Y,$

a jej funkcja charakterystyczna to:

$\phi_X(t) = \phi_Y(\frac{1}{n} t),$

$\phi_X(t) = \exp\left[ni\mu \frac{1}{n}t - \frac{n\sigma^2\left(\frac{1}{n}t\right)^2}{2}\right] =  \exp\left(i\mu t - \frac{\sigma^2 t^2}{2n}\right).$

Jest to funkcja charakterystyczna zmiennej losowej pochodzącej z rozkładu $N(\mu, \frac{\sigma}{\sqrt{n}})$.
```

## Zadanie 9

$X$ i $Y$ są niezależnymi zmiennymi losowymi o rozkładach normalnych: $N(\mu_1, \sigma_1)$, $N(\mu_2, \sigma_2)$. Wyznaczyć rozkład zmiennej losowej $Z=aX+bY$.

```{dropdown} Rozwiązanie

Ponownie korzystam ze wzoru z zadania nr 2.

$\begin{aligned}\phi(t) &= \exp(i\mu_1at - \frac{\sigma^2a^2t^2}{2})\exp(i\mu_1bt - \frac{\sigma^2b^2t^2}{2}) = \\
&= \exp\left[it(a\mu_1 + b\mu_2) - \frac{t^2}{2}(a^2\sigma_1^2 + b^2\sigma_2^2)\right].\end{aligned}$

Jest to funkcja charakterystyczna zmiennej losowej pochodzącej z rozkładu $N(a\mu_1 + b\mu_2, \sqrt{a^2\sigma_1^2 + b^2\sigma_2^2})$.
```

## Zadanie 10

Niech $X$ i $Y$ będą niezależnymi zmiennymi losowymi o tym samym rozkładzie wykładniczym o gęstości:

$f(x) = \begin{cases}
e^{-x} & \text{dla } x>0, \\
0      & \text{dla } x\le0.
\end{cases}$

Wyznaczyć rozkład zmiennej losowej $Z = X - Y.$

```{dropdown} Rozwiązanie

Korzystam z wzoru z zadania nr 2 oraz z funkcji charakterystycznej rozkłady wykładniczego o parametrze $\lambda = 1$:

$\phi(t) = \frac{1}{1-it}\frac{1}{1+it} = \frac{1}{1+t^2}.$

Jest to funkcja charakterystyczna zmiennej losowej pochodzącej z rozkładu Laplace'a.
```

## Zadanie 11

Niech $X$ i $Y$ będą niezależnymi zmiennymi losowymi o jednakowych funkcjach charakterystycznych $\phi(t)$. Wyznaczyć funkcję charakterystyczną zmiennej losowej $Z = X - Y.$

```{dropdown} Rozwiązanie

$\phi_Z(t) = \phi(t)\phi(-t) = \phi(t)\overline{\phi(t)} = |\phi(t)|^2,$

gdzie $\overline{\phi(t)}$ oznacza liczbę zespoloną sprzężoną z $\phi(-t)$.
```

## Zadanie 12

Wyznaczyć funkcję charakterystyczną rozkładu prawdopodobieństwa o gęstości:

$f(x) = \begin{cases}
\frac{1}{2}-\frac{|x|}{4} & \text{dla } |x| \le 2, \\
0                         & \text{dla pozostałych } x.
\end{cases}$

```{dropdown} Rozwiązanie

$\phi(t) = \int\limits_{-2}^2 \left(\frac{1}{2}-\frac{|x|}{4}\right)e^{itx}dx = \int\limits_{-2}^0 \left(\frac{1}{2}+\frac{x}{4}\right)e^{itx}dx +  \int\limits_0^2 \left(\frac{1}{2}-\frac{x}{4}\right)e^{itx}dx$

Obliczę powyższe całki oddzielnie:

$\int\limits_{-2}^0 \left(\frac{1}{2} + \frac{x}{4}\right) e^{itx} dx = \int\limits_{-2}^0 \left(\frac{1}{2} + \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right)' dx =$

$= \left[\left(\frac{1}{2} + \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) - \int\limits_{-2}^0 \frac{1}{4it} e^{itx} dx \right]_{-2}^0 = \left[\left(\frac{1}{2} + \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) - \frac{e^{itx}}{4i^2t^2}  \right]_{-2}^0 =$

$= \left[\left(\frac{1}{2} + \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) + \frac{e^{itx}}{4t^2}  \right]_{-2}^0 = \left[\frac{1}{2it} + \frac{1}{4t^2}  \right] - \left[\frac{e^{-2it}}{4t^2}  \right] =$

$= \frac{-2it}{4t^2} + \frac{1}{4t^2} - \frac{e^{-2it}}{4t^2} = \frac{-2it + 1 - e^{-2it}}{4t^2}$

$\int\limits_0^2 \left(\frac{1}{2} - \frac{x}{4}\right) e^{itx} dx = \int\limits_0^2 \left(\frac{1}{2} - \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right)' dx =$

$= \left[\left(\frac{1}{2} - \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) + \int\limits_0^2 \frac{1}{4it} e^{itx} dx \right]_0^2= \left[\left(\frac{1}{2} - \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) + \frac{e^{itx}}{4i^2t^2}  \right]_0^2 =$

$= \left[\left(\frac{1}{2} - \frac{x}{4}\right) \left(\frac{e^{itx}}{it}\right) - \frac{e^{itx}}{4t^2}  \right]_0^2 = \left[- \frac{e^{2it}}{4t^2} \right] - \left[\frac{1}{2it} - \frac{1}{4t^2} \right] =$

$= - \frac{e^{2it}}{4t^2} + \frac{2it}{4t^2} + \frac{1}{4t^2} = \frac{-e^{2it} + 2it + 1}{4t^2}$

Stąd:

$\begin{aligned}\phi(t) &= \frac{-2it + 1 - e^{-2it}}{4t^2} + \frac{-e^{2it} + 2it + 1}{4t^2} = \frac{2 - e^{-2it} - e^{2it}}{4t^2} \\
&= \frac{2 - 2\left(\frac{e^{-2it} + e^{2it}}{2}\right)}{4t^2} = \frac{2 - 2\cos(2t)}{4t^2} = \frac{1 - \cos(2t)}{2t^2} = \\
&= \frac{1 - 1 + 2\sin^2(t)}{2t^2} = \frac{\sin^2(t)}{t^2}.\end{aligned}$
```

## Zadanie 13

Zmienna losowa $X$ ma rozkład wykładniczy z parametrem $\lambda > 0$. Jaki rozkład ma zmienna $Y=\lambda X$.

```{dropdown} Rozwiązanie

$\phi_Y(t) = \phi_X(\lambda t) = \frac{1}{1-i\lambda^2 t}$,

jest to funkcja charakterystyczna rozkładu wykładniczego z parametrem $\lambda^2$.
```

## Zadanie 14

Zmienna losowa ma rozkład gamma z parametrami $\lambda, p > 0$. Jaki rozkład ma zmienna $Y = pX$?

```{dropdown} Rozwiązanie

$\phi_Y(t) = \phi_X(pt) = \frac{1}{(1-i\lambda pt)^p}$,

jest to funkcja charakterystyczna rozkładu gamma z parametrami $\lambda p$, $p$.
```

## Zadanie 15

Zmienna losowa ma rozkład Cauchy'ego z parametrami $\lambda>0,\ \mu \in R$.

Jaki rozkład ma zmienna losowa $Y = (X-\mu)/ \lambda?$

```{dropdown} Rozwiązanie

$Y = \frac{1}{\lambda}X - \frac{\mu}{\lambda}$

$\phi_Y(t) = \exp(-it\frac{\mu}{\lambda})\phi_X(\frac{1}{\lambda}t) =  \exp(-it\frac{\mu}{\lambda})\exp(it\frac{\mu}{\lambda} - \lambda |\frac{1}{\lambda}t|) = \exp(-|t|)$,

jest to funkcja charakterystyczna rozkładu Cauchy'ego z parametrami $\lambda = 1$, $\mu=0$.
```
