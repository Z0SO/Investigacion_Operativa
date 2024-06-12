
### Teoría de Stock y Modelos de Inventario

La teoría de stock se ocupa de estudiar y determinar las políticas óptimas de reabastecimiento en inventarios para minimizar los costos asociados. Estos costos incluyen el costo de almacenamiento, costo de desabastecimiento, y otros costos relacionados con la gestión de inventarios. El objetivo es encontrar un equilibrio entre mantener un inventario suficiente para satisfacer la demanda y minimizar los costos asociados.

### Modelos de Inventario

1. **Modelo de Stock Simple (Determinístico)**
   - **Demanda Constante**: Se asume que la demanda es constante y conocida. Los reabastecimientos se realizan a intervalos regulares y el inventario se agota a una tasa constante.
   - **Stock Medio**: El valor medio del stock es \(q/2\), donde \(q\) es el tamaño del lote de reabastecimiento.
   - **Curva de Demanda**: La demanda en función del tiempo puede representarse como un diagrama de "diente de sierra".

2. **Modelo de Stock Simple sin Agotamiento y con Stock de Protección**
   - **Stock de Protección**: Se mantiene un stock mínimo (\(Sp\)) para cubrir eventualidades y evitar el desabastecimiento.
   - **Reordenes**: Los reabastecimientos se realizan antes de que el inventario caiga por debajo del nivel de protección.

3. **Modelo de Stock Simple con Agotamiento**
   - **Agotamiento Permitido**: Se permite que ocasionalmente el inventario se agote, lo que introduce un costo de desabastecimiento en el modelo.
   - **Costo de Almacenamiento vs. Costo de Desabastecimiento**: Este modelo es útil cuando los costos de almacenamiento son altos y se prefiere aceptar el riesgo de desabastecimiento.

4. **Modelo Triangular**
   - **Reposición No Instantánea**: La reposición de inventarios no es instantánea y ocurre a medida que se produce.
   - **Producción vs. Demanda**: Se asume que la tasa de producción (\(p\)) es mayor que la demanda (\(d\)). El stock se acumula durante el periodo de producción y luego se consume.
   - **Velocidad de Producción**: Puede ser constante o dependiente del tiempo.

5. **Modelo Simple sin Agotamiento con Precios Variables**
   - **Costos de Adquisición Variables**: El costo de adquisición o producción varía en función del tamaño del lote. Esta variación puede ser continua y no lineal, o escalonada.
   - **Costo de Capital Inmovilizado**: Se incluye el costo del capital inmovilizado en el inventario.
   - **Optimización del Lote de Reabastecimiento**: Se busca el tamaño del lote que minimice el costo total esperado (\(CTE\)).

### Resolución de Problemas de Stock

Resolver un problema de stock implica determinar las fechas y volúmenes óptimos de reaprovisionamiento para minimizar los costos totales. Esto generalmente se logra utilizando fórmulas específicas para cada modelo de inventario.

#### Ejemplo de Cálculo para el Modelo de Stock Simple (EOQ)

El **Modelo de Cantidad Económica de Pedido (EOQ)** es un modelo determinístico clásico que calcula el tamaño óptimo del lote de pedido (\(Q\)) para minimizar los costos totales de inventario. Los principales componentes son:

1. **Costo de Pedido (\(C_p\))**: Costo fijo asociado con realizar un pedido.
2. **Costo de Mantenimiento (\(C_h\))**: Costo de mantener una unidad de producto en inventario por un periodo de tiempo.
3. **Demanda Anual (\(D\))**: Cantidad total demandada por año.

La fórmula EOQ se expresa como:

\[ Q^* = \sqrt{\frac{2DC_p}{C_h}} \]

Donde:
- \(Q^*\) es el tamaño óptimo del lote de pedido.
- \(D\) es la demanda anual.
- \(C_p\) es el costo de realizar un pedido.
- \(C_h\) es el costo de mantener una unidad en inventario por un año.

**Ejemplo:**

Supongamos que:
- La demanda anual (\(D\)) es de 10,000 unidades.
- El costo por pedido (\(C_p\)) es de $50.
- El costo de mantenimiento por unidad por año (\(C_h\)) es de $2.

Aplicamos la fórmula EOQ:

\[ Q^* = \sqrt{\frac{2 \times 10000 \times 50}{2}} = \sqrt{500000} \approx 707 \text{ unidades} \]

El tamaño óptimo del lote de pedido es de 707 unidades.

### Utilización de Modelos de Inventario

Estos modelos ayudan a los tomadores de decisiones a:

