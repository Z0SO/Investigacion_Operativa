
---

###### Al momento de identificar los $Rn$ hacerlo de la siguiente manera
- $R1 (Mineral de Alta Calidad)$         $X1+2X2>=80$ 

###### Tener en cuenta las unidades
- $[Dias Minando]= [Toneladas/Dias Minando]$ -> $[Toneladas]$

---


### Planteo del Modelo

1. Identificar las variables, **productos** con sus **ventas/incrementos**.
2. identificar la funcion objetivo (*ej: z= 3 x1 + 4 x2*).
3. Identificar Restricciones.
4. Armar el cuadro.

| Sector \| Producto |     |     |
| ------------------ | --- | --- |
|                    |     |     |
|                    |     |     |
5. Definir la hipotesis.
6. Identificar la restriccion de no negatividad.
7. Analizar y definir la **funcion objetivo** (*tener en cuenta que siempre tiene que ver con optiimzaciones*)
8. Armar el sistema de ecuaciones con el analisis de las restricciones **R$n$**. *Recordar que se hace con el cuadro*.
	1. Primer restriccion del Modelo Matematico.
	2. Segunda restriccion del Modelo Matematico.
	3. Tercera restriccion del Modelo Matematico.
	4. Estas forman un **Condicion de Ligadura**.
9. Puede existir variables en el ***SE*** que no esten de manera explicita.
	1. Estas se llaman **Holgura** o **Slack** y tienen la forma -> $0Xn$
10. Aplicar la Solucion grafica. Recordar que las areas se pintan dependiendo de la restriccion.
11. Para cada ecuacion despejar cada variable $Xn=0$ asi se trazan todas las rectas en el grafico.
12. Luego todas las intersecciones dibujaran un area denominada **Area Factible**.
	1. Es el area donde todas las areas de cada recta estan pintadas.
13. Con cada *punto interseccion* reemplazar con la funcion objetivo y evaluar.

###### Puede ser que nos den en 3 formas diferentes
- Metodo grafico
- Modelado
- Una vez que me dan el enunciado, el modelo, el metodo simplex. Hacer el **informe de interpretacion**.


---

# Pautas de Resolución por el Método Gráfico

La resolución de problemas utilizando el método gráfico en Investigación Operativa sigue una serie de pasos para encontrar la solución óptima. A continuación, se detallan las pautas a seguir:

1. **Transformar las Inecuaciones a Ecuaciones - Agregado de Slacks:**
   - Se transforman las inecuaciones del problema en ecuaciones mediante el agregado de variables de holgura (slacks) para convertirlas en igualdades.

2. **Graficar cada una de las restricciones:**
   - Cada restricción del problema se grafica en un plano cartesiano, representando las ecuaciones obtenidas en el paso anterior como rectas en el plano.

3. **Identificar los semiplanos definidos por cada inecuación; identificar la recta límite:**
   - Se identifican los semiplanos definidos por cada ecuación en el plano, determinando qué regiones del espacio cumplen con las restricciones del problema. Se identifica la recta límite de cada restricción.

4. **Identificar del convexo de soluciones:**
   - Se identifica el conjunto convexo de soluciones, que es la región factible del problema definida por la intersección de todos los semiplanos definidos por las restricciones.

5. **Graficar el z (funcional) sobre los mismos ejes. Graficar las Rectas de isocosto o isobeneficio:**
   - Se grafica la función objetivo (z) sobre los mismos ejes, representando las rectas de isocosto o isobeneficio para visualizar las posibles soluciones óptimas.

6. **Identificar de la Solución óptima:**
   - Se identifica la solución óptima como el punto donde la función objetivo alcanza su máximo o mínimo, dentro del conjunto convexo de soluciones.

7. **Análisis de vértices - Hallazgo algebraico de las incógnitas para la solución óptima:**
   - Se realiza un análisis de vértices para hallar algebraicamente las coordenadas de la solución óptima, verificando cada uno de los vértices del conjunto convexo de soluciones.

*Aclaración:* En todos los ejercicios, se establece la condición de no negatividad de las variables (Xi ≥ 0 para todo i).

--- 
