# 📖 Catálogo de Mascotas Limpiadoras

Descripción detallada de los **personajes**, la **casa** y las **cartas** del escenario por defecto.
Los datos coinciden con `datos_escenario.xlsx`. Si cambias el Excel, actualiza también este documento.

---

## 🎲 El dado de las mascotas

Dado de 6 caras: **1 · 2 · 3 · 4 · 5 · X**

| Dato | Valor |
|---|---|
| Probabilidad de X | 1 de 6 (≈ 17 %) |
| Promedio si no sale X | 3 puntos |
| Promedio contando la X | 2,5 puntos por turno |

La **X** representa que, al fin y al cabo, son animales: se distraen con una mosca, se duermen en el sofá o se van a perseguir su cola.

---

## 🐾 Personajes

### 🐶 Perro — *El entusiasta*
Le pone muchísimas ganas a todo: corre, empuja y frota con energía.
- **Habilidad:** lanza **1d4 adicional** y lo suma al dado de mascota.
- **Rendimiento:** 5,5 puntos de promedio cuando no sale X (≈ 4,6 por turno contando la X). Es la mascota que más limpia.
- **Punto débil:** sufre las penalizaciones completas de los objetos delicados. Si sale X, también pierde su d4.
- **Le conviene:** objetos grandes con muchas FS (alfombras, cama, tina, piso).

### 🐱 Gato — *El delicado*
Se mueve con elegancia entre vasos y cristales sin romper nada.
- **Habilidad:** **ignora las penalizaciones** de los objetos delicados.
- **Rendimiento:** 2,5 puntos por turno, pero siempre completos.
- **Punto débil:** es la mascota que menos puntos saca.
- **Le conviene:** vasos, vajilla, espejo, ventanal, florero y lámpara.

### 🐰 Conejo — *El ágil*
Salta de un lado a otro sin perder el ritmo.
- **Habilidad:** puede **repartir su tirada entre 2 objetos** (ej.: saca 5 → 2 FS en uno y 3 FS en otro).
- **Rendimiento:** 2,5 puntos por turno, casi sin desperdicio, porque usa los puntos sobrantes en un segundo objeto.
- **Punto débil:** si reparte hacia dos objetos delicados, paga la penalización en ambos.
- **Le conviene:** terminar objetos con pocas FS y cerrar habitaciones para conseguir recompensas.

---

## 🏠 La casa (escenario por defecto)

**5 habitaciones · 22 objetos · 70 FS en total · 10 rondas**

🟤 = 1 ficha de suciedad · ⚠️ = objeto delicado (resta al dado)

### 1. Sala — 14 FS
| Objeto | FS | Penalización | Nota |
|---|---|---|---|
| Sofá | 4 | — | Lleno de pelos de mascota. |
| Alfombra | 5 | — | El objeto más sucio de la sala. |
| Mesa de centro | 3 | — | |
| Florero ⚠️ | 2 | -1 | Cuidado con tumbarlo. |

### 2. Cocina — 16 FS
| Objeto | FS | Penalización | Nota |
|---|---|---|---|
| Mesa | 4 | — | |
| Silla 1 | 2 | — | |
| Silla 2 | 2 | — | |
| Vasos ⚠️ | 3 | -2 | Muy frágiles: ideal para el gato. |
| Piso | 5 | — | Huellas de patitas por todos lados. |

### 3. Baño — 12 FS
| Objeto | FS | Penalización | Nota |
|---|---|---|---|
| Lavamanos | 3 | — | |
| Espejo ⚠️ | 2 | -1 | |
| Tina | 5 | — | Nadie quiere entrar ahí. |
| Toalla | 2 | — | |

### 4. Dormitorio — 13 FS
| Objeto | FS | Penalización | Nota |
|---|---|---|---|
| Cama | 5 | — | Su lugar favorito para dormir… |
| Alfombra | 3 | — | |
| Lámpara ⚠️ | 2 | -1 | |
| Ropero | 3 | — | |

### 5. Comedor — 15 FS
| Objeto | FS | Penalización | Nota |
|---|---|---|---|
| Mesa | 4 | — | |
| Silla 1 | 2 | — | |
| Silla 2 | 2 | — | |
| Vajilla ⚠️ | 4 | -2 | El objeto delicado más difícil. |
| Ventanal ⚠️ | 3 | -1 | |

**Objetos delicados:** 6 en total (florero, vasos, espejo, lámpara, vajilla y ventanal), con 16 FS entre todos.

---

## 🎁 Recompensas

Al dejar una habitación sin suciedad, la mascota que la terminó roba **1 carta** del mazo de recompensas.
El mazo tiene **14 cartas**: 9 consumibles y 5 objetos de limpieza. Como hay 5 habitaciones, en cada partida salen como máximo 5 recompensas.

### 🍖 Consumibles (un solo uso, van a la mochila)

| Carta | Copias | Efecto | Cuándo usarla |
|---|---|---|---|
| **Ración de comida** | 3 | `evitar_x` — Si sale X, te la comes y **vuelves a tirar**. | Solo justo después de sacar X. |
| **Galleta** | 3 | `bonus` +2 — Suma **2 puntos** a la tirada actual. | Después de tirar, antes de terminar de asignar. |
| **Hueso de goma** | 2 | `relanzar` — **Repite la tirada**. | Tras sacar X o un número bajo, antes de asignar puntos. |
| **Siesta corta** | 1 | `turno_extra` — Al terminar este turno, **juegas otro**. | En cualquier momento de tu turno. |

> *Ración de comida:* una mascota con la panza llena no se distrae.
> *Siesta corta:* una pequeña siesta recarga energías para seguir limpiando.

### 🧽 Objetos de limpieza (equipo, quedan con la mascota)

| Objeto | Copias | Efecto | Duración |
|---|---|---|---|
| **Trapito** | 2 | `bonus` +1 — **+1 punto** en todas tus tiradas. | Permanente |
| **Guantes suaves** | 1 | `ignorar_fragil` — **Ignoras las penalizaciones** de objetos delicados. | Permanente |
| **Plumero** | 1 | `reducir_fragil` 1 — Las penalizaciones se **reducen en 1**. | Permanente |
| **Esponja mágica** | 1 | `dado_extra` d4 — Lanzas **1d4 extra** en cada tirada. | 3 usos |

**Combinaciones interesantes:**
- **Guantes suaves en el perro:** convierte a la mascota más fuerte en experta en objetos delicados.
- **Trapito en el conejo:** más puntos para repartir entre dos objetos.
- **Esponja mágica en el perro:** d6 + d4 + d4, el turno más potente posible.
- **Plumero en el gato:** no le sirve (ya ignora penalizaciones). ¡Mejor dárselo a otro!

> Nota: en el prototipo, las cartas las recibe la mascota que terminó la habitación y no se pueden intercambiar (pendiente de decidir).

---

## 📊 Balance (referencia rápida)

Con las 3 mascotas, el equipo limpia en promedio ≈ **9–10 FS por ronda** (antes de penalizaciones y recompensas).
70 FS ÷ 10 rondas = 7 FS por ronda necesarias, así que hay margen, pero las X y los objetos delicados lo reducen.
Con menos mascotas conviene **subir el número de rondas** en el menú.
