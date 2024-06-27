

![[Pasted image 20240626213906.png]]


### Matriz 3x3

# Interpretación de una Matriz Hessiana 3x3

Para una matriz Hessiana $(3 \times 3)$, la interpretación sigue principios similares a una $(2 \times 2)$, aunque el análisis es más complejo debido al mayor número de términos involucrados. La matriz Hessiana para una función de tres variables $f(x, y, z)$ es:

$$
H = \begin{pmatrix}
\frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} & \frac{\partial^2 f}{\partial x \partial z} \\
\frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2} & \frac{\partial^2 f}{\partial y \partial z} \\
\frac{\partial^2 f}{\partial z \partial x} & \frac{\partial^2 f}{\partial z \partial y} & \frac{\partial^2 f}{\partial z^2}
\end{pmatrix}
$$

Para analizar la matriz Hessiana $(3 \times 3)$, puedes usar los siguientes pasos:

1. **Determinante y menores principales:**
   Analizar los menores principales (determinantes de las submatrices $(k \times k)$ comenzando en la esquina superior izquierda) te proporciona información sobre la naturaleza del punto crítico. Los menores principales son:
   - El menor de orden 1: $(\frac{\partial^2 f}{\partial x^2})$
   - El menor de orden 3: $\det(H)$
- El menor de orden 2:
  $$
  \begin{vmatrix}
  \frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \\
  \frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2}
  \end{vmatrix}
  $$

2. **Criterio de Sylvester:**
   El criterio de Sylvester para determinar la naturaleza de un punto crítico en una función de tres variables es el siguiente:
   - Si todos los menores principales son positivos, el punto crítico es un **mínimo local**.
   - Si los menores principales alternan en signo, comenzando con un menor positivo, el punto crítico es un **máximo local**.
   - Si $(\det(H) < 0)$, el punto crítico es un **punto de silla**.
   - Si uno de los menores principales es cero, la prueba es inconclusa y se necesita más información.

3. **Valores propios:**
   Otra manera de interpretar la matriz Hessiana es analizar sus valores propios. Los valores propios de $H$ se pueden encontrar resolviendo la ecuación característica:
   $$
   \det(H - \lambda I) = 0
   $$
   Donde $I$ es la matriz identidad. La naturaleza del punto crítico se puede determinar como sigue:
   - Si todos los valores propios son positivos, el punto crítico es un **mínimo local**.
   - Si todos los valores propios son negativos, el punto crítico es un **máximo local**.
   - Si hay una mezcla de valores propios positivos y negativos, el punto crítico es un **punto de silla**.

### Ejemplo

Supongamos que tienes la siguiente matriz Hessiana para una función $f(x, y, z)$:

$$
H = \begin{pmatrix}
4 & 1 & 0 \\
1 & 3 & 1 \\
0 & 1 & 2
\end{pmatrix}
$$

- Menor de orden 1: $4 > 0$
- Menor de orden 2:
  $$
  \begin{vmatrix}
  4 & 1 \\
  1 & 3
  \end{vmatrix} = 4 \cdot 3 - 1 \cdot 1 = 12 - 1 = 11 > 0
  $$
- Menor de orden 3: $\det(H)$:
  $$
  \det(H) = 4(3 \cdot 2 - 1 \cdot 1) - 1(1 \cdot 2 - 1 \cdot 0) + 0 = 4(6 - 1) - 1(2) = 4 \cdot 5 - 2 = 20 - 2 = 18 > 0
  $$

Dado que todos los menores principales son positivos, el punto crítico es un **mínimo local**.


## Lagrange - Verificacion del Hessiano

**Verificar la naturaleza de los puntos críticos usando la matriz Hessiana:**

- Si todos los valores propios de $H_{\mathcal{L}}$ son positivos, el punto crítico es un **mínimo local**.
- Si todos los valores propios de $H_{\mathcal{L}}$​ son negativos, el punto crítico es un **máximo local**.
- Si hay una mezcla de valores propios positivos y negativos, el punto crítico es un **punto de silla**.