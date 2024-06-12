

---
### Programación Lineal Entera

#### ¿Para qué se utiliza la programación lineal entera?
La programación lineal entera se utiliza para resolver problemas de optimización en los cuales las variables de decisión deben tomar valores enteros. Esto es común en situaciones donde las decisiones son discretas, como la asignación de recursos, la planificación de la producción, la ubicación de instalaciones, y problemas de logística. Se requiere cuando las soluciones deben ser números enteros debido a la naturaleza del problema, como en el caso de unidades de productos, empleados, vehículos, etc.

#### Diferencia entre las programaciones
Existen diferentes tipos de programación lineal entera:

- **Programación Entera Pura:** Todas las variables de decisión deben ser enteras.
- **Programación Entera Mixta:** Algunas variables de decisión deben ser enteras mientras que otras pueden ser continuas.
- **Programación Entera Binaria:** Todas las variables de decisión deben ser enteras y tomar valores 0 o 1.

La principal diferencia con la programación lineal estándar es la restricción adicional de que las variables deben ser enteras, lo cual complica la solución del problema.

#### ¿Qué métodos se utilizan en la programación lineal entera?
Los métodos principales para resolver problemas de programación lineal entera son:

- **Método de Ramificación y Acotamiento (Branch and Bound):** Se basa en dividir el problema en subproblemas más pequeños y acotar las soluciones posibles.
- **Método de Planos de Corte (Cutting Planes):** Agrega restricciones adicionales al problema para eliminar soluciones no enteras y acercarse a la solución entera óptima.

### Modelo de Inventario

Los modelos de inventario se utilizan para determinar las políticas óptimas de gestión de inventarios, respondiendo a preguntas como cuánto y cuándo ordenar. Los modelos pueden ser determinísticos o probabilísticos, y pueden incluir costos de pedido, almacenamiento y faltantes.

#### ¿Cuántos costos se manejan en un modelo de inventario?
En un modelo de inventario se manejan principalmente tres tipos de costos:

- **Costo de Pedido o Preparación:** Costo asociado a realizar un pedido o preparar una producción.
- **Costo de Mantenimiento o Almacenamiento:** Costo de mantener inventario en stock, incluyendo almacenamiento, seguros, y deterioro.
- **Costo de Faltante:** Costo asociado a no poder satisfacer la demanda, incluyendo pérdida de ventas y penalizaciones.

#### Diferencia entre un costo faltante y un costo de mantenimiento (ejemplo)
- **Costo de Mantenimiento:** Es el costo incurrido por mantener inventario en stock. Por ejemplo, si una empresa mantiene 100 unidades de un producto en su almacén, incurrirá en costos de almacenamiento, seguros y deterioro de esos productos.
- **Costo de Faltante:** Es el costo incurrido cuando no se puede satisfacer la demanda. Por ejemplo, si una tienda no tiene suficiente inventario para satisfacer la demanda de un cliente, podría perder esa venta y posiblemente futuros negocios con ese cliente.

#### ¿Para qué se usa un modelo u otro?
- **Modelos Determinísticos:** Se utilizan cuando la demanda y otros parámetros son conocidos y constantes.
- **Modelos Probabilísticos:** Se utilizan cuando hay incertidumbre en la demanda o en otros parámetros.

#### ¿Cuáles son los tipos de inventario?
- **Materia Prima:** Materiales básicos que se utilizan en la producción.
- **Productos en Proceso:** Productos que están en proceso de fabricación.
- **Productos Terminados:** Productos que están listos para ser vendidos.

#### ¿Para qué se usa cada modelo?
- **Modelo de Cantidad Económica de Pedido (EOQ):** Se usa para determinar la cantidad óptima de pedido que minimiza los costos totales de inventario.
- **Modelo de Revisión Continua:** Se usa para gestionar inventarios mediante un monitoreo continuo del nivel de inventario y realizar pedidos cuando se alcanza un nivel de reorden.
- **Modelo de Revisión Periódica:** Se usa para revisar y ordenar inventarios a intervalos de tiempo fijos.

### Clasificación ABC

La clasificación ABC es una técnica de gestión de inventarios que categoriza los artículos en tres clases basadas en su importancia:

- **A:** Artículos de alto valor monetario pero bajo volumen.
- **B:** Artículos de valor y volumen intermedio.
- **C:** Artículos de bajo valor monetario pero alto volumen.

Esta clasificación ayuda a enfocar los recursos de gestión en los artículos más importantes (A) y aplicar controles más relajados a los menos importantes (C).

---
