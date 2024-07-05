
---
# Ejercicio 4: Análisis Óptimo (15p)

## Casos Posibles en el Método Simplex

### Solución No Factible (Infactible):

   - Al menos uno de los valores en la columna de soluciones es negativo, lo que indica que la solución viola alguna de las restricciones del problema.

###  **Solución No Óptima:**
   - Al menos un coeficiente en la fila Z para las variables no básicas no cumple el criterio de optimalidad (es decir, hay al menos un coeficiente positivo en problemas de maximización o negativo en minimización). Esto indica que aún se puede mejorar el valor de la función objetivo.

### **Solución Óptima y Factible:**
   - Todos los coeficientes en la fila Z para las variables no básicas cumplen el criterio de optimalidad.
   - **Factible**: Todos los valores en la columna de soluciones **son positivos**.

### **Múltiples Soluciones Óptimas:**
   - Esto ocurre cuando, en la tabla óptima, al menos un coeficiente de una variable no básica en la fila Z es exactamente cero en un problema de maximización o minimización. Esto indica que esa variable no básica puede entrar en la base sin cambiar el valor óptimo de la función objetivo, lo que sugiere la existencia de múltiples soluciones óptimas.


### **Degeneración:**
   - Ocurre cuando **uno o más de los valores básicos en la columna de soluciones son = 0**.
   - Esto puede llevar a ciclos y requerir estrategias especiales como la regla de Bland para evitar ciclos infinitos.


### **Problema No Acotado:**

   - En una iteración del simplex, si todos los elementos en una columna de una variable no básica que tiene un coeficiente positivo en la fila Z (para maximización) son negativos o cero, entonces el problema no tiene solución acotada. Esto significa que el valor de la función objetivo puede incrementarse indefinidamente.

   - **Todos los elementos de Columna pivote son negativos o cero**


### **Solución alternativa:** 

- Hay mas ceros en la fila Z que filas en todas la tabla (sin contar Z) o restricciones. Una solución negativa se puede dar, es factible









---