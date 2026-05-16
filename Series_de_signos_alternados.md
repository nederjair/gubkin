# Series numéricas de signos alternados

---

## Convergencia absoluta y condicional

Para una serie de signos alternados:

$$\sum_{n=1}^{\infty} a_n = a_1 + a_2 + \ldots + a_n + \ldots$$

se construye la serie de los valores absolutos de sus términos:

$$\sum_{n=1}^{\infty} |a_n| = |a_1| + |a_2| + \ldots + |a_n| + \ldots$$

Para estudiar la convergencia de esta última serie se utilizan los criterios de convergencia de series de términos positivos.

> **Definición.** Una serie de signos alternados se llama **absolutamente convergente** si converge la serie de los valores absolutos de sus términos.

---

## Teorema sobre convergencia absoluta

> **Teorema.** Toda serie absolutamente convergente es convergente.

Si una serie de signos alternados **no** converge absolutamente, no se puede afirmar que sea divergente. Es necesario realizar un estudio adicional.

> **Definición.** Una serie de signos alternados se llama **condicionalmente convergente** si converge, pero no converge absolutamente.

Para estudiar la convergencia de una serie de signos alternados de la forma:

$$\sum_{n=1}^{\infty} a_n b_n = a_1 b_1 - a_2 b_2 + a_1 b_1 - \ldots + a_n b_n - \ldots$$

se utilizan los dos teoremas siguientes.

---

## Criterio de Dirichlet

Sean para la serie $\displaystyle\sum_{n=1}^{\infty} a_n b_n$ las siguientes condiciones:

1. La sucesión de sumas parciales de la serie $\displaystyle\sum_{n=1}^{\infty} b_n$ es **acotada**.
2. La sucesión $(a_n)$ **decrece monótonamente** tendiendo a cero.

Entonces la serie $\displaystyle\sum_{n=1}^{\infty} a_n b_n$ **converge**.

---

## Criterio de Abel

Sean para la serie $\displaystyle\sum_{n=1}^{\infty} a_n b_n$ las siguientes condiciones:

1. La sucesión $(a_n)$ es **monótona y acotada**.
2. La serie $\displaystyle\sum_{n=1}^{\infty} b_n$ **converge**.

Entonces la serie $\displaystyle\sum_{n=1}^{\infty} a_n b_n$ **converge**.

---

## Criterio de Leibniz

Sea una serie **estrictamente alternada**:

$$\sum_{n=1}^{\infty} (-1)^{n-1} a_n = a_1 - a_2 + a_3 - a_4 + \ldots + (-1)^{n-1} a_n + \ldots$$

donde $a_n > 0$, $n \in \mathbb{N}$, que cumple las condiciones:

1. La serie es **estrictamente alternada**.
2. Los valores absolutos de sus términos forman una sucesión **monótonamente no creciente**: $a_1 \geq a_2 \geq \ldots \geq a_n \geq \ldots$
3. $\displaystyle\lim_{n \to \infty} a_n = 0$

Entonces la serie **converge**.

> Una serie que satisface las condiciones del criterio de Leibniz se llama **serie de Leibniz**.

---

## Corolarios del criterio de Leibniz

**Corolario 1.** Si para una serie estrictamente alternada se cumplen las condiciones del criterio de Leibniz, entonces para su suma $S$ es válida la estimación:

$$S \leq a_1$$

**Corolario 2.** Para el resto $R_n$ de una serie estrictamente alternada que satisface el criterio de Leibniz, es válida la estimación:

$$|R_n| \leq a_{n+1} \quad (n \in \mathbb{N})$$

> Este corolario se utiliza para el cálculo aproximado de la suma de la serie con una precisión dada: se toman tantos términos de la serie hasta que el siguiente término sea menor que la precisión requerida.

---

## Ejemplos

### Ejemplo 1. Estudiar la convergencia (absoluta, condicional o divergente)

#### (1) $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{7n+11}$

**Paso 1. Comprobación de la convergencia absoluta.**

Estudiamos $\displaystyle\sum_{n=1}^{\infty} \frac{1}{7n+11}$.

Aplicamos el criterio límite de comparación con la serie armónica $\displaystyle\sum \frac{1}{n}$:

$$\lim_{n \to \infty} \frac{1/(7n+11)}{1/n} = \lim_{n \to \infty} \frac{n}{7n+11} = \frac{1}{7} \neq 0$$

