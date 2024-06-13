
### Teoría de Stock y Modelos de Inventario

- La teoría de stock se ocupa de estudiar y determinar las **políticas óptimas de reabastecimiento** en inventarios para *minimizar los costos asociados*.
- Estos costos incluyen el costo de **almacenamiento**, costo de **desabastecimiento**, y otros costos relacionados con la gestión de inventarios.
- El **objetivo es encontrar un equilibrio** entre mantener un inventario suficiente para *satisfacer la demanda* y *minimizar los costos asociados*.


Claro, aquí te proporciono una explicación breve y clara de cada modelo de inventario mencionado, junto con su aplicación típica:



**Modelo de Período Único (sin Agotamiento de Stock)**


# Modelos de Inventario

## Stocks con Demanda DETERMINISTICA

> Son utilizados en entornos donde la demanda es predecible o estable, permitiendo una gestión eficiente del inventario y minimizando los costos asociados.
  

### Modelo I: Modelo de Wilson
- **Descripción**: Este modelo asume una demanda determinística y constante, sin agotamiento del stock.
- **Aplicación**: Se utiliza para gestionar inventarios cuando la demanda es estable y predecible, como en artículos de consumo regular.

- **Demanda:** Determinística y constante.
- **![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXfSxEBaJ1rpSVwEbDJcBTSob-3oPutZSZyCz25kIYimaAhIkUnepAY8SzVdq7IyBz30e3ZBSeGBFTgh0yKYRSeoGVITtLLlQDhhbszy6-wGdUXfUz7KGLrCvObMVYqbrBbZeep_pHlKq9sC_CXrd9mngu4?key=ESjnCozrK6HeQO4PkjCJug)**
- **Características:** 
  - Demanda continua asimilada a una recta.
  -  No permite agotamiento de stock.
  - ![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXftIMGclDBr2QkWkQQvR93_TDQ_FCYEYqdiDNpBQqMq5BXWaxNIxlhWPhvFUVWxS9rqzZNq4UvaHfyyGkXM1V1uBUCVtgKKqESPt1wTCmgFvtcJ561MIes4UOGP1CGyP1-DVJeIgAB8LzRj2AbVpZEiUg?key=ESjnCozrK6HeQO4PkjCJug)
  - ![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXej6E6IOpelxfJ6y-gp5G1CCKaYS2LNad7rUp_l6yH6IK9qKZO-YJUSAt4HFt7piusfyDY_QXQtYTmTFV5aGS0gHjBhF5VqTjysjB4AGeLNkSE9zsbWRdx1LbxcfdXmOfNiB0ULSfWA17OG2EIcRjYZy1q4?key=ESjnCozrK6HeQO4PkjCJug)

#### Costos de Gestión de Stocks
- **Costo de Preparación (K):** Independiente de la cantidad ordenada.
- **Costo de Producto (b):** Costo unitario de adquisición o producción.
- **Costo de Almacenamiento (c1):** Incluye costos reales (seguros, impuestos, alquiler, etc.) y el costo de oportunidad.
- **Costo de Escasez (c2):** Aparece en modelos con ruptura de stock, implica ingresos retrasados y pérdida de prestigio.
- **![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXfaFRnsxv1sUTh05QHX2e9yOrsF1IQRULtmgd1GaYKBmIs17Pq2r7g75B-t9741UrBl2M0WYKFQosa8fkKrL2Kw2pFJOMOGaafVFAfvZdmZdQgTRAoY4aRruhegqfH86TZ4q7deZVWkABxtBH0sOz9QNhF9?key=ESjnCozrK6HeQO4PkjCJug)**
### Modelo II: Demanda Constante con Inventario de Emergencia
-  **Descripción**: Incluye un *stock de protección* para manejar errores de estimación en la demanda.
- **Aplicación**: Ideal para productos donde la demanda puede variar o hay incertidumbre en las estimaciones, asegurando disponibilidad en caso de fluctuaciones imprevistas.

- **Características:**
  - Incluye un inventario de contingencia para cubrir errores de estimación.
  - Utiliza un stock mínimo de protección

### Modelo III: Demanda Constante con Agotamiento
-  **Descripción**: Acepta la posibilidad de agotamiento del stock, es decir, *permite que ocurran situaciones donde no se puede satisfacer toda la demanda*.
- **Aplicación**: Útil cuando los costos de mantener inventario adicional son altos y se prefieren políticas más flexibles que puedan manejar faltantes ocasionales.
- **Características:**
  - Permite faltantes de inventario.
  - No permitido en el Modelo I.
  - ![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXckvy_NNa3gZlYlxtSXeOLe7CVjmGLG9DApB7WzPqZVGaDWhspjL2sadW3r_3A-WzTyLaB6t5bmY4x-R-S0NtG6I6b1GM9n9sEUOY4hwfF4Wu-VinDhVmXbafNtKhzugtj_NZKiJrtpBnYfkq9Rbgj2UUjZ?key=ESjnCozrK6HeQO4PkjCJug)

### Modelo IV: Stock con Producción y Demanda Conjunta (Modelo Triangular)
- **Descripción**: *Considera la producción y la demanda simultáneamente*, con un tiempo de reposición no instantáneo.
- **Aplicación**: Aplicable a productos manufacturados donde la reposición no es inmediata, como en industrias de producción continua.
- **Características:**
  - La reposición no es instantánea.
  - Aplicable a ítems almacenados a medida que termina la producción.
  - *La demanda se mide por unidad de tiempo* (d).
