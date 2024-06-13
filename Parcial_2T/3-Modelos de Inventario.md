
### Teoría de Stock y Modelos de Inventario

La teoría de stock se ocupa de estudiar y determinar las políticas óptimas de reabastecimiento en inventarios para minimizar los costos asociados. Estos costos incluyen el costo de almacenamiento, costo de desabastecimiento, y otros costos relacionados con la gestión de inventarios. El objetivo es encontrar un equilibrio entre mantener un inventario suficiente para satisfacer la demanda y minimizar los costos asociados.

# Modelos de Inventario

## Stocks con Demanda Determinística

### Modelo I: Modelo de Wilson
- **Demanda:** Determinística y constante.
- **Características:** 
  - Demanda continua asimilada a una recta.
  - No permite agotamiento de stock.

#### Costos de Gestión de Stocks
- **Costo de Preparación (K):** Independiente de la cantidad ordenada.
- **Costo de Producto (b):** Costo unitario de adquisición o producción.
- **Costo de Almacenamiento (c1):** Incluye costos reales (seguros, impuestos, alquiler, etc.) y el costo de oportunidad.
- **Costo de Escasez (c2):** Aparece en modelos con ruptura de stock, implica ingresos retrasados y pérdida de prestigio.

### Modelo II: Demanda Constante con Inventario de Contingencia
- **Características:**
  - Incluye un inventario de contingencia para cubrir errores de estimación.
  - Utiliza un stock mínimo de protección.

### Modelo III: Demanda Constante con Agotamiento
- **Características:**
  - Permite faltantes de inventario.
  - No permitido en el Modelo I.

### Modelo IV: Stock con Producción y Demanda Conjunta (Modelo Triangular)
- **Características:**
  - La reposición no es instantánea.
  - Aplicable a ítems almacenados a medida que termina la producción.
  - La demanda se mide por unidad de tiempo (d).

### Modelo V: Stock sin Agotamiento con Descuento por Cantidad
- **Características:**
  - Costos de compra variables según el tamaño del lote.
  - El costo unitario decrece exponencialmente y se estabiliza.
  - Costos de mantenimiento incluyen el costo del dinero inmovilizado y otros costos adicionales.

## Stocks con Demanda Aleatoria

### Modelo de Período Único (sin Agotamiento de Stock)
- **Características:**
  - Determina la probabilidad de cada tipo de demanda.
  - Calcula el lote que minimiza el Costo Total Esperado (CTE).
  - Aplicable a ítems con alto costo unitario, almacenamiento despreciable, alto costo de agotamiento y obsolescencia rápida.

#### Ejemplo
- **Artículos:** Repuestos de un avión de guerra, joyas costosas con moda pasajera.

### Variables y Definiciones
- **Probabilidad (p(0)):** Indica la probabilidad de demanda cero.
- **Demanda Efectiva:** Variable aleatoria que debe ser manejada con esperanzas matemáticas.




**La clasificación ABC es una técnica de gestión de inventarios que categoriza los artículos en tres clases basadas en su importancia económica y volumen:**

- **A**: Artículos de alto valor monetario pero de bajo volumen. Estos son los productos más valiosos y generalmente representan una pequeña parte del inventario total en términos de cantidad, pero una gran parte en términos de valor. 

- Ejemplo: Equipos electrónicos costosos, piezas críticas de maquinaria.

  - Nivel de exactitud en el control: +-0,2%.

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
