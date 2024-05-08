
---
### Problema Tipo 2

Un fabricante de bombones entrega sus productos en cajas de un kilogramo, en dos variedades: A y B. La caja tipo A contiene 300 gramos de bombones de licor, 500 gramos de bombones de nuez y 200 gramos de bombones de fruta. La caja tipo B contiene 400 gramos, 200 gramos y 400 gramos de cada tipo de bombón, respectivamente. La utilidad por cada caja de bombones tipo A es de $120, y por cada caja de tipo B es de $90. 

El fabricante dispone de 100 kilogramos de bombones de licor, 120 kilogramos de bombones de nuez, 100 kilogramos de bombones de fruta. Se desea definir la cantidad de cajas de cada tipo que debe armar en esta situación para que su beneficio sea máximo.

---
#### Resolución del Problema

**Identificación de las Incógnitas con sus Unidades:**
- $X_1$: Producción de cajas tipo A [Nº de cajas/período]
- $X_2$: Producción de cajas tipo B [Nº de cajas/período]

**Planteo de las Inecuaciones y Funcional:**
- $0.3X_1 + 0.4X_2 \leq 100$ $\Rightarrow$ Licor
- $0.5X_1 + 0.2X_2 \leq 120$ $\Rightarrow$ Nuez
- $0.2X_1 + 0.4X_2 \leq 100$ $\Rightarrow$ Fruta
- $X_1, X_2 \geq 0$
- $Z = 120X_1 + 90X_2$ $\Rightarrow$ Máx

#### Interpretación

Para maximizar su beneficio, el fabricante debe producir cierta cantidad de cajas tipo A y tipo B, considerando las restricciones de disponibilidad de cada tipo de bombón. El objetivo es determinar la cantidad óptima de cajas de cada tipo que maximice el beneficio total.

#### Representacio Grafica

![[Pasted image 20240507200011.png]]



Vamos a seguir con la resolución del problema. Aquí están los valores de las variables \($X_1$\), \($X_2$\) y \($Z$\) en los vértices:

- Punto 0:
  - \($X_1$ = 0\)
  - \($X_2$ = 0\)
  - \($Z$ = 0\)

- Punto A:
  - \($0.5X_1 + 0.2X_2$ = 120\)
  - \($X_1$ = 240\)
  - \($X_2$ = 0\)
  - \($Z$ = 28800\)

- Punto B:
  - \($0.5X_1$ + $0.2X_2$ = 120\)
  - \($0.3X_1 + 0.4X_2$ = 100\)
  - \($X_1$ = 200\)
  - \($X_2$ = 100\)
  - \($Z$ = 33000\)

- Punto C:
  - \($0.3X_1$ + 0.4X_2 = 100\)
  - \($X_1$ = 0\)
  - \($X_2$ = 250\)
  - \($Z$ = 22500\)

El punto C, al ser un extremo "degenerado", también puede definirse con uno de los siguientes sistemas de ecuaciones:
- \($0.3X_1$ + $0.4X_2$ = 100\)
- \($0.2X_1$ + $0.4X_2$ = 100\)

O también como:

- \($0.2X_1$ + $0.4X_2$ = 100\)
- \($X_1$ = 0\)

Ahora procederemos con el planteo de las ecuaciones de las variables Slacks:
$$
\begin{align*}
X_3 & : 0.3X_1 + 0.4X_2 + X_3 = 1000 \\
X_4 & : 5X_1 + 0.2X_2 + X_4 = 1200 \\
X_5 & : 2X_1 + 0.4X_2 + X_5 = 100
\end{align*}
$$
| Variable | Slack | Descripción                                     | Unidad                              |
|----------|-------|-------------------------------------------------|-------------------------------------|
| X3       |       | Sobrante de bombones de licor                   | kilogramos/período                 |
| X4       |       | Sobrante de bombones de nuez                    | kilogramos/período                 |
| X5       |       | Sobrante de bombones de fruta                   | kilogramos/período                 |

Para hallar algebraicamente el valor de las variables en el óptimo, observamos que el punto extremo B, que es óptimo del problema, se define por la anulación de las variables \(X_3\) y \(X_4\). Por lo tanto, el valor del resto de las variables en el óptimo surge del siguiente sistema de ecuaciones:

$$
\begin{align*}
0.3X_1 + 0.4X_2 &= 1000 \\
5X_1 + 0.2X_2 &= 1200 \\
2X_1 + 0.4X_2 + X_5 &= 100
\end{align*}
$$

Por lo tanto, el valor de todas las variables y el funcional, en el óptimo, será:

- \($X_1$ = 200\) Cajas bombones tipo “A”/período 
- \($X_2$ = 100\) Cajas bombones tipo “B”/período 
- \($X_3$ = 0\) kg de bombones de licor/período
- \($X_4$= 0\) kg de bombones de nuez/período 
- \($X_5$ = 20\) kg de bombones de fruta/período 
- \($Z$ = 33,000\) $/período



---
