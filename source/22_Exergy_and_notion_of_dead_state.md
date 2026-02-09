(sec_exergy_and_dead_state)=
## Exergía y la noción de estado muerto

Las **$1^{\text{a}}$** y **$2^{\text{a}}$ leyes de la termodinámica** expresan dos aspectos fundamentales, pero distintos, de todas las transformaciones físicas.

* La **$1^{\text{a}}$ ley** trata de la **cantidad de energía**, estableciendo que la energía se conserva: no puede crearse ni destruirse, solo transformarse.
* La **$2^{\text{a}}$ ley** trata de la **calidad de la energía**, indicando que todo proceso real genera **entropía**, que solo permanece constante bajo condiciones perfectamente reversibles.

Ambos principios distinguen entre **cuánta energía** existe y **cuán útil** es esa energía. Aunque la energía se conserva, su *utilidad* disminuye continuamente a medida que aumenta la entropía.

Como la entropía introduce una **dirección en el tiempo** — la “flecha” irreversible de los procesos naturales — la primera ley es un principio *cuantitativo*, mientras que la segunda es *cualitativa*. Sin embargo, estas magnitudes son **inconmensurables**: la energía se mide en **julios ($\text{J}$)**, mientras que la entropía se mide en **julios por kelvin ($\text{J}/\text{K}$)**. No pueden, por tanto, compararse ni combinarse directamente.

Esto plantea una pregunta fundamental:

:::{epigraph}
¿Puede la *calidad* de la energía — tal como la expresa la $2^{\text{a}}$ ley — traducirse a una **magnitud energética**?
:::

Si así fuera, podríamos cuantificar las **irreversibilidades** en términos de energía y evaluar cuánta de la energía total sigue siendo *útil* para producir trabajo.

La respuesta surge al combinar la $1^{\text{a}}$ y la $2^{\text{a}}$ leyes. De este modo obtenemos una nueva magnitud — la **exergía** — que mide el **máximo trabajo útil** que puede extraerse cuando un sistema evoluciona hasta alcanzar el equilibrio con su entorno. La exergía no es, por tanto, un principio independiente, sino una **propiedad derivada**, una síntesis de ambas leyes que expresa el *valor energético* de la energía misma.

No obstante, definir la exergía requiere comprender qué significa que un sistema esté en **equilibrio** con su entorno: este es el concepto de **estado muerto**.

::::{note}

**EXERGÍA Y DISPONIBILIDAD**

El concepto de **exergía** apareció inicialmente bajo el nombre de **disponibilidad**, reflejando un intento temprano de cuantificar cuánta energía de un sistema podía **convertirse en trabajo útil** bajo las condiciones impuestas por su **entorno**. Dicho de otra forma, la preocupación que llevó a concebir la noción de “disponibilidad” fue:

:::{epigraph}
¿Cuánta energía puede extraerse de un sistema situado en un entorno dado?
:::

La respuesta depende no solo del estado interno del sistema, sino también del estado de su entorno. Cuando ambos se hallan en **equilibrio completo** — el **estado muerto** — ningún proceso espontáneo puede ocurrir, y la energía del sistema, aunque presente, es **inútil**. Un ejemplo ilustrativo es la **atmósfera**: contiene una enorme cantidad de energía, pero no puede entregar trabajo mientras permanezca uniforme. Solo cuando existen **gradientes** de temperatura, presión o composición, un sistema posee **exergía** — el *potencial medible para producir trabajo*.

::::

---

(subsec_dead_state_and_work_potential)=
### El estado muerto y el potencial de trabajo

Un sistema se halla en su **estado muerto** cuando está en **equilibrio termodinámico completo con el entorno** — es decir, cuando no existen gradientes de temperatura, presión o potencial químico entre ellos. En ese punto, **no puede extraerse más trabajo** del sistema.

La **atmósfera** ilustra bien este concepto: aunque contiene una cantidad enorme de energía, un dispositivo en equilibrio con ella no puede extraer trabajo, ya que no existen diferencias de propiedades que explotar. Para generar trabajo, un sistema debe estar inicialmente **fuera del equilibrio**, con mayor temperatura, presión o algún otro potencial respecto al entorno.

Por tanto, extraer energía de un sistema significa extraer **energía organizada y útil** — aquella capaz de realizar **trabajo mecánico**. El **trabajo máximo** que puede obtenerse cuando un sistema pasa desde un *estado inicial* dado hasta el *estado muerto* se denomina su **potencial de trabajo**.

