# Libro de lecciones aprendidas — protocolo de afinado automático

**Qué es.** Un registro acumulativo (`lecciones.csv`) donde cada autopsia, desvío confirmado, salida cerrada a 72h o falla de flota deja una lección con su enmienda propuesta, la regla que toca, la métrica que la valida, el umbral y una fecha de vencimiento. La máquina se afina sola porque **ninguna enmienda entra al Testamento por convicción: entra cuando su métrica cumple el umbral, y sale cuando vence sin cumplirlo.**

**Estados de una lección.**
`propuesta` → la escribió el chat o MÉTRICAS-E; no cambia ninguna regla todavía.
`en prueba` → aprobada en el checkpoint del domingo (o por José en el chat); tiene métrica, umbral y `vence`. Durante la prueba se aplica como regla provisional y se mide.
`validada` → cumplió el umbral: se escribe en el Testamento (nueva versión) y en el prompt que corresponda. La fila no se borra; `resultado` guarda la evidencia.
`descartada` → venció sin cumplir o la evidencia la contradijo; se anota por qué. Tampoco se borra.
`observacion` → no cambia regla; queda para que la próxima autopsia la retome.

**Quién escribe qué.**
- *MÉTRICAS-E (diario, E8-bis "Marcador de enmiendas"):* lee `lecciones.csv`, y para cada fila `en prueba` intenta sumar una observación de hoy a su métrica (un stop ejecutado → latencia para L3; una compra de José → tipo de desvío para L2/L4; un evento del calendario → L1; una entrada de titular → alza/baja para L7; un "s/d" por insumo → L8). Escribe en el informe una línea por lección: `Lx: [métrica] hoy = [valor] | acumulado [n/umbral] | vence [fecha]`. **No edita `lecciones.csv`**: el estado lo cambia solo el checkpoint. Además propone filas nuevas (estado `propuesta`) cuando detecta: (a) una salida a 72h con calidad mala; (b) un desvío confirmado que se repite por tercera vez con el mismo tipo; (c) un rasgo de ganador que aparece ≥3 veces en `control-perdedores.csv`; (d) un mapa condicional disparado que a 72h está −25%.
- *Chat (autopsias, cada caso relevante):* escribe el relato en `informes/autopsia-YYYY-MM-DD.md` y las lecciones numeradas en `lecciones.csv` como `propuesta` o, si José las aprueba en el momento, `en prueba`.
- *Checkpoint del domingo:* recorre las `en prueba`: cumplió → `validada` (+ Testamento vX.Y + prompt); venció sin cumplir → `descartada`; sigue → se deja. Recorre las `propuesta` y decide. Tres líneas fijas nuevas en el checkpoint: enmiendas validadas esta semana, descartadas, y en prueba con su marcador.

**Reglas del libro.** Append-only. Una lección por fila; una fila por lección (no se duplica al reabrirla: se agrega otra fila con `origen = reapertura` y referencia al id). Los ids son L1, L2, … en orden de creación. Una lección que gana plata sigue siendo lección si rompió una regla (L4/BREW). Ninguna lección se valida con n<3.

**Estado al 10-sep-2026.** L1–L9 creadas (ver `informes/autopsia-2026-09-10.md`): 7 en prueba, 1 validada (L6, stops por cierre + 72h, 5/5), 1 observación (L9). Vencimientos: L2/L4 el 27-sep, L8 el 20-sep, L1/L3/L5/L7 el 5-oct.
