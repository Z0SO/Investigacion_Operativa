

### Programación Lineal Entera

#### ¿En qué consiste un problema de Programación Lineal Entera?
La programación lineal entera se caracteriza por la restricción adicional de que los valores de todas o algunas de las variables de decisión sean enteros (o discretos). Esta condición adicional se conoce como integridad.

#### ¿Cuál es la justificación de su existencia?
La programación entera se utiliza para resolver problemas en los cuales las variables de decisión deben ser enteras. Esto es común en situaciones donde las decisiones son discretas, como la asignación de recursos o la planificación de producción.

#### ¿Qué casos se pueden presentar en Programación Lineal Entera?
- **Programas Enteros Puros:** Exige que todas las variables de decisión tengan valores enteros.
- **Programas Enteros Mixtos:** Algunas variables deben ser enteras mientras que otras pueden asumir cualquier número no negativo.
- **Programas Enteros 0-1 (binarios):** Variables que solo pueden tomar valores 0 o 1, representando decisiones dicotómicas.

**Ejemplos de aplicación:** Asignación, Ubicación de Plantas, Planes de producción, Elaboración de cartera, etc.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdlUUlz_p14Mu_dpMMHiI6aoD-ZxSZoss3w9AqSHcF3pRDR5T4G58r9W5h1clsTHu0qg9GuGpDbeT3FXY0dgny1emQWAbVSZ6hgw4TAQrYUd83FsH2-91fN10dU56NU1pUUHApYH_RRglLqh3-lFjRqPEdK?key=iTPa6W9OMH7L3aG9DQ3z0g)

#### ¿Cuáles son las características de un problema de costo fijo en Programación Lineal Entera?
- **Costo fijo:** Involucra variables binarias asociadas a las variables de decisión continuas. Este tipo de problemas incluye dos tipos de costos: un costo fijo necesario para iniciar la actividad y un costo variable proporcional al nivel de la actividad.
- **Función de costo:** Expresa la relación entre costos fijos y variables. Es analíticamente insoluble debido a una discontinuidad en \( x = 0 \).
**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcWRPMRCZWiGbEABl_TYQKPMJuI61m50NgCjHSjz0Nfyo_SIIyVx2EwBUEAvZOyjMSYGeHSlS1VoCU52iEXvLVWyRzFLVxrCNcU9uixKlmrhbExtCx5otFPvNCvQfADmM1viwDc1XKRRPiLMrNCNhVJJxo?key=iTPa6W9OMH7L3aG9DQ3z0g)**
#### ¿Cuáles son las características de un problema de cobertura de conjuntos en Programación Lineal Entera?
- **Variables:** Todas las variables son binarias.
- **Restricciones:** Para cada restricción, todos los coeficientes del lado izquierdo son 0 o 1, y el lado derecho tiene la forma “≥1”.
- **Función objetivo:** Minimiza siempre, con coeficientes estrictamente positivos que suelen representar costos.

#### ¿Cuáles son las características de un problema de restricciones de uno o de otra en Programación Lineal Entera?
- **Restricciones:** Utiliza variables binarias auxiliares para transformar restricciones dependientes (Si - entonces) en restricciones “and” (“y”).
- **Tipos de restricciones:**
  - **Restricciones de no-interferencia:** Para trabajos que deban ejecutarse en tiempos distintos.
  - **Restricciones de fecha de vencimiento.**

#### ¿Cuáles son los métodos de resolución del modelo de Programación Lineal Entera?
- **Método del Plano de Corte o Gomory**
- **Método de Ramificación y Corte**

#### ¿Cuál es el algoritmo general de funcionamiento del método de ramificar y acotar en Programación Lineal Entera? Ventajas y desventajas del mismo
El algoritmo B&B se utiliza para problemas generales de programación lineal entera mixta y pura:

1. Resolver el problema lineal (continuo).
2. Si la solución no satisface los requisitos enteros, seleccionar una variable entera cuyo valor óptimo no sea entero.
3. Modificar el espacio de soluciones y resolver una sucesión de programas lineales continuos, eliminando rangos no enteros.
4. Considerar agotado un problema cuando no se puede seguir investigando sus ramas.

**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfRH61OY_eXgFnkRY6z_4Ta0-dT_iWgVzQu5cwOqn9wvQWmycyJXZ-KJDB4t6r4mtZywKpqHGuhKAXkUrEmzTbsL0Pra-naAksYZ7IUt3jtVGUj311QOelOEkGG2zUN-yBtB6fo0Iu_AbYQmYUWsJqG4-YA?key=iTPa6W9OMH7L3aG9DQ3z0g)**
**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXci7zZ-dUCPlVw-LEzmZ9L5L0wZC4e8PPpeC5WQwjKm4xzA4Hnt-4BJAf8kS3kh_KNV9pmaMkD_iIxT0wQz0GtNPvbt0PLSIURvfuURYfrpGJpajt4j8RwF-UvfzwFWawHcRpzbewGRfRnbBV8yROMrIJpE?key=iTPa6W9OMH7L3aG9DQ3z0g)**


**Problemas del algoritmo:**
- Dificultad para elegir la siguiente rama a examinar.
- Se utilizan técnicas heurísticas para la selección de ramas.
- Aplicable también a PLE mixta.

#### ¿Cuál es el algoritmo general de funcionamiento del método de Gomory en Programación Lineal Entera?
1. Iniciar en el óptimo del PL continuo original.
2. Generar cortes en el espacio de soluciones mediante nuevas restricciones que eliminen puntos no factibles y pasen por al menos un punto entero factible.
3. Agregar estas restricciones al problema y operar usando el “simplex dual”.

**![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdgTN-j2EHz1vE6udtsxas_qyzgNzWbW4MpC_gh9J5EbiIJURx9g13K_GgNUa3g3RNB3L3hkCDRZkGZ9ydzooAr87quai3nUbCHOLc29DRJ3fi1I0DhhI4iJ-oyrDrnqdt05rCt2Z2zuzW3h99aDitsh8A?key=iTPa6W9OMH7L3aG9DQ3z0g)**


**Características:**
- Los cortes agregados no eliminan puntos enteros factibles originales.
- La cantidad de cortes es finita, pero puede variar según el tamaño del problema.
- Extensible para problemas mixtos.

**Consejos para evitar problemas computacionales:**
- Aproximar las variables enteras con las continuas cuando sea posible.
- Restringir los intervalos factibles de las variables enteras.
- Evitar el uso de no linealidades en el modelo.

#### ¿Cómo se resuelven los problemas por enumeración implícita en Programación Lineal Entera?
Se basa en el hecho de que un número finito de puntos puede ser solución óptima. Se busca esta solución mediante la enumeración implícita de dichos puntos, descartando los no necesarios sin enumerarlos explícitamente. Se utiliza el Algoritmo Aditivo de Balas para problemas de tipo binario.

---
