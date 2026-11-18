# 🧹 Mascotas Limpiadoras

Juego **cooperativo** pensado para mesa, aquí en versión prototipo para el navegador.
Un perro, un gato y un conejo deben **limpiar la casa antes de que vuelvan los dueños**.

> Detalle de personajes, objetos y cartas: ver [catalogo.md](catalogo.md).
> Reglas de diseño y decisiones del proyecto: ver [contexto.md](contexto.md).

---

## Cómo abrir el prototipo
1. Haz doble clic en `index.html` (se abre en tu navegador).
2. En el menú elige qué mascotas juegan (1 a 3) y cuántas rondas hay antes de que lleguen los dueños.
3. Pulsa **▶ Jugar**.

> Cargar/descargar Excel requiere conexión a internet (usa una librería online). El resto funciona sin conexión.

---

## Objetivo
Dejar **todas las fichas de suciedad (FS)** de la casa en 0 antes de que termine la última ronda.
- ✅ Si la casa queda limpia → **ganan todos**.
- 🚪 Si llegan los dueños y queda suciedad → **pierden** (se muestra el % que alcanzaron a limpiar).

## Preparación
- La casa tiene **5 habitaciones** con varios objetos cada una.
- Cada objeto tiene un número de **FS** (fichas marrones).
- Algunos objetos son **delicados** y tienen una penalización <span>`-x`</span> al dado.
- Se baraja un **mazo de recompensas** (consumibles + objetos de limpieza).

## El dado especial (1d6)
| Cara | Efecto |
|---|---|
| 1 – 5 | Puntos de limpieza |
| ❌ X | La mascota se distrae y **pierde el turno** (¡aún son animales!) |

## Turno de una mascota
1. **Lanza el dado.**
   - Si sale **X**, pierdes el turno (salvo que uses una carta que lo evite).
   - El perro suma 1d4 y el equipo puede sumar puntos o dados extra.
2. **Asigna los puntos** haciendo clic en un objeto de cualquier habitación.
   - Se limpian tantas FS como puntos tengas, **menos la penalización** si el objeto es delicado.
   - Los puntos que sobren se pierden.
   - El conejo puede repartir sus puntos entre **dos** objetos.
3. Si con tu limpieza una **habitación queda sin FS**, robas **1 recompensa**.
4. Pasa el turno a la siguiente mascota. Cuando todas jugaron, avanza una **ronda**.

## Recompensas
- **Consumibles** 🍖: se guardan en la mochila y se gastan al usarlos (clic sobre la carta cuando está resaltada).
- **Objetos de limpieza** 🧽: se equipan y dan su efecto en todas las tiradas (algunos tienen usos limitados).

## Las mascotas (resumen)
| | Habilidad |
|---|---|
| 🐶 Perro | +1d4 a su tirada |
| 🐱 Gato | Ignora penalizaciones de objetos delicados |
| 🐰 Conejo | Reparte su tirada entre 2 objetos |

---

## Editar el escenario
Hay dos formas:

**1. Desde el juego** → menú **✏️ Editar escenario**. Pestañas para Config, Habitaciones, Objetos, Consumibles y Limpieza. Pulsa *Guardar cambios* (se guarda en el navegador).

**2. Con Excel** → edita `datos_escenario.xlsx` y cárgalo con **📂 Cargar Excel**. Para obtener el escenario actual como Excel usa **💾 Descargar Excel**.

### Hojas del Excel
| Hoja | Columnas |
|---|---|
| Config | `clave`, `valor` (`rondas`, `recompensas_por_habitacion`) |
| Habitaciones | `id`, `nombre`, `orden` |
| Objetos | `habitacion_id`, `nombre`, `fs`, `penalizacion`, `cantidad` |
| Consumibles | `nombre`, `efecto`, `valor`, `cantidad`, `descripcion` |
| Limpieza | `nombre`, `efecto`, `valor`, `usos`, `cantidad`, `descripcion` |

### Códigos de efecto
| Código | Dónde | Efecto |
|---|---|---|
| `evitar_x` | Consumibles | Si sale X, vuelve a tirar |
| `relanzar` | Consumibles | Repite la tirada (antes de asignar puntos) |
| `bonus` | Ambos | +`valor` puntos (consumible: una vez · limpieza: siempre) |
| `turno_extra` | Consumibles | Juegas otro turno después de este |
| `ignorar_fragil` | Limpieza | Ignora penalizaciones de objetos delicados |
| `reducir_fragil` | Limpieza | Reduce la penalización en `valor` |
| `dado_extra` | Limpieza | Lanza un dado extra de `valor` caras |

## Archivos
| Archivo | Para qué |
|---|---|
| `index.html` | El prototipo jugable |
| `datos_escenario.xlsx` | Datos editables del escenario |
| `README.md` | Este documento |
| `catalogo.md` | Descripción detallada de personajes y cartas |
| `contexto.md` | Notas de diseño y decisiones del proyecto |
