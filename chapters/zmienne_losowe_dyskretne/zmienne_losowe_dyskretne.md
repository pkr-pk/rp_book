# Zmienne losowe dyskretne

<h3>Zmienna losowa dyskretna</h3>

W skrócie jest to funkcja, która przypisuje liczby zdarzeniom elementarnym. Zmienna losowa jest określona na przestrzeni zdarzeń elementarnych a jej wartości są ze zbioru liczb rzeczywistych. Zmienna losowa jest dyskretna jeśli jej zbiór wartości jest dyskretny.

<h3>Rozkład prawdopodobieństwa</h3>

Jest to miara probabilistyczna (nie będę wnikał co to jest) przypisująca prawdopodobieństwa zbiorom wartości danej zmiennej, odpowiadającym zdarzeniom elementarnym.

Dla zmiennej losowej dyskretnej możemy wprowadzić pojęcie funkcji prawdopodobieństwa: 

$$P(X=x_i) = p_i,$$

jest to prawdopodobieństwo kiedy zmienna losowa $X$ przyjmuje konkretną wartość $x_i$.

Przykład: 

Dla rzutów monetą funkcję prawdopodobieństwa można zobrazować jako tabelkę:

| Zdarzenie | | orzeł | reszka |
| :-: | :-: | :-: | :-: |
|Zmienna losowa | $x_i$ | 0 | 1 |
|Prawdopodobieństwo | $p_i$ | 0.5 | 0.5 |

<h3>Dystrybuanta</h3>

Dystrybuantą zmiennej losowej $X$ nazywamy funkcję $F(x)$ określoną na zbiorze liczb rzeczywistych jako: 

$$F(x) = P(X \le x)$$

Dla zmiennej dyskretnej:

$$F(x) = P(X \le x) = \sum\limits_{x_i < x}{P(X = x_i) } =  \sum\limits_{x_i < x}p_i$$

<h3>Wartość oczekiwana</h3>

Wartość oczekiwana zmiennej losowej $X$ określona jest wzorem:

$$E(X) = \sum\limits_{i=1}^n x_ip_i.$$

<h3>Własności wartości oczekiwanej</h3>

* $E(c) = c,$
* $E(aX+b) = aE(X) + b,$
* $E(X + Y) = E(X) + E(Y),$
* $E(X - Y) = E(X) - E(Y),$
* $E(X_1+X_2+...+X_n)=E(X_1)+E(X_2)+...+E(X_n),$
* Jeżeli zmienne losowe $X$ i $Y$ są niezależne to $E(XY)=E(X)E(Y).$
* Twierdzenie LOTUS:

$$E[g(X)]=\sum\limits_{x_k∈R_X}g(x_k)P_X(x_k).$$

<h3>Wariancja</h3>

Wariancja zmiennej losowej $X$ określona jest wzorem:

$$Var(X) = \sum\limits_{i=1}^n [x_i - E(X)]^2 p_i,$$

można zapisać również:

$$Var(X) = E\{[X - E(X)]^2\}.$$

<h3>Własności wariancji</h3>

* $Var(X)=E(X^2)-[E(X)]^2,$
* $Var(c)=0,$
* $Var(a\cdot X)=a^2\cdot Var(X),$
* $D^{2}(X+b)=D^{2}(X),$
* jeżeli zmienne losowe $X$ i $Y$ są niezależne to $D^{2}(X\pm Y)=D^{2}(X)+D^{2}(Y),$
* $Var(X) = E(X^2) - (E(X))^2.$

<h3>Mediana</h3>

Kwantylem rzędu $p$, gdzie $0\le p\le 1$, w rozkładzie empirycznym $P_{X}$ zmiennej losowej $X$ nazywamy taką wartość $x_{p}$ zmiennej losowej $X$  dla której spełnione są nierówności:

$P_{X}((-\infty, x_{p}]) \ge p$

oraz

$P_{X}([x_{p}, \infty)) \ge 1 - p.$

Kwantyl rzędu $\frac{1}{2}$ to inaczej mediana.

<h3>Dominanta</h3>

Dominanta to statystyka dla zmiennych o rozkładzie dyskretnym, wskazująca na wartość o największym prawdopodobieństwie wystąpienia.

<h3>Rozkład dwumianowy, rozkład Bernoulliego</h3>

Dyskretny rozkład prawdopodobieństwa opisujący liczbę sukcesów $k$ w ciągu $n$ niezależnych prób, z których każda ma stałe prawdopodobieństwo sukcesu równe $p$. Pojedynczy eksperyment nosi nazwę próby Bernoulliego. Jeżeli zmienna losowa $X$ pochodzi z rozkładu dwumianowego to oznaczamy $X \sim B(n, p)$

Funkcja rozkładu prawdopodobieństwa:

$$P(X = k) = P_n(k) = {n \choose k}p^k(1-p)^{n - k}.$$

Wartość oczekiwana:

$$E(X) = np.$$

Wariancja:

$$Var(X) = np(1 - p).$$

<h3>Rozkład Poissona</h3>

Dyskretny rozkład prawdopodobieństwa, wyrażający prawdopodobieństwo szeregu wydarzeń mających miejsce w określonym czasie, gdy te wydarzenia występują ze znaną średnią częstotliwością $\lambda$ i w sposób niezależny od czasu jaki upłynął od ostatniego zajścia takiego zdarzenia. Rozkład Poissona można również stosować w odniesieniu do liczby zdarzeń w innych określonych przedziałach, takich jak odległość, powierzchnia lub objętość. Jeżeli zmienna losowa $X$ pochodzi z rozkładu Poissona to oznaczamy $X \sim Pois(\lambda)$ lub $X \sim P(\lambda)$

Funkcja rozkładu prawdopodobieństwa:

$$P(X = k) = f(k, \lambda) = \frac{\lambda^ke^{-\lambda}}{k!}.$$

Wartość oczekiwana:

$$E(X) = \lambda.$$

Wariancja:

$$Var(X) = \lambda.$$