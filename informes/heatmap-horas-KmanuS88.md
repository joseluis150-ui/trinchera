# Mapa de calor de horas — KmanuS88 (instrumento #3)

Fuente: xlsx/Ballenas_Trinchera.xlsx, hoja Datos_KmanuS88, 139 operaciones (10-ago→6-sep 2026); se usan solo las 109 con hora real (feed All swaps y modales que sí exponen hora). Las 30 leídas de modales sin hora (cargadas como 12:00 por convención) quedan AFUERA para no fabricar un pico falso al mediodía. Horas en Asunción (UTC-3). Generado 8-sep-2026.

## Por hora del día (compras / ventas / $ comprado / $ vendido)

hora | compras | ventas | $ comprado | $ vendido | barra compras
---|---|---|---|---|---
00:00 | 3 | 3 | $1,393 | $9,381 | ███
01:00 | 0 | 0 | $0 | $0 | 
02:00 | 0 | 0 | $0 | $0 | 
03:00 | 0 | 0 | $0 | $0 | 
04:00 | 0 | 0 | $0 | $0 | 
05:00 | 0 | 0 | $0 | $0 | 
06:00 | 2 | 2 | $996 | $3,369 | ██
07:00 | 2 | 0 | $852 | $0 | ██
08:00 | 1 | 0 | $496 | $0 | █
09:00 | 6 | 0 | $1,861 | $0 | ██████
10:00 | 8 | 1 | $2,878 | $1,989 | ████████
11:00 | 13 | 2 | $7,679 | $4,213 | █████████████
12:00 | 3 | 0 | $1,415 | $0 | ███
13:00 | 5 | 4 | $2,909 | $840 | █████
14:00 | 2 | 0 | $384 | $0 | ██
15:00 | 10 | 0 | $6,957 | $0 | ██████████
16:00 | 1 | 1 | $498 | $1,000 | █
17:00 | 9 | 1 | $5,871 | $3,015 | █████████
18:00 | 6 | 1 | $3,371 | $338 | ██████
19:00 | 6 | 4 | $3,712 | $2,677 | ██████
20:00 | 2 | 2 | $995 | $1,135 | ██
21:00 | 3 | 2 | $1,449 | $6,414 | ███
22:00 | 1 | 2 | $1,044 | $475 | █
23:00 | 1 | 0 | $199 | $0 | █

## Lectura

- Total con hora: 84 compras y 25 ventas. Horas con más compras: 11:00 (13), 15:00 (10), 17:00 (9), 10:00 (8).
- Por día de la semana (operaciones / $): lunes 13 ($10,638), martes 13 ($13,312), miércoles 24 ($15,106), jueves 18 ($7,645), viernes 11 ($3,712), sábado 15 ($13,215), domingo 15 ($16,177).
- Bloques de 3 horas (compras): 00–02h 3, 06–08h 5, 09–11h 27, 12–14h 10, 15–17h 20, 18–20h 14, 21–23h 5.
- Bloques de 3 horas (ventas): 00–02h 3, 06–08h 2, 09–11h 3, 12–14h 4, 15–17h 2, 18–20h 7, 21–23h 4.
- Ventana muerta: 01:00–05:59 no hay una sola operación en 4 semanas (Manu está en horario europeo/español: sus mediodías son nuestras mañanas).

## Uso en el sistema
- Latencia del espejo (instrumento #4): la flota corre 6:45–7:45 y Manu compra sobre todo entre 09:00 y 17:00 (Asunción) — el escaneo de la mañana lee sus compras de AYER, con 14–22 horas de retraso. Si el espejo quiere valer, necesita una lectura de tarde (15:30–18:00) del feed de Manu; hoy no existe.
- Se repite para unipcs, ether_monk y DCE cuando tengan pestaña en el Excel (el feed expone 100 filas como máximo, así que cada pestaña se arma por acumulación: MÉTRICAS-E anexa las operaciones nuevas cada mañana).
- No se opera con esto: es un dato de comportamiento de la ballena, no una señal.
