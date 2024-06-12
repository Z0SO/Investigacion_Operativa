
## ¿Qué conceptos se definen específicamente en la terminología de redes?
Las situaciones en las que se pueden aplicar estos algoritmos también se pueden formular y resolver en forma de programas lineales explícitos. Sin embargo, los algoritmos basados en redes son más eficientes que el método simplex.

### Definiciones para Redes

1. **Red:** Una red consiste en una serie de nodos enlazados con arcos (o ramas). Cada red se asocia a algún tipo de flujo, limitado por la capacidad de sus arcos, que pueden ser finitos o infinitos.

2. **Arco dirigido u orientado:** Permite un flujo positivo en una dirección y flujo cero en la dirección opuesta. Una red dirigida tiene todos sus arcos dirigidos.

3. **Ruta:** Una sucesión de arcos distintos que unen dos nodos pasando por otros nodos, independientemente de la dirección de flujo en cada arco. Una ruta forma un ciclo si conecta un nodo consigo mismo, pasando por otros nodos.

4. **Red conectada:** Aquella en que cada dos nodos distintos están enlazados al menos por una ruta.

5. **Árbol:** Una red conectada que puede consistir solo en un subconjunto de todos los nodos en ella, donde no se permiten ciclos.

6. **Árbol de expansión:** Un árbol que enlaza todos los nodos de la red.

## ¿Cuál es el mecanismo general de funcionamiento del algoritmo del Árbol de Extensión Mínima?
El algoritmo de árbol de expansión mínima enlaza los nodos de una red, en forma directa o indirecta, con la mínima longitud de las ramas enlazantes. 

**Procedimiento:**
1. Sea N = {1, 2, ..., n} el conjunto de nodos de la red.
2. Ck = Conjunto de nodos conectados en forma permanente en la iteración k.
3. Ck' = Conjunto de nodos que todavía se deben conectar en forma permanente.

## ¿Cuáles son las características del problema de la RUTA MÁS CORTA? ¿Cómo se formula el problema? ¿Cómo funciona el algoritmo de resolución?
En el problema de la ruta más corta se determina la ruta entre una fuente y un destino en una red de transporte. Existen dos algoritmos para resolver redes tanto cíclicas como acíclicas:
- **Algoritmo de Dijkstra:** Determina las rutas más cortas entre el nodo fuente y todos los demás nodos de la red.
- **Algoritmo de Floyd:** Permite determinar la ruta más corta entre dos nodos cualesquiera en la red.

## ¿Qué elementos distintivos tiene un problema del FLUJO MÁXIMO? ¿En qué consiste la enumeración de cortes? ¿Cuál es el mecanismo general de funcionamiento del algoritmo del flujo máximo?
Un flujo viaja desde un único lugar de origen hacia un único lugar de destino a través de arcos que conectan nodos intermediarios. Los arcos tienen una capacidad máxima de flujo, y se trata de enviar desde la fuente al destino la mayor cantidad posible de flujo.

- **Flujo:** Circulación de unidades homogéneas de un lugar a otro, definida por la capacidad de unidades que pueden entrar por el nodo fuente y salir por el nodo destino.
- **Capacidad de flujo:** Capacidad de unidades que pueden ser transportadas.

**Enumeración de corte:**
Un corte define un conjunto de arcos que, cuando se eliminan de la red, causan una interrupción total del flujo entre los nodos fuente y sumidero. La capacidad de corte es igual a la suma de las capacidades de los arcos.

**Algoritmo de Flujo Máximo:**
1. Buscar caminos para aumentar el flujo hasta alcanzar el flujo máximo.
2. Encontrar una ruta de penetración con un flujo positivo neto que una los nodos origen y destino.
3. Actualizar las capacidades residuales a medida que se contribuye al flujo en el arco.

**Pasos del algoritmo:**
1. Igualar la capacidad residual con la capacidad inicial para todos los arcos (i, j).
2. Etiquetar el nodo fuente 1 con [∞, -].
3. Determinar el conjunto de nodos j no etiquetados alcanzables directamente desde el nodo i con arcos residuales positivos.
4. Etiquetar el nodo k con [𝑎𝑘, i] si k = n, y si se encuentra una ruta de irrupción, proceder al paso 5.
5. Definir los nodos de la ruta de irrupción del nodo fuente 1 al nodo destino n.
6. Calcular el flujo máximo de la ruta y actualizar las capacidades residuales.

**Solución:**
El flujo máximo en la red se determina al detectar las rutas de irrupción y calcular el flujo óptimo en cada arco. La capacidad residual final se utiliza para obtener el flujo óptimo.



## Problema del Flujo Capacitado con Costo Mínimo

