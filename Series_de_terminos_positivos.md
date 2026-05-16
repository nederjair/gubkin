# Series numéricas de términos positivos

---

## Concepto de serie numérica

Se llama **serie numérica** a una expresión de la forma:

$$a_1 + a_2 + \ldots + a_n + \ldots = \sum_{n=1}^{\infty} a_n$$

donde $a_1, a_2, \ldots, a_n$ es una sucesión de números, $a_n \in \mathbb{R}$, $n \in \mathbb{N}$.

$a_n$ es el **término n-ésimo de la serie**. La expresión analítica del término n-ésimo en forma de fórmula se llama **término general de la serie**.

- Una serie se llama **de signo constante** si todos sus términos tienen el mismo signo.
- Una serie se llama **de signos alternados** si los términos de la serie tienen signos distintos.
- Una serie se llama **de términos positivos** si todos los términos de la serie son positivos.

---

## Convergencia de una serie

La suma de los primeros $n$ términos de la serie:

$$S_n = a_1 + a_2 + \ldots + a_n = \sum_{k=1}^{n} a_k$$

se llama su **suma parcial n-ésima**.

**Una serie se llama convergente** si la sucesión $(S_n)$ de sus sumas parciales tiene límite:

$$\lim_{n \to \infty} S_n = S$$

El valor $S$ se llama **suma de la serie**, lo que se escribe:

$$\sum_{n=1}^{\infty} a_n = S$$

Si para la sucesión $(S_n)$ el límite cuando $n \to \infty$ no existe o es infinito, la serie se llama **divergente**. Una serie divergente no tiene suma.

---

## Resto de una serie

La serie:

$$R_n = a_{n+1} + a_{n+2} + \ldots = \sum_{k=n+1}^{\infty} a_k$$

que se obtiene de la original descartando los primeros $n$ términos consecutivos, se llama **resto n-ésimo de la serie**.

Si una serie converge (diverge), entonces cualquiera de sus restos también converge (diverge).

Si las series $\sum_{n=1}^{\infty} a_n$ y $\sum_{n=1}^{\infty} b_n$ convergen a sumas $S_1$, $S_2$ respectivamente, entonces la serie $\sum_{n=1}^{\infty}(c_1 a_n + c_2 b_n)$ converge a la suma $c_1 S_1 + c_2 S_2$, donde $c_1, c_2 \in \mathbb{R}$.

---

## Condición necesaria de convergencia (CNC)

> **Teorema.** Si la serie $\sum_{n=1}^{\infty} a_n$ converge, entonces su término general tiende a cero cuando $n$ crece sin límite:
> $$\lim_{n \to \infty} a_n = 0$$

**Corolario.** Si el término general de la serie no tiende a cero cuando $n$ crece sin límite, es decir $\lim_{n \to \infty} a_n \neq 0$, entonces la serie **diverge**.

> El estudio de la convergencia de una serie conviene comenzar con la condición necesaria de convergencia. Si esta se cumple, el estudio continúa con criterios suficientes de convergencia.

---

## Series de referencia

### 1. Serie geométrica

$$\sum_{n=0}^{\infty} q^n = 1 + q + q^2 + \ldots + q^n + \ldots$$

- Para $|q| < 1$ — **converge**
- Para $|q| \geq 1$ — **diverge**

### 2. Serie de Dirichlet (serie-p)

$$\sum_{n=1}^{\infty} \frac{1}{n^p} = 1 + \frac{1}{2^p} + \frac{1}{3^p} + \frac{1}{4^p} + \ldots + \frac{1}{n^p} + \ldots$$

- Para $p > 1$ — **converge**
- Para $p \leq 1$ — **diverge**

### 3. Serie armónica (caso particular de la serie de Dirichlet con $p = 1$)

