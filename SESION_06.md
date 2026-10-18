# Estudio y Diseño de Trabajo — Contenido temático de la Sesión 6 (Semana 6)

**Tema (programa oficial, Unidad III: Estudio de tiempos):** 3.3 Tiempos predeterminados — 3.3.1 MTM; 3.3.2 MODAPTS
**Fecha:** 14 al 20 de octubre de 2026 (sesión presencial: sábado 17 de octubre)
**Actividad de la unidad:** Actividad 3, Foro colaborativo sobre proyecto de estudio de tiempos — 10 puntos, vence el **27 de octubre** (abarca las Semanas 6 y 7).
**Propósito de la sesión:** Que el estudiante (1) distinga con claridad los cinco diagramas del estudio del trabajo (DOP, flujo del proceso, recorrido, hombre-máquina y bimanual) y (2) asigne tiempos predeterminados MTM-1 a los movimientos de una operación manual, compare dos métodos y reconozca el alcance de MODAPTS.

> **Organización de la sesión:** bloque 1 de 30 minutos con rotafolios impresos en la pared para aclarar los diagramas, y bloque 2 de 30 minutos con la actividad en aula por equipo (tiempos predeterminados MTM-1 sobre el acordonado del zapato de la Zapatería XYZ). Los tiempos restantes los define el docente.

> **Nota de uso:** los valores de MTM-1 provienen de la **Tabla MTM-1 v3 de MTM Ingenieros** (2 páginas, la que se usa en clase) y coinciden con las Tablas 3.1 a 3.6 del capítulo 3 de Peralta salvo dos celdas que la actividad no usa: alcanzar C o D a 40 cm (16.8 en la tabla v3; 16.6 en el libro) y mover C a 10 cm (7.9 contra 7.8). Verifíquense contra el libro impreso antes de evaluar. El PDF no cubre MODAPTS; la sección 4 se basa en conocimiento general de la técnica y debe contrastarse con el material del curso.

---

## Índice

0. Definiciones conceptuales clave
1. Bloque 1: los cinco diagramas, cómo se leen y cuándo usar cada uno
2. 3.3.1 MTM (Methods-Time Measurement)
3. Ejemplo resuelto de MTM-1
4. 3.3.2 MODAPTS
5. Actividad en aula: del diagrama bimanual a los TMU
6. Cierre de la sesión
7. Referencias (formato APA)

---

## 0. Definiciones conceptuales clave

**Sistema de tiempos predeterminados.** Técnica que descompone una operación manual en movimientos básicos y asigna a cada uno un tiempo estándar establecido de antemano, según su naturaleza y las condiciones en que se realiza. No requiere cronómetro ni calificación de la actuación.

**MTM (Methods-Time Measurement).** Procedimiento que analiza cualquier operación o método manual con base en los movimientos básicos requeridos para desarrollarla y asigna a cada movimiento un estándar de tiempo predeterminado (Peralta, cap. 3).

**TMU (Time Measurement Unit).** Unidad de tiempo del sistema MTM: 1 TMU = 0.00001 h = 0.0006 min = 0.036 s. *(El PDF imprime «0.006 min» en esa línea; es una errata, porque 0.00001 h × 60 = 0.0006 min.)*

**Movimientos básicos MTM-1.** Alcanzar, mover, girar, aplicar presión, coger, posicionar, desmontar, soltar y manivela, además de los movimientos de ojos y de cuerpo (Figura 3.2 del libro).

**Nivel de control.** Grado de control mental y visual que exige un movimiento (bajo, medio o alto); explica por qué un alcanzar o un mover tiene distintos casos (A, B, C…).

**Tipo de movimiento.** Tipo I: la mano parte y termina en reposo. Tipo II: está en movimiento al principio o al final. Tipo III: en movimiento al principio y al final. Las tablas de la sesión usan el Tipo I.

**Tiempo normal con PTS.** Los TMU de las tablas representan el tiempo de un operario capacitado con ritmo normal y método definido; no incluyen suplementos. Para llegar a un tiempo estándar se agregan los suplementos de la Sesión 5.

**MODAPTS (Modular Arrangement of Predetermined Time Standards).** Sistema de tiempos predeterminados más simple que MTM-1: usa un número reducido de movimientos con valor en unidades MOD.

---

## 1. Bloque 1: los cinco diagramas, cómo se leen y cuándo usar cada uno

En las actividades anteriores se mezclaron los diagramas. Cada uno responde una pregunta distinta sobre el mismo proceso:

