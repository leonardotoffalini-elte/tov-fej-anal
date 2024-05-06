date: 2024.02.20

pelda normara:
3. $(C[0, 1]), \lvert\lvert \cdot \rvert\rvert_{1}$, $f \in C[0, 1], \lvert\lvert f \rvert\rvert_{1} = \int _{0}^{1}\lvert f \rvert \,$.
Tulajdonsagok kozul az 2. es a 3. trivi
Kell 1. tulajdonsag:
$$
\int _{0}^{1}\lvert f \rvert  \, = 0 \xRightarrow[]{?}  f \equiv 0
$$
Mivel $f$ folytonos ezert ha egy $a \in [0, 1]$ es $f(a) \neq 0$ volna akkor $\exists B_{\delta}$ ugy hogy $f \rvert_{B_{\delta}} \neq 0 \implies \int _{0}^{1}\lvert f \rvert \, \neq 0$

***Megj***.: A normalt ternek a normaja altal indukalt metrika eltolas invarians, vagyis igaz, hgoy $\rho_{\lvert\lvert \cdot \rvert\rvert} (x+z, y+z) = \rho_{\lvert\lvert \cdot \rvert\rvert}(x,y)$ $\forall x, y, z \in X$.

*Feladat*: Mutassunk olyan metrikat $\mathbb{R}$-en, mely nem eltolas invarians, tehat nem normanak az indukalt metrikaja.

### Banach-ter

***Def***.: Azt mondjuk, hogy $(X, \lvert\lvert \cdot \rvert\rvert)$ normalt ter egy *Banach-ter*, ha $X$ teljes metrikus ter a norma altal indukalt metrikaval, ($\rho_{\lvert\lvert \cdot \rvert\rvert}(x,y) := \lvert\lvert x - y \rvert\rvert$)-al.
Vagyis az $(x_{n}) \subset X$-ra: $\lvert\lvert x_{n}-x \rvert\rvert \to 0, \iff \exists N \in \mathbb{N}: \forall n,m > N \text{ melyre } \lvert\lvert x_{n} - x_{m} \rvert\rvert \to 0$.

peldak:
1. $(C[0, 1], \lvert\lvert \cdot \rvert\rvert)$ Banach-ter
Bizonyitas volt elozo felevben. Itt $f_{n}$ tart $f$-hez a normaban, ha egyenletesen tart hozza.

2. $(\mathbb{R}^{d}, \lvert\lvert \cdot \rvert\rvert_{p})$ Banach-ter $\forall d, p \geq 0$
*Biz*.: $(x^{n}) \subset \mathbb{R}^{d}$ Cauchy-sorozat $\lvert\lvert \cdot \rvert\rvert_{p}$ szerint $\iff$ $\forall 1 \leq i \leq d$ es $(x_{i}^{d})\subset \mathbb{R}$ Cauchy-sorozat $\lvert \cdot \rvert$ szerint.
$\implies (x_{i}^{n})\subset \mathbb{R}$ konvergens, $\exists x_{i}\in \mathbb{R}$ $x_{i}^{n}\to x$, $n\to \infty$
$\implies$ $x := (x_{1}, \dots, x_{n})$, $x^{n}\to x$ $(\mathbb{R}^{d}, \lvert\lvert \cdot \rvert\rvert_{p})$-ben

3. $(C[0, 1]), \lvert\lvert \cdot \rvert\rvert_{1}$, $f \in C[0, 1], \lvert\lvert f \rvert\rvert_{1} = \int _{0}^{1}\lvert f \rvert \,$ *NEM* Banach-ter!
*Biz*.: Ellenpelda:
![[nem banach ter pelda]]

Azt latjuk be hogy ha $f_{n}\to f$, akkor $f\rvert_{\left[ 0, \frac{1}{2} \right]} \equiv 0$, $f \rvert_{\left[ \frac{1}{2}, 1 \right]} \equiv 1$ ellentmondas, mert ekkor $f \not\in C[0, 1]$.
$$
\int _{0}^{1/2}\lvert f \rvert  \, = \int _{0}^{1/2}\lvert f-f_{n} \rvert  \, \leq \int _{0}^{1}\lvert f-f_{n} \rvert  \, = \lvert\lvert f-f_{n} \rvert\rvert \to 0
$$
$$
\implies \int _{0}^{1/2}\lvert f \rvert  \, = 0 \implies f \equiv 0 \left[ 0, \frac{1}{2} \right] \text{-en}
$$

