

----
## Ej 2 - De Recuperatorio

![[Pasted image 20240510124820.png]]


Entendido, aquí tienes la información formateada para Obsidian:

---

## Problema de Optimización de Compra de Combustible

### Hipótesis

- Se considera el periodo de tiempo por un MES.

### Variables de Decisión

- **x1:** Cantidad de combustible que se debe comprar del vendedor 1 [galones/mes]
- **x2:** Cantidad de combustible que se debe comprar del vendedor 2 [galones/mes]
- **x3:** Cantidad de combustible que se debe comprar del vendedor 3 [galones/mes]

### Función Objetivo

$$ Z = x1 + x2 + x3 \rightarrow \text{MINIMIZAR} \quad [galones] $$
### Restricciones

1. $$ x1 \leq 300 \quad [galones/mes] $$
2. $$ x2 \leq 600 \quad [galones/mes] $$
3. $$ x3 \leq 700 \quad [galones/mes] $$
4. $$ 900x1 + 800x2 + 900x3 \geq 150 \quad [$/mes] $$
5. $$ 900x1 + 1200x2 + 1300x3 \geq 250 \quad [$/mes] $$
6. $$ 800x1 + 1300x2 + 500x3 \geq 350 \quad [$/mes] $$

### Slacks
##### Interpretacion de Slacks

$≥ →-→$ ***Por* *encima* del minimo**

$≤ →+→$  ***Por debajo* del minimo**

- **s4:** Cantidad por encima del mínimo de combustible para el aeropuerto 1.
- **s5:** Cantidad por encima del mínimo de combustible para el aeropuerto 2.
- **s6:** Cantidad por encima del mínimo de combustible para el aeropuerto 3.

### Ecuaciones

1. $$ 900x1 + 800x2 + 900x3 - s4 - 0s5 - 0s6 = 150 \quad [$/mes] $$
2. $$ 900x1 + 1200x2 + 1300x3 - 0s4 - s5 - 0s6 = 250 \quad [$/mes] $$
3. $$ 800x1 + 1300x2 + 500x3 - 0s4 - 0s5 - s6 = 350 \quad [$/mes] $$

---
