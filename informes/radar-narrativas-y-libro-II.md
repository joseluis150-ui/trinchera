# Radar de Narrativas (Sistema N) y Libro II "Mayores" — diseño 6/7-sep-2026

## A. Radar de Narrativas — definido el 6-sep 17:30, ampliado el 7-sep 22:30

**N0. Definición operativa.** Una narrativa es una frase de una línea que explica *por qué entra dinero*, con una moneda madre identificable y al menos 3 hijas vivas (>$1M). Si no se puede nombrar madre e hijas, no es narrativa: es un token que subió.

**N1. Fuentes (6 desde el 7-sep).**
1. fomo Trending top 20 — qué cadena / launchpad / par se repite (cluster, no ticker).
2. X, tesis escritas — lista de voces (smoothietrades, AJC, tomfastlane, lemonxest, PoorGoat_, Bankless): hilo >10K vistas con el token <$10M.
3. Prensa y conflicto — CoinDesk / Bitcoin.com / KuCoin blog: ¿un CEO, regulador o exchange habló esta semana?
4. Calendario — anuncios @BinanceWallet Alpha, listados, lockups (SPCX: 9-sep, 24-sep, 9-oct, 24-oct, 8-dic), eventos (Apple 9-sep 14:00).
5. Ballenas como voto — unipcs / ether_monk / DCE rotando *hacia un cluster*, no hacia un token.
6. **NUEVO 7-sep — Puentes (DefiLlama Bridges):** flujo neto de capital entre cadenas en 24h y 7d. Es la única fuente que anticipa la rotación (RH → Solana/Base el 6/7-sep) en vez de contarla después. Se lee todos los días en el escaneo FLUJOS-D.