#### Descripción del Problema
El problema del flujo capacitado con costo mínimo busca determinar los flujos en los distintos arcos de una red de transporte que minimizan el costo total y satisfacen las restricciones de flujo, así como las cantidades de oferta y demanda en los nodos.

#### Hipótesis del Problema
1. A cada arco se le asocia un costo de flujo unitario.
2. Los arcos pueden tener límites inferiores positivos de capacidad.
3. Todo nodo en la red puede funcionar como fuente o como sumidero.

#### Representación en Red
- Una red capacitada se denota como $( G = (N, A) ), donde ( N )$ es el conjunto de nodos y \( A \) es el conjunto de arcos.
- Se define:
  - \( x_{ij} \): Cantidad de flujo del nodo \( i \) al nodo \( j \).
  - \( u_{ij} \) (\( l_{ij} \)): Capacidad máxima (mínima) del arco \( (i, j) \).
  - \( c_{ij} \): Costo de flujo unitario del nodo \( i \) al nodo \( j \).
  - \( f_i \): Flujo neto en el nodo \( i \).

#### Formulación con Programación Lineal
La formulación del problema como un programa lineal es la base para el desarrollo del algoritmo simplex capacitado. La ecuación para el nodo \( j \) mide el flujo neto \( f_j \) en el nodo \( j \) de la siguiente manera:

\[ \sum_{i} x_{ij} - \sum_{k} x_{jk} = f_j \]

El nodo \( j \) funciona como fuente si \( f_j > 0 \) y como sumidero si \( f_j < 0 \).

#### Algoritmo Simplex de Red Capacitada
El objetivo del algoritmo es aprovechar la estructura especial de red del modelo de flujo con costo mínimo. La red debe satisfacer la condición de balanceo de flujo:

\[ \sum_{i} f_i = 0 \]

Esto indica que la oferta total en la red es igual a la demanda total. Este requisito se puede satisfacer agregando una fuente o un destino ficticios para balancear, conectados con todos los demás nodos de la red con arcos de costo unitario cero y capacidad infinita.

**Pasos del Algoritmo Simplex Capacitado:**
1. **Balanceo de la Red:** Asegurar que toda la oferta total en la red sea igual a la demanda total agregando nodos ficticios si es necesario.
2. **Solución Básica Inicial:** Encontrar una solución básica inicial que corresponde a un árbol de expansión mínima de la red.
3. **Iteraciones:** Realizar iteraciones para optimizar el flujo, utilizando el método simplex capacitado para mover el flujo en la red mientras se cumple con las restricciones de capacidad y minimizando el costo.
4. **Actualización de Flujos:** Actualizar los flujos en los arcos y las capacidades residuales después de cada iteración hasta que no se pueda mejorar más el costo total.

#### Método PERT y CPM

##### Descripción y Objetivo
Los métodos CPM (Critical Path Method) y PERT (Program Evaluation and Review Technique) se basan en redes para auxiliar en la planeación, programación y control de proyectos. Ambos métodos buscan proporcionar un análisis sistemático de las actividades de un proyecto para mejorar su programación.

##### Diferencias y Similitudes
- **CPM:** Supone duraciones determinísticas de actividad.
- **PERT:** Supone duraciones probabilísticas de actividad.

##### Representación en Red
Cada actividad del proyecto se representa con un arco que apunta en la dirección de avance del proyecto. Los nodos de la red establecen las relaciones de precedencia entre las diferentes actividades del proyecto.

**Reglas para Configurar la Red:**
1. **Regla de Secuenciación:** Los nodos de inicio y fin de cada actividad deben reflejar la precedencia de las actividades.
2. **Actividades Ficticias (Dummy):** Utilizar actividades ficticias para representar dependencias que no consumen tiempo o recursos, representadas normalmente con arcos de línea interrumpida.


Por ejemplo:



Ambos métodos, CPM y PERT, proporcionan una representación visual y analítica del proyecto, permitiendo identificar la ruta crítica y calcular los tiempos de inicio y finalización de cada actividad, optimizando así la gestión del proyecto.

### Resumen

- **Flujo Capacitado con Costo Mínimo:** Busca minimizar el costo total del flujo en una red, cumpliendo con las restricciones de capacidad y balanceo de oferta-demanda.
- **Algoritmo Simplex de Red Capacitada:** Utiliza una estructura de red para optimizar los flujos y costos, partiendo de una solución básica inicial y actualizando iterativamente los flujos.
- **Métodos CPM y PERT:** Herramientas de planificación de proyectos que difieren en la suposición de duraciones determinísticas (CPM) vs. probabilísticas (PERT), pero comparten una representación en red y el objetivo de optimizar la programación y control de actividades del proyecto.

### Cálculo de la Ruta Crítica (CPM)

