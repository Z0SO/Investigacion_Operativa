
---
# Problema Tipo Nº 4

Dos aditivos "1" y "2" deben ser empleados para mejorar la calidad de una nafta. Se deben cumplir las siguientes condiciones:

**a)** Como los aditivos no producen combustión, es conveniente, para evitar la formación de depósitos en el carburador, que por cada 10 litros de gasolina no se agregue más de 1/2 litro de aditivos.

**b)** La cantidad de aditivo "2" más dos veces la cantidad de aditivo "1" debe ser, como mínimo, 1/2 litro por cada 10 litros de gasolina. De esta manera, se logra una nafta de color óptimo.

**c)** Agregar un litro de aditivo "1" significa que a la nafta se agregan 10 unidades de octanaje, y agregar un litro de aditivo "2", 20 unidades de octanaje. La nafta sin aditivos posee un octanaje de 84 y se quiere que, como mínimo, la gasolina obtenida posea un número de octanos superior a 90.

El costo del aditivo "1" es de $153/litro y el del "2", $400/litro.


---

## Resolución del problema

##### Representación gráfica del subsistema a modelizar

![[Pasted image 20240508013712.png]]


## Objetivo del problema

Determinar la cantidad de cada uno de los aditivos a agregar a la nafta virgen por cada 10 litros de gasolina de manera de minimizar los costos.

## Hipótesis

- No hay mermas en el proceso de mezcla.
- No hay costo en el proceso de mezcla.
- La relación de octanos es lineal.
- No hay costo de M.O.
- Todas las naftas vírgenes que pueda usar tienen igual costo.
- El aumento en unidades de octanaje de los aditivos se considera por cantidad agregada cada 10 litros de gasolina.
## Variables
- $X1$: Cantidad de aditivo "1" a agregar a la nafta por cada 10 litros [litros / 10 litros]
- $X2$: Cantidad de aditivo "2" a agregar a la nafta por cada 10 litros [litros / 10 litros]
## Restricciones

1. No agregar más de 0.5 litros de aditivos cada 10 litros de gasolina.
2. Relación entre el aditivo "1" y "2" por el color de la gasolina.
3. Número total de octanos de la gasolina.

### Inecuaciones

1. Aditivo "1" + Aditivo "2" + Nafta virgen = 10 litros de gasolina. La restricción dice que el agregado total de aditivos no puede ser superior a 1/2 litro, entonces: 

$$ X1 + X2 \leq 0.5 \text{ [litros / 10 litros]}$$


2. Para obtener una coloración final óptima: 
   $$
   2X1 + X2 \geq 0.5 \text{ [litros / 10 litros]}
   $$

3. Dado que partimos de 84 octanos, debemos mejorar por lo menos en 6, por lo que debemos agregar aditivos "1" y "2" para que se cumpla esto: 
![[Pasted image 20240508014302.png]]

$$
   X1, X2 \geq 0
$$
##### Funcional
$$
Z = 153X1 + 400X2 \quad [\$/10 \, \text{lts.}] \rightarrow \text{Mín}
$$


Nota: Un planteo más general puede ser:

- $X1$: Cantidad de aditivo “1” a agregar a una producción $N$
- $X2$: Cantidad de aditivo “2” a agregar a una producción $N$
- $V$: Cantidad de nafta virgen a agregar a una producción $N$

$$N = X1 + X2 + V $$
$$ N \leq M \quad \text{(En el supuesto de demanda máxima)} $$$$ \geq m \quad \text{(En el supuesto de demanda mínima)}$$

Las restricciones serían:

1. $X1 + X2 \leq 0.5/10 \times (X1 + X2 + V)$
2. $2X1 + X2 \leq 0.5/10 \times (X1 + X2 + V)$
3. $10X1 + 20X2 \geq 6 \times (X1 + X2 + V)$

Fijarse que haciendo $M \rightarrow \infty$ y $m = 0$, $N = 10$ obtenemos el planteo propuesto.


Si hubiéramos definido las variables así:
- $X1$ = % de Aditivo “1”
- $X2$ = % de Aditivo “2”

Las restricciones serían:
1. $X1 + X2 \leq 5\%$
2. $2X1 + X2 \geq 5\%$
3. La tercera no se puede manejar con inecuaciones de Programación Lineal.




---
