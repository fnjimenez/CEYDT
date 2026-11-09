<h1 id="estudio-y-diseño-de-trabajo-—-contenido-temático-de-la-sesión-10-semana-10">Estudio y Diseño de Trabajo — Contenido temático de la Sesión 10 (Semana 10)</h1>
<p><strong>Tema (programa oficial, Unidad V: Diagnóstico y mejoramiento de procesos):</strong> 5.1 Tipos de distribución de planta según el producto y proceso; 5.2 Diagrama de hilos y diagrama de precedencia; 5.3 Técnicas de distribución de áreas; 5.4 Costos y tarifas de operaciones<br>
<strong>Fecha:</strong> 11 al 17 de noviembre de 2026 (sesión presencial: sábado 14 de noviembre)<br>
<strong>Actividades de la semana:</strong> Revisión de contenido en plataforma, asesoría presencial, Foro 10 (que enlaza las semanas 9 y 10) y cierre de la <strong>Actividad 4: Balanceo de línea</strong> (integrador, 10 puntos, individual).<br>
<strong>Propósito de la sesión:</strong> Que el estudiante (1) complete los cálculos de balanceo que pide la Actividad 4 —tiempo disponible con receso, ciclo, estaciones, tiempo de reubicación, cinta transportadora, operarios y eficiencia—; (2) use el <strong>diagrama de precedencia</strong> y el <strong>diagrama de hilos</strong> como herramientas de diagnóstico; (3) relacione el balanceo con la <strong>distribución de planta</strong> y con el <strong>costo de operación</strong>; y (4) resuelva sus propios ejercicios con un <strong>cuaderno de Python en Google Colab</strong>.</p>
<blockquote>
<p><strong>Uso de este documento.</strong> Es el material explicativo de la semana: lectura previa, guía de exposición y manual del cuaderno de Python. Todos los datos de los ejemplos son <strong>didácticos</strong>. Los ejercicios con matrícula son individuales: cada estudiante tiene valores distintos.</p>
</blockquote>
<blockquote>
<p><strong>Continuidad.</strong> Este documento continúa la Sesión 9 (peso posicional, Kilbridge &amp; Wester y dos modelos). Si necesitas repasar esos métodos, vuelve a esa sesión; aquí solo se citan.</p>
</blockquote>
<hr>
<h2 id="índice">Índice</h2>
<ol>
<li>Teoría: lo que falta del balanceo y lo que sigue en la Unidad 5</li>
<li>Fórmulas (hoja de consulta)</li>
<li>Ejemplo resuelto 1: línea con receso y tiempo de reubicación</li>
<li>Ejemplo resuelto 2: cinta transportadora y número de operarios</li>
<li>Ejemplo resuelto 3: peso posicional contra Kilbridge &amp; Wester</li>
<li>Ejemplo resuelto 4: dos modelos</li>
<li>Por qué usar Python</li>
<li>Explicación de las librerías</li>
<li>Explicación del script</li>
<li>Cómo usar el cuaderno</li>
<li>Distribución de planta, diagramas y costos (5.1 a 5.4)</li>
<li>Errores frecuentes</li>
<li>Cómo se conecta con la Actividad 4 y el Foro 10</li>
<li>Cierre de la sesión</li>
<li>Referencias (formato APA)</li>
</ol>
<hr>
<h2 id="teoría-lo-que-falta-del-balanceo-y-lo-que-sigue-en-la-unidad-5">1. Teoría: lo que falta del balanceo y lo que sigue en la Unidad 5</h2>
<h3 id="tiempo-disponible-real">1.1 Tiempo disponible real</h3>
<p>La jornada no se trabaja completa. Antes de calcular el ciclo se descuentan los tiempos que la línea <strong>no produce</strong>: receso o comida, arranque, limpieza, paros programados. Si olvidas este paso, el ciclo sale más grande de lo real y la línea no alcanza la demanda.</p>
<p>Cuando el problema da una <strong>eficiencia operativa</strong> (por ejemplo 88 %), significa que, de las horas disponibles, solo esa proporción se convierte en tiempo productivo; el resto se pierde en ajustes, esperas y pequeños paros. En ese caso el tiempo útil es el tiempo disponible multiplicado por esa eficiencia.</p>
<h3 id="de-demanda-anual-a-demanda-diaria">1.2 De demanda anual a demanda diaria</h3>
<p>Cuando el dato viene por año, se convierte:</p>
<ol>
<li>Se calculan los <strong>días laborables al año</strong> = semanas por año × días por semana.</li>
<li>La <strong>demanda diaria</strong> es la demanda anual entre esos días.</li>
<li>Con la demanda diaria y el tiempo útil del día se obtiene el ciclo.</li>
</ol>
<h3 id="tiempo-de-reubicación-entre-tareas">1.3 Tiempo de reubicación entre tareas</h3>
<p>A veces cambiar de una tarea a otra dentro de la misma estación cuesta tiempo (tomar otra herramienta, mover la pieza, cambiar de posición). Ese tiempo se llama aquí <strong>tiempo de reubicación</strong>. En este material se maneja así:</p>
<ul>
<li>La <strong>carga de una estación</strong> es la suma de los tiempos de sus tareas <strong>más</strong> la reubicación por cada cambio de tarea.</li>
<li>Una estación con <em>k</em> tareas tiene <em>k − 1</em> cambios; por lo tanto: carga = Σ t + (k − 1) × r.</li>
<li>La carga de la estación debe ser <strong>menor o igual</strong> que el ciclo.</li>
<li>La <strong>eficiencia</strong> se calcula con el tiempo productivo (Σ t), no con la reubicación, porque la reubicación es un desperdicio que el balanceo busca reducir.</li>
</ul>
<blockquote>
<p><strong>Nota.</strong> Algunos libros tratan la reubicación como tiempo que se suma a cada tarea o a cada estación. Si tu docente o tu libro usa otra convención, <strong>declara cuál usaste</strong> en tu PDF; lo importante es que sea coherente en todo el ejercicio.</p>
</blockquote>
<h3 id="cinta-transportadora-de-avance-constante">1.4 Cinta transportadora de avance constante</h3>
<p>En una cinta transportadora las unidades avanzan a velocidad constante frente a las estaciones, que están <strong>en serie</strong>. Dos ideas nuevas:</p>
<ul>
<li><strong>Operarios por estación.</strong> Si el trabajo total por unidad es mucho mayor que el ciclo, se necesitan muchos operarios. Pueden repartirse en muchas estaciones de un operario o en menos estaciones con varios operarios cada una. El <strong>número ideal de operarios</strong> es el mismo en ambos casos: Σ t ÷ c, redondeado hacia arriba.</li>
<li><strong>Traslado entre estaciones.</strong> Es el tiempo que la unidad tarda en moverse de una estación a la siguiente. <strong>No entra al ciclo</strong> (el ciclo lo marca la demanda); entra en el <strong>tiempo de recorrido</strong> de la unidad por la línea y en el <strong>inventario en proceso</strong>.</li>
</ul>
<p><a href="https://claude.ai/chat/imagenes/Esquema_Cinta_Transportadora.png">Esquema de la cinta transportadora</a></p>
<h3 id="factibilidad-cuando-una-tarea-es-más-larga-que-el-ciclo">1.5 Factibilidad: cuando una tarea es más larga que el ciclo</h3>
<p>Si la tarea más larga dura más que el ciclo, <strong>una sola persona por estación no puede cumplir la demanda</strong>. Opciones:</p>
<ol>
<li>Duplicar la estación de esa tarea (estaciones en paralelo).</li>
<li>Dividir la tarea en elementos más pequeños (si el método lo permite).</li>
<li>Revisar los datos: ¿están en las mismas unidades?, ¿la demanda es la correcta?</li>
<li>Reducir la demanda o ampliar el tiempo disponible.</li>
</ol>
<p>Este diagnóstico se escribe <strong>antes</strong> de balancear. Es parte de la rúbrica de la Actividad 4 (aplicación de conceptos).</p>
<h3 id="qué-sigue-en-la-unidad-5">1.6 Qué sigue en la Unidad 5</h3>
<p>El balanceo dice <strong>cuántas estaciones</strong> y <strong>qué tareas</strong> va en cada una. La Unidad 5 pregunta <strong>dónde</strong> va cada estación y <strong>cuánto cuesta</strong> operarla:</p>
<ul>
<li>5.1 Tipos de distribución de planta: por producto, por proceso, de posición fija y celular.</li>
<li>5.2 Diagrama de hilos y diagrama de precedencia: el primero muestra <strong>recorridos</strong> sobre el plano; el segundo muestra <strong>el orden obligatorio</strong> entre tareas.</li>
<li>5.3 Técnicas de distribución de áreas: relación de actividades y diagrama relacional.</li>
<li>5.4 Costos y tarifas de operaciones: cuánto cuesta cada minuto y cada unidad.</li>
</ul>
<p>Los detalles de 5.1 a 5.4 están en la sección 11.</p>
<hr>
<h2 id="fórmulas-hoja-de-consulta">2. Fórmulas (hoja de consulta)</h2>
<p>Todas las fórmulas de la Actividad 4 en un solo lugar. Símbolos: <strong>t</strong> = tiempo de una tarea, <strong>Σt</strong> = suma de tiempos, <strong>c</strong> = tiempo de ciclo, <strong>N</strong> = número de estaciones u operarios.</p>
<h3 id="tiempos-y-ciclo">2.1 Tiempos y ciclo</h3>
<ol>
<li>Tiempo disponible (min) = jornada (h) × 60 − receso (min)</li>
<li>Tiempo útil (min) = tiempo disponible × eficiencia operativa (si el problema da eficiencia operativa)</li>
<li>Ciclo c = tiempo disponible (o útil) ÷ demanda del periodo</li>
<li>Días laborables al año = semanas × días por semana</li>
<li>Demanda diaria = demanda anual ÷ días laborables al año</li>
</ol>
<h3 id="estaciones-y-eficiencia">2.2 Estaciones y eficiencia</h3>
<ol start="6">
<li>Número mínimo de estaciones: N mín. = ⌈ Σt ÷ c ⌉</li>
<li>Condición de factibilidad: t máx. ≤ c</li>
<li>Carga de una estación con reubicación r: carga = Σ t de sus tareas + (k − 1) × r</li>
<li>Eficiencia: E = Σt ÷ (N × c) × 100</li>
<li>Retraso de balanceo = 100 − E</li>
<li>Ocio de una estación = c − carga</li>
<li>Producción real = tiempo disponible ÷ carga mayor (cuello de botella)</li>
</ol>
<h3 id="métodos-de-asignación-de-la-sesión-9">2.3 Métodos de asignación (de la Sesión 9)</h3>
<ol start="13">
<li>Peso posicional de una tarea = su tiempo + los tiempos de <strong>todas</strong> sus tareas sucesoras</li>
<li>Kilbridge &amp; Wester: columna más temprana (nivel) y columna más tardía; prioridad: columna más tardía menor, luego columna más temprana menor, luego tiempo mayor (regla de este curso)</li>
</ol>
<h3 id="varios-modelos">2.4 Varios modelos</h3>
<ol start="15">
<li>Tiempo ponderado de una tarea = (t₁ × d₁ + t₂ × d₂) ÷ (d₁ + d₂)</li>
<li>Ciclo = tiempo disponible ÷ (d₁ + d₂)</li>
<li>Revisión: la carga de cada estación <strong>en cada modelo</strong> no debe rebasar el ciclo, o hay que explicar cómo se absorbe (secuencia, reserva de tiempo, apoyo entre estaciones).</li>
</ol>
<h3 id="cinta-transportadora">2.5 Cinta transportadora</h3>
<ol start="18">
<li>Número ideal de operarios = ⌈ Σt ÷ c ⌉</li>
<li>Si hay <em>k</em> operarios por estación: estaciones = ⌈ operarios ÷ k ⌉</li>
<li>Tiempo de recorrido = (número de estaciones × k × c) + (estaciones − 1) × traslado</li>
<li>Unidades en proceso ≈ tiempo de recorrido ÷ c</li>
</ol>
<h3 id="costos-tema-5.4">2.6 Costos (tema 5.4)</h3>
<ol start="22">
<li>Costo de mano de obra por unidad = (N × tarifa por hora × c) ÷ 60 (c en minutos)</li>
<li>Costo del ocio por unidad = (N × c − Σt) × tarifa por hora ÷ 60 (en minutos)</li>
<li>Ahorro por mejora = costo anterior − costo nuevo</li>
</ol>
<hr>
<h2 id="ejemplo-resuelto-1-línea-con-receso-y-tiempo-de-reubicación">3. Ejemplo resuelto 1: línea con receso y tiempo de reubicación</h2>
<p><strong>Datos (tomados de la estructura del Ejercicio 1 de la Actividad 4).</strong> Componente electrónico. Jornada de 7.5 h con receso de 15 min. Tareas (min, precedencia): A 6 (—); B 2 (A); C 5 (A); D 4 (B); E 3 (B); F 2 ©; G 5 (D, E, F); H 3 (G). Reubicación entre tareas de una estación: 1 min.</p>
<blockquote>
<p><strong>Aviso sobre la demanda.</strong> El enunciado de la plataforma indica <strong>480 unidades diarias</strong>. Con ese valor el ciclo sale en 0.906 min y la tarea A (6 min) lo rebasa: la línea es <strong>infactible con un operario por estación</strong> (se necesitarían ⌈30 ÷ 0.906⌉ = 34 puestos trabajando en paralelo). Para mostrar el método completo se resuelve aquí con <strong>48 unidades diarias</strong>, que es el valor con el que el problema queda balanceable. Consulta con el docente cuál es el dato vigente para tu entrega; tu ejercicio personalizado del cuaderno ya viene con datos factibles.</p>
</blockquote>
<p><a href="https://claude.ai/chat/imagenes/Diagrama_Precedencia_Ejercicio1.png">Diagrama de precedencia del Ejercicio 1</a></p>
<h3 id="paso-1.-tiempo-disponible-y-ciclo">Paso 1. Tiempo disponible y ciclo</h3>
<ul>
<li>Tiempo disponible = 7.5 × 60 − 15 = <strong>435 min</strong></li>
<li>Ciclo c = 435 ÷ 48 = <strong>9.0625 min/unidad</strong></li>
<li>Σt = 6 + 2 + 5 + 4 + 3 + 2 + 5 + 3 = <strong>30 min</strong></li>
<li>Tarea más larga: 6 min ≤ 9.0625 → <strong>factible</strong></li>
</ul>
<h3 id="paso-2.-número-mínimo-de-estaciones">Paso 2. Número mínimo de estaciones</h3>
<p>N mín. = ⌈30 ÷ 9.0625⌉ = ⌈3.31⌉ = <strong>4 estaciones</strong></p>
<h3 id="paso-3.-pesos-posicionales">Paso 3. Pesos posicionales</h3>
<p>Peso = tiempo + todos los sucesores:</p>
<ul>
<li>A = 6 + (B 2 + C 5 + D 4 + E 3 + F 2 + G 5 + H 3) = <strong>30</strong></li>
<li>B = 2 + (D 4 + E 3 + G 5 + H 3) = <strong>17</strong></li>
<li>C = 5 + (F 2 + G 5 + H 3) = <strong>15</strong></li>
<li>D = 4 + (G 5 + H 3) = <strong>12</strong></li>
<li>E = 3 + (G 5 + H 3) = <strong>11</strong></li>
<li>F = 2 + (G 5 + H 3) = <strong>10</strong></li>
<li>G = 5 + 3 = <strong>8</strong></li>
<li>H = <strong>3</strong></li>
</ul>
<p>Lista de prioridad: A, B, C, D, E, F, G, H.</p>
<h3 id="paso-4.-asignación-carga-con-reubicación-≤-9.0625">Paso 4. Asignación (carga con reubicación ≤ 9.0625)</h3>
<ul>
<li><strong>Estación 1:</strong> A (6). Se agrega B: 6 + 2 + 1 = 9 ≤ 9.0625. Ya no cabe C (9 + 1 + 5 = 15). Carga <strong>9</strong>.</li>
<li><strong>Estación 2:</strong> C (5). D no cabe (5 + 1 + 4 = 10); E sí (5 + 1 + 3 = 9). Carga <strong>9</strong>.</li>
<li><strong>Estación 3:</strong> D (4). Se agrega F: 4 + 1 + 2 = 7. G exige que D, E y F estén hechos y ya lo están, pero no cabe (7 + 1 + 5 = 13). Carga <strong>7</strong>.</li>
<li><strong>Estación 4:</strong> G (5) + H (3) + 1 = <strong>9</strong>.</li>
</ul>
<p><a href="https://claude.ai/chat/imagenes/Carga_Estaciones_Ejercicio1.png">Carga por estación</a></p>
<h3 id="paso-5.-eficiencia-y-producción">Paso 5. Eficiencia y producción</h3>
<ul>
<li>E = 30 ÷ (4 × 9.0625) × 100 = <strong>82.8 %</strong></li>
<li>Retraso de balanceo = <strong>17.2 %</strong></li>
<li>Cuello de botella = 9 min → producción real = 435 ÷ 9 = 48.3 → <strong>48 unidades</strong>: se cumple la demanda sin holgura.</li>
</ul>
<h3 id="lectura-para-el-análisis-base-de-las-tres-mejoras">Lectura para el análisis (base de las tres mejoras)</h3>
<ul>
<li>La estación 3 trabaja 7 min y descansa 2.06 min por ciclo: ahí hay ocio concentrado.</li>
<li>Las reubicaciones suman 4 min por ciclo (una por cada estación con dos tareas): reducirlas a la mitad mejora el margen.</li>
<li>El ciclo tiene apenas 0.06 min de holgura sobre el cuello de botella: cualquier aumento de demanda rompe el balance.</li>
</ul>
<p>Estas observaciones se convierten en mejoras <strong>cuantificadas</strong>. Ejemplo: si la demanda subiera de 48 a 56 unidades diarias, el ciclo baja a 7.77 min; con 1 min de reubicación se necesitan <strong>6 estaciones (eficiencia 64.4 %)</strong>, pero si una charola de herramientas baja la reubicación a 0.5 min, bastan <strong>5 estaciones (eficiencia 77.2 %)</strong>. Así se escribe una mejora: cambio concreto, efecto calculado y condición.</p>
<hr>
<h2 id="ejemplo-resuelto-2-cinta-transportadora-y-número-de-operarios">4. Ejemplo resuelto 2: cinta transportadora y número de operarios</h2>
<p><strong>Datos (estructura del Ejercicio 2 de la Actividad 4).</strong> Demanda anual 120,000 unidades. Cinta de avance constante con estaciones en serie. Tiempo total de ensamblaje 66 min/unidad. 48 semanas/año, 6 días/semana, 7 h efectivas/día. Eficiencia operativa 88 %. Traslado entre estaciones 2 min.</p>
<h3 id="paso-1.-demanda-diaria">Paso 1. Demanda diaria</h3>
<ul>
<li>Días laborables al año = 48 × 6 = <strong>288</strong></li>
<li>Demanda diaria = 120,000 ÷ 288 = <strong>416.67 unidades/día</strong></li>
</ul>
<h3 id="paso-2.-tiempo-útil-y-ciclo">Paso 2. Tiempo útil y ciclo</h3>
<ul>
<li>Tiempo disponible = 7 × 60 = 420 min/día</li>
<li>Tiempo útil = 420 × 0.88 = <strong>369.6 min/día</strong></li>
<li>Ciclo c = 369.6 ÷ 416.67 = <strong>0.887 min/unidad</strong> (53.2 segundos)</li>
</ul>
<h3 id="paso-3.-operarios-y-estaciones">Paso 3. Operarios y estaciones</h3>
<ul>
<li>Operarios ideales = ⌈66 ÷ 0.887⌉ = ⌈74.4⌉ = <strong>75 operarios</strong></li>
<li>Si hay <strong>1 operario por estación:</strong> 75 estaciones.</li>
<li>Si hay <strong>3 operarios por estación:</strong> 25 estaciones (75 operarios).</li>
<li>Si hay <strong>5 operarios por estación:</strong> 15 estaciones (75 operarios).</li>
</ul>
<p><strong>Respuesta a las dos preguntas del ejercicio:</strong> el número ideal de operarios es 75; el mínimo de estaciones depende de cuántos operarios se asignen a cada una. Con una persona por estación, el mínimo es 75; si la planta permite equipos de 5, el mínimo es 15. <strong>Declara en tu PDF qué configuración elegiste y por qué.</strong></p>
<h3 id="paso-4.-tiempo-de-recorrido-con-traslado-de-2-min">Paso 4. Tiempo de recorrido (con traslado de 2 min)</h3>
<p>Con 75 estaciones de un operario: recorrido = 75 × 0.887 + 74 × 2 = <strong>214.5 min</strong>, y unidades en proceso ≈ 214.5 ÷ 0.887 = <strong>242 unidades</strong> sobre la cinta.</p>
<h3 id="lectura-para-el-análisis">Lectura para el análisis</h3>
<ul>
<li>El traslado pesa más que el trabajo: 148 de 214.5 min son transporte. Reducir estaciones (equipos de varios operarios) recorta el recorrido.</li>
<li>Con eficiencia operativa de 88 %, cada punto ganado reduce el ciclo y los operarios necesarios. Con 92 %, el ciclo sube a 0.927 min y N baja a 72.</li>
<li>El inventario en proceso (242 unidades) es capital inmovilizado: acortar el recorrido lo reduce.</li>
</ul>
<hr>
<h2 id="ejemplo-resuelto-3-peso-posicional-contra-kilbridge--wester">5. Ejemplo resuelto 3: peso posicional contra Kilbridge &amp; Wester</h2>
<p><strong>Datos (didácticos, distintos a los de la Sesión 9).</strong> Línea de ensamble con 11 tareas. Jornada de 8 h con receso de 30 min; demanda de 390 unidades por día. Tiempos en <strong>segundos</strong>. Precedencias: A (—, 20 s); B (—, 15 s); C (A, 45 s); D (A, B, 30 s); E (C, 20 s); F (D, 15 s); G (C, D, 50 s); H (E, G, 10 s); I (F, 55 s); J (H, I, 40 s); K (J, 45 s).</p>
<h3 id="paso-1.-ciclo-y-estaciones-mínimas">Paso 1. Ciclo y estaciones mínimas</h3>
<ul>
<li>Tiempo disponible = 8 × 3600 − 30 × 60 = <strong>27,000 s</strong></li>
<li>Ciclo c = 27,000 ÷ 390 = <strong>69.23 s</strong></li>
<li>Σt = 20 + 15 + 45 + 30 + 20 + 15 + 50 + 10 + 55 + 40 + 45 = <strong>345 s</strong></li>
<li>Tarea más larga: 55 s ≤ 69.23 → <strong>factible</strong></li>
<li>N mín. = ⌈345 ÷ 69.23⌉ = ⌈4.98⌉ = <strong>5 estaciones</strong></li>
</ul>
<h3 id="paso-2.-peso-posicional">Paso 2. Peso posicional</h3>
<p>Peso = tiempo + todos los sucesores:</p>
<ul>
<li>A = 20 + C, D, E, F, G, H, I, J, K = <strong>330</strong></li>
<li>B = 15 + D, F, G, H, I, J, K = <strong>260</strong></li>
<li>D = 30 + F, G, H, I, J, K = <strong>245</strong></li>
<li>C = 45 + E, G, H, J, K = <strong>210</strong></li>
<li>F = 15 + I, J, K = <strong>155</strong></li>
<li>G = 50 + H, J, K = <strong>145</strong></li>
<li>I = 55 + J, K = <strong>140</strong></li>
<li>E = 20 + H, J, K = <strong>115</strong></li>
<li>H = 10 + J, K = <strong>95</strong></li>
<li>J = 40 + K = <strong>85</strong></li>
<li>K = <strong>45</strong></li>
</ul>
<p>Lista de prioridad: A, B, D, C, F, G, I, E, H, J, K.</p>
<h3 id="paso-3.-asignación-por-peso-posicional-carga-≤-69.23-s">Paso 3. Asignación por peso posicional (carga ≤ 69.23 s)</h3>
<ul>
<li><strong>Estación 1:</strong> A (20) + B (15) + D (30) = <strong>65</strong>. C ya no cabe (65 + 45).</li>
<li><strong>Estación 2:</strong> C (45) + F (15) = <strong>60</strong>. G (50), I (55) y E (20) no caben.</li>
<li><strong>Estación 3:</strong> G (50) = <strong>50</strong>. E (20) rebasa: 50 + 20 = 70 &gt; 69.23; I (55) no cabe.</li>
<li><strong>Estación 4:</strong> I (55) = <strong>55</strong>. E (20) rebasa: 75.</li>
<li><strong>Estación 5:</strong> E (20) + H (10) = <strong>30</strong>. J (40) rebasa: 70 &gt; 69.23.</li>
<li><strong>Estación 6:</strong> J (40) = <strong>40</strong>. K (45) rebasa.</li>
<li><strong>Estación 7:</strong> K (45) = <strong>45</strong>.</li>
</ul>
<p><strong>Resultado:</strong> 7 estaciones; eficiencia = 345 ÷ (7 × 69.23) × 100 = <strong>71.2 %</strong>; retraso de balanceo = 28.8 %. El método dejó dos estaciones muy cargadas y varias con mucho ocio (la 5 descansa 39.2 s por ciclo).</p>
<h3 id="paso-4.-kilbridge--wester-columnas">Paso 4. Kilbridge &amp; Wester: columnas</h3>
<p>Columna más temprana (nivel) de cada tarea: A y B = 1; C y D = 2; E, F y G = 3; H e I = 4; J = 5; K = 6. En esta red <strong>no hay tareas flotantes</strong>: la columna más tardía coincide con la más temprana para todas.</p>
<p>Regla de prioridad (la del curso): menor columna más tardía; si empatan, menor columna más temprana; si empatan, mayor tiempo.</p>
<h3 id="paso-5.-asignación-por-kilbridge--wester">Paso 5. Asignación por Kilbridge &amp; Wester</h3>
<ul>
<li><strong>Estación 1:</strong> A (20) + B (15) + D (30) = <strong>65</strong>.</li>
<li><strong>Estación 2:</strong> C (45). En la columna 3 el de mayor tiempo que cabe es E (20): 65. G (50) no cabe. <strong>65</strong>.</li>
<li><strong>Estación 3:</strong> G (50) + F (15) = <strong>65</strong>.</li>
<li><strong>Estación 4:</strong> I (55) + H (10) = <strong>65</strong>.</li>
<li><strong>Estación 5:</strong> J (40) = <strong>40</strong>.</li>
<li><strong>Estación 6:</strong> K (45) = <strong>45</strong>.</li>
</ul>
<p><strong>Resultado:</strong> 6 estaciones; eficiencia = 345 ÷ (6 × 69.23) × 100 = <strong>83.1 %</strong>; retraso = 16.9 %.</p>
<h3 id="paso-6.-comparación-y-recomendación">Paso 6. Comparación y recomendación</h3>
<ul>
<li><strong>Estaciones:</strong> 7 con peso posicional y 6 con Kilbridge &amp; Wester (el mínimo teórico es 5).</li>
<li><strong>Eficiencia:</strong> 71.2 % contra 83.1 %.</li>
<li><strong>Cuello de botella:</strong> 65 s en ambos; la producción real es 27,000 ÷ 65 = 415 unidades, por encima de la demanda de 390.</li>
<li><strong>Por qué cambió el resultado:</strong> el peso posicional adelanta las tareas con muchos sucesores (C antes que E) y dejó tareas largas aisladas (G, I); Kilbridge &amp; Wester avanza <strong>por columnas</strong> y así combinó G con F e I con H, que sumaron 65 s.</li>
</ul>
<p><strong>Recomendación:</strong> Kilbridge &amp; Wester, porque ahorra una estación y sube la eficiencia casi 12 puntos con el mismo cuello de botella. Esto <strong>no</strong> significa que siempre gane uno: con otros tiempos puede ser al revés. Por eso en la Actividad 4 se aplican los dos y se compara.</p>
<hr>
<h2 id="ejemplo-resuelto-4-dos-modelos">6. Ejemplo resuelto 4: dos modelos</h2>
<p><strong>Datos.</strong> La misma línea del ejemplo 3 produce dos modelos con los mismos pasos y distinto tiempo. Demanda por día: modelo 1 = 210 unidades; modelo 2 = 140 unidades. Tiempos del modelo 2 (s): A 20; B 15; C 35; D 30; E 25; F 20; G 60; H 10; I 45; J 45; K 40. Los tiempos del modelo 1 son los del ejemplo 3. Mismo tiempo disponible: 27,000 s.</p>
<h3 id="paso-1.-tiempo-ponderado">Paso 1. Tiempo ponderado</h3>
<p>Tiempo ponderado = (t₁ × 210 + t₂ × 140) ÷ 350. Ejemplos:</p>
<ul>
<li>C = (45 × 210 + 35 × 140) ÷ 350 = <strong>41.0 s</strong></li>
<li>G = (50 × 210 + 60 × 140) ÷ 350 = <strong>54.0 s</strong></li>
<li>E = (20 × 210 + 25 × 140) ÷ 350 = <strong>22.0 s</strong></li>
</ul>
<p>Resultado completo: A 20.0; B 15.0; C 41.0; D 30.0; E 22.0; F 17.0; G 54.0; H 10.0; I 51.0; J 42.0; K 43.0. Σ ponderada = <strong>345 s</strong>.</p>
<h3 id="paso-2.-ciclo-y-estaciones-mínimas">Paso 2. Ciclo y estaciones mínimas</h3>
<ul>
<li>Demanda total = 210 + 140 = <strong>350 unidades/día</strong></li>
<li>Ciclo c = 27,000 ÷ 350 = <strong>77.14 s</strong></li>
<li>N mín. = ⌈345 ÷ 77.14⌉ = ⌈4.47⌉ = <strong>5 estaciones</strong></li>
</ul>
<h3 id="paso-3.-asignación-con-peso-posicional-ponderado">Paso 3. Asignación con peso posicional ponderado</h3>
<p>Pesos ponderados: A 330; B 262; D 247; C 212; F 153; G 149; I 136; E 117; H 95; J 85; K 43. Lista: A, B, D, C, F, G, I, E, H, J, K.</p>
<ul>
<li><strong>Estación 1:</strong> A + B + D = 20 + 15 + 30 = <strong>65</strong>. C (41) no cabe.</li>
<li><strong>Estación 2:</strong> C (41) + F (17) = <strong>58</strong>. G (54) no cabe.</li>
<li><strong>Estación 3:</strong> G (54) + E (22) = <strong>76</strong>.</li>
<li><strong>Estación 4:</strong> I (51) + H (10) = <strong>61</strong>.</li>
<li><strong>Estación 5:</strong> J (42) = <strong>42</strong>. K (43) rebasa: 85 &gt; 77.14.</li>
<li><strong>Estación 6:</strong> K (43) = <strong>43</strong>.</li>
</ul>
<p><strong>Resultado:</strong> 6 estaciones; eficiencia = 345 ÷ (6 × 77.14) × 100 = <strong>74.5 %</strong>.</p>
<h3 id="paso-4.-revisión-por-modelo-el-paso-que-se-olvida">Paso 4. Revisión por modelo (el paso que se olvida)</h3>
<p>La carga real de cada estación con los tiempos de cada modelo:</p>
<ul>
<li><strong>Modelo 1:</strong> 65, 60, 70, 65, 40, 45 s. Todas ≤ 77.14.</li>
<li><strong>Modelo 2:</strong> 65, 55, <strong>85</strong>, 55, 45, 40 s. <strong>La estación 3 rebasa el ciclo en 7.86 s</strong> cuando pasa el modelo 2.</li>
</ul>
<p>Aunque el balance ponderado «cuadra», la estación 3 no alcanza el ciclo con el modelo 2.</p>
<h3 id="paso-5.-qué-hacer-con-el-exceso">Paso 5. Qué hacer con el exceso</h3>
<ol>
<li><strong>Secuenciar los modelos</strong> (la mezcla es de 3 unidades del modelo 1 por cada 2 del modelo 2; se intercalan en lugar de producir por lotes) para que el exceso se compense con la holgura del modelo 1 (7.14 s en esa estación).</li>
<li><strong>Dar apoyo desde la estación 2 o 4</strong>, que con el modelo 2 tienen holgura de 22 y 22 s.</li>
<li><strong>Probar reasignar</strong> la tarea E (25 s en el modelo 2). Con tiempos ponderados, pasarla a la estación 2 deja 80 s y a la estación 4 deja 83 s, ambas por encima del ciclo de 77.14 s: <strong>no es viable</strong> sin reducir antes algún tiempo (por ejemplo, el de E o el de C).</li>
<li>Si nada de lo anterior es viable, subir el ciclo o añadir una estación.</li>
</ol>
<blockquote>
<p>Los números de los ejemplos 3 y 4 se calcularon con las funciones del cuaderno. Como práctica, reproduce el ejemplo 3 en Colab escribiendo estos tiempos y precedencias en <code>T</code> y <code>P</code> (sección 12 del cuaderno): debes obtener los mismos resultados.</p>
</blockquote>
<hr>
<h2 id="por-qué-usar-python">7. Por qué usar Python</h2>
<p>El balanceo se puede hacer a mano, y <strong>debe hacerse a mano al menos una vez</strong> para entenderlo. Python se usa porque:</p>
<ol>
<li><strong>Evita errores aritméticos repetidos.</strong> Un cambio de dato obliga a recalcular todo; en código es solo volver a ejecutar.</li>
<li><strong>Permite probar escenarios.</strong> «¿Y si la demanda sube 10 %?», «¿y si reduzco 20 % la tarea más larga?» se responden en segundos.</li>
<li><strong>Hace visible el algoritmo.</strong> Para programar la regla de asignación hay que escribir cada paso sin ambigüedad: es la mejor forma de comprobar que entendiste el método.</li>
<li><strong>Es reproducible.</strong> El mismo código con los mismos datos da el mismo resultado; otra persona puede revisarlo.</li>
<li><strong>Es la herramienta de la industria.</strong> El análisis de datos, la simulación y la optimización de procesos usan Python y sus librerías; practicarlo ahora te prepara para materias posteriores y para el trabajo.</li>
<li><strong>Cada alumno puede tener sus propios datos.</strong> El cuaderno genera valores distintos por matrícula sin que el docente tenga que preparar cuarenta enunciados.</li>
</ol>
<p><strong>Lo que Python no hace por ti:</strong> decidir si un balance es razonable, interpretar el cuello de botella, proponer mejoras viables y comunicar resultados a una persona de dirección. Eso es lo que evalúa la rúbrica.</p>
<hr>
<h2 id="explicación-de-las-librerías">8. Explicación de las librerías</h2>
<p>Una <strong>librería</strong> es un conjunto de funciones ya escritas que se cargan con <code>import</code>. El cuaderno usa estas:</p>
<ol>
<li><strong><code>math</code></strong> (viene con Python). Funciones matemáticas básicas. Se usa <code>math.ceil()</code> para redondear hacia arriba el número de estaciones, que es exactamente lo que pide ⌈ ⌉.</li>
<li><strong><code>hashlib</code></strong> (viene con Python). Convierte un texto (tu matrícula) en un número fijo. Así la misma matrícula produce siempre los mismos datos.</li>
<li><strong><code>random</code></strong> (viene con Python). Genera números aleatorios. Con la semilla que sale de tu matrícula, los valores «aleatorios» son siempre los mismos para ti y distintos de los de tus compañeros.</li>
<li><strong><code>numpy</code></strong> (<code>import numpy as np</code>). Cálculo numérico con arreglos. Es la base de pandas y de matplotlib; en el cuaderno se importa para que lo practiques en los ejercicios finales.</li>
<li><strong><code>pandas</code></strong> (<code>import pandas as pd</code>). Tablas llamadas <em>DataFrame</em>, como una hoja de Excel dentro de Python. Se usa para mostrar tareas, estaciones y escenarios, y para exportar a Excel.</li>
<li><strong><code>matplotlib</code></strong> (<code>import matplotlib.pyplot as plt</code>). Gráficas: barras de carga por estación con la línea del ciclo.</li>
<li><strong><code>networkx</code></strong> (<code>import networkx as nx</code>). Grafos (nodos y flechas). Dibuja el <strong>diagrama de precedencia</strong> a partir del diccionario de precedencias.</li>
</ol>
<p>Ejemplo mínimo de cada una:</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">import</span> math
math<span class="token punctuation">.</span>ceil<span class="token punctuation">(</span><span class="token number">3.31</span><span class="token punctuation">)</span>          <span class="token comment"># 4  → número mínimo de estaciones</span>

