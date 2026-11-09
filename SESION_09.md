<h1 id="estudio-y-diseño-de-trabajo-—-contenido-temático-de-la-sesión-9-semana-9">Estudio y Diseño de Trabajo — Contenido temático de la Sesión 9 (Semana 9)</h1>
<p><strong>Tema (programa oficial, Unidad IV: Balanceo de líneas):</strong> 4.3 Aplicación de métodos para el balanceo de líneas de producción: peso posicional y Kilbridge &amp; Wester, de acuerdo con un volumen de producción; 4.4 Balanceo de líneas de ensamble para la producción simultánea de más de un modelo<br>
<strong>Fecha:</strong> 4 al 10 de noviembre de 2026 (sesión presencial: sábado 7 de noviembre)<br>
<strong>Actividad de la unidad:</strong> Actividad 4, Ejercicio de balanceo de líneas (integrador) — 10 puntos, individual, en plataforma.<br>
<strong>Propósito de la sesión:</strong> Que el estudiante (1) calcule el tiempo de ciclo, el número mínimo de estaciones y la eficiencia de una línea a partir de un volumen de producción; (2) balancee una línea con el método de <strong>peso posicional</strong> y con el de <strong>Kilbridge &amp; Wester</strong>; (3) balancee una línea para <strong>dos modelos</strong> con un tiempo ponderado por la demanda; y (4) arranque su Actividad 4.</p>
<blockquote>
<p><strong>Uso de este documento.</strong> Es el material explicativo de la semana: guía para la exposición y lectura previa o de repaso. Todos los datos de los ejemplos son <strong>didácticos</strong> (no provienen de una empresa real). Las reglas de asignación de cada método están escritas paso a paso para que cualquiera obtenga el mismo resultado; si en tu libro de texto el procedimiento tiene variantes, <strong>cita cuál usaste</strong>.</p>
</blockquote>
<blockquote>
<p><strong>Nota sobre el nombre.</strong> El programa oficial escribe «Kildbride &amp; Wester». El método lo propusieron M. D. Kilbridge y L. Wester (1961); en este material se escribe <strong>Kilbridge &amp; Wester</strong>.</p>
</blockquote>
<hr>
<h2 id="índice">Índice</h2>
<ul>
<li>
<ol start="0">
<li>Definiciones conceptuales clave</li>
</ol>
</li>
<li>
<ol>
<li>Repaso: qué es balancear una línea (4.1 y 4.2)</li>
</ol>
</li>
<li>
<ol start="2">
<li>Los cuatro cálculos de partida</li>
</ol>
</li>
<li>
<ol start="3">
<li>4.3 Método del peso posicional</li>
</ol>
</li>
<li>
<ol start="4">
<li>Ejemplo resuelto: peso posicional</li>
</ol>
</li>
<li>
<ol start="5">
<li>4.3 Método de Kilbridge &amp; Wester</li>
</ol>
</li>
<li>
<ol start="6">
<li>Ejemplo resuelto: Kilbridge &amp; Wester</li>
</ol>
</li>
<li>
<ol start="7">
<li>Comparación de los dos resultados</li>
</ol>
</li>
<li>
<ol start="8">
<li>4.4 Balanceo para más de un modelo</li>
</ol>
</li>
<li>
<ol start="9">
<li>Ejemplo resuelto: dos modelos</li>
</ol>
</li>
<li>
<ol start="10">
<li>Errores frecuentes</li>
</ol>
</li>
<li>
<ol start="11">
<li>Arranque de la Actividad 4 (integrador)</li>
</ol>
</li>
<li>
<ol start="12">
<li>Cierre de la sesión</li>
</ol>
</li>
<li>
<ol start="13">
<li>Referencias (formato APA)</li>
</ol>
</li>
</ul>
<hr>
<h2 id="definiciones-conceptuales-clave">0. Definiciones conceptuales clave</h2>
<p><strong>Línea de ensamble.</strong> Conjunto de estaciones de trabajo por las que pasa el producto en un orden fijo; en cada estación se hace una parte del trabajo.</p>
<p><strong>Tarea (elemento de trabajo).</strong> Unidad mínima de trabajo que no se divide entre estaciones (por ejemplo, «pegar la suela»). Cada tarea tiene un <strong>tiempo</strong> y, casi siempre, <strong>tareas que deben terminar antes</strong>.</p>
<p><strong>Precedencia.</strong> Relación de orden entre tareas: B tiene como precedente a A si A debe terminar antes de empezar B. Se dibuja en un <strong>diagrama de precedencia</strong>.</p>
<p><strong>Estación de trabajo.</strong> Lugar donde uno o varios operarios hacen un grupo de tareas. <strong>El tiempo de la estación es la suma de los tiempos de sus tareas.</strong></p>
<p><strong>Tiempo de ciclo ©.</strong> Tiempo máximo que puede ocupar una estación por unidad producida; marca el ritmo de la línea. Se obtiene del volumen que se quiere producir.</p>
<p><strong>Tiempo disponible.</strong> Tiempo de producción del turno <strong>sin</strong> comida, paros programados ni limpieza. Es la base para calcular el ciclo.</p>
<p><strong>Número mínimo teórico de estaciones (N mín.).</strong> Cota inferior: con menos estaciones no alcanza el tiempo. Se redondea <strong>hacia arriba</strong>.</p>
<p><strong>Eficiencia de la línea.</strong> Porcentaje del tiempo de las estaciones que se usa en trabajo (el resto es tiempo ocioso).</p>
<p><strong>Retraso de balanceo (balance delay).</strong> Complemento de la eficiencia: porcentaje de tiempo perdido por mala repartición.</p>
<p><strong>Cuello de botella.</strong> Estación con el mayor tiempo; determina la producción real de la línea.</p>
<p><strong>Peso posicional (PP).</strong> Para una tarea: su propio tiempo <strong>más</strong> los tiempos de <strong>todas</strong> las tareas que dependen de ella, directa o indirectamente.</p>
<p><strong>Columna (Kilbridge &amp; Wester).</strong> Nivel del diagrama de precedencia: la columna 1 tiene las tareas sin precedentes; la columna 2, las que solo dependen de la columna 1; y así sucesivamente.</p>
<p><strong>Tarea flotante.</strong> Tarea que puede colocarse en más de una columna sin romper ninguna precedencia.</p>
<p><strong>Modelo.</strong> Variante del producto que se arma en la misma línea (por ejemplo, tenis de dos versiones).</p>
<p><strong>Tiempo ponderado.</strong> Tiempo promedio de una tarea entre los modelos, pesado por la proporción de la demanda de cada uno.</p>
<hr>
<h2 id="repaso-qué-es-balancear-una-línea-4.1-y-4.2">1. Repaso: qué es balancear una línea (4.1 y 4.2)</h2>
<p>Balancear una línea es <strong>repartir las tareas entre las estaciones</strong> de modo que:</p>
<ol>
<li>Se respeten las <strong>precedencias</strong>.</li>
<li>Ninguna estación pase del <strong>tiempo de ciclo</strong>.</li>
<li>Se use el <strong>menor número de estaciones</strong> posible (mayor eficiencia).</li>
</ol>
<p>Una línea mal balanceada tiene una estación saturada (cuello de botella) y otras con tiempo ocioso. Producir más rápido que el cuello de botella no es posible: <strong>la línea produce al ritmo de su estación más lenta</strong>.</p>
<p>Los métodos de la unidad son <strong>heurísticos</strong>: siguen reglas sencillas que dan buenas soluciones, pero no garantizan la mejor. Por eso dos métodos pueden dar repartos distintos con la misma eficiencia, o uno puede ser mejor en un caso y peor en otro.</p>
<hr>
<h2 id="los-cuatro-cálculos-de-partida">2. Los cuatro cálculos de partida</h2>
<p>Antes de asignar tareas se calcula:</p>
<ol>
<li><strong>Tiempo de ciclo:</strong> c = tiempo disponible ÷ unidades a producir</li>
<li><strong>Número mínimo de estaciones:</strong> N mín. = ⌈ Σ tiempos de las tareas ÷ c ⌉ (se redondea hacia arriba)</li>
<li><strong>Eficiencia:</strong> E = Σ tiempos ÷ (N real × c) × 100</li>
<li><strong>Retraso de balanceo:</strong> 100 − E</li>
</ol>
<p><strong>Condición de factibilidad.</strong> La tarea más larga debe ser <strong>menor o igual</strong> que el ciclo. Si no, ninguna asignación sirve: hay que dividir la tarea, duplicar la estación o cambiar el volumen.</p>
<p><strong>Producción real.</strong> Si el cuello de botella es la estación más cargada (t máx.), la línea produce tiempo disponible ÷ t máx. unidades. Un balance puede tener un ciclo «de diseño» de 50 s y un cuello de botella de 48 s; en ese caso la línea alcanza el volumen con holgura.</p>
<hr>
<h2 id="método-del-peso-posicional">3. 4.3 Método del peso posicional</h2>
<p>Se conoce también como método de <strong>Helgeson–Birnie</strong>. Da prioridad a las tareas que «arrastran» más trabajo detrás de ellas.</p>
<p><strong>Pasos:</strong></p>
<ol>
<li>Dibuja el diagrama de precedencia con los tiempos.</li>
<li>Calcula el <strong>peso posicional</strong> de cada tarea: su tiempo + los tiempos de todas las tareas que vienen después de ella.</li>
<li>Ordena las tareas de <strong>mayor a menor</strong> peso posicional. Esa es la lista de prioridad.</li>
<li><strong>Abre la estación 1</strong> con tiempo disponible igual al ciclo.</li>
<li>Asigna la <strong>primera tarea de la lista</strong> que cumpla las dos condiciones: (a) todos sus precedentes ya están asignados (en esta estación o en una anterior) y (b) su tiempo cabe en el tiempo restante de la estación.</li>
<li>Repite el paso 5 hasta que ninguna tarea quepa. <strong>Cierra la estación</strong> y abre la siguiente.</li>
<li>Termina cuando todas las tareas estén asignadas.</li>
<li>Calcula tiempo de cada estación, ocio, eficiencia y retraso de balanceo.</li>
</ol>
<p><strong>Truco de revisión:</strong> después de cada asignación vuelve a recorrer la lista <strong>desde arriba</strong>; una tarea que antes no estaba disponible puede estarlo ahora.</p>
<hr>
<h2 id="ejemplo-resuelto-peso-posicional">4. Ejemplo resuelto: peso posicional</h2>
<p><strong>Caso.</strong> Línea de ensamble final de la Zapatería Industrial XYZ. Se quieren <strong>540 pares por turno</strong> con <strong>7.5 horas</strong> de tiempo disponible.</p>
<p><a href="https://claude.ai/chat/imagenes/Diagrama_Precedencia_Ejemplo.png">Diagrama de precedencia del ejemplo</a></p>
<p><strong>Tareas, tiempos y precedentes:</strong></p>
<ul>
<li>A, 30 s, sin precedentes</li>
<li>B, 20 s, después de A</li>
<li>C, 25 s, después de A</li>
<li>D, 35 s, después de B</li>
<li>E, 15 s, después de C</li>
<li>F, 40 s, después de C</li>
<li>G, 20 s, después de D y E</li>
<li>H, 30 s, después de A</li>
<li>I, 25 s, después de G, F y H</li>
<li>J, 15 s, después de I</li>
</ul>
<p><strong>Paso 1. Cálculos de partida.</strong></p>
<ul>
<li>Tiempo disponible: 7.5 h × 3 600 = <strong>27 000 s</strong></li>
<li>Ciclo: c = 27 000 ÷ 540 = <strong>50 s</strong></li>
<li>Suma de tiempos: 30 + 20 + 25 + 35 + 15 + 40 + 20 + 30 + 25 + 15 = <strong>255 s</strong></li>
<li>N mín. = 255 ÷ 50 = 5.1, que se redondea a <strong>6 estaciones</strong></li>
<li>Factibilidad: la tarea más larga es F con 40 s, que es menor que 50 s. Sí se puede.</li>
</ul>
<p><strong>Paso 2. Pesos posicionales.</strong></p>
<ul>
<li>A = 30 + todo lo demás = <strong>255</strong></li>
<li>C = 25 + E (15) + F (40) + G (20) + I (25) + J (15) = <strong>140</strong></li>
<li>B = 20 + D (35) + G (20) + I (25) + J (15) = <strong>115</strong></li>
<li>D = 35 + G (20) + I (25) + J (15) = <strong>95</strong></li>
<li>F = 40 + I (25) + J (15) = <strong>80</strong></li>
<li>E = 15 + G (20) + I (25) + J (15) = <strong>75</strong></li>
<li>H = 30 + I (25) + J (15) = <strong>70</strong></li>
<li>G = 20 + I (25) + J (15) = <strong>60</strong></li>
<li>I = 25 + J (15) = <strong>40</strong></li>
<li>J = <strong>15</strong></li>
</ul>
<p><strong>Lista de prioridad (de mayor a menor PP):</strong> A, C, B, D, F, E, H, G, I, J.</p>
<p><strong>Paso 3. Asignación.</strong></p>
<ul>
<li><strong>Estación 1 (restan 50 s).</strong> A (30) entra; restan 20. Siguiente en la lista: C (25) no cabe; B (20) sí cabe y su precedente A ya está. Restan 0. <strong>Estación 1 = A, B → 50 s.</strong></li>
<li><strong>Estación 2 (restan 50 s).</strong> C (25) entra; restan 25. D (35) no cabe. F (40) no cabe. E (15) cabe y C ya está: entra; restan 10. Ninguna otra cabe. <strong>Estación 2 = C, E → 40 s.</strong></li>
<li><strong>Estación 3 (restan 50 s).</strong> D (35) entra; restan 15. F (40) no cabe; H (30) no cabe; G (20) no cabe. <strong>Estación 3 = D → 35 s.</strong></li>
<li><strong>Estación 4 (restan 50 s).</strong> F (40) entra; restan 10. H (30) y G (20) no caben. <strong>Estación 4 = F → 40 s.</strong></li>
<li><strong>Estación 5 (restan 50 s).</strong> H (30) entra; restan 20. G (20) cabe (sus precedentes D y E ya están) y entra; restan 0. <strong>Estación 5 = H, G → 50 s.</strong></li>
<li><strong>Estación 6 (restan 50 s).</strong> I (25) entra (G, F y H ya están); restan 25. J (15) entra. <strong>Estación 6 = I, J → 40 s.</strong></li>
</ul>
<p><strong>Resultado:</strong></p>
<ul>
<li>Estación 1: A, B = 50 s</li>
<li>Estación 2: C, E = 40 s</li>
<li>Estación 3: D = 35 s</li>
<li>Estación 4: F = 40 s</li>
<li>Estación 5: H, G = 50 s</li>
<li>Estación 6: I, J = 40 s</li>
<li><strong>Total: 255 s ✔</strong> (coincide con la suma de las tareas)</li>
</ul>
<p><strong>Indicadores:</strong></p>
<ul>
<li>Estaciones usadas: 6 (igual al mínimo teórico, así que no se podía mejorar)</li>
<li>Tiempo ocioso total: 6 × 50 − 255 = <strong>45 s</strong></li>
<li>Eficiencia: 255 ÷ (6 × 50) = <strong>85 %</strong></li>
<li>Retraso de balanceo: <strong>15 %</strong></li>
<li>Cuello de botella: 50 s (estaciones 1 y 5) = ciclo; la línea produce 27 000 ÷ 50 = <strong>540 pares</strong>, justo lo pedido.</li>
</ul>
<p><strong>Lectura.</strong> El balance cumple el volumen con el número mínimo de estaciones. La pérdida del 15 % viene de que los tiempos de las tareas no «encajan» exactamente en 50 s. Si se quisiera subir la eficiencia habría que <strong>modificar el método</strong> (dividir F, que tiene 40 s, o combinar tareas), no reasignar.</p>
<hr>
<h2 id="método-de-kilbridge--wester">5. 4.3 Método de Kilbridge &amp; Wester</h2>
<p>Este método trabaja con <strong>columnas</strong> del diagrama de precedencia. Su ventaja es que muestra <strong>qué tareas tienen holgura</strong> (pueden moverse) y cuáles no.</p>
<p><strong>Pasos:</strong></p>
<ol>
<li>Dibuja el diagrama de precedencia y ordénalo en <strong>columnas</strong>: la columna 1 con las tareas sin precedentes; la columna 2 con las que solo dependen de la 1; la columna 3 con las que dependen de tareas hasta la 2; y así sucesivamente.</li>
<li>Para cada tarea anota su <strong>columna más temprana</strong> (en la que quedó) y su <strong>columna más tardía</strong> (la más a la derecha donde podría estar sin retrasar a sus sucesoras). Si son distintas, la tarea <strong>flota</strong> entre ambas.</li>
<li>Calcula ciclo, N mín. y eficiencia (sección 2).</li>
<li><strong>Abre la estación 1.</strong> Entre las tareas disponibles (con todos sus precedentes asignados y que quepan) elige con esta regla de prioridad:
<ul>
<li>primero la de <strong>columna más tardía menor</strong> (la que menos holgura tiene);</li>
<li>si empatan, la de <strong>columna más temprana menor</strong> (la más a la izquierda);</li>
<li>si todavía empatan, la de <strong>mayor tiempo</strong>.</li>
</ul>
</li>
<li>Repite hasta que ninguna tarea quepa; cierra la estación y abre otra.</li>
<li>Termina cuando todas estén asignadas y calcula los indicadores.</li>
</ol>
<p><strong>Idea clave.</strong> Las tareas <strong>críticas</strong> (sin holgura) se asignan primero; las <strong>flotantes</strong> se usan para rellenar el tiempo que sobra en una estación.</p>
<hr>
<h2 id="ejemplo-resuelto-kilbridge--wester">6. Ejemplo resuelto: Kilbridge &amp; Wester</h2>
<p>Se usa el mismo caso del apartado 4 (c = 50 s, 255 s de trabajo, N mín. = 6).</p>
<p><strong>Paso 1 y 2. Columnas.</strong></p>
<ul>
<li>Columna 1: A</li>
<li>Columna 2: B, C y H</li>
<li>Columna 3: D, E y F</li>
<li>Columna 4: G</li>
<li>Columna 5: I</li>
<li>Columna 6: J</li>
</ul>
<p><strong>Holgura (columna más temprana → más tardía):</strong></p>
<ul>
<li>A: 1 → 1 (sin holgura)</li>
<li>B: 2 → 2; C: 2 → 2; D: 3 → 3; E: 3 → 3; G: 4 → 4; I: 5 → 5; J: 6 → 6 (sin holgura)</li>
<li><strong>H: 2 → 4.</strong> Solo necesita a A y es precedente de I (columna 5); por eso <strong>flota</strong> entre las columnas 2 y 4.</li>
<li><strong>F: 3 → 4.</strong> Solo es precedente de I; flota entre las columnas 3 y 4.</li>
</ul>
<p><strong>Paso 3. Asignación.</strong></p>
<ul>
<li><strong>Estación 1.</strong> Disponible: A. Entra (30), restan 20. Disponibles ahora: B (20, límite col. 2), C (25, no cabe), H (30, no cabe). Entra B. <strong>Estación 1 = A, B → 50 s.</strong></li>
<li><strong>Estación 2.</strong> Disponibles: C (límite 2), D (límite 3), H (límite 4). Entra C (25), restan 25. Ahora está disponible E (límite 3, 15 s), que cabe: entra; restan 10. D (35) no cabe. <strong>Estación 2 = C, E → 40 s.</strong></li>
<li><strong>Estación 3.</strong> Disponibles al abrir: D (límite 3), F (límite 4) y H (límite 4). Primero la de menor límite: D (35); restan 15. G ya está disponible (D y E asignadas), pero 20 s no caben; F (40) y H (30) tampoco. <strong>Estación 3 = D → 35 s.</strong></li>
<li><strong>Estación 4.</strong> Disponibles: F, H y G, las tres con límite 4. Se desempata por la columna más temprana: H (col. 2), luego F (col. 3) y luego G (col. 4). Entra H (30); restan 20. F (40) no cabe. G (20) cabe: entra; restan 0. <strong>Estación 4 = H, G → 50 s.</strong></li>
<li><strong>Estación 5.</strong> Disponible: F (40). Entra; restan 10. I necesita a F y G (ya asignadas); I (25) no cabe. <strong>Estación 5 = F → 40 s.</strong></li>
<li><strong>Estación 6.</strong> I (25) entra; J (15) entra. <strong>Estación 6 = I, J → 40 s.</strong></li>
</ul>
<p><strong>Resultado:</strong></p>
<ul>
<li>Estación 1: A, B = 50 s</li>
<li>Estación 2: C, E = 40 s</li>
<li>Estación 3: D = 35 s</li>
<li>Estación 4: H, G = 50 s</li>
<li>Estación 5: F = 40 s</li>
<li>Estación 6: I, J = 40 s</li>
<li><strong>Total: 255 s ✔</strong></li>
</ul>
<p><strong>Indicadores:</strong> 6 estaciones, eficiencia <strong>85 %</strong>, retraso de balanceo <strong>15 %</strong>, ocio 45 s.</p>
<hr>
<h2 id="comparación-de-los-dos-resultados">7. Comparación de los dos resultados</h2>
<ul>
<li><strong>Mismo número de estaciones (6) y misma eficiencia (85 %).</strong> En este caso ambos llegan al mínimo teórico.</li>
<li><strong>Reparto distinto:</strong> en peso posicional F va antes (estación 4) y H con G después (estación 5); en Kilbridge &amp; Wester H y G van juntas (estación 4) y F queda sola después (estación 5). Las dos soluciones son válidas porque respetan todas las precedencias.</li>
<li><strong>Cuándo se separan los métodos.</strong> Cuando hay muchas tareas con holgura o tiempos que no encajan en el ciclo, un método puede usar una estación más que el otro. <strong>Ningún método garantiza el óptimo.</strong></li>
<li><strong>Cómo elegir.</strong> Si dos métodos dan el mismo número de estaciones, se prefiere el que deja una estación con <strong>mayor ocio al final</strong> (más fácil de absorber un cambio) o el que <strong>agrupa tareas parecidas</strong> (mismo operario, misma herramienta). Es un criterio de ingeniería, no un cálculo.</li>
</ul>
<p><strong>Preguntas para comparar en tu actividad.</strong> ¿Qué método dio mayor eficiencia? ¿En qué estación está el cuello de botella? ¿Qué tarea modificarías para quitar una estación?</p>
<hr>
<h2 id="balanceo-para-más-de-un-modelo">8. 4.4 Balanceo para más de un modelo</h2>
<p>Cuando la misma línea arma <strong>dos o más modelos</strong> parecidos, las tareas casi siempre son las mismas, pero <strong>cambian los tiempos</strong> (por ejemplo, el modelo con suela especial tarda más en «pegar suela»).</p>
<p><strong>Método del tiempo ponderado (modelo promedio):</strong></p>
<ol>
<li>Con la demanda de cada modelo calcula su <strong>proporción</strong> (por ejemplo, 360 y 180 pares, es decir, 2/3 y 1/3).</li>
<li>Para cada tarea calcula el <strong>tiempo ponderado</strong>: suma del tiempo de cada modelo multiplicado por su proporción.</li>
<li>Calcula el <strong>ciclo con la demanda total</strong>: tiempo disponible ÷ (demanda del modelo 1 + demanda del modelo 2).</li>
<li><strong>Balancea con los tiempos ponderados</strong> usando peso posicional o Kilbridge &amp; Wester, igual que en una línea de un solo modelo.</li>
<li><strong>Revisa cada modelo por separado:</strong> suma, para cada estación, los tiempos reales del modelo 1 y los del modelo 2. Si una estación de un modelo <strong>rebasa mucho el ciclo</strong>, esa estación se atrasará cuando pase ese modelo; hay que secuenciar los modelos (mezclarlos, no hacerlos por lotes largos) o dar apoyo a esa estación.</li>
</ol>
<p><strong>Por qué se promedia.</strong> Si los modelos se alternan en la línea, cada estación «ve» en promedio el tiempo ponderado. Pero un modelo pesado seguido de otro pesado puede congestionar una estación aunque el promedio esté bien; por eso el paso 5.</p>
<hr>
<h2 id="ejemplo-resuelto-dos-modelos">9. Ejemplo resuelto: dos modelos</h2>
<p><strong>Caso.</strong> Se arman dos versiones de calzado en la misma línea: <strong>Modelo 1 (Oxford)</strong>, 360 pares por turno, y <strong>Modelo 2 (Mocasín)</strong>, 180 pares por turno. Tiempo disponible: 27 000 s.</p>
<p><strong>Precedencias comunes:</strong> A → B; A → C; B → D; C → E; D y E → F.</p>
<p><strong>Tiempos por modelo (s):</strong></p>
<ul>
<li>A: Modelo 1 = 45, Modelo 2 = 50</li>
<li>B: 30, 35</li>
<li>C: 20, 15</li>
<li>D: 45, 50</li>
<li>E: 15, 15</li>
<li>F: 35, 25</li>
</ul>
<p><strong>Suma por modelo:</strong> Modelo 1 = 190 s; Modelo 2 = 190 s.</p>
<p><strong>Paso 1. Ciclo con la demanda total.</strong> Demanda = 360 + 180 = 540 pares. c = 27 000 ÷ 540 = <strong>50 s</strong>.</p>
<p><strong>Paso 2. Proporciones.</strong> Modelo 1 = 360 ÷ 540 = 2/3; Modelo 2 = 1/3.</p>
<p><strong>Paso 3. Tiempos ponderados</strong> (= 2/3 × Modelo 1 + 1/3 × Modelo 2):</p>
<ul>
<li>A = 2/3 × 45 + 1/3 × 50 = 30 + 16.67 = <strong>46.67</strong></li>
<li>B = 20 + 11.67 = <strong>31.67</strong></li>
<li>C = 13.33 + 5 = <strong>18.33</strong></li>
<li>D = 30 + 16.67 = <strong>46.67</strong></li>
<li>E = 10 + 5 = <strong>15.00</strong></li>
<li>F = 23.33 + 8.33 = <strong>31.67</strong></li>
<li><strong>Suma = 190.00 s.</strong> N mín. = 190 ÷ 50 = 3.8, que se redondea a <strong>4 estaciones</strong>.</li>
</ul>
<p><strong>Paso 4. Peso posicional con tiempos ponderados.</strong></p>
<ul>
<li>A = 190.00 (todo el trabajo)</li>
<li>B = 31.67 + D (46.67) + F (31.67) = 110.00</li>
<li>C = 18.33 + E (15.00) + F (31.67) = 65.00</li>
<li>D = 46.67 + F (31.67) = 78.33</li>
<li>E = 15.00 + 31.67 = 46.67</li>
<li>F = 31.67</li>
</ul>
<p>Lista: A (190.00), B (110.00), D (78.33), C (65.00), E (46.67), F (31.67).</p>
<p><strong>Asignación (c = 50 s):</strong></p>
<ul>
<li><strong>Estación 1:</strong> A (46.67), restan 3.33; nada cabe. → <strong>A = 46.67 s</strong></li>
<li><strong>Estación 2:</strong> B (31.67), restan 18.33; D no cabe (precedente B ya está, pero 46.67 &gt; 18.33); C (18.33) cabe: entra, restan 0. → <strong>B, C = 50.00 s</strong></li>
<li><strong>Estación 3:</strong> D (46.67), restan 3.33. → <strong>D = 46.67 s</strong></li>
<li><strong>Estación 4:</strong> E (15.00) y F (31.67) → <strong>E, F = 46.67 s</strong></li>
</ul>
<p>Suma: 46.67 + 50.00 + 46.67 + 46.67 = 190.00 ✔.</p>
<p><strong>Indicadores:</strong> 4 estaciones (igual al mínimo teórico); eficiencia = 190 ÷ (4 × 50) = <strong>95 %</strong>; retraso de balanceo 5 %.</p>
<p><strong>Paso 5. Revisión por modelo.</strong></p>
<ul>
<li>Estación 1 (A): Modelo 1 = 45 s; Modelo 2 = 50 s</li>
<li>Estación 2 (B, C): Modelo 1 = 30 + 20 = 50 s; Modelo 2 = 35 + 15 = 50 s</li>
<li>Estación 3 (D): Modelo 1 = 45 s; Modelo 2 = 50 s</li>
<li>Estación 4 (E, F): Modelo 1 = 15 + 35 = 50 s; Modelo 2 = 15 + 25 = 40 s</li>
</ul>
<p>Ningún modelo pasa de 50 s en ninguna estación. <strong>El balance es válido para ambos modelos</strong> y no requiere mezclar de forma especial la producción. Si algún modelo hubiera pasado del ciclo, se habría revisado la secuenciación o se habría cambiado la asignación.</p>
<hr>
<h2 id="errores-frecuentes">10. Errores frecuentes</h2>
<ol>
<li><strong>Redondear N mín. hacia abajo.</strong> Siempre hacia arriba: 3.8 estaciones son 4.</li>
<li><strong>Usar el tiempo bruto del turno</strong> (8 h) sin descontar comida y paros. El ciclo sale más largo que el real y el balance no cumple el volumen; usa siempre el tiempo disponible.</li>
<li><strong>Mezclar unidades.</strong> Si los tiempos están en segundos, el ciclo también.</li>
<li><strong>Olvidar las precedencias indirectas</strong> al calcular el peso posicional: cuenta todas las tareas que dependen de la tarea, no solo las inmediatas.</li>
<li><strong>Asignar una tarea cuyo precedente aún no está asignado.</strong> Revisa cada tarea contra el diagrama.</li>
<li><strong>No volver a revisar la lista desde arriba</strong> después de cada asignación.</li>
<li><strong>Calcular la eficiencia con el ciclo teórico</strong> en vez de con el número real de estaciones.</li>
<li><strong>En multimodelo, ciclo con la demanda de un solo modelo.</strong> Se usa la demanda total.</li>
<li><strong>Dar por bueno un balance sin comprobar que suma el total</strong> de los tiempos de las tareas.</li>
</ol>
<hr>
<h2 id="arranque-de-la-actividad-4-integrador">11. Arranque de la Actividad 4 (integrador)</h2>
<p>La <strong>Actividad 4, Ejercicio de balanceo de líneas (integrador)</strong>, vale <strong>10 puntos</strong> y es <strong>individual</strong>. En la sesión:</p>
<ol>
<li>Cada estudiante recibe su <strong>variante</strong> (según el último dígito de su matrícula) y descarga la <strong>plantilla de Excel</strong>.</li>
<li>Se explica la <strong>estructura del entregable</strong>: datos y ciclo; peso posicional; Kilbridge &amp; Wester; comparación; dos modelos; conclusión.</li>
<li>Se resuelve juntos la <strong>Parte A</strong> (ciclo, N mín.) de una variante como ejemplo de lectura de datos.</li>
<li>El resto se trabaja en casa. Las instrucciones completas, la rúbrica y la fecha están en el documento <strong>Instrucciones de la Actividad 4</strong>.</li>
</ol>
<p><strong>Qué sí se puede preguntar al docente:</strong> cómo leer el diagrama, cómo dibujar columnas, cómo comprobar precedencias. <strong>Qué no:</strong> el resultado.</p>
<hr>
<h2 id="cierre-de-la-sesión">12. Cierre de la sesión</h2>
<ul>
<li>Para balancear se parte de un <strong>volumen de producción</strong>: de él sale el <strong>ciclo</strong> y con el ciclo el <strong>número mínimo de estaciones</strong>.</li>
<li>Un buen balance <strong>respeta precedencias</strong>, <strong>no rebasa el ciclo</strong> y <strong>usa pocas estaciones</strong>.</li>
<li>El <strong>peso posicional</strong> prioriza las tareas con más trabajo posterior; <strong>Kilbridge &amp; Wester</strong> prioriza las que tienen <strong>menos holgura de columna</strong>.</li>
<li>Los dos son <strong>heurísticos</strong>: pueden dar repartos distintos; no garantizan el óptimo.</li>
<li>Para <strong>dos modelos</strong> se balancea con <strong>tiempos ponderados</strong> y se <strong>revisa cada modelo</strong> en cada estación.</li>
<li><strong>Lo que viene.</strong> Unidad V: diagnóstico y mejoramiento de procesos (distribución de planta, diagramas de hilos y de precedencia).</li>
</ul>
<p><strong>Preguntas para reflexionar o comentar.</strong></p>
<ol>
<li>En el ejemplo, la eficiencia es 85 % con el número mínimo de estaciones. ¿Cómo la subirías sin cambiar el volumen?</li>
<li>¿Qué pasaría con el balance si el ciclo se redujera a 40 s? ¿Es factible? Justifica con la tarea más larga.</li>
<li>En el ejemplo de dos modelos, ¿qué estación sería la más crítica si el Modelo 2 pasara a 360 pares y el Modelo 1 a 180?</li>
<li>¿Por qué es peligroso hacer un modelo en lotes largos aunque el balance con tiempos ponderados sea bueno?</li>
</ol>
<hr>
<h2 id="referencias-formato-apa">13. Referencias (formato APA)</h2>
<p>Kilbridge, M. D., &amp; Wester, L. (1961). A heuristic method of assembly line balancing. <em>Journal of Industrial Engineering, 12</em>(4), 292–298.</p>
<p>Niebel, B. W., &amp; Freivalds, A. (2009). <em>Ingeniería industrial: Métodos, estándares y diseño del trabajo</em> (12.ª ed.). McGraw-Hill Interamericana.</p>
<p>Peralta, J. (s. f.). <em>Estudio del trabajo: Una nueva visión</em> (capítulo de balanceo de líneas). Grupo Editorial Patria. <em>(Año de edición por confirmar con la portada del libro.)</em></p>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