| Diagrama | Qué responde | Qué muestra | Símbolos principales |
|---|---|---|---|
| **DOP** (diagrama de operaciones del proceso) | ¿Qué operaciones e inspecciones tiene todo el proceso y cómo entran los materiales? | Visión sinóptica de todo el producto | Operación ○ e inspección □ |
| **Flujo del proceso** | ¿Qué pasa paso a paso en un proceso, con qué distancias y tiempos? | Un solo recorrido con detalle: transportes, demoras y almacenamientos | ○ operación, ⇨ transporte, □ inspección, D demora, ▽ almacenamiento |
| **Recorrido sobre layout** | ¿Por dónde se mueve el material o la persona en la planta? | El mismo flujo dibujado sobre el plano a escala | Los símbolos del flujo, numerados igual |
| **Hombre-máquina** | ¿Quién espera a quién y cuánto tiempo? | Escala de tiempo con una columna para el operario y otra para la máquina | Barras de trabajo, trabajo combinado y ocioso |
| **Bimanual** | ¿Qué hace cada mano y dónde hay desequilibrio? | Mano izquierda y mano derecha, un renglón por movimiento | ○ operación, ⇨ transporte, D espera, ▽ sostener |

**Cómo elegir (preguntas rápidas):**

- Quiero ver **todo el proceso de un vistazo** → DOP.
- Quiero detectar **demoras, almacenamientos y transportes** de un proceso → flujo del proceso.
- Quiero reducir **metros recorridos y cruces** → recorrido sobre layout.
- La **máquina o el operario esperan** → hombre-máquina; el número de máquinas por operario sale de n = (t + w) / t, con t el tiempo de la máquina por ciclo y w el del operario.
- Una operación es **manual y repetitiva** y quiero revisar manos y movimientos → bimanual.

**Errores frecuentes:**

1. Poner transportes y demoras en el DOP (el DOP solo lleva operaciones e inspecciones).
2. Dibujar el recorrido sin escala o sin numerar los símbolos como en el diagrama de flujo.
3. En el hombre-máquina, no cerrar el ciclo: la suma de las barras de cada columna debe igualar el tiempo del ciclo.
4. En el bimanual, dejar a una mano «sosteniendo» todo el ciclo sin cuestionarlo: sostener es una oportunidad de mejora, no una actividad productiva.
5. Mezclar unidades (segundos con minutos) en la misma tabla.

**Rotafolios para la pared (90 × 60 cm):** un rotafolio por diagrama con un ejemplo anotado, los elementos que debe llevar, la simbología y cómo se lee. Orden sugerido: DOP → flujo → recorrido → hombre-máquina → bimanual. Cada alumno pasa sus diagramas definitivos a hoja normalizada A4 o A3 según el formato del curso.

---

## 2. 3.3.1 MTM (Methods-Time Measurement)

### 2.1 Idea central

Un trabajo manual se descompone en movimientos básicos; a cada movimiento, según su distancia, su dificultad y su peso, la tabla le asigna un tiempo en TMU. La suma de los TMU da el tiempo normal del método, aun antes de que el método exista. Por eso sirve para **comparar métodos propuestos sin cronometrar**.

### 2.2 Los movimientos básicos y su notación

| Movimiento | Símbolo | Qué es | Qué define el tiempo |
|---|---|---|---|
| **Alcanzar** | R o AL | Mover la mano o los dedos a un destino | Distancia (cm) y caso (A, B, C o D, E) |
| **Mover** | M | Trasladar un objeto a un lugar | Distancia, caso (A, B, C) y peso |
| **Coger** | G | Asegurar el control de un objeto | Caso (1A, 1B, 1C, 2, 3, 4, 5) |
| **Posicionar** | P | Alinear, orientar y encajar | Clase de ajuste, simetría y facilidad de manejo |
| **Soltar** | RL | Dejar el control del objeto | RL1 normal, RL2 al contacto |
| **Girar** | T | Girar la mano sobre el eje del antebrazo | Grados y peso |
| **Aplicar presión** | AP | Fuerza muscular para vencer una resistencia | Caso A o B |
| **Desmontar** | D | Separar partes con una separación repentina | Clase de ajuste y facilidad |
| **Manivela** | C | Movimiento circular con la mano | Número de revoluciones |

**Claves como en el libro:** R35B = alcanzar 35 cm, caso B · M20B = mover 20 cm, caso B · G1A = coger, caso 1A · P1SE = posicionar con ajuste holgado (clase 1), simétrico (S), fácil de manejar (E) · RL1 = soltar normal · T90S = girar 90°, peso pequeño.