- Determinar cuándo y cuánto pedir para minimizar costos.
- Asegurar que haya suficiente inventario para satisfacer la demanda sin incurrir en costos excesivos.
- Adaptarse a variaciones en la demanda y la oferta.
- Optimizar la gestión del inventario para mejorar la eficiencia y reducir costos.

Cada modelo tiene sus propias aplicaciones y se elige en función de las características específicas del entorno de inventario y las necesidades de la organización.

### Características del Modelo General de Inventario Determinístico

El modelo general de inventario determinístico se caracteriza por:

1. **Demanda y Parámetros Conocidos**: La demanda y otros parámetros relevantes, como los costos de pedido y almacenamiento, son conocidos y constantes.
2. **Reabastecimiento Instantáneo**: Los pedidos se realizan y se reciben instantáneamente, sin demoras en el tiempo de entrega.
3. **Costos Fijos**: No hay variación en los costos de preparación o pedido a lo largo del tiempo.
4. **Política de Reabastecimiento Determinada**: La política de reabastecimiento, como la cantidad óptima de pedido, se determina de manera precisa y no cambia con el tiempo.

### Modelos Estáticos de Cantidad Económica de Pedido (CEP o EOQ)

Los modelos estáticos de Cantidad Económica de Pedido (EOQ) son una clase específica de modelos determinísticos de inventario. Sus características principales son:

1. **Demanda Constante**: Se asume una demanda constante y conocida.
2. **Costos Fijos**: Los costos de pedido y almacenamiento son constantes y conocidos.
3. **Reabastecimiento Instantáneo**: Los pedidos se realizan y reciben al instante.
4. **Optimización del Tamaño del Lote de Pedido**: El objetivo es encontrar el tamaño óptimo del lote de pedido para minimizar los costos totales de inventario.
5. **Política de Reorden Determinística**: Se establece una política de reorden basada en la cantidad de inventario en un momento dado.

### Modelos Dinámicos de Cantidad Económica de Pedido

Los modelos dinámicos de Cantidad Económica de Pedido se diferencian de los estáticos en que consideran la variación de la demanda y otros parámetros a lo largo del tiempo. Estos modelos pueden ser con o sin costo de reposición. Sus características destacadas incluyen:

1. **Revisión Periódica**: El nivel de inventario se revisa en intervalos regulares durante un número finito de periodos.
2. **Demanda Dinámica Determinista**: La demanda puede variar de un periodo a otro, pero sigue un patrón predecible.
3. **Inventario Acumulado**: Se acumula inventario en periodos de alta producción para cubrir la demanda en periodos de baja producción.
4. **Costos Variables**: Se pueden incurrir en costos variables, como costos de almacenamiento adicionales durante periodos de alta producción.

### Características del Modelo General de Inventario Probabilístico

El modelo general de inventario probabilístico se caracteriza por:

1. **Demanda Probabilística**: La demanda se describe mediante una distribución de probabilidades en lugar de un valor determinístico.
2. **Incertidumbre en los Parámetros**: Los parámetros, como la demanda y los tiempos de entrega, pueden variar y están sujetos a incertidumbre.
3. **Política de Reabastecimiento Adaptativa**: La política de reabastecimiento puede ajustarse en función de las condiciones y la variabilidad observada en la demanda y otros factores.
4. **Modelos de Revisión Continua y Periódica**: Se pueden utilizar tanto modelos de revisión continua como de revisión periódica, dependiendo de las características específicas del inventario y las necesidades del negocio.

### Características de los Modelos de Revisión Continua

Los modelos de revisión continua se caracterizan por:

1. **Revisión Constante del Inventario**: El nivel de inventario se revisa continuamente a medida que se realizan ventas o se reciben pedidos.
2. **Reabastecimiento Instantáneo**: Los pedidos se realizan tan pronto como el inventario alcanza un nivel de reorden predeterminado.
3. **Demanda Continua**: La demanda se produce de manera continua en lugar de en intervalos discretos de tiempo.

### Características de los Modelos de Períodos

Los modelos de períodos se caracterizan por:

1. **Revisión Periódica del Inventario**: El nivel de inventario se revisa en intervalos regulares de tiempo, como al final de cada periodo de planificación.
2. **Demanda Acumulada**: La demanda se acumula durante el periodo y se satisface con un solo pedido al final del periodo.
3. **Costos de Preparación o Pedido**: Puede haber costos asociados con la preparación o el pedido de inventario, dependiendo de las políticas de reabastecimiento y las condiciones del negocio.