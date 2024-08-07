
# Modelos de Redes

## Conceptos Específicos en la Terminología de Redes

Las situaciones en las que se pueden aplicar estos algoritmos también se pueden formular y resolver en forma de programas lineales explícitos. Sin embargo, los algoritmos basados en redes son más eficientes que el método simplex.

### Definiciones para Redes

1. **Red:** 
   Una red consiste en una serie de nodos enlazados con arcos (o ramas). Cada red se asocia a algún tipo de flujo, limitado por la capacidad de sus arcos, que pueden ser finitos o infinitos.

2. **Arco dirigido u orientado:**
   Permite un flujo positivo en una dirección y flujo cero en la dirección opuesta. Una red dirigida tiene todos sus arcos dirigidos.

3. **Ruta:**
   Una sucesión de arcos distintos que unen dos nodos pasando por otros nodos, independientemente de la dirección de flujo en cada arco. Una ruta forma un ciclo si conecta un nodo consigo mismo, pasando por otros nodos.

4. **Red conectada:**
   Aquella en que cada dos nodos distintos están enlazados al menos por una ruta.

5. **Árbol:**
   Una red conectada que puede consistir solo en un subconjunto de todos los nodos en ella, donde no se permiten ciclos.

6. **Árbol de expansión:**
   Un árbol que enlaza todos los nodos de la red.

## Algoritmo del Árbol de Extensión Mínima

El algoritmo de árbol de expansión mínima enlaza los nodos de una red, en forma directa o indirecta, con la mínima longitud de las ramas enlazantes. 

**Procedimiento:**
1. Sea $N = \{1, 2, \ldots, n\}$ el conjunto de nodos de la red.
2. $C_k =$ Conjunto de nodos conectados en forma permanente en la iteración $k$.
3. $C_k' =$ Conjunto de nodos que todavía se deben conectar en forma permanente.

## Problema de la Ruta más Corta

En el problema de la ruta más corta se determina la ruta entre una fuente y un destino en una red de transporte. Existen dos algoritmos para resolver redes tanto cíclicas como acíclicas:
- **Algoritmo de Dijkstra:** Determina las rutas más cortas entre el nodo fuente y todos los demás nodos de la red.
- **Algoritmo de Floyd:** Permite determinar la ruta más corta entre dos nodos cualesquiera en la red.

## Problema del Flujo Máximo

Un flujo viaja desde un único lugar de origen hacia un único lugar de destino a través de arcos que conectan nodos intermediarios. Los arcos tienen una capacidad máxima de flujo, y se trata de enviar desde la fuente al destino la mayor cantidad posible de flujo.

### Definiciones
- **Flujo:** Circulación de unidades homogéneas de un lugar a otro, definida por la capacidad de unidades que pueden entrar por el nodo fuente y salir por el nodo destino.
- **Capacidad de flujo:** Capacidad de unidades que pueden ser transportadas.

### Enumeración de corte
Un corte define un conjunto de arcos que, cuando se eliminan de la red, causan una interrupción total del flujo entre los nodos fuente y sumidero. La capacidad de corte es igual a la suma de las capacidades de los arcos.

**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdmtLfR5l3x0jFu-QkmrXsQvIKXNPJGsKBsqbK5ywC3c_2F9IRermksdT1ENZsw2lJCBELuhc7rN8zmMIAlp9krxzRzQ079COdkhuncYG40VZzJ-WbCyAZnAKKQfD8suDGJDzJGdWLvnpy-qVCdd33OYmnM?key=iTPa6W9OMH7L3aG9DQ3z0g)**

### Algoritmo de Flujo Máximo

1. Buscar caminos para aumentar el flujo hasta alcanzar el flujo máximo.
2. Encontrar una ruta de penetración con un flujo positivo neto que una los nodos origen y destino.
3. Actualizar las capacidades residuales a medida que se contribuye al flujo en el arco.

**Solución:**
El flujo máximo en la red se determina al detectar las rutas de irrupción y calcular el flujo óptimo en cada arco. La capacidad residual final se utiliza para obtener el flujo óptimo.

## Problema del Flujo Capacitado con Costo Mínimo

### Descripción del Problema
El problema del flujo capacitado con costo mínimo busca determinar los flujos en los distintos arcos de una red de transporte que minimizan el costo total y satisfacen las restricciones de flujo, así como las cantidades de oferta y demanda en los nodos.

### Algoritmo Simplex de Red Capacitada
El objetivo del algoritmo es aprovechar la estructura especial de red del modelo de flujo con costo mínimo. La red debe satisfacer la condición de balanceo de flujo.

## Método PERT y CPM

### Descripción y Objetivo
Los métodos CPM (Critical Path Method) y PERT (Program Evaluation and Review Technique) se basan en redes para auxiliar en la planeación, programación y control de proyectos. Ambos métodos buscan proporcionar un análisis sistemático de las actividades de un proyecto para mejorar su programación.

### Diferencias y Similitudes
- **CPM:** Supone duraciones determinísticas de actividad.
- **PERT:** Supone duraciones probabilísticas de actividad.

