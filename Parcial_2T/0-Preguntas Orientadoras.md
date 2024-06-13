# Preguntas de Parcial: Conceptos Cortos

## ¿Qué es un inventario?

Un inventario es la cantidad de artículos que son almacenados y se mantienen inactivos en un instante de tiempo dado. Incluye la cantidad de productos, sus características y su estado.

## ¿Para qué se utiliza la programación lineal entera?
La programación lineal entera se utiliza para resolver problemas de optimización en los cuales las variables de decisión deben tomar valores enteros. Es común en situaciones donde las decisiones son discretas, como la asignación de recursos, la planificación de la producción, la ubicación de instalaciones y problemas de logística. Específicamente, se requiere cuando las soluciones deben ser números enteros debido a la naturaleza del problema, como en el caso de unidades de productos, empleados, vehículos, etc.

## Diferencia entre las programaciones
Existen diferentes tipos de programación lineal entera:
- **Programación Entera Pura:** Todas las variables de decisión deben ser enteras.
- **Programación Entera Mixta:** Algunas variables de decisión deben ser enteras mientras que otras pueden ser continuas.
- **Programación Entera Binaria:** Todas las variables de decisión deben ser enteras y tomar valores 0 o 1.

La principal diferencia con la programación lineal estándar es la restricción adicional de que las variables deben ser enteras, lo cual complica la solución del problema.

## ¿Qué métodos se utilizan en la programación lineal entera?
Los métodos principales para resolver problemas de programación lineal entera son:
- **Método de Ramificación y Acotamiento (Branch and Bound):** Se basa en dividir el problema en subproblemas más pequeños y acotar las soluciones posibles.
- **Método de Planos de Corte (Cutting Planes):** Agrega restricciones adicionales al problema para eliminar soluciones no enteras y acercarse a la solución entera óptima.

## Modelo de Inventario
Los modelos de inventario se utilizan para determinar las políticas óptimas de gestión de inventarios, respondiendo a preguntas como cuánto y cuándo ordenar. Los modelos pueden ser determinísticos o probabilísticos, y pueden incluir costos de pedido, almacenamiento y faltantes.

## ¿Cuántos costos se manejan en un modelo de inventario?
En un modelo de inventario se manejan principalmente tres tipos de costos:
1. **Costo de Pedido o Preparación:** Costo asociado a realizar un pedido o preparar una producción.
2. **Costo de Mantenimiento o Almacenamiento:** Costo de mantener inventario en stock, incluyendo almacenamiento, seguros, y deterioro.
3. **Costo de Faltante:** Costo asociado a no poder satisfacer la demanda, incluyendo pérdida de ventas y penalizaciones.
4. **Costo de Producto:** Costo de adquisición o de producción. Supondremos que es el costo unitario, independiente (salvo para un modelo en especial) de la cantidad comprada.

## Diferencia entre un costo faltante y un costo de mantenimiento (ejemplo)
- **Costo de Mantenimiento:** Es el costo incurrido por mantener inventario en stock. Por ejemplo, si una empresa mantiene 100 unidades de un producto en su almacén, incurrirá en costos de almacenamiento, seguros y deterioro de esos productos.
- **Costo de Faltante:** Es el costo incurrido cuando no se puede satisfacer la demanda. Por ejemplo, si una tienda no tiene suficiente inventario para satisfacer la demanda de un cliente, podría perder esa venta y posiblemente futuros negocios con ese cliente, lo cual afecta negativamente la reputación de la marca.

## ¿Para qué se usa un modelo u otro?
- **Modelos Determinísticos:** Se utilizan cuando la demanda y otros parámetros son conocidos y constantes.
  - **Modelo I:** Modelo de Wilson. Demanda determinística y constante. Sin agotamiento.
  - **Modelo II:** Demanda constante con inventario de contingencia (Modelo con Stock de Protección).
  - **Modelo III:** Demanda constante con agotamiento. Se aceptan faltantes.
  - **Modelo IV:** Stock con producción y demanda conjunta (Modelo Triangular). La reposición no es instantánea.
  - **Modelo V:** Stock sin agotamiento con costos de compra variables según el tamaño del lote ordenado (Descuento por cantidad).

- **Modelos Probabilísticos:** Se utilizan cuando hay incertidumbre en la demanda o en otros parámetros.
  - **Modelo de Período Único (sin agotamiento de stock):** Se determina la probabilidad de cada tipo de demanda y se calcula el lote que minimiza el CTE. Se utiliza para ítems con alto costo unitario, costo de almacenamiento despreciable, alto costo de agotamiento y obsolescencia rápida.

## ¿Cuáles son los tipos de inventario?
- **Materia Prima:** Materiales básicos utilizados en la producción.
- **Productos en Proceso:** Productos que están en proceso de fabricación.
- **Productos Terminados:** Productos que están listos para ser vendidos.

## Clasificación ABC
La clasificación ABC es una técnica de gestión de inventarios que categoriza los artículos en tres clases basadas en su importancia:
- **A:** Artículos de alto valor monetario pero de bajo volumen. Nivel de exactitud de control: ±0,2%.
- **B:** Artículos de valor y volumen intermedio. Nivel de exactitud de control: ±1,0%.
- **C:** Artículos de bajo valor monetario pero alto volumen. Nivel de exactitud de control: ±5,0%.

("Volumen" se refiere a la cantidad física de artículos o unidades en stock. "Nivel de exactitud en el control" se refiere a la precisión con la que se gestiona y cuenta el inventario.)

Esta clasificación ayuda a enfocar los recursos de gestión en los artículos más importantes (A) y aplicar controles más relajados a los menos importantes (C).
