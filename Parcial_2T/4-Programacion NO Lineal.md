
# PROGRAMACIÓN NO LINEAL

## Diferencia entre los métodos: Jacobiano, Lagrange, y Kuhn-Tucker

En la programación no lineal, existen varios métodos para resolver problemas con restricciones de igualdad y desigualdad. A continuación se describen las diferencias y características de los métodos de: 
- Jacobiano
- Lagrange
- Kuhn-Tucker

### Restricciones de Igualdad

#### Método de Jacobi/Gradiente

El método de Jacobi, también conocido como método del gradiente, se utiliza para resolver un sistema de ecuaciones no lineales iterativamente. La fórmula utilizada para actualizar las variables es la siguiente:

$$
x_i^{(k+1)} = x_i^{(k)} - \alpha \frac{\left[\nabla f(x^{(k)})\right]_i}{\left[\nabla g_j(x^{(k)})\right]_i}
$$

- **Gradiente:** Determina la dirección en la que nos acercaremos al punto óptimo.
- **Multiplicador $\alpha$:** Determina cuánto nos moveremos en la dirección del gradiente.
- **Iterativo:** El proceso se repite hasta que el gradiente indique que no hay más aumento o disminución.

##### ¿Para qué se usa el método jacobiano?
Se utiliza principalmente para resolver sistemas de ecuaciones no lineales iterativamente.

##### ¿En qué se basa?
Se basa en el gradiente de la función objetivo y las restricciones, utilizando un multiplicador para ajustar la dirección y magnitud del movimiento hacia el punto óptimo.

#### Método de Lagrange

El método de Lagrange introduce un conjunto de multiplicadores de Lagrange, uno para cada restricción de igualdad, y reformula el problema como una función lagrangiana:

$$
L(x, \lambda) = f(x) + \sum \lambda_j g_j(x)
$$

La solución del problema se obtiene buscando los valores de $x$ y $\lambda$ que satisfacen las siguientes condiciones:

$$
\nabla L(x, \lambda) = 0
$$

$$
g_j(x) = 0
$$

### Restricciones de Desigualdad

#### Método de Kuhn-Tucker

El método de Kuhn-Tucker, también conocido como las condiciones de Karush-Kuhn-Tucker (KKT), se utiliza para problemas con restricciones de desigualdad. Este método introduce variables de holgura y reformula las restricciones de desigualdad como restricciones de igualdad con variables de holgura no negativas.

La solución del problema se obtiene buscando los valores de $x$, $\lambda$ y $s$ que satisfacen las siguientes condiciones:

1. **Estacionaridad:** 
   $$
   \nabla f(x) + \sum \lambda_j \nabla g_j(x) + \sum \mu_i \nabla h_i(x) = 0
   $$
2. **Primaria:** 
   $$
   g_j(x) = 0
   $$ 
   (para todas las restricciones de igualdad)
3. **Complementaria:** 
   $$
   \lambda_i h_i(x) = 0
   $$ 
   (para todas las restricciones de desigualdad)
4. **Dualidad:** 
   $$
   \lambda_i \geq 0
   $$ 
   $$
   h_i(x) \leq 0
   $$

