# Prawdopodobieństwo klasyczne

Wzór na prawdopodobieństwo klasyczne:

$$P(A)=\frac{|A|}{|\Omega|},$$

gdzie:

$|A|$ - to liczba zdarzeń sprzyjających (moc zbioru $A$),

$|\Omega|$ - to liczba wszystkich możliwych zdarzeń (moc zbioru $\Omega$).

---

<h3>Własności prawdopodobieństwa</h3>

- Prawdopodobieństwo dowolnego zdarzenia losowego $A$ jest zawsze liczbą z przedziału $[0, 1]$: 

$$0 \le P(A) \le 1.$$

- Prawdopodobieństwo zdarzenia pewnego jest równe 1.

$$P(\Omega) = 1.$$

- Prawdopodobieństwo zdarzenia niemożliwego jest równe 0.

$$P(\emptyset) = 0.$$

---

<h3>Przydatne wzory</h3>

* Prawdopodobieństwo zdarzenia przeciwnego:

$$P(A') = 1 − P(A).$$

* Prawdopodobieństwo sumy zdarzeń:

$$P(A \cup B) = P(A) + P(B) − P(A \cap B).$$
      
Ogólnie:

$$P\left(\bigcup\limits_{i=1}^n A_i\right) = 
\sum\limits_{i=1}^nP(A_i) -
\sum\limits_{i < j} P(A_i \cap A_j) +
\sum\limits_{i < j < k} P(A_i \cap A_j \cap A_k) - \ldots +
(-1)^{n-1}P\left(\bigcap\limits_{i=1}^n A_i\right)$$

* Prawa De Morgana:

$$(A_1 \cup A_2 \cup ... \cup A_n)' = A_1' \cap A_2' \cap ... \cap A_n',$$

$$(A_1 \cap A_2 \cap ... \cap A_n)' = A_1' \cup A_2' \cup ... \cup A_n'.$$

* Prawo dystrybucji:

$$A \cap (B \cup C) = (A \cap B) \cup (A \cap C),$$

$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C).$$

---

<h3>Kombinatoryka</h3>

* Kombinacja pozwala policzyć na ile sposobów można wybrać k elementów z n-elementowego zbioru. Wzór na kombinację jest następujący:

$$C^k_n = \frac{n!}{k!(n − k)!}.$$

Kombinacje zapisujemy krótko za pomocą symbolu Newtona:

$${n \choose k} = \frac{n!}{k!(n − k)!}.$$

* Kombinacje z powtórzeniami pozwala policzyć na ile sposobów można wybrać k-elementowy multizbiór złożony z elementów danego zbioru n-elementowego. Liczba k-elementowych kombinacji z powtórzeniami zbioru n-elementowego wyraża się wzorem:

$$\bar{C}_n^k = {k + n - 1 \choose k} = \frac{(k + n - 1)!}{k!(n-1)!}$$

* Permutacja bez powtórzeń zbioru n-elementowego to dowolny n-wyrazowy ciąg utworzony ze wszystkich elementów tego zbioru. Liczbę permutacji zbioru n-elementowego możemy obliczyć ze wzoru:

$$P_n = n!.$$

* Permutacja z powtórzeniami zbioru n-elementowego z powtarzającymi się elementami to dowolny n-wyrazowy ciąg utworzony ze wszystkich elementów tego zbioru. Liczbę permutacji z powtórzeniami zbioru n-elementowego, gdzie element $a_1$ powtarza się $n_1$ razy, ..., $a_k$ powtarza się $n_k$ razy możemy obliczyć ze wzoru:

$$P_n^{n_1,...,n_k} = \frac{n!}{n_1!...n_k!}.$$

* Wariacja z powtórzeniami. Przyjmijmy, że mamy dany zbiór elementów. Wariacja z powtórzeniami pozwala na utworzenie ciągu z elementów tego zbioru, z tym, że dopuszcza powtarzanie elementów. Wzór na wariację z powtórzeniami jest następujący:

$$W^k_n = n^k.$$

* Wariacja bez powtórzeń. Przyjmijmy, że mamy dany zbiór elementów. Wariacja bez powtórzeń pozwala na utworzenie ciągu z elementów tego zbioru, z tym, że nie dopuszcza powtarzania elementów. Wzór na wariację bez powtórzeń jest następujący:

$$V^k_n = \frac{n!}{(n − k)!}.$$

---

<h3>Metoda bootstrap</h3>

Jest to metoda estymacji polegająca na wielokrotnym losowaniu ze zwracaniem z próby. Jest przydatna gdy nie wiemy z jakiego rozkładu pochodzą zmienne losowe. Przykład użycia tej metody do oszacowania prawdopodobieństwa będzie pokazany w kilku zadaniach.