#### Pasos para Calcular la Ruta Crítica
El cálculo de la ruta crítica en un proyecto implica determinar las actividades críticas, es decir, aquellas actividades que no tienen margen de tiempo (holgura) en su programación y que, por tanto, determinan la duración total del proyecto. Para lograr esto, se siguen dos pasos principales: el paso hacia adelante y el paso hacia atrás.

##### Paso Hacia Adelante
1. **Calcular los Tiempos Más Tempranos**:
   - **Tiempo más temprano de inicio de una actividad** \( E_i \): Es el tiempo más temprano en que puede comenzar una actividad sin demorar el proyecto.
   - **Tiempo más temprano de finalización de una actividad** \( E_j \): Es el tiempo más temprano en que puede finalizar una actividad.
   - Para cada nodo \( j \):
     \[ E_j = \max (E_i + D_{ij}) \]
     donde \( E_i \) es el tiempo más temprano de inicio del nodo predecesor \( i \) y \( D_{ij} \) es la duración de la actividad de \( i \) a \( j \).

##### Paso Hacia Atrás
2. **Calcular los Tiempos Más Tardíos**:
   - **Tiempo más tardío de finalización de una actividad** \( L_j \): Es el tiempo más tardío en que una actividad puede finalizar sin demorar el proyecto.
   - **Tiempo más tardío de inicio de una actividad** \( L_i \): Es el tiempo más tardío en que una actividad puede comenzar sin demorar el proyecto.
   - Para cada nodo \( i \):
     \[ L_i = \min (L_j - D_{ij}) \]
     donde \( L_j \) es el tiempo más tardío de finalización del nodo sucesor \( j \).

##### Condiciones para que una Actividad sea Crítica
Una actividad \( (i, j) \) es crítica si cumple con las siguientes tres condiciones:
1. \( E_i = L_i \)
2. \( E_j = L_j \)
3. \( L_i - E_i = 0 \)

Esto indica que los tiempos más tempranos y más tardíos de inicio y finalización de la actividad son iguales, y que la duración \( D_{ij} \) se ajusta exactamente al intervalo especificado de tiempo.

### Construcción del Cronograma

#### Desarrollo del Programa de Tiempos
Para desarrollar un cronograma adecuado, se deben considerar los tiempos de inicio más temprano y más tardío de las actividades. Las actividades críticas deben programarse una inmediatamente después de la otra para asegurar que el proyecto se complete dentro del tiempo especificado. Las actividades no críticas se pueden programar con holgura, permitiendo flexibilidad en caso de demoras inesperadas.

**Observaciones Importantes:**
1. **Actividades Críticas**: Deben programarse consecutivamente para asegurar que el proyecto se termine a tiempo.
2. **Actividades No Críticas**: Se pueden iniciar lo más temprano posible para absorber demoras inesperadas. Esto es preferible ya que garantiza que el programa resultante sea factible y no viole relaciones de precedencia.

### Método PERT

#### Diferencias entre PERT y CPM
- **CPM (Critical Path Method)**: Supone duraciones determinísticas de las actividades.
- **PERT (Program Evaluation and Review Technique)**: Supone duraciones probabilísticas y utiliza tres estimaciones para calcular la duración esperada de las actividades: tiempo optimista (a), tiempo más probable (m) y tiempo pesimista (b).

#### Cálculo en PERT
1. **Tiempo Promedio de Duración**:
   \[ D' = \frac{a + 4m + b}{6} \]
2. **Varianza**:
   \[ v = \left(\frac{b - a}{6}\right)^2 \]

Los cálculos de la ruta crítica se pueden aplicar de manera similar al CPM, pero usando \( D' \) en lugar de una estimación única \( D \). Las variables de tiempo temprano y tiempo programado especificado se manejan como variables aleatorias.

### Utilidad de los Diagramas PERT para la Toma de Decisiones
Los diagramas PERT son herramientas útiles para la gestión de proyectos, ya que proporcionan una representación gráfica clara de las tareas necesarias para completar un proyecto. Ayudan a:

- Aclarar las limitaciones de tiempo.
- Ofrecer una vista detallada de la secuencia de tareas.
- Gestionar el tiempo y los recursos con mayor eficiencia.
- Reducir costos y desperdicios en el desarrollo del proyecto.

### Resumen
El método CPM permite calcular la ruta crítica y construir un cronograma eficiente, asegurando que las actividades críticas se programen adecuadamente y que las actividades no críticas se manejen con holgura para absorber demoras inesperadas. PERT, por su parte, añade un nivel de análisis probabilístico, proporcionando una visión más detallada y flexible del tiempo de finalización del proyecto y las incertidumbres asociadas. Ambos métodos son esenciales para la planificación y control de proyectos, facilitando la toma de decisiones informadas y optimizando la gestión del tiempo y los recursos.