![300x200](https://lh7-us.googleusercontent.com/docsz/AD_4nXfi9qz7_1HmjAYlZglx_hFjYDQTrsZ-3C_1yFCKLQjDtrr0G_456uUP71Ba7v4hQUpN3FEVfrCGjJ3oMr92jyRJOuxkCM_vX1QzI-KBUJMwEOoIeTJfelTZr4xDwBqconVgkz7h-ufO7tUJpR3Lsp5dxtKW?key=ESjnCozrK6HeQO4PkjCJug)

### Modelo V: Stock sin Agotamiento con Descuento por Cantidad
- **Descripción**: Incorpora **descuentos por volumen** en los costos de compra, *incentivando pedidos en grandes cantidades.*
- **Aplicación**: Se utiliza para maximizar el beneficio al comprar grandes cantidades, **considerando tanto los costos de mantenimiento como los descuentos por compra al por mayor**.

- **Características:**
  - Costos de compra variables según el tamaño del lote.
  - El costo unitario **decrece exponencialmente** y **se estabiliza**.
  - Costos de mantenimiento incluyen el costo del dinero inmovilizado y otros costos adicionales.

**![300](https://lh7-us.googleusercontent.com/docsz/AD_4nXcqbiq7Bw-BQOxjfkZ3KSJ430aRe2aW4iDXrJdAGXh0Ecf5-cn54r6bWOQzbFC-xPnIIw1Jw_u-_x_2eVsMzlZvMBZhtakb2YENSqad-pmLKlvHR0nDfef89Bw38WiP6JC9srALkweBycGpqsgVawraBJwx?key=ESjnCozrK6HeQO4PkjCJug)**

## Stocks con Demanda Aleatoria

> Se emplean cuando **la demanda varía de manera impredecible**, ayudando a mitigar los riesgos de agotamiento del stock y optimizando los niveles de inventario bajo incertidumbre.


### Modelo de Período Único (sin Agotamiento de Stock)
-  **Descripción**: *Calcula el tamaño del lote de pedido óptimo considerando* la incertidumbre en la demanda.
- **Aplicación**: Adecuado para artículos con alta variabilidad en la demanda o cuando el costo de no satisfacer la demanda (agotamiento) es significativo.

- **Características:**
  - Determina la probabilidad de cada tipo de demanda.
  - Calcula el lote que minimiza el Costo Total Esperado (CTE).
  - Aplicable a ítems con alto costo unitario, almacenamiento despreciable, alto costo de agotamiento y obsolescencia rápida.

#### Ejemplo
- **Artículos:** Repuestos de un avión de guerra, joyas costosas con moda pasajera.

### Variables y Definiciones
- **Probabilidad (p(0)):** Indica la probabilidad de demanda cero.
- **Demanda Efectiva:** Variable aleatoria que debe ser manejada con esperanzas matemáticas.

# Clasificación ABC

La clasificación ABC es una técnica de gestión de inventarios que categoriza los artículos en tres clases basadas en su importancia económica y volumen:

- **A**: Artículos de alto valor monetario pero de bajo volumen. Estos son los productos más valiosos y generalmente representan una pequeña parte del inventario total en términos de cantidad, pero una gran parte en términos de valor. 

- Ejemplo: Equipos electrónicos costosos, piezas críticas de maquinaria.
  - **Nivel de exactitud en el control**: +-0,2%.

- **B**: Artículos de valor y volumen intermedio. Estos productos tienen un valor y volumen moderado, y son menos críticos que los artículos A pero aún así importantes.
  - Ejemplo: Productos de consumo regular como materiales de oficina o componentes estándar.
  - **Nivel de exactitud en el control**: +-1,0%.

- **C**: Artículos de bajo valor monetario pero alto volumen. Estos artículos son los menos valiosos y suelen representar la mayor parte del inventario en términos de cantidad, pero una pequeña parte en términos de valor.
- Ejemplo: Tornillos, tuercas, y otros artículos de bajo costo.
  - **Nivel de exactitud en el control**: +-5,0%.

**Importancia de la Clasificación ABC**

- Esta clasificación permite a las empresas enfocar sus recursos de gestión en los artículos más importantes (A), asegurando un control más preciso y minucioso.
- Para los artículos de clase B, se aplican controles de gestión moderados, mientras que los artículos de clase C reciben controles más relajados, reduciendo así los costos de gestión y almacenamiento.


**Ventajas de la Clasificación ABC**

1. **Optimización de Recursos**: Permite asignar recursos y esfuerzos de gestión de manera más eficiente, centrándose en los artículos que más impactan en el valor del inventario.

2. **Mejora en la Exactitud de Inventarios**: Los artículos de mayor valor (A) se gestionan con mayor precisión, reduciendo errores y pérdidas costosas.

3. **Reducción de Costos**: Al aplicar controles menos estrictos a los artículos de menor valor (C), se reducen los costos operativos y administrativos.

**Aplicación de la Clasificación ABC**
Según la American Production and Inventory Control Society (APICS), la exactitud en el control de inventarios varía para cada categoría, reflejando la importancia de cada clase:

- **Artículo A**: +-0,2%
- **Artículo B**: +-1,0%
- **Artículo C**: +-5,0%

Estas variaciones en la exactitud permiten a las empresas mantener un equilibrio entre la eficiencia operativa y el control preciso del inventario.