<span class="token keyword">import</span> pandas <span class="token keyword">as</span> pd
pd<span class="token punctuation">.</span>DataFrame<span class="token punctuation">(</span><span class="token punctuation">{</span><span class="token string">"Tarea"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token string">"A"</span><span class="token punctuation">,</span> <span class="token string">"B"</span><span class="token punctuation">]</span><span class="token punctuation">,</span> <span class="token string">"t (min)"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token number">6</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">]</span><span class="token punctuation">}</span><span class="token punctuation">)</span>

<span class="token keyword">import</span> matplotlib<span class="token punctuation">.</span>pyplot <span class="token keyword">as</span> plt
plt<span class="token punctuation">.</span>bar<span class="token punctuation">(</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">]</span><span class="token punctuation">,</span> <span class="token punctuation">[</span><span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span> plt<span class="token punctuation">.</span>show<span class="token punctuation">(</span><span class="token punctuation">)</span>

</code></pre>
<hr>
<h2 id="explicación-del-script">9. Explicación del script</h2>
<p>El cuaderno está dividido en secciones. Las funciones están en la sección 3 («Caja de herramientas»). Lo que hace cada una:</p>
<ol>
<li><strong><code>rng_from(matricula)</code></strong>: convierte la matrícula en un generador de números aleatorios reproducible.</li>
<li><strong><code>datos_alumno(matricula)</code></strong>: arma los cuatro ejercicios con valores propios: tiempos de las tareas, jornada, receso, reubicación, demanda, datos de la cinta y dos modelos. Se asegura de que los datos sean <strong>factibles</strong> y de que el balance no quede lejos del mínimo teórico.</li>
<li><strong><code>sucesores(P)</code> y <code>descendientes(P)</code></strong>: a partir del diccionario de precedencias <code>P</code> (tarea → lista de predecesores) encuentran qué tareas vienen después, directa e indirectamente.</li>
<li><strong><code>peso_posicional(T, P)</code></strong>: tiempo de la tarea + los tiempos de todos sus descendientes. Es la fórmula 13.</li>
<li><strong><code>columnas_kw(T, P)</code></strong>: calcula la columna más temprana y la más tardía de cada tarea para Kilbridge &amp; Wester.</li>
<li><strong><code>asignar(T, P, c, prioridad, reub)</code></strong>: el corazón del balanceo. Abre una estación, mira qué tareas ya pueden hacerse (todas sus predecesoras listas) y cuáles <strong>caben</strong> en lo que resta del ciclo (incluida la reubicación); elige la de mayor prioridad; repite hasta llenar la estación y pasa a la siguiente. Si una tarea es mayor que el ciclo, avisa que la línea es infactible.</li>
<li><strong><code>carga_est(...)</code> y <code>metricas(...)</code></strong>: cargas, ocio, número de estaciones, eficiencia y retraso de balanceo.</li>
<li><strong><code>nmin(T, c)</code></strong>: ⌈Σt ÷ c⌉.</li>
<li><strong><code>peso_multimodelo(...)</code></strong>: tiempos ponderados por la demanda de cada modelo.</li>
<li><strong><code>resolver(D)</code></strong>: ejecuta los cuatro ejercicios y devuelve los resultados de referencia con las <strong>mismas fórmulas</strong> de esta sesión.</li>
</ol>
<p>Pseudocódigo de <code>asignar</code> (para que lo puedas seguir a mano):</p>
<pre class=" language-text"><code class="prism  language-text">mientras queden tareas sin asignar:
    abrir estación nueva, carga = 0
    repetir:
        candidatas = tareas cuyas predecesoras ya están asignadas
        factibles  = candidatas con carga + t (+ reubicación si no es la primera) ≤ ciclo
        si no hay factibles: cerrar estación
        si hay: elegir la de mayor prioridad, asignarla, actualizar la carga

</code></pre>
<p>La <strong>prioridad</strong> cambia el método: en peso posicional es el peso mayor primero; en Kilbridge &amp; Wester es columna más tardía menor, luego columna más temprana menor, luego tiempo mayor.</p>
<hr>
<h2 id="cómo-usar-el-cuaderno">10. Cómo usar el cuaderno</h2>
<p>El archivo es <code>Actividad4_Balanceo_Linea_EYDT.ipynb</code>.</p>
<h3 id="abrirlo-en-google-colab">8.1 Abrirlo en Google Colab</h3>
<ol>
<li>Entra a <strong><a href="http://colab.research.google.com">colab.research.google.com</a></strong> con tu cuenta de Google.</li>
<li>Elige <strong>Archivo → Subir cuaderno</strong> y selecciona el archivo <code>.ipynb</code> (o abre el enlace que publique el docente).</li>
<li>Guarda tu copia: <strong>Archivo → Guardar una copia en Drive</strong>. Trabaja en tu copia.</li>
</ol>
<h3 id="ejecutarlo">8.2 Ejecutarlo</h3>
<ol>
<li>Una celda de código se ejecuta con <strong>Shift + Enter</strong> o con el botón de reproducir.</li>
<li>Si es la primera vez, ejecuta las celdas <strong>en orden</strong>, de arriba abajo. Las celdas de abajo usan lo que definieron las de arriba.</li>
<li>En la celda 2 cambia <code>MATRICULA = "ESCRIBE-AQUI-TU-MATRICULA"</code> por tu matrícula, entre comillas, y ejecútala. Después ejecuta todo el cuaderno con <strong>Entorno de ejecución → Ejecutar todo</strong>.</li>
<li>Si vuelves otro día, <strong>vuelve a ejecutar desde la primera celda</strong> (Colab olvida las variables al desconectarse).</li>
</ol>
<h3 id="qué-obtienes">8.3 Qué obtienes</h3>
<ul>
<li><strong>Tus datos</strong> de los cuatro ejercicios (sección 4). Cópialos tal cual a tu PDF.</li>
<li>El <strong>diagrama de precedencia</strong> de los ejercicios 1 y 3.</li>
<li>Las <strong>tablas de estaciones</strong> con carga y ocio, las <strong>eficiencias</strong> y las <strong>gráficas de carga</strong>.</li>
<li>Los <strong>cálculos del ejercicio 2</strong> con la tabla de operarios por estación y el tiempo de recorrido.</li>
<li>Un <strong>simulador de mejoras</strong> (sección 10) para respaldar con números tus tres propuestas por ejercicio.</li>
<li>Una <strong>descripción de tu caso</strong> y <strong>hallazgos calculados</strong> (hechos medidos: cuello de botella, ocio, holgura, reubicaciones) por ejercicio (sección 11).</li>
<li><strong>Gráficas y tablas etiquetadas con tu matrícula</strong>, guardadas en una carpeta de evidencias, un <strong>reporte descargable</strong> (HTML que puedes imprimir como PDF) y un <strong>archivo de Excel</strong> (sección 11).</li>
</ul>
<p>El cuaderno <strong>no escribe tu análisis ni tus mejoras</strong>: el reporte trae recuadros en blanco («Tu análisis» y «Tus tres mejoras») que debes llenar tú en tu PDF.</p>
<h3 id="qué-debes-hacer-tú">8.4 Qué debes hacer tú</h3>
<p>El cuaderno calcula; la calificación depende de lo que <strong>tú</strong> expliques:</p>
<ol>
<li>Escribe en tu PDF el <strong>procedimiento</strong> con tus propias palabras (fórmula → sustitución → resultado → unidad).</li>
<li>Explica por qué la solución es razonable y qué limita la línea (cuello de botella, ocio, reubicación).</li>
<li>Propón <strong>al menos tres mejoras por ejercicio</strong>, viables y con un cálculo que las respalde (puedes usar el simulador).</li>
<li>Prepara la <strong>presentación ejecutiva</strong> de un solo problema con una herramienta distinta a PowerPoint.</li>
</ol>
<h3 id="problemas-comunes">8.5 Problemas comunes</h3>
<ul>
<li><strong><code>NameError</code></strong>: no ejecutaste una celda anterior. Usa <strong>Ejecutar todo</strong>.</li>
<li><strong>«Tarea mayor que el ciclo»</strong>: con ese dato la línea no es factible con una persona por estación; es un resultado, no un fallo del cuaderno. Explícalo en tu análisis.</li>
<li><strong>No se descarga el Excel</strong>: el navegador bloqueó la descarga; en el panel de carpetas (ícono de archivo) de Colab, clic derecho sobre el archivo y <strong>Descargar</strong>.</li>
<li><strong>Quieres otra red o más tareas</strong>: edita el diccionario de precedencias <code>P</code> y los tiempos <code>T</code>; es parte de la práctica de «Tu turno» (sección 12 del cuaderno).</li>
</ul>
<hr>
<h2 id="distribución-de-planta-diagramas-y-costos-5.1-a-5.4">11. Distribución de planta, diagramas y costos (5.1 a 5.4)</h2>
<h3 id="tipos-de-distribución-de-planta-según-el-producto-y-proceso-5.1">9.1 Tipos de distribución de planta según el producto y proceso (5.1)</h3>
<ol>
<li><strong>Por producto (en línea).</strong> Las estaciones se acomodan en el orden de las operaciones. Es la distribución del balanceo de línea: alto volumen, poca variedad. Ventaja: flujo continuo y poco inventario. Riesgo: si una estación se detiene, para toda la línea.</li>
<li><strong>Por proceso (funcional).</strong> Se agrupan máquinas semejantes (tornos juntos, soldadura junta). Alta variedad, bajo volumen. Ventaja: flexibilidad. Riesgo: recorridos largos e inventario en proceso.</li>
<li><strong>De posición fija.</strong> El producto no se mueve; llegan personas y equipo (construcción, barcos, aviones).</li>
<li><strong>Celular (tecnología de grupos).</strong> Se forman células para familias de productos. Mezcla flexibilidad con flujo corto.</li>
</ol>
<p>Cómo se elige: volumen y variedad. A mayor volumen y menor variedad, más sentido tiene la distribución por producto, que es donde el balanceo de la Unidad 4 se aplica.</p>
<h3 id="diagrama-de-hilos-y-diagrama-de-precedencia-5.2">9.2 Diagrama de hilos y diagrama de precedencia (5.2)</h3>
<ul>
<li><strong>Diagrama de precedencia</strong> (ya lo usas): círculos con tareas y flechas de «debe hacerse antes que». No tiene escala ni plano. Responde: <strong>¿qué orden es obligatorio?</strong></li>
<li><strong>Diagrama de hilos:</strong> se dibuja sobre el <strong>plano a escala</strong> de la planta; con un hilo o línea se traza el recorrido real de la persona o del material. Responde: <strong>¿cuánto se camina y por dónde se cruzan los flujos?</strong> La longitud total del hilo (en metros) es una medida de desperdicio por transporte.</li>
</ul>
<p>Cómo se usan juntos: el precedencia fija <strong>qué se puede agrupar</strong>; el de hilos revisa <strong>si la distribución física lo permite sin recorridos innecesarios</strong>.</p>
<p>Cómo hacer un diagrama de hilos:</p>
<ol>
<li>Obtén el plano a escala y marca los puestos de trabajo.</li>
<li>Observa o toma el recorrido de un ciclo completo.</li>
<li>Traza el hilo en el orden de los desplazamientos.</li>
<li>Mide la longitud con la escala y calcula metros por ciclo y por turno.</li>
<li>Propón un acomodo que acorte o descruce los hilos.</li>
</ol>
<h3 id="técnicas-de-distribución-de-áreas-5.3">9.3 Técnicas de distribución de áreas (5.3)</h3>
<p>Para decidir <strong>qué área va junto a cuál</strong>, se usa la <strong>tabla relacional de actividades</strong> (planeación sistemática de la distribución, Muther). Cada par de áreas recibe un código de cercanía:</p>
<ul>
<li><strong>A:</strong> absolutamente necesaria la cercanía.</li>
<li><strong>E:</strong> especialmente importante.</li>
<li><strong>I:</strong> importante.</li>
<li><strong>O:</strong> cercanía ordinaria, sin importancia particular.</li>
<li><strong>U:</strong> sin importancia.</li>
<li><strong>X:</strong> no deseable (ruido, polvo, riesgo).</li>
</ul>
<p>Cada código lleva el <strong>motivo</strong> (flujo de material, uso del mismo personal, ruido, seguridad). Con la tabla se arma el <strong>diagrama relacional</strong>: las áreas con A se dibujan pegadas y las X, separadas. Después se calcula el <strong>espacio necesario</strong> de cada área (máquinas, circulación, almacén) y se acomoda sobre el plano.</p>
<h3 id="costos-y-tarifas-de-operaciones-5.4">9.4 Costos y tarifas de operaciones (5.4)</h3>
<p>El balanceo tiene un precio. Con una tarifa por hora de mano de obra (dato didáctico, <strong>no</strong> una tarifa real de la empresa; sustitúyela por la tarifa de tu caso), se calcula:</p>
<ul>
<li><strong>Costo de mano de obra por unidad</strong> = (N × tarifa × c) ÷ 60, con c en minutos y tarifa por hora.</li>
<li><strong>Costo del ocio por unidad</strong> = (N × c − Σt) × tarifa ÷ 60.</li>
</ul>
<p>Ejemplo con el Ejercicio 1 y una tarifa didáctica de 100 pesos por hora:</p>
<ul>
<li>Mano de obra por unidad = 4 × 100 × 9.0625 ÷ 60 = <strong>60.42 pesos</strong></li>
<li>Tiempo productivo = 30 min → costo productivo = 100 × 30 ÷ 60 = <strong>50 pesos</strong></li>
<li>Costo del ocio = 60.42 − 50 = <strong>10.42 pesos por unidad</strong> (17.2 %, el mismo retraso de balanceo)</li>
<li>Con 48 unidades diarias el ocio cuesta 10.42 × 48 ≈ <strong>500 pesos al día</strong>.</li>
</ul>
<p>Esto convierte una mejora en dinero: si bajar un minuto de ciclo elimina una estación, el ahorro se calcula con estas mismas fórmulas y se presenta a dirección.</p>
<hr>
<h2 id="errores-frecuentes">12. Errores frecuentes</h2>
<ol>
<li><strong>No descontar el receso</strong> antes de calcular el ciclo.</li>
<li><strong>Mezclar unidades</strong> (minutos con segundos, horas con minutos).</li>
<li><strong>Olvidar el redondeo hacia arriba</strong> del número de estaciones y de operarios.</li>
<li><strong>Usar la demanda anual como si fuera diaria.</strong> Convierte primero.</li>
<li><strong>Meter el traslado entre estaciones dentro del ciclo.</strong> El traslado afecta el tiempo de recorrido, no el ciclo.</li>
<li><strong>Calcular la eficiencia con el N mínimo</strong> en lugar del N real que obtuviste.</li>
<li><strong>Sumar la reubicación a la eficiencia</strong> como si fuera tiempo productivo.</li>
<li><strong>No revisar la factibilidad</strong> (tarea más larga contra el ciclo).</li>
<li><strong>Presentar solo números.</strong> Sin interpretación ni mejoras no hay puntos en los criterios 3 y 5 de la rúbrica.</li>
<li><strong>Copiar el resultado del cuaderno sin entenderlo.</strong> El docente puede pedir que expliques cualquier paso en la sesión presencial.</li>
<li><strong>Mejoras genéricas</strong> («capacitar al personal») sin cálculo. Una mejora viable dice qué se cambia, cuánto mejora el indicador y cuánto cuesta o requiere.</li>
<li><strong>Usar PowerPoint para la presentación ejecutiva.</strong> La actividad pide otra herramienta.</li>
</ol>
<hr>
<h2 id="cómo-se-conecta-con-la-actividad-4-y-el-foro-10">13. Cómo se conecta con la Actividad 4 y el Foro 10</h2>
<ul>
<li><strong>Actividad 4 (10 puntos, individual):</strong> se entrega un PDF con nombre <code>APELLIDOS_NOMBRES_ACTIVIDAD4</code>. Se evalúa con cinco elementos de 2 puntos: desarrollo técnico, aplicación de conceptos, análisis y propuestas de mejora (mínimo tres por ejercicio), presentación ejecutiva (herramienta distinta a PowerPoint) y claridad y orden. Entregar a destiempo resta 2 puntos.</li>
<li><strong>Foro 10:</strong> el foro retoma lo visto en las semanas 9 y 10 (peso posicional, Kilbridge &amp; Wester, varios modelos, cinta, operarios, diagrama de hilos y costos) para que discutas <strong>una decisión de balanceo</strong> con otro compañero. Las instrucciones del foro están en un documento aparte.</li>
<li><strong>Presentación ejecutiva:</strong> se usa la <strong>diapositiva ejecutiva</strong> (machote en archivo aparte) con una sola idea: <em>problema → cálculo → decisión → resultado</em>.</li>
</ul>
<hr>
<h2 id="cierre-de-la-sesión">14. Cierre de la sesión</h2>
<p>Al terminar la semana debes poder:</p>
<ol>
<li>Calcular el ciclo a partir de una demanda anual o diaria, con receso y eficiencia operativa.</li>
<li>Decidir si una línea es factible y, si no, qué hacer.</li>
<li>Balancear con peso posicional y con Kilbridge &amp; Wester considerando reubicación.</li>
<li>Calcular operarios, estaciones, tiempo de recorrido e inventario en proceso de una cinta.</li>
<li>Convertir una mejora en eficiencia y en dinero.</li>
<li>Usar el cuaderno de Python para verificar y comparar escenarios.</li>
<li>Comunicar una decisión en una diapositiva ejecutiva.</li>
</ol>
<p><strong>Autoevaluación (responde sin mirar):</strong></p>
<ol>
<li>¿Por qué el traslado entre estaciones no cambia el ciclo?</li>
<li>Una línea tiene ciclo de 54 s y una tarea de 60 s. ¿Qué haces?</li>
<li>¿Qué diferencia hay entre el diagrama de precedencia y el de hilos?</li>
<li>Si reduces la reubicación a la mitad, ¿qué indicador mejora primero: eficiencia, número de estaciones o cuello de botella?</li>
</ol>
<hr>
<h2 id="referencias-formato-apa">15. Referencias (formato APA)</h2>
<p>Harris, C. R., Millman, K. J., van der Walt, S. J., Gommers, R., Virtanen, P., Cournapeau, D., … Oliphant, T. E. (2020). Array programming with NumPy. <em>Nature, 585</em>(7825), 357–362. <a href="https://doi.org/10.1038/s41586-020-2649-2">https://doi.org/10.1038/s41586-020-2649-2</a></p>
<p>Hagberg, A. A., Schult, D. A., &amp; Swart, P. J. (2008). Exploring network structure, dynamics, and function using NetworkX. En G. Varoquaux, T. Vaught &amp; J. Millman (Eds.), <em>Proceedings of the 7th Python in Science Conference</em> (pp. 11–15).</p>
<p>Helgeson, W. B., &amp; Birnie, D. P. (1961). Assembly line balancing using the ranked positional weight technique. <em>Journal of Industrial Engineering, 12</em>(6), 394–398.</p>
<p>Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. <em>Computing in Science &amp; Engineering, 9</em>(3), 90–95. <a href="https://doi.org/10.1109/MCSE.2007.55">https://doi.org/10.1109/MCSE.2007.55</a></p>
<p>Kilbridge, M. D., &amp; Wester, L. (1961). A heuristic method of assembly line balancing. <em>Journal of Industrial Engineering, 12</em>(4), 292–298.</p>
<p>Muther, R. (1973). <em>Systematic layout planning</em> (2.ª ed.). Cahners Books.</p>
<p>Niebel, B. W., &amp; Freivalds, A. (2014). <em>Ingeniería industrial: Métodos, estándares y diseño del trabajo</em> (13.ª ed.). McGraw-Hill. [Verificar edición y capítulos de la bibliografía oficial del curso.]</p>
<p>The pandas development team. (2020). <em>pandas-dev/pandas: Pandas</em> [Software]. Zenodo. <a href="https://doi.org/10.5281/zenodo.3509134">https://doi.org/10.5281/zenodo.3509134</a></p>
<p>Python Software Foundation. (s. f.). <em>Python documentation</em>. <a href="https://docs.python.org/3/">https://docs.python.org/3/</a></p>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

