
---


### Problema Tipo Nº 1

En un taller metalúrgico se fabrican dos tipos de piezas: A y B, las que deben seguir los siguientes procesos:

- Estampado en hojas metálicas.
- Soldado.
- Pintado.

La operación de estampado consiste en preparar partes idénticas que luego serán soldadas formando la pieza A. El mismo proceso se realiza para la pieza B. Los insumos de equipos, para la realización de cada una de las operaciones (expresados en segundos por pieza), son los siguientes:

| OPERACIÓN | A     | B     | TIEMPO DISPONIBLE (SEG/SEM) |
|-----------|-------|-------|-----------------------------|
| Estampado | 3     | 8     | 48000                       |
| Soldado   | 12    | 6     | 42000                       |
| Pintado   | 9     | 9     | 36000                       |

La utilidad unitaria de cada pieza es de $4 para A y de $3 para B. Establecer un programa semanal que maximice las ganancias.

#### Planteo del Modelo

Definimos las variables de decisión:

- $X_1$: unidades de piezas A a fabricar por semana [u/s]
- $X_2$: unidades de piezas B a fabricar por semana

Función objetivo:

$$Z = 4X_1 + 3X_2 \rightarrow \text{Maximizar ganancias} (\$/u \times u/s)$$

Sujeto a:

$$X_1 \geq 0$$
$$X_2 \geq 0$$

Restricciones:

$$3X_1 + 8X_2 \leq 48000$$
$$12X_1 + 6X_2 \leq 42000$$
$$9X_1 + 9X_2 \leq 36000$$

Extendemos el modelo introduciendo las variables de exceso de tiempo:

$$R_1: 3X_1 + 8X_2 + X_3 = 48000$$
$$R_2: 12X_1 + 6X_2 + X_4 = 42000$$
$$R_3: 9X_1 + 9X_2 + X_5 = 36000$$

Donde:

- $X_3$: sobrante de tiempo en segundos por semana en estampado
- $X_4$: sobrante de tiempo en segundos por semana en soldado
- $X_5$: sobrante de tiempo en segundos por semana en pintado

Buscamos el óptimo que utilizará todo el tiempo disponible de los sectores, por lo que las slacks tomarán valores iguales a cero.

#### Análisis de las Restricciones

**R1:**
- Si $X_1 = 0$ entonces $8X_2 = 48000 \Rightarrow X_2 = 6000$ (0,6000)
- Si $X_2 = 0$ entonces $3X_1 = 48000 \Rightarrow X_1 = 16000$ (16000,0)

**R2:**
- Si $X_1 = 0$ entonces $6X_2 = 42000 \Rightarrow X_2 = 7000$ (0,7000)
- Si $X_2 = 0$ entonces $12X_1 = 42000 \Rightarrow X_1 = 3500$ (3500,0)

**R3:**
- Si $X_1 = 0$ entonces $9X_2 = 36000 \Rightarrow X_2 = 4000$ (0,4000)
- Si $X_2 = 0$ entonces $9X_1 = 36000 \Rightarrow X_1 = 4000$ (4000,0)


![[Pasted image 20240507193909.png]]



$$Z = 4x_1 + 3x_2 \rightarrow \text{Maximizar}$$

#### Análisis de Puntos Críticos

Si $X_1 = 3$ entonces $X_2 = -4$ [3,-4] $X_2 = -\frac{4X_1}{3}$

Si $X_1 = -3$ entonces $X_2 = 4$ [-3,4]

#### Vértices:

**A** = $X_2 \cap R_3$:
- Si $X_1 = 0$ entonces $9X_2 = 36000 \Rightarrow X_2 = 4000$

**B** = $R_2 \cap R_3$:
- Operación auxiliar:

  | 12 | 6  | 42 |
  |----|----|----|
  | 9  | 9  | 36 |
  

  $2F * (-12) + 1F$
  
  
  | 12 | 6  | 42 |
  |----|----|----|
  | 0  | -6 | -6 |
  

  $X_2 = 1$: reemplazo y despejo en $R_1$: $12X_1 + 6 = 42 \Rightarrow X_1 = 3$

  Otra manera es igualando las rectas: $12X_1+6X_2-42 = 9X_1 +9X_2-36$, tal que operando queda $X_1 = X_2+2$. Reemplazando en la primera restricción queda $X_2=1$, reemplazo $X_1$ y obtengo $X_1=3$.

**C** = $X_1 \cap R_2$:
- Si $X_2 = 0$ entonces $12x_1 = 42000 \Rightarrow X_1=3500$

#### Tabla de Vértices

| Vertices | $X_1$ | $X_2$ | $X_3$ | $X_4$ | $X_5$ | $Z=4x_1+3x_2$ |
| -------- | ----- | ----- | ----- | ----- | ----- | ------------- |
| Origen   | 0     | 0     | 48    | 42    | 36    | 0             |
| A        | 0     | 4     | 16    | 18    | 0     | 12            |
| B        | 3     | 1     | 31    | 0     | 0     | 15            |
| C        | 3,5   | 0     | 37,5  | 0     | 4,5   | 14            |

#### Interpretación

Se deben fabricar 3000 unidades de piezas A por semana y 1000 unidades de B. Con esto, se espera ganar 15000 pesos semanales. Sobrarán 31000 segundos/semana en estampado, y se ocupará todo el tiempo en pintado y soldado.