### Representación en Red
Cada actividad del proyecto se representa con un arco que apunta en la dirección de avance del proyecto. Los nodos de la red establecen las relaciones de precedencia entre las diferentes actividades del proyecto.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcGyMfOPf1CaI7TzV8mUiK1fZvJEdeIOc0rbActk49uguuCJ9YcWeYY5NiyyXlkhc_LbGIvjL3rsWDh4crjy1qZsM79EK_0UAVkh0958nelv22O4qGmoVxUa3Z6701ZFGFQkiQlkzERjaT_PffYuk9_4h_C?key=iTPa6W9OMH7L3aG9DQ3z0g)

**Reglas para Configurar la Red:**
**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfjcI1a31Egj3z-HSJ3q7kdfhbRhtLJNNrzMfroeP-F4kbuT4EuAcYh7zu-JjYEatGxMP4Z8zVTV2hoIT-8vTIIWl8TgTo2s5W1OHshkreTKTK5x3xTc9useht3AoOU4_gGu_IR5LwkyNVyNIt_gNlrXBY?key=iTPa6W9OMH7L3aG9DQ3z0g)**


Por ejemplo:
![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcnudNpPs2oXxEWx73Ebjb-0doI6dK15kUt6rwQeufBOatRwDYsoqKDYRHVE1-TPp70--WJSbR_RTwp-t1nVx6qjzqu-dO_7csKnij5rjqgxtceohEO6c44XXffRsZ-fD6LbMoYij5Zv2RO1FpQA6RyXoAA?key=iTPa6W9OMH7L3aG9DQ3z0g)

### Resumen

- **Flujo Capacitado con Costo Mínimo:** Busca minimizar el costo total del flujo en una red, cumpliendo con las restricciones de capacidad y balanceo de oferta-demanda.
- **Algoritmo Simplex de Red Capacitada:** Utiliza una estructura de red para optimizar los flujos y costos, partiendo de una solución básica inicial y actualizando iterativamente los flujos.
- **Métodos CPM y PERT:** Herramientas de planificación de proyectos que difieren en la suposición de duraciones determinísticas (CPM) vs. probabilísticas (PERT), pero comparten una representación en red y el objetivo de optimizar la programación y control de actividades del proyecto.

### Cálculo de la Ruta Crítica (CPM)

#### Pasos para Calcular la Ruta Crítica
El cálculo de la ruta crítica en un proyecto implica determinar las actividades críticas, es decir, aquellas actividades que no tienen margen de tiempo (holgura) en su programación y que, por tanto, determinan la duración total del proyecto. Para lograr esto, se siguen dos pasos principales: el paso hacia adelante y el paso hacia atrás.

#### Condiciones para que una Actividad sea Crítica
Una actividad $ (i, j) $ es crítica si cumple con las siguientes tres condiciones:

$$
E_i = L_i
$$
$$
E_j = L_j
$$
$$
L_i - E_i = 0
$$

Esto indica que los tiempos más tempranos y más tardíos de inicio y finalización de la actividad son iguales, y que la duración $ D_{ij} $ se ajusta exactamente al intervalo especificado de tiempo.

### Construcción del Cronograma

#### Desarrollo del Programa de Tiempos
Para desarrollar un cronograma adecuado, se deben considerar los tiempos de inicio más temprano y más tardío de las actividades. Las actividades críticas deben programarse una inmediatamente después de la otra para asegurar que el proyecto se complete dentro del tiempo especificado. Las actividades no críticas se pueden programar con holgura, permitiendo flexibilidad en caso de demoras inesperadas.

**Observaciones Importantes:**
1. **Actividades Críticas:** Deben programarse consecutivamente para asegurar que el proyecto se termine a tiempo.
2. **Actividades No Críticas:** Se pueden iniciar lo más temprano posible para absorber demoras inesperadas. Esto es preferible ya que garantiza que el programa resultante sea factible y no viole relaciones de precedencia.

### Método PERT

#### Diferencias entre PERT y CPM
- **CPM (Critical Path Method):** Supone duraciones **determinísticas de las actividades**.
- **PERT (Program Evaluation and Review Technique):** Supone duraciones **probabilísticas** y utiliza tres estimaciones para calcular la duración esperada de las actividades: tiempo optimista (**a**), tiempo más probable (**m**) y tiempo pesimista (**b**).

### Utilidad de los Diagramas PERT para la Toma de Decisiones
Los diagramas PERT son herramientas útiles para la gestión de proyectos, ya que proporcionan una representación gráfica clara de las tareas necesarias para completar un proyecto. Ayudan a:

- Aclarar las limitaciones de tiempo.
- Ofrecer una vista detallada de la secuencia de tareas.
- Gestionar el tiempo y los recursos con mayor eficiencia.
- Reducir costos y desperdicios en el desarrollo del proyecto.

### Resumen
El método CPM permite calcular la ruta crítica y construir un cronograma eficiente, asegurando que las actividades críticas se programen adecuadamente y que las actividades no críticas se manejen con holgura para absorber demoras inesperadas. PERT, por su parte, añade un nivel de análisis probabilístico, proporcionando una visión más detallada y flexible del tiempo de finalización del proyecto y las incertidumbres asociadas. Ambos métodos son esenciales para la planificación y control de proyectos, facilitando la toma de decisiones informadas y optimizando la gestión del tiempo y los recursos.
