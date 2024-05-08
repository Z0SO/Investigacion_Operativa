
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