**N2. Índice de Narrativa (0–100), todas las noches.** Dinero 30 (volumen 24h agregado de las hijas y % del top 20 de fomo) · Amplitud 20 (# hijas >$1M; # nacidas en 48h) · Madre 15 (sostiene tendencia >7 días) · Catalizador 20 (fecha concreta a ≤14 días; sin fecha = 0) · Voz 15 (tesis escritas, prensa, conflicto). Valores 6-sep: RH pares ~85 · infra RH ~70 · escalera Binance ~72 · SpaceX ~55 · blue chips ~50 · Musk/Solana ~30.

**N3. Fases.** ① Semilla (una madre, una tesis, hijas <$10M: aquí el 10x y aquí el −100%; entra la sonda) · ② Expansión (3–10 hijas, prensa cripto: mejor riesgo/retorno; madre + hija líder) · ③ Euforia (prensa mainstream, CEOs enojados, forks que mueren el mismo día: solo madre e infra) · ④ Agotamiento (madre −30% desde ATH con volumen cayendo y 3 hijas −50%: afuera) · ⑤ Segunda vida (catalizador nuevo).

**N4. Operar solo por narrativa.** Las 2 narrativas con mayor índice en fase ①–②; por narrativa tres fichas: madre, un vehículo de infraestructura, la hija líder. Rotar cuando el índice cae 20 puntos o la fase pasa a ④. Pregunta diaria: "¿la narrativa sigue viva?", no "¿el token sube?". El radar dice *dónde*, no *cuánto* ni *a qué precio*.

**N5. Registro.** `narrativas.csv` (fecha, narrativa, fase, índice, madre, hijas, catalizador+fecha, fuente de la tesis, voto ballena, flujo de puentes) y sección "Radar de Narrativas" en el dash. La autopsia diaria alimenta la columna `narrativa_madre`.

**N6. Nacimiento y muerte.** Nace: 2 tokens >$1M con el mismo tema en 48h + una tesis escrita + una madre nombrable. Muere: madre −30% desde ATH, volumen agregado cayendo 3 días, 3 hijas −50%.

**Ranking 6-sep 21:00 (de más a menos caliente):** MEME/AMC, PONS, BONER/HIMS (hirviendo) · CNPY, MarsCoin, SHROOM, AI/NVDA, PAIR (caliente) · ZZZ, ROBINVAULT, PENGU, TRUMP, CATE, SHIB, SPCX, Saylormoon/Clippy/fone (tibia) · JIMOTHY, QUBIT, MOO, CETS/ICOIN/PROLOGUE (fría) · CACHE/STOCKKIT/canasta BNB (muerta).

**Cambios del 7-sep.** Tema #1 de X rotó de AMC/MEME a **BONER/HIMS** (el CEO de Hims siguió a la cuenta del token, 6-sep 17:53). Sub-narrativa nueva **#1b: memes apareados contra CRIPTO vía StonkFun** (Solana): ZCAT/ZEC es la hija líder, STONK es su PONS. Explicación de la pausa RH: la red se paralizó el viernes 5-sep con volumen récord y no se podía vender (fuente: video de Manu 7-sep). Fantom Troupe único clan grande en rojo el 7-sep = capital saliendo del cluster RH.

## B. Libro II — "Mayores" (altcoins) — diseño 7-sep 22:00

Libro aparte de la trinchera, contabilidad separada, nunca mezclado. Reutiliza el framework de altcoins de José (FDV/MC, desbloqueos, TVL, dominancia, altseason) y el de ciclo de BTC (MVRV, Mayer, 200 semanas, M2, DXY, ETFs, zonas acumulación/neutral/distribución).

- **Universo:** BTC/ETH/SOL núcleo + 3–6 alts investigadas (arranque: ZEC, SUI, Canton). Solo activos con producto, ingresos o uso medible.
- **Alt Score 100:** A Tokenomics 25 (FDV/MC, desbloqueos 90d, inflación) · B Uso real 30 (fees/ingresos, TVL, usuarios activos y tendencia) · C Mercado 25 (fuerza relativa vs BTC, liquidez en exchanges grandes, distancia al ATH) · D Catalizadores 20 (upgrades con fecha, ETF/regulación, listados; desbloqueos en contra).
- **Régimen / semáforo de alts (NUEVO 7-sep):** OTHERS/BTC (todo menos el top 10, medido en BTC) + BTC.D + ETH/BTC. VERDE = OTHERS/BTC sube en la semana y BTC.D baja; ROJO = lo inverso; AMARILLO = mixto. Sin VERDE el libro compra solo BTC/ETH. Referencia: OTHERS/BTC cae desde enero 2022, piso junio 2025, sin ruptura al 7-sep.
- **Unidad de cuenta (NUEVO 7-sep):** el PnL del Libro II se mide en BTC, no en dólares. Ganarle al dólar y perder contra BTC = perder.
- **Ejecución:** 5–15% del capital del libro por activo; entrada en 3 tramos DCA en 2–4 semanas dentro de zona de acumulación (nunca en vela semanal); salida por zona de distribución o ruptura de tesis; stop de emergencia por cierre semanal −30% o desbloqueo grande; revisión semanal domingo, en el checkpoint.
- **Instrumentos:** `mayores.csv` (universo, score, zona, tramos), sección plegada en el dash con Marcador propio; la llamada se escribe antes y no se edita.
- **Capital:** no sale de la trinchera. Fuente designada: bot Pionex (~$690) tras el gate del 19-sep; DCA desde MPA si funciona. Primeras 2 semanas en papel.
- **Advertencia registrada:** la mayoría de las alts rinde peor que BTC en un ciclo; el 10x semanal no existe ahí; el juego es 3–5x anual acertando zona y activo.

## C. Escaneo nuevo FLUJOS-D (aprobado por José 7-sep 22:30)

Cuarto atajo diario (propuesto 7:45, después de Escaneo-B): D1 puentes DefiLlama por cadena (neto 24h/7d, ranking, variación vs ayer) · D2 OTHERS/BTC, BTC.D, ETH/BTC en TradingView + semáforo mecánico + alerta BTC $75,500 · D3 meta "apareados": fichas PONS y STONK, Trending top 10 por cadena, pares nuevos · D4 cruce (¿la cadena que recibe capital es la que domina el Trending?; unidad de cuenta BTC del día). Archivo: `flujos-D-[fecha]-[hora].txt`. Prompt: `prompts/FLUJOS-D_v1.txt`. Los prompts A/B/X siguen congelados (v5) hasta que José cierre su lista de ideas.