$$
\int _{\frac{1}{2} + \frac{1}{n}} ^{1} \, \lvert f-1 \rvert   = \int _{\frac{1}{2} + \frac{1}{n}} ^{ 1} \lvert f - f_{n} \rvert  \, \leq \int _{0}^{1}\lvert f - f_{n} \rvert  \, \to 0
$$
$$
\implies \int  _{\frac{1}{2} + \frac{1}{n}} ^{ 1} \lvert  f-1 \rvert  \,\to 0, n \to \infty \implies \int _{\frac{1}{2}}^{1} \lvert f-1 \rvert  \, = 0
$$

### Skalaris szorzas

***Def***.: $(\cdot, \cdot) : X \times X \to \mathbb{R}$  *skalaris szorzas* ($X$ valos vektorter), ha kovetkezok teljesulnek:
1. $(x, x) = 0 \iff x = 0_{X}$
2. $(x,x) \geq 0$ $\forall x \in X$
3. $(x, y) = (y, x) \forall x,y \in X$ (szimmetria)
4. $(\alpha x + \beta y, z) = \alpha(x, z) + \beta(y, z)$ (bilinearitas)
(Pozitív szemidefinit, szimmetrikus bilinearis forma, valos vektorteren)

*peldak*:
1. $\mathbb{R}^{d}$-n $(x,y) := \sum_{i=1}^{d}x_{i}\cdot y_{i}$, $x, y \in \mathbb{R}^{d}$
2. $C[0, 1]$ $(f, g) := \int _{0}^{1}f\cdot g \,$
3. $\mathscr{l}^{2} := \left\{  (x_{n}) \subset \mathbb{R} : \sum_{n = 1}^{\infty}\lvert x_{n} \rvert^{2} < \infty \right\}$ $(x, y) := \sum_{n=1}^{\infty}x_{n}y_{n}$ 

*Biz*.:
1. $\mathscr{l}^{2}$ vektorter, $\lambda \in \mathbb{R}, (x_{n}) \in e^{2} \implies (\lambda \cdot x_{n}) \in e^{2}$
$$
(x_{n}), (y_{n}) \in e^{2}, \sum_{n = 1} ^{\infty} \lvert x_{n} + y_{n} \rvert ^{2} \leq 2\sum_{n=1}^{\infty} \lvert x_{n} \rvert ^{2} + 2 \sum_{n=1}^{\infty} \lvert y_{n} \rvert ^{2} < \infty \text{ (szamtani, mertani kozep)}
$$

$\sum x_{n}\cdot y_{n} \in R$:
$$
\sum_{n=1}^{\infty} \lvert x_{n}y_{n} \rvert \leq \frac{1}{2} \sum_{n=1}^{\infty} \lvert x_{n} \rvert ^{2} + \frac{1}{2} \sum_{n=1}^{\infty}\lvert y_{n} \rvert ^{2} < \infty
$$

$\implies$ skalaris szorzas tulajdonsagai teljesulnek!! :)



***Def***.: Legyen $(\cdot, \cdot) : X \times X \to \mathbb{R}$  skalaris szorzas, ekkor: $\lvert\lvert x \rvert\rvert := (x, x)^{1/2}$ definicioval $(X, \lvert\lvert \cdot \rvert\rvert)$ normalt ter.

***Biz***.:
1. $\lvert\lvert x \rvert\rvert = 0 \iff x = 0$
2. $\lvert\lvert \lambda x \rvert\rvert = \lvert \lambda \rvert \cdot \lvert\lvert x \rvert\rvert$ 
$\lvert\lvert \lambda x \rvert\rvert = (\lambda x, \lambda x)^{1/2} = (\lambda ^{2}(x, x))^{1/2} = \lvert \lambda \rvert (x, x)^{1/2} = \lvert \lambda \rvert \cdot \lvert\lvert x \rvert\rvert$

3. Kicsit kesobb belatjuk egy tetel kapcsan a haromszog egyenlotlenseget is.


***All***.: Legyen $(X, (\cdot, \cdot))$ egy skalaris szorzassal ellatot ter, ekkor
1. Teljesul a Cauchy-Schwartz-Bunyakovszkij egyenlotlenseg, azaz:
$$
\lvert (x,y) \rvert \leq \lvert\lvert x \rvert\rvert \cdot \lvert\lvert y \rvert\rvert 
$$
2. Paralelogramma azonossag
$$
\lvert\lvert x + y \rvert\rvert  ^{2} + \lvert\lvert x-y \rvert\rvert ^{2} = 2 \cdot \lvert\lvert x \rvert\rvert ^{2} + 2 \cdot \lvert\lvert y \rvert\rvert  ^{2}
$$
3. Skalaris szorzas folytonos , azaz
$$
x_{n} \to x, y_{n} \to y \implies (x_{n}, y_{n}) \to (x,y)
$$
***Biz***.:
2. HF kiszamolni, csak definicioba be kell helyettesiteni.
1. 
	1. tfh $\lvert\lvert y \rvert\rvert = 1$,