$$\sum_{n=1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \ldots + \frac{1}{n} + \ldots$$

— **diverge**.

---

## Criterios suficientes de convergencia para series de términos positivos

### Criterio de comparación (CC)

Sean dos series de términos positivos:

$$\sum_{n=1}^{\infty} a_n \qquad (1)$$

$$\sum_{n=1}^{\infty} b_n \qquad (2)$$

para las cuales, a partir de cierto $n$ ($n \in \mathbb{N}$), se cumple la condición $a_n \leq b_n$. Entonces:

1. De la convergencia de la serie (2) se deduce la convergencia de la serie (1).
2. De la divergencia de la serie (1) se deduce la divergencia de la serie (2).

---

### Criterio límite de comparación (CLC)

Si para las series de términos positivos (1) y (2) existe el límite finito:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = C \neq 0$$

entonces estas series convergen o divergen simultáneamente.

> La comparación de las series estudiadas se realiza habitualmente con las **series de referencia**.

---

### Criterio de D'Alembert (CD)

Sea para la serie de términos positivos $\sum_{n=1}^{\infty} a_n$:

$$\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = C$$

Entonces:
1. Si $C < 1$ — la serie **converge**.
2. Si $C > 1$ — la serie **diverge**.

> ⚠️ Si $C = 1$, el criterio de D'Alembert no da respuesta — se usan otros criterios.

---

### Criterio límite de Cauchy (CLC)

Sea para la serie de términos positivos:

$$\lim_{n \to \infty} \sqrt[n]{a_n} = C$$

Entonces:
1. Si $C < 1$ — la serie **converge**.
2. Si $C > 1$ — la serie **diverge**.

Al aplicar el criterio límite de Cauchy es útil la fórmula:

$$\lim_{n \to \infty} \sqrt[n]{n} = 1$$

> ⚠️ Si $C = 1$, los criterios límite de D'Alembert y Cauchy no dan respuesta. En este caso, la convergencia de la serie se estudia con otros criterios.

---

### Criterio integral de Cauchy (CIC)

Una serie con términos positivos y monótonamente decrecientes $a_n = f(n)$ **converge (diverge)** si y solo si la integral impropia:

$$\int_1^{+\infty} f(x)\,dx$$

**converge (diverge)**, donde $f(x)$ es una función continua y decreciente.

---

## Ejemplos

### Ejemplo 1. Hallar la suma de la serie

#### (1) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$

Descomponemos el término general en fracciones simples:

$$\frac{1}{n(n+1)} = \frac{A}{n} + \frac{B}{n+1} = \frac{A(n+1) + Bn}{n(n+1)}$$

Igualando coeficientes: $A = 1$, $B = -1$. Entonces:

$$\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}$$

Suma parcial (telescópica):

$$S_n = \left(\frac{1}{1} - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \ldots + \left(\frac{1}{n} - \frac{1}{n+1}\right) = 1 - \frac{1}{n+1}$$

$$S = \lim_{n \to \infty} S_n = \lim_{n \to \infty} \left(1 - \frac{1}{n+1}\right) = 1$$

> Esta serie **converge** a la suma $S = 1$.

---

#### (2) $\displaystyle\sum_{n=2}^{\infty} \frac{4}{4n^2 + 4n - 3}$

Factorizamos: $4n^2 + 4n - 3 = (2n+3)(2n-1)$, entonces:

$$\frac{4}{(2n+3)(2n-1)} = \frac{A}{2n-1} + \frac{B}{2n+3}$$

Resolviendo el sistema: $A = 1$, $B = -1$. Entonces:

$$\frac{4}{(2n+3)(2n-1)} = \frac{1}{2n-1} - \frac{1}{2n+3}$$

Escribimos los términos:

| $n$ | $a_n$ |
|-----|-------|
| $a_2$ | $\frac{1}{3} - \frac{1}{7}$ |
| $a_3$ | $\frac{1}{5} - \frac{1}{9}$ |
| $a_4$ | $\frac{1}{7} - \frac{1}{11}$ |
| $a_5$ | $\frac{1}{9} - \frac{1}{13}$ |

$$S_n = 1 + \frac{1}{3} - \frac{1}{2n-1} - \frac{1}{2n+1}$$

$$S = \lim_{n \to \infty} S_n = \frac{4}{3}$$

> Esta serie **converge** a la suma $S = \dfrac{4}{3}$.

---

#### (3) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{9^n}$

Es una serie geométrica con razón $q = \frac{1}{9} < 1$.

$$S = \frac{b_1}{1-q} = \frac{1/9}{1 - 1/9} = \frac{1}{8}$$

> Esta serie **converge** a la suma $S = \dfrac{1}{8}$.

---

### Ejemplo 2. Condición necesaria de convergencia

#### (1) $\displaystyle\sum_{n=1}^{\infty} \frac{3n}{5n+1}$

$$\lim_{n \to \infty} \frac{3n}{5n+1} = \frac{3}{5} \neq 0$$

> La serie **diverge** por la condición necesaria de convergencia.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n}$

