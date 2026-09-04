# Embudo de la Cantera — protocolo de captura y maduración
**Creado 4-sep-2026 20:45. Nace de un hallazgo del barrido de cantera de esa tarde.**

## El problema que resuelve

La regla 10 (semillero propio) pide un token con una ventana muy específica: **más de 48 horas
de vida, todavía chico, con narrativa identificable y sin vetos estructurales.**

Ninguna pantalla de fomo muestra esa ventana:

| Pantalla | Qué muestra | Por qué no sirve |
|---|---|---|
| Graduated | tokens de segundos a 2 horas | reprueban el filtro de >48h |
| Trending  | lo que ya corrió | reprueban la regla 2 (vela >+40%) |
| Most held | los grandes | fuera de escala |
| Leaderboard | quien ya cobró | premia distribuidores, no sembradores |

Por eso la regla 10 nunca se estrenó desde que se firmó el 2-sep: **no faltaban candidatas,
faltaba dónde mirarlas.** El embudo construye esa pantalla nosotros mismos.

## Cómo funciona

### DÍA 0 — captura barata, sin análisis
Del listado *Graduated* se fichan los graduados del día. **No se analizan.** Se anota solo lo
que la pantalla ya muestra: token, edad, MC, volumen, % del día. Más una única marca de
criterio: **bandera copycat**.

La bandera copycat se aplica en el acto porque la regla 10 la veta sin apelación: marcas
registradas (Coca Cola, Redbull, POKEMON), tickers imitados (USDG), copias de tokens vivos
(CLANKSEN de Clanker, KEYCAT de Keycat, fone de apeonfone) y memes preexistentes.

Costo: una fila por token, sin abrir ninguna ficha. Es una línea más del escaneo de la flota.

### DÍA 3 — re-evaluación, ahí sí con criterio
Al tercer día el token ya cumple las 48 horas y tiene historia de precio. Recién ahí se
completa la ficha: MC contra el día 0, liquidez %, top 10 %, holders, % 24h, si viene de una
vela >+40%, y si tiene narrativa identificable (macro → conector → fundador).

**Veredictos posibles:**
- `candidata-semilla` — pasa todo → sube al Observatorio y queda disponible para la regla 10
- `observacion` — pasa estructura pero le falta narrativa → se re-mira al día 7
- `baja` — murió, reprueba un veto, o sigue siendo vela

### PROMOCIÓN
Solo las `candidata-semilla` entran al Observatorio. El embudo **nunca genera una compra
por sí mismo**: entrega candidatas, y la regla 10 decide.

## Reglas del embudo

1. **Ninguna fila se borra ni se edita hacia atrás.** El día 3 se completa la fila existente.
2. **El día 0 no juzga.** Solo la bandera copycat, que es mecánica.
3. **Nada se compra desde el embudo el mismo día que se captura.** La ventana de 48h es el
   punto entero del instrumento.
4. **Los muertos se quedan escritos.** El valor estadístico está en la tasa de mortalidad,
   no en los sobrevivientes.

## Para qué sirve el acumulado

La enmienda 3 del 4-sep (semillero de 2 a 4 semillas, con candidatas elegidas *desde el CSV
por perfil estadístico y no por corazonada*) tiene una condición de arranque:
**≥10 tokens con 7 días de seguimiento continuo, de los cuales ≥3 con movimiento >100%.**

Con ~20 capturas diarias, el embudo cumple esa condición alrededor del **11-sep**. Sin él,
no se cumple nunca — que es exactamente lo que venía pasando.

## Primera cosecha — 4-sep 20:45

20 tokens capturados. **10 vetados en el acto por copycat (50%).** Sobreviven 10 al día 3.

Dos observaciones de la primera camada, anotadas antes de que el sesgo retrospectivo las borre:

- **19 de 20 son velas verticales** (+668% a +9,774% en su primer día). El único en rojo es
  AGI (-25.43%) y el único con porcentaje contenido es SQUEEZE (+56.39%). Si al día 3 los
  sobrevivientes son los que NO hicieron la vela más grande, es un hallazgo con valor.
- **Apareció un copycat de `fone`** — nuestro mapa 9, muerto ayer por stop estructural — a
  $203.3K. Los copycats brotan cuando el original muere. Es una señal de tope de narrativa,
  no una oportunidad.