$$
0 \leq \lvert\lvert x - (x,y) \cdot y \rvert\rvert ^{2} = (x-(x,y)y, x-(x,y)y)= (x,x) - (x,y)(y,x) - (x,y)(x,y) + (x,y)^{2} \cdot (y,y)
$$
$$
= \lvert\lvert x \rvert\rvert ^{2} - (x,y)^{2} \implies (x,y)^{2} \leq \lvert\lvert x \rvert\rvert ^{2}\implies \lvert (x,y) \rvert \leq \lvert\lvert x \rvert\rvert \cdot 1
$$
	2.  ha $\lvert\lvert y \rvert\rvert \neq 1$ csak skalazzuk jol es keszen vagyunk
$y = t\cdot y'$ $\lvert\lvert y' \rvert\rvert = 1$, $\dots$ a tobbi hf ig?

3. haromszog egyenlotlenseg
$$
\lvert\lvert x + y \rvert\rvert ^{2} = (x+y, x+y) = (x,x) + (y,y) + 2(x,y) = \lvert\lvert x \rvert\rvert ^{2} + \lvert\lvert y \rvert\rvert ^{2} + 2(x,y) \buildrel \text{Cauchy Schwartz} \over \leq \lvert\lvert x \rvert\rvert ^{2} + \lvert\lvert y \rvert\rvert ^{2} + 2 \lvert\lvert x \rvert\rvert \cdot \lvert\lvert y \rvert\rvert = (\lvert\lvert x \rvert\rvert  + \lvert\lvert y \rvert\rvert ) ^{2}
$$
4. Folytonossag
$$
\lvert (x_{n}, y_{n}) - (x,y) \rvert = \lvert (x_{n} - x, y_{n}-y) + (x_{n}-x, y) + (x, y_{n}-y) \rvert
$$
$$
\buildrel \text{Cauchy Schwartz} \over \leq \lvert\lvert x_{n}-x \rvert\rvert \cdot \lvert\lvert y_{n}-y \rvert\rvert  + \lvert\lvert x_{n} - x \rvert\rvert \cdot \lvert\lvert y \rvert\rvert + \lvert\lvert x \rvert\rvert \cdot \lvert\lvert y_{n}-y \rvert\rvert  \to 0 \text{ mert minden tag tart } 0 \text{-hoz}
$$


### Hilbert-ter

***Def***.:  Ha $(X, (\cdot, \cdot))$ Banach-ter a skalaris szorzat altal indukalt normara nezve, akkor $X$ *Hilbert-ter*.
Tehat, ha $\lvert\lvert x \rvert\rvert := (x, x)^{1/2}$, tovabba $\rho_{\lvert\lvert \cdot \rvert\rvert }(x,y) := \lvert\lvert y-x \rvert\rvert$ metrikaval a $(X, \rho_{\lvert\lvert \cdot \rvert\rvert})$ metrikus ter teljes.

Azt mondjuk, hogy $(X, (\cdot, \cdot))$ Hilbert-ter, ha a skalaris szorzat altal indukalt norma altal indukalt metrikaval $X$ teljes metrikus ter.

*peldak*:
1. $(\mathbb{R}^{d}, (\cdot,\cdot))$, $(x,y) = \sum x_{i}\cdot y_{i}$ $\implies \lvert\lvert x \rvert\rvert = (\sum \lvert x_{i} \rvert^{2})^{1/2} = \lvert\lvert x \rvert\rvert_{2}$ Hilbert-ter

2. $(\mathscr{l}^{2}, (\cdot,\cdot))$ Hilbert-ter

*Biz*.: Lasd jegyzet...

3. $\left( C[0, 1], \int _{0}^{1}fg \, \right)$ *NEM* Hilbert-ter!
$$
\lvert\lvert f \rvert\rvert_{2} := \left( \int _{0}^{1}\lvert f \rvert ^{2} \,  \right)^{1/2}
$$
Ellenpelda, ugyanaz mint $C[0,1]$-ben volt $\lvert\lvert \cdot \rvert\rvert_{1}$-al.


### Ortogonalitas

***Def***.: $x, y \in H$, $A, B \subset H$.
1. $x \perp y$, ha $(x, y) = 0$
2. $x \perp A$, ha $\forall y \in A$-ra $(x,y) = 0$
3. $A \perp B$, ha $\forall x \in A$ es $\forall y \in B$ -re $(x,y) = 0$