### 2.3 Los casos de alcanzar y mover

| Caso | Alcanzar | Mover |
|---|---|---|
| **A** | A un objeto en ubicación fija, en la otra mano o sobre el que descansa la otra mano | Objeto a la otra mano o contra un tope |
| **B** | A un solo objeto cuya ubicación puede variar poco de ciclo a ciclo | Objeto a una posición aproximada o indefinida (el caso más frecuente) |
| **C** | A un objeto mezclado con otros: hay que buscar y seleccionar | Objeto a una posición exacta |
| **D** | A un objeto muy pequeño o que se debe asir con precisión | — |
| **E** | A una ubicación indefinida (poner la mano en posición para el siguiente movimiento) | — |

### 2.4 Valores de tabla que se usan en la sesión (TMU, Tipo I)

| Distancia (cm) | Alcanzar A | Alcanzar B | Alcanzar C o D | Alcanzar E | Mover A | Mover B | Mover C |
|---|---|---|---|---|---|---|---|
| 20 | 7.8 | 10.0 | 11.4 | 9.2 | 9.6 | 10.5 | 11.7 |
| 24 | 8.5 | 11.1 | 12.5 | 10.2 | 10.8 | 11.8 | 13.0 |
| 30 | 9.5 | 12.8 | 14.1 | 11.7 | 12.7 | 13.3 | 15.1 |
| 35 | 10.4 | 14.2 | 15.5 | 12.9 | 14.3 | 14.5 | 16.8 |
| 40 | 11.3 | 15.6 | 16.8 | 14.1 | 15.8 | 15.6 | 18.5 |

**Coger (Tabla 3.4):** 1A = 2.0 (objeto pequeño, mediano o grande, fácil de tomar) · 1B = 3.5 (muy pequeño o sobre una superficie plana) · 1C1 = 7.3 · 1C2 = 8.7 · 1C3 = 10.8 (con interferencia en el fondo o a un lado) · 2 = 5.6 (volver a coger) · 3 = 5.6 (coger para trasladar) · 4A = 7.3 · 4B = 9.1 · 4C = 12.9 (objeto mezclado con otros) · 5 = 0 (al contacto, deslizamiento o gancho).

**Posicionar con introducción (tabla P, columna izquierda):** la clave se arma con la clase de ajuste, la simetría y el manejo (P1S con manejo difícil = P1SD).


| Clase de ajuste | Simetría | Manejo fácil | Manejo difícil |
|---|---|---|---|
| 1 Holgado (sin presión) | S | 5.6 | 11.2 |
| | SS | 9.1 | 14.7 |
| | NS | 10.4 | 16.0 |
| 2 Estrecho (presión ligera) | S | 16.2 | 21.8 |
| | SS | 19.7 | 25.3 |
| | NS | 21.0 | 26.6 |
| 3 Exacto (presión intensa) | S | 43.0 | 48.6 |
| | SS | 46.5 | 52.1 |
| | NS | 47.8 | 53.4 |

**Posicionar sin introducción (tabla de tolerancia de la tabla v3):** si no hay encaje, no se busca en la tabla de posición, sino por la tolerancia: T mayor que ±12 mm = solo un Mover B; ±6 mm < T ≤ ±12 mm = Mover C; ±1.5 mm < T ≤ ±6 mm = Mover C + P1; T ≤ ±1.5 mm = Mover C + P2. Así, orientar un zapato con tolerancia de ±10 mm es un Mover C y no un posicionar aparte.

**Soltar (Tabla 3.6):** RL1 = 2.0 · RL2 = 0 (al contacto). **Girar (Tabla 3.3), peso pequeño (0 a 1 kg):** 30° = 2.8 · 45° = 3.5 · 60° = 4.1 · 75° = 4.8 · 90° = 5.4 · 120° = 6.8 · 180° = 9.4 TMU.

### 2.5 Peso en el mover

Para un peso neto efectivo (PNE) de 1 kg o menos, el factor es 1.00 y la constante 0.0 TMU: el valor de tabla no cambia. Para pesos mayores, la tabla de mover da un factor y una constante por rango de peso: hasta 2 kg → 1.04 y 1.6 TMU; hasta 4 kg → 1.07 y 2.8; hasta 6 kg → 1.12 y 4.3; hasta 8 kg → 1.17 y 5.8; hasta 10 kg → 1.22 y 7.3. **TMU del mover = valor de tabla × factor + constante.**