$$\lim_{n \to \infty} \frac{1}{n} = 0$$

La condición necesaria se cumple, pero no es suficiente. Es la serie armónica — **diverge**.

---

### Ejemplo 3. Criterio de comparación

#### (1) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n \cdot 2^n}$

Comparamos con la serie geométrica $\sum \frac{1}{2^n}$:

$$\frac{1}{n \cdot 2^n} \leq \frac{1}{2^n}$$

La serie geométrica con $q = \frac{1}{2} < 1$ converge → la serie dada **converge**.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{\sqrt{n}}$

Comparamos con la serie armónica $\sum \frac{1}{n}$:

$$\frac{1}{n} \leq \frac{1}{\sqrt{n}}$$

La serie armónica diverge → la serie dada **diverge**.

---

### Ejemplo 4. Criterio de D'Alembert

#### (1) $\displaystyle\sum_{n=1}^{\infty} \frac{n}{3^n}$

$$C = \lim_{n \to \infty} \frac{a_{n+1}}{a_n} = \lim_{n \to \infty} \frac{(n+1)/3^{n+1}}{n/3^n} = \lim_{n \to \infty} \frac{n+1}{3n} = \frac{1}{3} < 1$$

> La serie **converge**.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \frac{(2n)! \cdot (n+1)}{3^n(n+2)}$

$$C = \lim_{n \to \infty} \frac{a_{n+1}}{a_n} = \lim_{n \to \infty} \frac{(2n+2)! \cdot 3^n(n+1)}{3^{n+1}(n+2)(2n)!} = \frac{1}{3}\lim_{n \to \infty} \frac{(2n+1)(2n+2)(n+1)}{n+2} = +\infty > 1$$

> La serie **diverge**.

---

#### (3) $\displaystyle\sum_{n=1}^{\infty} \frac{2^n}{(2n+1)!}$

$$C = \lim_{n \to \infty} \frac{a_{n+1}}{a_n} = \lim_{n \to \infty} \frac{2^{n+1}}{(2n+3)!} \cdot \frac{(2n+1)!}{2^n} = 2\lim_{n \to \infty} \frac{1}{(2n+2)(2n+3)} = 0 < 1$$

> La serie **converge**.

---

### Ejemplo 5. Criterio de Cauchy

#### (1) $\displaystyle\sum_{n=1}^{\infty} \left(\frac{2n+1}{3n-2}\right)^n$

$$C = \lim_{n \to \infty} \sqrt[n]{a_n} = \lim_{n \to \infty} \frac{2n+1}{3n-2} = \frac{2}{3} < 1$$

> La serie **converge**.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \ln^n(n^2+1)$

$$a_n = \ln^n(n^2+1), \quad C = \lim_{n \to \infty} \sqrt[n]{a_n} = \lim_{n \to \infty} \ln(n^2+1) = +\infty > 1$$

> La serie **diverge**.

