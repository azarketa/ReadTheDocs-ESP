(sec_reversible_irreversible_processes)=
## Procesos reversibles e irreversibles

Los procesos termodinámicos pueden darse de dos formas fundamentalmente distintas, según puedan deshacerse por completo o no. Esta distinción se encuentra en el núcleo de la **$2^{\text{a}}$ ley**, pues separa el **comportamiento idealizado** (reversible) del **comportamiento real** (irreversible).

---

(subsec_definition_reversibility)=
### Definición de reversibilidad

Un **proceso reversible** es aquel que puede *deshacerse completamente*: tanto el sistema como sus alrededores podrían, en principio, regresar a sus estados originales **sin ningún cambio macroscópico neto** en el entorno. Tales procesos deben desarrollarse **infinitamente despacio** (cuasiestáticamente) y **sin efectos disipativos** — es decir, sin fricción, viscosidad, turbulencia, resistencia eléctrica o diferencias de temperatura finitas durante la transferencia de calor.

Por el contrario, un **proceso irreversible** es aquel que **no puede invertirse** sin dejar alguna huella permanente en los alrededores. En estos procesos, la **disipación** es inevitable: fricción, flujo viscoso, mezclado espontáneo, expansión no restringida o transferencia de calor a través de diferencias de temperatura finitas contribuyen a la irreversibilidad de los fenómenos reales.

:::{important}

**LA REVERSIBILIDAD COMO IDEALIZACIÓN**

Los procesos reversibles son **constructos ideales**. No ocurren en la práctica, pero sirven como **límites teóricos** que los procesos reales — irreversibles — solo pueden aproximar, nunca alcanzar.
:::

---

(subsec_internal_external_reversibility)=
### Reversibilidad interna y externa

La reversibilidad puede considerarse desde dos puntos de vista complementarios:

* Un proceso se dice **internamente reversible** si *no ocurren efectos disipativos dentro del propio sistema*. El sistema atraviesa una secuencia de estados de equilibrio, y todas sus interacciones internas (mecánicas, térmicas, etc.) son ideales y sin pérdidas.

* Un proceso es **externamente reversible** si las **interacciones entre el sistema y sus alrededores** — aquellas a través de la **frontera** — ocurren **sin gradientes finitos** ni **cambios netos** en el entorno. Por ejemplo, la transferencia de calor entre el sistema y sus alrededores debe producirse mediante una **diferencia de temperatura infinitesimal** para ser externamente reversible. Por el contrario, si el calor fluye a través de una **diferencia de temperatura finita**, el proceso se vuelve **externamente irreversible**, incluso si permanece **internamente reversible** dentro del sistema.

En la práctica, muchos procesos reales pueden ser **internamente reversibles** (si el sistema se idealiza como libre de fricción interna, turbulencias o viscosidad), pero **externamente irreversibles**, ya que los intercambios de calor o trabajo con el entorno ocurren a través de **gradientes finitos de temperatura o presión** que dejan un cambio apreciable en los alrededores.

:::{note}

**EJEMPLO DE UN PROCESO IRREVERSIBLE**

Considera una **lata de refresco** inicialmente a $5 \ ^{\circ}\mathrm{C}$ colocada en una habitación a $20 \ ^{\circ}\mathrm{C}$. El calor fluye de forma natural del aire más cálido hacia la lata más fría hasta que ambos alcanzan la misma temperatura. Para devolver la lata a su estado inicial, haría falta un **refrigerador**, que extrae calor de la lata y lo expulsa al aire de la habitación.

Al finalizar esta restauración, la lata recupera su estado inicial, pero la **habitación se ha calentado ligeramente** — ha absorbido el calor rechazado por el refrigerador. Por tanto, aunque el sistema (la lata) retorna a su condición inicial, el **entorno no lo hace**. El proceso global es, por tanto, **irreversible**.

No obstante, la **transferencia de calor dentro de la lata** — es decir, dentro de los límites del sistema — puede aproximarse como **internamente reversible** si ocurre cuasiestáticamente y sin disipación. La **irreversibilidad** del proceso proviene de la **diferencia finita de temperatura** entre la lata y la habitación, es decir, de la **interacción externa** entre el sistema y su entorno.

:::

---

(subsec_interest_reversibility)=
### Por qué importa la reversibilidad

Aunque los procesos reversibles son idealizaciones, distinguirlos de los irreversibles es esencial por dos razones principales:

1. **Simplicidad analítica:**  
   Los procesos reversibles evolucionan **cuasiestáticamente**, pasando por una serie continua de estados de equilibrio. Esto los hace **matemáticamente tratables** y permite aplicar las relaciones termodinámicas exactamente en cada punto del proceso.

2. **Referencias teóricas:**  
   Los procesos reversibles sirven como **límites de referencia** para los sistemas reales:

   * En **motores térmicos**, proporcionan el **máximo rendimiento posible**.  
   * En **ciclos de refrigeración y bombas de calor**, requieren el **mínimo trabajo posible**.

Así, los procesos reversibles definen los **límites superior e inferior del desempeño** de todos los ciclos termodinámicos prácticos, proporcionando el estándar frente al cual se mide el **comportamiento real e irreversible**.

:::{note}

**LA IRREVERSIBILIDAD GLOBAL O UNIVERSAL**

Como siempre puede definirse un sistema mayor que incluya tanto el **sistema original como su entorno**, es conceptualmente posible encerrar *todas las interacciones* dentro de un único **sistema aislado** — el llamado **universo termodinámico**. En esta visión global, no existe distinción entre irreversibilidad interna y externa: cualquier efecto disipativo, ya sea dentro del sistema o en su frontera, contribuye a la **irreversibilidad total** del universo.

Esta idea conduce directamente a una de las implicaciones más profundas de la **$2^{\text{a}}$ ley**: la **irreversibilidad total del universo aumenta** con cada proceso real, y **ninguna transformación natural puede ocurrir de manera perfectamente reversible** cuando se analiza en su conjunto.

:::

---

(subsec_conceptual_closure_reversibility)=
### Cierre conceptual

* Los **procesos reversibles** son transformaciones **idealizadas** que pueden deshacerse sin dejar ningún cambio macroscópico en los alrededores. Avanzan **cuasiestáticamente** y **sin disipación**, permitiendo que el sistema atraviese continuamente estados de equilibrio.
* Los **procesos irreversibles**, en contraste, son **reales** y **espontáneos**: involucran fricción, viscosidad, turbulencia o gradientes de temperatura finitos que impiden reconstruir exactamente el estado inicial.
* La distinción entre **reversibilidad interna** y **externa** aclara si la disipación se produce dentro del sistema o en su frontera con el entorno. En la realidad, la mayoría de los procesos son internamente reversibles pero externamente irreversibles.
* Aunque la reversibilidad perfecta es inalcanzable, los **modelos reversibles** proporcionan **límites teóricos de referencia** — definiendo el **máximo rendimiento** de los motores térmicos y el **mínimo trabajo requerido** por los ciclos de refrigeración.

En esencia, la reversibilidad marca el **límite ideal** de perfección termodinámica, mientras que la **$2^{\text{a}}$ ley** nos recuerda que los **procesos reales siempre conllevan un coste irreversible** — la firma del sentido termodinámico del tiempo.
