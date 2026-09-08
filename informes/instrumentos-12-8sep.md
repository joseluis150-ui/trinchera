# Los 12 instrumentos nuevos — aprobados por José el 7-sep-2026 ("armemos todo")

Origen: José pidió "ser dinámicos y proponer otras cosas que podemos evaluar"; se propusieron 12 y aprobó todos. Este documento fija qué mide cada uno, dónde vive (archivo en la raíz del repo), quién lo alimenta y qué pregunta contesta. Principio común: **ningún instrumento genera compra**; informan al checkpoint y a los mapas. Ninguna fila de ningún CSV se borra ni se edita hacia atrás.

Alimentación: la tarea diaria **MÉTRICAS-E** (Cowork, 8:15, prompt en `prompts/METRICAS-E_v1.txt`) anota lo mecánico; lo que requiere criterio (confirmar un desvío, cerrar una salida a 72h, puntuar un overhang) se hace en el chat y en el checkpoint del domingo.

| # | Instrumento | Archivo | Pregunta que contesta | Alimenta |
|---|---|---|---|---|
| 1 | Benchmarks en BTC | `benchmarks.csv` | ¿El sistema le gana a no hacer nada (solo BTC), a copiar a Manu y a copiar a DCE? | E (diario) |
| 2 | Grupo de control (perdedores) | `control-perdedores.csv` | ¿Los "rasgos de ganador" de la autopsia también aparecen en los que se hunden? Si sí, no son señal | E (diario) |
| 3 | Mapa de calor de horas de ballenas | `informes/heatmap-horas-*.md` | ¿A qué hora compra cada ballena? ¿La flota la lee antes o después? | Excel Ballenas (semanal) |
| 4 | Latencia del espejo | `latencia-espejo.csv` | ¿Cuántos minutos y cuánto % de MC después de la ballena entramos? | chat (por operación) |
| 5 | Overhang de snipers | columna en `fichas-E.csv` + sub-ítem del Token Score | ¿Cuánto supply está en manos que entraron a <10% del MC actual y todavía no vendieron? | E (diario) |
| 6 | Niveles de liquidación como imán | `liquidaciones.csv` | ¿El precio va a buscar los niveles públicos (Coinglass / lookonchain)? | E (diario) |
| 7 | Salud de Robinhood Chain | `red-rh.csv` | ¿La red está viva? (el 5-sep se paralizó y no se podía vender) | E (diario) |
| 8 | Calendario de acciones madre | `calendario-acciones.csv` | ¿Cuándo reporta/anuncia la acción de cada par meme-acción? (bandera D) | E (avisa a 14 y 3 días) + chat |
| 9 | Atención: Thesis(N) | columna en `fichas-E.csv` | ¿Crece la cantidad de tesis escritas por cada 1.000 holders? (derivada de atención) | E (diario) |
| 10 | Índice de desvío de José | `desvios.csv` | ¿Qué % de las entradas de la semana rompió una regla y cuánto costó? | E (candidatos) + checkpoint |
| 11 | Stress test semanal | `stress-semanal.csv` | Si mañana pasa lo peor plausible, ¿cuánto pierde el patrimonio y a qué distancia queda el techo R30? | checkpoint (domingo) |
| 12 | Calidad de salida / plata en la mesa | `salidas.csv` | ¿Vendemos bien? ¿Cuánto dejamos en la mesa a 72h de cada salida? | E (MC post-salida) + chat |

## Definiciones que importan

**#1 Benchmarks.** Tres varas, todas en dólares y en BTC: *solo BTC* = los $300 depositados comprados en BTC el 30-ago ($79,000 de base, banda $78–80K al cierre de ese día) y no tocados; *espejo Manu* = valor de la cuenta de @KmanuS88 (se indexa desde el 4-sep, $47,500); *canasta DCE* = $100 repartidos en partes iguales entre las 5 posiciones más grandes de DCE el 8-sep, valuadas a diario sin rebalancear. Columna clave: `cuenta_en_btc`. Si la cuenta sube en dólares y baja en BTC, el sistema perdió. Al 7-sep: sistema +60.6% vs solo-BTC +0.2% — pero el 83% de eso es MarsCoin comprada antes de que existiera el sistema; el benchmark empieza a decir algo recién con 3–4 semanas.

**#2 Grupo de control.** Cada día, los 10 tokens de Trending con MC >$1M que MÁS cayeron en 24h, con las mismas columnas estructurales que `autopsias.csv` (top1 holder, Received, titular presente, base antes de la vela, narrativa madre). La pregunta no es "por qué cayeron" sino: *¿cuántos de los rasgos que la autopsia atribuye a los ganadores están también acá?* Un rasgo que aparece en ambos grupos no discrimina y se saca del Token Score.

**#3 Heatmap.** Primer resultado (Manu, 109 operaciones con hora): compra entre 09:00 y 17:00 Asunción (bloque 09–11h 27 compras, 15–17h 20), ventana muerta 01:00–05:59, ventas concentradas 18–20h. Consecuencia directa: la flota de las 6:45–7:45 lee sus compras de AYER con 14–22 horas de retraso. **Si el espejo va a valer algo, hace falta una lectura de tarde (15:30–18:00).** Se repite para unipcs, ether_monk y DCE cuando el Excel tenga sus pestañas (se arman por acumulación diaria: el feed expone 100 filas).