---

#### (3) $\displaystyle\sum_{n=1}^{\infty} \frac{1}{2^n}\left(\frac{n}{n+1}\right)^{n^2}$

$$C = \lim_{n \to \infty} \sqrt[n]{a_n} = \lim_{n \to \infty} \frac{1}{2}\left(\frac{n}{n+1}\right)^n = \frac{1}{2} \cdot \lim_{n \to \infty}\left(1 - \frac{1}{n+1}\right)^n = \frac{1}{2} \cdot e^{-1} = \frac{1}{2e} < 1$$

> La serie **converge**.

---

### Ejemplo 6. Criterio integral de Cauchy

#### (1) $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n \ln n}$

$f(x) = \frac{1}{x \ln x}$ — función continua y decreciente en $[2, +\infty)$.

$$\int_2^{+\infty} \frac{dx}{x \ln x} = \lim_{b \to \infty} \ln\ln x \Big|_2^b = +\infty$$

> La integral diverge → la serie **diverge**.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \frac{2\ln n}{n(1+\ln^2 n)}$

$$\int_1^{+\infty} \frac{2\ln x}{x(1+\ln^2 x)}\,dx = \lim_{b \to \infty} \ln(1+\ln^2 x)\Big|_1^b$$

El cálculo da: $\lim_{b \to \infty}\left(-\frac{1}{1+\ln^2 b} + \frac{1}{1+\ln^2 1}\right) = 0 + 1 = 1$

> La integral converge → la serie **converge**.

---

#### (3) $\displaystyle\sum_{n=1}^{\infty} \frac{14n+1}{7n^2+n-1}$

$$\int_1^{+\infty} \frac{14x+1}{7x^2+x-1}\,dx = \lim_{b \to \infty} \ln(7x^2+x-1)\Big|_1^b = +\infty$$

> La integral diverge → la serie **diverge**.

---

### Ejemplo 7*. Cálculo aproximado de la suma de una serie

#### $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2}$ con precisión hasta $0{,}1$

Estimación del resto de la serie mediante la integral:

$$R_n \leq \int_n^{+\infty} \frac{dx}{x^2} = \frac{1}{n}$$

$$R_n \leq \int_{n+1}^{+\infty} \frac{dx}{x^2} = \frac{1}{n+1}$$

Para garantizar una precisión de $0{,}1$:

$$\frac{1}{n+1} < \frac{1}{10} \implies n \geq 10$$

Tomamos 10 términos de la serie:

$$S \approx \frac{1}{1} + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \frac{1}{25} + \frac{1}{36} + \frac{1}{49} + \frac{1}{64} + \frac{1}{81} + \frac{1}{100} \approx 1{,}6$$

---

## Tarea

### Tarea 1. Condición necesaria de convergencia
Escriba los cinco primeros términos de la serie y compruebe la CNC:

1. $\displaystyle\sum_{n=2}^{\infty} \frac{3n-1}{n(2n-3)}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{7n}{\sqrt{3n^2+1}}$
3. $\displaystyle\sum_{n=1}^{\infty} \tan\frac{2}{n}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{(n+2)!(n+1)!}{n!(n+1)!}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{5n}{2^n}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{2^n}{3^{n-1}(2n-1)!}$

### Tarea 2. Criterios de comparación

1. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n \cdot 11^n}$
2. $\displaystyle\sum_{n=4}^{\infty} \frac{1}{\sqrt{n-3}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{7^n+2}$
4. $\displaystyle\sum_{n=2}^{\infty} \frac{1}{5n-7}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{2n^2-1}{5n^4+2}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{(3n+8)^3}$

### Tarea 3. Criterio de D'Alembert

1. $\displaystyle\sum_{n=1}^{\infty} \frac{n^3}{5^n}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{n \cdot 2^{n/2}}{\sqrt{n+3}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{2(n+1)!}{(n+5) \cdot 3^{n+1}}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{5^{3n}}{(3n)!}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{7^{7n+1}}{5^{5n-2}}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{(3n+2)!}{(4n-1)!}$

### Tarea 4. Criterio de Cauchy

1. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{n+1}{11n-3}\right)^n$
2. $\displaystyle\sum_{n=4}^{\infty} \left(\frac{2n^2+1}{n-3}\right)^{n^2}$
3. $\displaystyle\sum_{n=8}^{\infty} \frac{5^n}{(n-7)^n}$
4. $\displaystyle\sum_{n=2}^{\infty} \left(\frac{7n^2-1}{3n^2-5}\right)^{n^2}$
5. $\displaystyle\sum_{n=2}^{\infty} \frac{(3n-1)^n}{125^n}$
6. $\displaystyle\sum_{n=2}^{\infty} \left(\frac{5}{7n+1} - \frac{1}{2n+7}\right)^n$

### Tarea 5. Criterio integral

1. $\displaystyle\sum_{n=1}^{\infty} \frac{2n}{n^2+5}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{5}{\sqrt{7n+1}}$
3. $\displaystyle\sum_{n=2}^{\infty} \frac{2}{(5n+2)^3}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{3}{n^2+9}$
5. $\displaystyle\sum_{n=2}^{\infty} \frac{13\ln n}{n}$
6. $\displaystyle\sum_{n=3}^{\infty} \frac{7}{3n-2}$

### Tarea 6. Hallar la suma de la serie

1. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{(n+2)(n+1)}$
2. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{3}{7n+2} - \frac{3}{7n+5}\right)$
3. $\displaystyle\sum_{n=2}^{\infty} \frac{1}{(3n-4)(3n-1)}$
4. $\displaystyle\sum_{n=2}^{\infty} \frac{4}{4n^2+4n-3}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{7}{25n^2-5n-6}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{11 \cdot 4^{n+1} + 35 \cdot 5^n}{13 \cdot 16^n}$

### Tarea 7. Criterios de comparación (nivel avanzado)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n-\ln n}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{(n+5)^{n-1}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{3^{n-1} \cdot 5n}$
4. $\displaystyle\sum_{n=2}^{\infty} \frac{7}{\ln(5n-7)}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{\ln(n+1)}{3^n-1}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{\sqrt[3]{n^5 \cdot 2n^4}}$

### Tarea 8. Criterio de D'Alembert (avanzado)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{2^{n+1} \cdot 3\sqrt[3]{n^3+6}}{(n-6)!}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(3n^2-2) \cdot 7^n}{(n+1) \cdot 3^{n/2}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{(3n+1)!}{(n+3)! \cdot 13^{n+2}}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{2n^3-5+7n}{15(n^2+4)^3}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(4n)!}{n^{3n}}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{2(7n+13)(3n+2)!}{n^7}$

### Tarea 9. Criterio de Cauchy (avanzado)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{9}\left(\frac{7n+1}{11n-3}\right)^{-3n}$
2. $\displaystyle\sum_{n=4}^{\infty} \left(\frac{2n+1}{n-3}\right)^{n^2}$
3. $\displaystyle\sum_{n=8}^{\infty} \left(\frac{n-7}{n+5}\right)^{n^2}$
4. $\displaystyle\sum_{n=2}^{\infty} \left(\frac{2n^2-1}{3n^2-5}\right)^{n^2}$
5. $\displaystyle\sum_{n=2}^{\infty} \frac{(n-1)^{n^3}}{5^n \cdot n^{n^3}}$
6. $\displaystyle\sum_{n=2}^{\infty} \frac{7^n}{\ln^n(3n-2)}$

