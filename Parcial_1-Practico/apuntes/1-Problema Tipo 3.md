
----
## Problema Tipo Nº 2

Una empresa automotriz está equipada para producir automóviles y camiones. Su planta fabril está organizada en cuatro departamentos: estampado, montaje de motores, línea de montaje de automotores y línea de montaje de camiones. Las capacidades de cada departamento están limitadas de la siguiente forma: Estampado puede producir 25.000 autos ó 35.000 camiones por año. Montaje de motores puede producir 33.333 autos ó 16.667 camiones por año Montaje de autos: 25.000 por año. Montaje de camiones: 15.000 por año. Se desea producir como mínimo 12.000 autos y 8.000 camiones por año, estimándose asimismo en 18.000 unidades la cantidad demandada máxima anual de automóviles. El margen de beneficios es de 150.000 $ por auto y 125.000 $ por camión. Se desea conocer el plan de producción que haga máximo el margen total de beneficio.

---
### Resolución del problema

#### 1. Representación gráfica del subsistema a modelizar

- Fábrica – Subsistema Producción

![[Pasted image 20240507212730.png]]


## Objetivo del problema

Determinar el plan de producción de autos y camiones para el próximo año, de manera de maximizar la ganancia total de la empresa.

## Hipótesis

- No hay stock ni inicial ni final. Se vende todo lo que se produce.
- No existen costos fijos en el sistema de producción.
- Se vende al contado.
- Se planifica a moneda constante.
- Los excedentes de caja no se trabajan a interés.
- Las capacidades son prácticas, es decir, están afectadas por las paradas.
- No hay restricciones ni de mano de obra, ni de producción, ni de materia prima.
- No hay mermas en los procesos productivos.
- Se produce un solo tipo de auto y un solo modelo de camión.


## Variables

Variable | Descripción          | Unidad
-------- | -------------------- | --------------
X1       | Cantidad de autos a producir | unidades/año
X2       | Cantidad de camiones a producir | unidades/año

## Restricciones que debe cumplir el modelo

1. Capacidad de estampado (autos y/o camiones)
2. Capacidad de montaje de motores (autos y/o camiones)
3. Capacidad de montaje de autos.
4. Capacidad de montaje de camiones.
5. Demanda mínima y máxima de autos.
6. Demanda mínima de camiones.


## Restricciones que debe cumplir el modelo

1. **Capacidad de estampado (autos y/o camiones):**
   - $\frac{X1}{25000} + \frac{X2}{35000} \leq 1$

2. **Capacidad de montaje de motores (autos y/o camiones):**
   - $\frac{X1}{33333} + \frac{X2}{16667} \leq 1$

3. **Capacidad de montaje de autos:**
   - $X1 \leq 25000$

4. **Capacidad de montaje de camiones:**
   - $X2 \leq 15000$

5. **Demanda mínima y máxima de autos:**
   - $12000 \leq X1 \leq 18000$

6. **Demanda mínima de camiones:**
   - $X2 \geq 8000$

## Funcional

$150000X1 + 125000X2 \rightarrow \text{Max}$

_Nota: El funcional está expresado en $/unidad de tiempo (en este caso, $/año)._


Observar que el problema puede tener otros funcionales acorde a otros objetivos: Análisis posterior

| Objetivo Funcional                            |                         |
|----------------------------------------------|-------------------------|
| Maximizar ventas de camiones                 | $X_2 \rightarrow \text{Máx}$ |
| Minimizar producción de autos                | $X_1 \rightarrow \text{Mín}$ |
| Minimizar capacidad ociosa de estampado      | $X_1 + 0,71X_2 \rightarrow \text{Máx}$ |

¿Qué pasa si no se cumple alguna hipótesis (3.a - 3.i)?

a) Si no se vende todo lo que se produce hay que abrir las variables $X_1$ y $X_2$:
   - $X_1' \rightarrow$ cantidad de autos a producir
   - $X_1'' \rightarrow$ cantidad de autos a vender
   - $X_2' \rightarrow$ cantidad de camiones a producir
   - $X_2'' \rightarrow$ cantidad de camiones a vender

b) Si no es necesario considerar stocks, las ecuaciones a incorporar serían:
   - $X_1' \geq X_1''$
   - $X_2' \geq X_2''$

Donde las variables que representan stocks deben figurar también en otras restricciones o en el funcional, de lo contrario no tiene sentido para el modelo haberlas agregado. En cualquier caso, las capacidades de línea de montaje de autos y camiones serían:
   - $X_1' \leq 25.000$ [autos/año]
   - $X_2' \leq 15.000$ [camiones/año]

Análogamente, debería reemplazarse en las restricciones de capacidad de estampado y montaje de motores las variables $X_1$ y $X_2$ por $X_1'$ y $X_2'$. Mientras que las restricciones de demanda quedarían:
- $12.000 \leq X_1'' \leq 18.000$ [autos/año]
- $X_2'' \geq 8.000$ [camiones/año]

b) Si se consideraran los costos fijos, habría que agregarlos en el funcional:
   - $Z = 150.000X_1 + 125.000X_2 - \text{Costos fijos} \rightarrow \text{Máx}$

c) Si no se vende al contado, y se quiere el ingreso a valores actuales, hay que dividir el precio por un coeficiente mayor a 1 (pérdida por interés). Por ejemplo, si se vende a 360 días y "i" es la tasa a 360 días, el funcional sería:
   - $Z = \frac{150.000X_1}{1 + i} + \frac{125.000X_2}{1 + i} \rightarrow \text{Máx}$

d) Si hubiera inflación habría que multiplicar los coeficientes de Z por la tasa anual de inflación, para obtener el valor actualizado al año.

e) Si suponemos que cada auto que se vende genera un excedente de caja de "b" $/u y cada camión "c" $/u, y este excedente se trabaja a una tasa "i", el funcional sería:
   - $Z = 150.000X_1 + 125.000X_2 + (bX_1)i + (cX_2)i \rightarrow \text{Máx}$

f) Si las capacidades pudieran afectarse por 'paradas', habría que conocer un valor estimativo del porcentaje de pérdida de tiempo útil que estas provocan. Por ejemplo, si se usa un 10% de la línea de montaje de motores para preparar los equipos, entonces la restricción sería:
   - $X_1 + 2X_2 \leq 0,9 \times 33.333$

g) Si se consideraran más modelos de autos y/o camiones, habría que trabajar con más variables, probablemente una para cada modelo.