### 2.6 Movimientos simultáneos (tabla de la tarjeta MTM-1 v3)

Cuando las dos manos trabajan a la vez, la tabla de **movimientos simultáneos** dice si dos movimientos se pueden hacer juntos. Los renglones son el movimiento de una mano y las columnas el de la otra (es un triángulo: cada par tiene una sola celda). Los colores significan:

- **Blanco:** fácil de realizar simultáneamente. Cuenta la mano que más tarda; el menor tiempo se encierra en un círculo y no se suma.
- **Amarillo:** puede realizarse simultáneamente con práctica. Se trata igual que el blanco.
- **Gris:** difícil de ejecutar incluso con experiencia. Los tiempos **no** se traslapan: se suman.

Las letras **W** y **O** indican si el movimiento está dentro o fuera del área de visión normal; **E** y **D**, si el posicionar es fácil o difícil de manejar. Ejemplos de la actividad: alcanzar B con alcanzar B es blanco; coger G1A con G1B es blanco; mover B con mover C es blanco; posicionar P1NS con posicionar P1S es **gris**, por lo que no se hacen a la vez. «Sostener» no es un movimiento MTM: la mano que solo sostiene no tiene tiempo propio.

### 2.7 Pasos para aplicar MTM-1

1. Describir el método elemento por elemento y por mano (se puede partir de un diagrama bimanual).
2. Identificar el movimiento básico de cada descripción.
3. Determinar sus variables: distancia, caso o nivel de control, peso, ajuste, simetría y manejo.
4. Buscar el TMU en la tabla correspondiente.
5. Revisar en la tabla de simultáneos cada par de movimientos de las dos manos y, por elemento, tomar el tiempo de la mano que más tarda (blanco o amarillo) o sumar ambos (gris).
6. Convertir: TMU × 0.036 = segundos; TMU × 0.0006 = minutos.
7. Para un tiempo estándar, aplicar los suplementos.

---

## 3. Ejemplo resuelto de MTM-1

**Operación (datos ficticios):** empacar una pieza de 0.8 kg. La operaria alcanza la pieza en una charola a 30 cm (un solo objeto en lugar casi fijo), la toma (objeto mediano, fácil de tomar), la lleva 40 cm a la caja (posición aproximada) y la suelta abriendo los dedos. Tipo I, ritmo normal.

| Elemento | Clave | Cómo se obtiene | TMU |
|---|---|---|---|
| Alcanzar la pieza | R30B | Caso B, 30 cm | 12.8 |
| Tomar la pieza | G1A | Objeto fácil de tomar | 2.0 |
| Llevar la pieza a la caja | M40B | Caso B, 40 cm; 0.8 kg ≤ 1 kg, factor 1.00 | 15.6 |
| Soltar | RL1 | Soltar normal | 2.0 |
| **Total** | | | **32.4** |

**Conversión:** 32.4 TMU × 0.036 = **1.166 s** por pieza; en minutos, 32.4 × 0.0006 = 0.0194 min.

**Con una pieza de 3 kg:** el mover cae en el rango «hasta 4 kg» (factor 1.07, constante 2.8): 15.6 × 1.07 + 2.8 = 19.5 TMU, en lugar de 15.6; el total pasa a 36.3 TMU. Ese es el efecto del peso sobre el tiempo.

**Comparación de dos métodos (mismo caso):** si la charola se acerca a 20 cm y la caja a 20 cm, R20B = 10.0 y M20B = 10.5 (factor 1.00): 10.0 + 2.0 + 10.5 + 2.0 = 24.5 TMU = 0.882 s. El ahorro es de 7.9 TMU (24.4%) por pieza, calculado sin cronometrar nada y antes de mover la charola.

---

## 4. 3.3.2 MODAPTS

**Qué es.** Sistema de tiempos predeterminados desarrollado por Chris Heyde (1966) que simplifica el análisis: en lugar de buscar valores en tablas por distancia y caso, se asigna un número entero de **MOD** a cada movimiento según la parte del cuerpo que lo ejecuta. Un MOD equivale a 0.129 s (aproximadamente 3.6 TMU).

**Movimientos principales (conocimiento general; verificar con el material del curso):**