### Tarea 10. Criterio integral (avanzado)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{6n}{3n^2-5}$
2. $\displaystyle\sum_{n=2}^{\infty} \frac{5\ln n}{\sqrt{7\ln^2 n+1}}$
3. $\displaystyle\sum_{n=2}^{\infty} \frac{2}{(5n-2)\ln(5n-2)}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{3}{7n^4+25}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{3n}{4^{n^2}}$
6. $\displaystyle\sum_{n=3}^{\infty} \frac{3}{n^2-n-2}$

### Tarea 11. Series con términos positivos (mixta)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{\sqrt[5]{7n^5+\sqrt[5]{2n-1}}}{7+19^n}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{2n^3\sin^2 n}{\sqrt[3]{3n^{81}-2}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{9n^7+\sqrt[7]{2n-1}}{3n^{13}+\sqrt[9]{n+1} \cdot n^3}$
4. $\displaystyle\sum_{n=3}^{\infty} \frac{3}{n\sqrt[3]{\ln^2 n \cdot \ln(n-1)}}$
5. $\displaystyle\sum_{n=2}^{\infty} \frac{\cos^{2n} \pi n^3}{\sqrt[3]{n^{10}}}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{(3n+\sqrt[5]{3n-1})(2n)!}{(9n+12)(3n)!}$
7. $\displaystyle\sum_{n=2}^{\infty} \frac{2^n \cdot n!}{7n^n}$
8. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{7n(n+1)^3}{n^2+1}\right)^{n^3}$
9. $\displaystyle\sum_{n=1}^{\infty} \frac{35^n-23^n}{7 \cdot 15^n}$
10. $\displaystyle\sum_{n=1}^{\infty} \frac{1}{(1+n^3)(\arctan n + 1)^2}$

### Tarea 12. Hallar la suma de la serie (avanzado)

1. $\displaystyle\sum_{n=1}^{\infty} \ln^{3n}\frac{7}{5}$
2. $\displaystyle\sum_{n=2}^{\infty} \left(-\frac{12}{2(2n+1)} + \frac{1}{2}\right)$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{3n+1}{n(n-1)(n+1)}$
4. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{1}{2n-1} - \frac{1}{2n+1} - \frac{1}{2n+3} + \frac{1}{2n+5}\right)$
5. $\displaystyle\sum_{n=2}^{\infty} \frac{2^{3n+1} \cdot 5^{n+2}}{19^n \cdot 2^{n+1}}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{n^2-6n+6}{n^4+6n^3+11n^2+6n}$

### Tarea 13. Series con términos positivos (difícil)

1. $\displaystyle\sum_{n=1}^{\infty} \tan\frac{2n^3}{\sqrt{|3n^4-\sin\!\left(\frac{\pi^2}{n^2+1}\right)|}}$
2. $\displaystyle\sum_{n=3}^{\infty} \frac{\cos\frac{\pi}{n}}{n^2\!\left(\sin^2\frac{2\pi}{n}+1\right)}$
3. $\displaystyle\sum_{n=2}^{\infty} \frac{2\tan\!\left(\frac{6n^2+1}{n^2+5}\right)}{\ln\!\left(\frac{11n-1}{5+3n}\right)}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{4^{1-\frac{1}{\ln(n+1)}}}{11n^{11}+115}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{\sqrt[3]{(4n-2n+1)(2n)!}}{2(2n+1) \cdot 15(3n)!}$
6. $\displaystyle\sum_{n=2}^{\infty} \frac{3\ln n}{\sqrt[3]{n^2-1}}$
7. $\displaystyle\sum_{n=2}^{\infty} \frac{\sin^2 n}{\sqrt[3]{n^{11}+1}}$
8. $\displaystyle\sum_{n=1}^{\infty} \frac{2n^2}{7n^3 - \arcsin\frac{1}{n}}$
9. $\displaystyle\sum_{n=1}^{\infty} n^3\sin\frac{2\pi}{3^n}$
10. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{7n+9\cdot\sqrt[3]{2n+1}}{n^3\cdot\sqrt[3]{n+1}\cdot\sqrt[6]{3n-2}}\right)^{n^3}$