**#4 Latencia.** Por cada entrada nuestra o de Manu que siga a una ballena: minutos desde la operación de la ballena y % de MC arriba (o abajo) de su precio. Entrar más barato porque el token cayó no es mérito, es riesgo (FATCOIN 7-sep: −6% de MC, −20% esa noche). Meta cuando haya n≥10: latencia mediana y delta de MC mediano; si el delta mediano es >+30%, el espejo compra la liquidez de salida de la ballena.

**#5 Overhang de snipers.** En el panel de holders de fomo (top 20 con avg. entry): sumar el % de supply de los holders cuyo MC promedio de entrada es <10% del MC actual y siguen enteros. Es supply que va a vender en cualquier rebote. Sub-ítem nuevo del Token Score, dentro de A-Estructura, **sin subir el total**: overhang <5% → 0 pts de castigo; 5–15% → −2; >15% → −5 (se descuenta de los 25 de estructura). Se anota en `fichas-E.csv`; se puntúa en el chat.

**#6 Liquidaciones.** Total 24h y longs/shorts (Coinglass, público), mayor liquidación, y los niveles "imán" publicados (lookonchain vía Radar X). Columna `toco_el_nivel` se completa al día siguiente. n=1 a favor (James Wynn $79,536 → mínimo $79,449). Uso: no dejar stops ni entradas justo debajo de un nivel público.

**#7 Red RH.** Blockscout de Robinhood Chain: transacciones totales y 24h, bloques, tiempo de bloque, gas. Estado mecánico: NORMAL / LENTA (tiempo de bloque >2× el de ayer) / PARADA (sin bloques nuevos en 10 min). En PARADA no se abre nada en RH y los stops de RH pasan a "no ejecutables" (se anota, no se finge).

**#8 Calendario.** Una fila por par meme-acción y evento (earnings, evento de producto, lockup, macro). `estado_fecha` distingue confirmada / estimada; E avisa cuando faltan 14 días (confirmar la fecha) y 3 días (bandera D: no comprar el satélite si la acción madre viene cayendo). Fechas de earnings de octubre-noviembre están cargadas como **estimadas por patrón histórico** y hay que confirmarlas en las webs de IR.

**#9 Thesis(N).** fomo muestra el contador de tesis por token. `thesis_por_1000_holders` y su variación diaria son una derivada de atención: sube antes que el precio cuando hay narrativa y cae antes cuando la narrativa se agota. Se mide sobre las posiciones abiertas, PONS y STONK (infra de la meta) y los tokens con mapa vigente. Sin n no hay regla; primero 2 semanas de datos.

**#10 Índice de desvío.** Semana 1–7 sep: **5 desvíos sobre 7 entradas = 71%; $115.81 en desvío sobre ~$125 desplegados = 93% → ROJO** (semáforo <20% verde, 20–40% amarillo, >40% rojo). Desvíos: microduck (tamaño), CETS (tiempo), ICOIN (tamaño), PROLOGUE (tamaño), SHROOM (tiempo + promedio). No son desvíos: SPACEHOOD (válvula R9) y FATCOIN (sonda según mapa 13). Un desvío que ganó sigue siendo desvío. Este número es el criterio 1 del checkpoint hecho métrica, y es el que hoy bloquea el depósito.

**#11 Stress test.** Cinco escenarios sobre las posiciones del día. Al 8-sep: peor caso plausible E2 (BTC −10% → memes −30% + gatillo maestro) = −$50 = −10.3% del patrimonio; techo R30 $150, consumido 0%. Lectura: el riesgo de tamaño está controlado; el riesgo real es el índice de desvío.

**#12 Salidas.** Cada venta (TP, stop, forzosa, discrecional) con el máximo y mínimo de las 72h posteriores y la "plata en la mesa" (lo que valdría lo vendido en el máximo posterior). Calidad: buena (≤10% en la mesa o stop validado), regular (10–50%), mala (>50% o stop no validado). Casos abiertos se cierran a las 72h, nunca antes (misma regla del Registro de Bandas). SHROOM resuelve el 10-sep 21:30.

## Qué cambia en la rutina

- Nueva tarea diaria de Cowork **MÉTRICAS-E 8:15** (después de FLUJOS-D 7:45). Es la única tarea que ESCRIBE en el repo (anexa filas a los CSV y hace commit); la flota A/B/X/D solo escribe .txt en Descargas. Nunca toca `index.html`.
- Propuesta derivada del heatmap, sin implementar: una lectura de tarde del feed de Manu y de los titulares (16:00–18:00) para que el espejo tenga latencia de horas y no de un día. Se decide cuando E lleve una semana estable.
- Checkpoint del domingo: se agregan tres líneas fijas — índice de desvío, stress test, y sistema vs solo-BTC.