Formalmente, dado que el trabajo es una **función de trayectoria**, puede escribirse:

$$
W = f(\text{estado inicial}, \text{trayectoria del proceso}, \text{estado final})
$$

En un **análisis exergético**:

* El **estado inicial** está dado.
* El **estado final** es el **estado muerto**, en equilibrio con el entorno.
* La **trayectoria** se supone **reversible**, puesto que solo las transformaciones reversibles producen **trabajo máximo**.

Cualquier **irreversibilidad** dentro del sistema o en sus alrededores inmediatos reduce este máximo teórico, originando **destrucción de exergía**.

:::{important}

**SIGNIFICADO DE LA EXERGÍA**

La exergía cuantifica el **máximo trabajo útil** que puede obtenerse cuando un sistema evoluciona reversiblemente desde su estado inicial hasta el **estado muerto**. Representa el **límite superior** impuesto por las leyes termodinámicas — la frontera entre la porción *útil* y la *inútil* de la energía.
:::

---

(subsec_boundaries_and_dead_state_considerations)=
### Fronteras, irreversibilidades y consideraciones finales sobre el estado muerto

Al estudiar la **exergía**, es esencial definir con precisión qué se entiende por **sistema**, **alrededores** y **entorno**, ya que estas distinciones determinan **dónde aparecen las irreversibilidades** y **cómo se pierde potencial de trabajo**.

* Los **alrededores** comprenden todo lo que está fuera de la frontera del sistema.
* Los **alrededores inmediatos** son la parte de esos alrededores directamente afectada por el proceso — donde existen gradientes de temperatura, presión o velocidad.
* El **entorno** es el gran reservorio no perturbado que define las **condiciones de referencia** para el **estado muerto**.

Las irreversibilidades aparecen tanto **dentro del sistema** como en sus **alrededores inmediatos**, donde diferencias finitas de temperatura o presión impulsan transferencias de calor o masa. En estas zonas de no equilibrio se produce **generación de entropía** y, en consecuencia, **destrucción de exergía**.

El concepto de **exergía** va más allá de los sistemas que producen directamente trabajo mecánico. Incluso si un dispositivo no realiza trabajo de eje, mientras no esté en equilibrio con su entorno posee un **potencial para producir trabajo** — una capacidad almacenada de conversión energética útil.

En efecto:

* Si la **temperatura** del sistema supera la del entorno $(T_f > T_{\text{ent.}})$, podría operar un **motor térmico** entre ambos para producir trabajo.
* Si su **presión** es mayor que la presión ambiente $(P_f > P_{\text{ent.}})$, la expansión podría generar energía mecánica.
* Si el sistema posee **energía cinética**, **potencial** o **química**, estas formas también pueden convertirse en trabajo — por ejemplo, cuando existen diferencias de velocidad $(c_f > 0)$ o de altura $(z_f > 0)$.

Cuando todas estas diferencias desaparecen, el sistema alcanza el **estado muerto** — el equilibrio termodinámico total con el entorno, donde no puede obtenerse más trabajo. El proceso reversible que conduce al sistema desde su condición inicial hasta este equilibrio define el **trabajo útil máximo** que puede entregar: su **exergía**.

:::{important}

**LA FUNCIÓN DEL ESTADO MUERTO**

El **estado muerto** es la referencia universal para todas las evaluaciones de exergía. En él, no existen gradientes, no puede ocurrir ningún proceso espontáneo y no puede extraerse trabajo alguno. La exergía cuantifica, así, la distancia entre un sistema y el equilibrio — y mide el **potencial de trabajo** perdido a medida que el sistema se acerca a dicho estado.
:::

---

(subsec_conceptual_closure_exergy)=
### Cierre conceptual

* La **exergía** enlaza las dos leyes de la termodinámica, expresando la calidad de la energía en **términos energéticos**.
* El **estado muerto** define la condición de **equilibrio completo** con el entorno — donde el potencial de trabajo desaparece.
* El **trabajo reversible máximo** entre un estado inicial y el estado muerto constituye la **exergía** de un sistema.
* Las **irreversibilidades** reducen este máximo, dando lugar a **destrucción de exergía**.
* La exergía proporciona así una **medida cuantitativa** de cómo la degradación de la calidad de la energía se traduce en **ineficiencia energética** — cerrando el puente conceptual entre la $1^{\text{a}}$ y la $2^{\text{a}}$ leyes.