Límite finito y no nulo — las series se comportan igual. La serie armónica diverge → **la serie de módulos diverge**.

**Paso 2. Comprobación de la convergencia condicional (criterio de Leibniz).**

- La serie es estrictamente alternada: $(-1)^{n-1}$.
- Los términos decrecen en valor absoluto: $\frac{1}{18} > \frac{1}{25} > \frac{1}{32} > \ldots > \frac{1}{7n+11} > \ldots$ ✓
- $\displaystyle\lim_{n \to \infty} \frac{1}{7n+11} = 0$ ✓

Por el criterio de Leibniz la serie **converge**.

> **Conclusión:** la serie es **condicionalmente convergente**.

---

#### (2) $\displaystyle\sum_{n=1}^{\infty} \frac{\sin(3n)}{(2n+7)!}$

**Comprobación de la convergencia absoluta.**

Como $\left|\dfrac{\sin(3n)}{(2n+7)!}\right| \leq \dfrac{1}{(2n+7)!}$, comparamos con la serie $\displaystyle\sum \frac{1}{(2n+7)!}$.

Aplicamos el criterio de D'Alembert a la serie $\displaystyle\sum \frac{1}{(2n+7)!}$:

$$b_n = \frac{1}{(2n+7)!}, \quad b_{n+1} = \frac{1}{(2n+9)!}$$

$$C = \lim_{n \to \infty} \frac{b_{n+1}}{b_n} = \lim_{n \to \infty} \frac{(2n+7)!}{(2n+9)!} = \lim_{n \to \infty} \frac{1}{(2n+8)(2n+9)} = 0 < 1$$

La serie $\displaystyle\sum \frac{1}{(2n+7)!}$ converge. Por el criterio de comparación, la serie de módulos también converge.

> **Conclusión:** la serie es **absolutamente convergente**.

---

#### (3) $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{(2n+2)(2n-1)}$

**Comprobación de la convergencia absoluta.**

Estudiamos $\displaystyle\sum \frac{1}{(2n+2)(2n-1)}$.

Aplicamos el criterio integral:

$$\int_1^{+\infty} \frac{dx}{(2x+2)(2x-1)} = \frac{1}{6}\lim_{b \to \infty}\left(\ln(2x-1) - \ln(2x+2)\right)\Big|_1^b$$

$$= \frac{1}{6}\lim_{b \to \infty} \ln\frac{2x-1}{2x+2}\Bigg|_1^b = \frac{1}{6}\left(\ln 1 - \ln\frac{1}{4}\right) = \frac{1}{6}\ln 4 = \frac{\ln 2}{3}$$

La integral converge →

> **Conclusión:** la serie es **absolutamente convergente**.

---

#### (4) $\displaystyle\sum_{n=1}^{\infty} \cos\frac{5\pi n}{13}$

Comprobamos la condición necesaria de convergencia:

$$\lim_{n \to \infty} \cos\frac{5\pi n}{13} \quad \text{— no existe}$$

($\cos\frac{5\pi n}{13}$ «oscila» entre $-1$ y $1$, sin tender a ningún número.)

> **Conclusión:** la serie **diverge**.

---

### Ejemplo 2. Cálculo aproximado de la suma de la serie

#### $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n^3+1}$ con precisión hasta $0{,}01$

**Comprobación de convergencia (criterio de Leibniz):**

- Los términos decrecen: $\frac{1}{2} > \frac{1}{9} > \frac{1}{28} > \frac{1}{65} > \ldots$ ✓
- $\displaystyle\lim_{n \to \infty} \frac{1}{n^3+1} = 0$ ✓

La serie converge.

**Cálculo de la suma.** Por el corolario 2, $|R_n| \leq a_{n+1}$, por lo que buscamos el primer término menor que $\frac{1}{100}$:

| $n$ | $a_n$ |
|-----|-------|
| 1 | $\frac{1}{2}$ |
| 2 | $\frac{1}{9}$ |
| 3 | $\frac{1}{28}$ |
| 4 | $\frac{1}{65}$ |
| **5** | $\frac{1}{126} < \frac{1}{100}$ ✓ |

Tomamos **cuatro términos** de la serie:

$$S \approx \frac{1}{2} - \frac{1}{9} + \frac{1}{28} - \frac{1}{65} \approx 0{,}41$$

---

## Tarea