| Clase | Clave | Significado | MOD |
|---|---|---|---|
| Movimientos | M1 | Dedos | 1 |
| | M2 | Mano | 2 |
| | M3 | Antebrazo | 3 |
| | M4 | Brazo completo | 4 |
| | M5 | Brazo extendido con movimiento del tronco | 5 |
| Coger | G0 | Al contacto | 0 |
| | G1 | Coger fácil | 1 |
| | G3 | Coger con atención o interferencia | 3 |
| Poner | P0 | Poner sin cuidado | 0 |
| | P2 | Poner con cuidado | 2 |
| | P5 | Poner con cuidado y dificultad | 5 |

**Fórmula:** tiempo = MOD totales × 0.129 s. Un movimiento típico se escribe como un patrón «mover – coger – mover – poner», por ejemplo **M4 G1 M4 P0** = 4 + 1 + 4 + 0 = 9 MOD = 1.161 s.

**MTM-1 frente a MODAPTS (aplicado al ejemplo anterior):** alcanzar 30 cm, coger una pieza fácil y llevarla 30 cm es aproximadamente M4 G1 M4 (9 MOD = 1.16 s, unos 32 TMU), frente a 28.1 TMU en MTM-1 (R30B + G1A + M30B). Los resultados son del mismo orden; MODAPTS sacrifica precisión por rapidez de análisis.

| Aspecto | MTM-1 | MODAPTS |
|---|---|---|
| Unidad | TMU (0.036 s) | MOD (0.129 s) |
| Base | Tablas por distancia, caso, peso y ajuste | Parte del cuerpo y clase de movimiento |
| Detalle | Alto | Medio |
| Velocidad de análisis | Lenta | Rápida |
| Uso típico | Estudios precisos en operaciones de ciclo corto y gran volumen | Estimaciones rápidas, evaluación de alternativas de método |

---

## 5. Actividad en aula: del diagrama bimanual a las UMT

**Modalidad:** por equipo (3–4 integrantes), 30 minutos, con el formato de la sesión (Variante A para equipos impares, B para pares) y la **Tabla MTM-1 v3** impresa o en el celular.

**Caso:** Zapatería Industrial XYZ, estación Acabados, acordonado de un zapato. Se parte del diagrama bimanual de la Sesión 4 y se asigna tiempo a seis elementos: alcanzar, coger, llevar al frente, posicionar el cordón en el ojillo, llevar a terminados y soltar.

**Qué hacen los equipos:**

1. **Método actual:** identifican el movimiento de cada mano, buscan su valor en la tabla, consultan en la tabla de simultáneos el color de la combinación y toman lo que cuenta en cada elemento.
2. **Método propuesto:** acercan las bandejas, agregan una guía que orienta el zapato (el mover pasa de caso C a caso B) y sustituyen la caja por un dispensador de cordones con herrete rígido; recalculan los elementos que cambian.
3. **Conversión y comparación:** suman, convierten a segundos y calculan el ahorro por zapato y por jornada (240 zapatos al día).
4. **Análisis:** colores de la tabla de simultáneos y mano que gobierna; por qué la mano izquierda solo sostiene (posicionar con posicionar es gris) y por qué «sostener» no tiene UMT; si el ahorro justifica el cambio y dónde buscar el siguiente; por qué MTM da menos que el cronómetro.

**Entrega:** hoja subida al **Foro 06 — Evidencia: Tiempos predeterminados (MTM, MODAPTS)** al terminar la clase.

---

## 6. Cierre de la sesión

- Un sistema de tiempos predeterminados permite **evaluar un método antes de implantarlo**, sin cronómetro y sin calificar el ritmo.
- Los TMU son tiempo normal; para obtener un tiempo estándar falta aplicar suplementos.
- MTM-1 es preciso pero lento de aplicar; MODAPTS es más rápido y menos preciso.
- Un ahorro de décimas de segundo por ciclo puede ser pequeño por jornada: conviene atacar primero los elementos que dominan el ciclo.
- La Semana 7 continúa con 3.3.3 Técnica MOT y 3.4 Muestreo del trabajo; la Actividad 3 (foro colaborativo sobre proyecto de estudio de tiempos) vence el 27 de octubre.

---

## 7. Referencias (formato APA)

MTM Ingenieros. (2013). *Tabla MTM-1* (versión 3) [Tabla de referencia, MR001V3]. www.mtmingenieros.com

Niebel, B. W., & Freivalds, A. (2009). *Ingeniería industrial: Métodos, estándares y diseño del trabajo* (12.ª ed.). McGraw-Hill Interamericana.

Peralta, J. (s. f.). *Estudio del trabajo: Una nueva visión* (cap. 3, Medición del método de trabajo). Grupo Editorial Patria. *(Año de edición por confirmar con la portada del libro.)*