***Tetel*** (Meroleges vetitesrol).:
1. Legyen $X \subset H$ nem ures konvex, zart halmaz, legyen $x \in H$.
Ekkor $\exists! y \in K$ ugy hogy $\lvert\lvert x- y \rvert\rvert \to \min$, vagyis ha $\operatorname{dist}(x, K) := \inf \{ \lvert\lvert x- z \rvert\rvert : z \in K \} = \lvert\lvert x-y \rvert\rvert$
*Jel*.: $y:= P_{K}x$, $P_{K} : H \to K$ Lipschitz tulajdonsagu $L\leq 1$-el.

2. Legyen $K \subset H$ nemures, zart *alter*, $x \in H$, ekkor a fenti tulajdonsagu $y$ az az egyetlen vektor $K$-ban, amire $x- y \perp K$.
Ilyenkor $P_{K}:H\to K$ linearis lekepezessel $y = P_{K}x$. Tovabba $P_{K}$ legfeljebb $1$ normaju.

***Biz***.:
1. Legyen $d:=\operatorname{dist}(x, K)$. definicio szerint $\exists(y_{n}) \subset K : \lvert\lvert x-y_{n} \rvert\rvert \to d$
Mutassuk meg, hogy $(y_{n})$ Cauchy sorozat
$$
\lvert\lvert y_{n} - y_{m} \rvert\rvert ^{2} = \lvert\lvert y_{n} -x + x - y_{m} \rvert\rvert ^{2} = 2\cdot \lvert\lvert y_{n} - x \rvert\rvert ^{2} + 2 \cdot \lvert\lvert x-y_{m} \rvert\rvert ^{2} - \lvert\lvert y_{n} - x - (x-y_{m}) \rvert\rvert ^{2}
$$
$$
= \dots + \dots - 4 \cdot \left\lvert \left\lvert  \frac{y_{n}+ y_{m}}{2} - x  \right\rvert \right\rvert ^{2} \leq 2 \cdot \lvert\lvert y_{n} - x \rvert\rvert  ^{ 2} + 2 \cdot \lvert\lvert x-y_{m} \rvert\rvert ^{2} - 4 \cdot d^{2} \to 2d^{2} + 2d^{2} - 4d^{2} = 0
$$

Mivel $H$ Hilbert-ter $\implies$ $\exists y =: \lim y_{n} \in K$  es $K$ zartsaga mitatt. Tovabba, $\lvert\lvert x-y_{n} \rvert\rvert \to \lvert\lvert x-y \rvert\rvert = d$.

2. Legyen $K$ zart alter, $x \in H$, $y$ a fenti vektor.
Legyen $z \in K$ tetszoleges. Ekkor kell: $(x-y, z) = 0$.
$$
0 \leq \lvert\lvert x-(y+z) \rvert\rvert ^{2} \text{ mivel } (y + z) \in K \text{ ezert } = \lvert\lvert x -y  \rvert\rvert ^{2} + \lvert\lvert z \rvert\rvert ^{2} - 2(x-y, z) \geq \lvert\lvert x-y \rvert\rvert ^{2}
$$
$$
\implies \lvert\lvert z \rvert\rvert ^{2} - 2(x-y, z)  \geq 0
$$
$$
\implies 2(x-y,z) \leq \lvert\lvert z \rvert\rvert ^{2}
$$
alkalmazzuk ezt $-z \in K$-ra:
$$
-2(x-y,z) \leq \lvert\lvert z \rvert\rvert ^{2}
$$
$$
\implies 2\lvert (x-y, z) \rvert \leq \lvert\lvert z \rvert\rvert ^{2}
$$
Mivel $t\cdot z \in K$, $t \geq 0$
$$
\implies 2t \lvert (x-y, z) \rvert  \leq t ^{2} \cdot \lvert\lvert z \rvert\rvert ^{2} \to 0, \text{ ha } t \to 0
$$
$$
\implies (x-y, z) = 0
$$
3. Ha $x-y \perp K$ akkor $\lvert\lvert x-y \rvert\rvert = \min \{ \lvert\lvert x-z \rvert\rvert : z \in K \}$.
Legyen $z \in K$ tetszoleges. Ekkor
$$
\lvert\lvert x-z \rvert\rvert ^{2} = \lvert\lvert x - y + y -z \rvert\rvert ^{2} = \lvert\lvert x - y \rvert\rvert ^{2} + \lvert\lvert y-z \rvert\rvert ^{2} + 2 (x-y,y-z)
$$
Mivel $y-z \in K$ es $x-y \perp K$ ezert $(x-y, y-z) = 0$
Tehat
$$
\lvert\lvert x-z \rvert\rvert ^{2} \geq \lvert\lvert x-y \rvert\rvert ^{2}
$$