### Tarea 1. Escribir los 5 primeros términos y estudiar la convergencia

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{2n-1}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(n+1)!}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{\sqrt{n+11}}$
4. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \frac{\ln n}{n}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{3^n}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n \cdot n}{n+1}$
7. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(n+1)^2}$
8. $\displaystyle\sum_{n=1}^{\infty} \sin(5\pi n)$
9. $\displaystyle\sum_{n=1}^{\infty} (-1)^n$
10. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \left(\frac{1}{n}\right)^n$

### Tarea 2. Estudiar la convergencia y calcular la suma con precisión hasta $0{,}01$

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^4}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(n+1)!}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{\sqrt{n^8+1}}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{3^n(n+1)}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{4^n}$
6. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \frac{1}{10(n^3+n)}$
7. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(2n-1)^3}$
8. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{2^n \cdot n!}$
9. $\displaystyle\sum_{n=1}^{\infty} \left(-\frac{1}{n}\right)^n$
10. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \left(\frac{1}{n^2+1}\right)^n$

### Tarea 3. Estudiar la convergencia de la serie de signos alternados

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{3(n+5)}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n \cdot 3^n}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{\cos \pi n}{n(n+11)}$
4. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \cos\frac{2\pi}{11n}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n\ln(2n)}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{\cos 3n}{3^{n-1}}$
7. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n \sqrt[3]{n+1}}{(n+1)^2}$
8. $\displaystyle\sum_{n=1}^{\infty} \frac{\sin 5n}{(n+1)!}$
9. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}\sin\frac{\pi}{n}}{20n+1}$
10. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \left(\frac{3n}{3n+1}\right)^n$

### Tarea 4. Estudiar la convergencia y calcular la suma con precisión hasta $0{,}01$

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{10\sqrt[3]{(2n-1)^3}}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(2n-1)!}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{\sin\frac{\pi n}{2}}{(n+1)!}$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{11n\ln(2n^2)}$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n(n+11)}$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{\cos\pi n}{4^{n-1}}$
7. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{2^{n-1}(2n-1)!}$
8. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n \cdot 3^n}$
9. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{3(n+5)}$
10. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}\sin\frac{\pi n}{20n+1}}{}$

### Tarea 5. Estudiar la convergencia de la serie de signos alternados (difícil)

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n \sqrt[5]{5n+1}}{\left(2+\frac{1}{n}\right)^n}$
2. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^2 \arcsin\frac{3n^2}{1+3n^2}}$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n\ln(\ln\ln n)}$
4. $\displaystyle\sum_{n=1}^{\infty} (-1)^n\left(\sin\frac{2\pi}{3n+1} \cdot \sqrt{\frac{n+1}{2}}\right)$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1} n^{99}}{(2n+1)^{100}}$
6. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \frac{\sqrt{1+n^2+\sqrt{1+n^4}}}{3^n}$
7. $\displaystyle\sum_{n=1}^{\infty} \cos n^3$
8. $\displaystyle\sum_{n=1}^{\infty} (-1)^n \left(\frac{3n^2}{3n^2+1}\right)^{n^3}$
9. $\displaystyle\sum_{n=1}^{\infty} \left(-\frac{1}{3n+2}\right)^{3n}$
10. $\displaystyle\sum_{n=1}^{\infty} \left(\frac{n+0{,}5\arctan\sin\left(1-\frac{1}{2n\arctan n}\right)}{6n}\right)^n$

### Tarea 6. Estudiar la convergencia y calcular la suma con precisión hasta $\alpha$

1. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n(n+1)}{13^n}$, $\alpha = 0{,}01$
2. $\displaystyle\sum_{n=1}^{\infty} \left(-\frac{2}{n^2+1}\right)^n$, $\alpha = 0{,}01$
3. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n(2n+1)}$, $\alpha = 0{,}01$
4. $\displaystyle\sum_{n=1}^{\infty} \frac{\cos 3\pi n}{n^6+1}$, $\alpha = 0{,}01$
5. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{\sqrt[3]{n^2}}$, $\alpha = 0{,}01$
6. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{(n+1)^3\ln(n+1)}$, $\alpha = 0{,}1$
7. $\displaystyle\sum_{n=3}^{\infty} \frac{(-1)^{n^2}}{n^3 e^n}$, $\alpha = 0{,}1$
8. $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{(2n)!\,\arctan^2(3n)}$, $\alpha = 0{,}001$
9. $\displaystyle\sum_{n=1}^{\infty} \frac{\sin^3\frac{\pi n}{2}}{(n+1)^3}$, $\alpha = 0{,}01$
