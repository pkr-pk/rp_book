# Funkcje charakterystyczne

Funkcją charakterystyczną zmiennej losowej $X$ nazywamy wartość oczekiwaną funkcji $e^{itX}$, gdzie $t$ jest zmienną rzeczywistą, a $i$ - tzw. jednostką urojoną; oznaczmy tę funkcję przez $\phi(t)$:

$$\forall_{t \in \mathbb{R}} \phi(t) = E(e^{itX}).$$

Korzystając z definicji wartości oczekiwanej można zapisać:

$$\phi(t) = \begin{cases}
\sum\limits_{k}p_ke^{itx_k}                 & \text{dla zm los. dyskretnej o rozkładzie } P(X = x_k) = p_k, \text{gdzie } \sum_k p_k = 1, \\
\int\limits_{-\infty}^{\infty}e^{itx}f(x)dx & \text{dla zm. los. typu ciągłego o gęstości } f. \\
\end{cases}$$

<h3>Wzór I</h3>

Przy założeniu istnienia skończonej całki $\int_{-\infty}^\infty |\phi(t)| dt$, zachodzi wzór:

$$f(x)=F'(x) = \frac{1}{2\pi} \int\limits_{-\infty}^\infty e^{-itx}\phi(t)dt.$$

<h3>Wzór II</h3>

Jeśli funkcja charakterystyczna ma okres $2\pi$, to przyjmuje tylko wartości całkowite:

$$\forall_{k \in \mathbb{Z}}p_k = \frac{1}{2\pi}\int\limits_{-\pi}^\pi e^{-itk}\phi(t)dt,$$

gdzie $p_k = P(X = k)$ dla $k = 0, \pm1, \pm2,...,$ oraz $\sum_{k}p_k=1,$ przy czym nie wszystkie $p_k$ muszą być dodatnie.

<h3>Twierdzenie I</h3>

Wygodnie jest używać funkcji charakterystycznych do badania rozkładów bo zachodzą następujące zależności:

1. Jeżeli istnieje k-ty moment zmiennej losowej $X$ o funkcji charakterystycznej $\phi$, to $\phi$ jest k-krotnie różniczkowalna (w sposób ciągły) i zachodzi związek: $$E(X^k) = \frac{1}{i^k}\phi^{(k)}(0)$$ oraz jeśli można rozwinąć $\phi(t)$ w szereg Maclaurina, to: $$\phi(t) = \sum_{k=0}^\infty a_k t^k,$$ gdzie: $$a_k = \frac{\phi^{(k)}(0)}{k!}.$$ Dowolny moment zwykły można policzyć z wzoru: $$E(X^k) = \frac{a_kk!}{i^k}.$$

2. Funkcja charakterystyczna sumy dowolnej skończonej liczby niezależnych zmiennych losowych równa się iloczynowi funkcji charakterystycznych tych zmiennych.

<h3>Wzór III</h3>

Funkcja charakterystyczna funkcji zmiennej losowej $Y = g(X)$ jest postaci:

$$\phi(t) = \begin{cases}
\sum\limits_{k}p_ke^{itg(x_k)}                 & \text{dla zmiennej losowej dyskretnej o rozkładzie } p_k = P(X = x_k), \\
\int\limits_{-\infty}^{\infty}e^{itg(x)}f(x)dx & \text{dla zmiennej losowej typu ciągłego o gęstości } f. \\
\end{cases}$$

<h3>Tabela z funkcjami charakterystycznymi poszczególnych rozkładów:</h3>

|Nazwa rozkładu|Rozkład prawdopodobieństwa &emsp;|Funkcja charakterystyczna|
|---|---|---|
|dwumianowy|$p_k = {n\choose k}p^kq^{n-k},$ <br> $k=0,1,...,n$ <br> $p, q > 0,$ $p+q=1$|$\phi(t) = (pe^{it}+q)^n$|
|ujemny dwumianowy|$p_k = {k-1\choose \nu-1}p^\nu q^{k-\nu},$ <br> $k = \nu, \nu + 1,...$ <br> $p, q >0,$ $p+q=1,$ <br> $\nu \in \mathbb{N}$|$\phi(t) = (\frac{pe^{it}}{1-qe^{it}})^\nu$|
|Poissona|$p_k = \frac{e^{-\lambda}\lambda^k}{k!},$ <br>$k\in\mathbb{N_0},$ $\lambda > 0$|$\phi(t)=\exp[\lambda(e^{it}-1)]$|
|jednostajny|$f(x) = \frac{1}{b-a},$<br>$a < x < b$|$\phi(t) = \frac{1}{b-a}\frac{e^{itb}-e^{ita}}{it}$|
|normalny|$f(x)=\frac{1}{\sigma\sqrt{2\pi}}\exp[-\frac{(x-\mu)^2}{2\sigma^2}],$ <br> $\sigma>0,$ $\mu\in\mathbb{R}$|$\phi(t) = \exp(i\mu t - \frac{\sigma^2t^2}{2})$|
|gamma|$f(x)=\frac{1}{\lambda^p\Gamma(p)}x^{p-1}\exp(-\frac{x}{\lambda}),$<br> $x, \lambda, p > 0$|$\phi(t)=\frac{1}{(1-i\lambda t)^p}$|
|Laplace'a|$f(x) = \frac{1}{2}e^{-\|x\|}$|$\phi(t)=\frac{1}{1+t^2}$|
|Cauchy'ego|$f(x)=\frac{\lambda}{\pi[\lambda^2+(x-\mu)^2]},$<br>$\lambda>0,$ $\mu\in\mathbb{R}$|$\phi(t) = e^{i\mu t-\lambda \|t\|}$|
|wykładniczy|$f(x)=\frac{1}{\lambda}\exp(-\frac{x}{\lambda}),$ <br> $x>0$|$\phi(t) = \frac{1}{1-i\lambda t}$|