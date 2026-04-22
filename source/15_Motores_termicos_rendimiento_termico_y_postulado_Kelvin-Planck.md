(sec_heat_engines_efficiency_kelvin_planck)=
## Motores térmicos, rendimiento térmico y el postulado de Kelvin–Planck

La discusión precedente mostró que muchos procesos naturales, aunque plenamente consistentes con la **$1^{\text{a}}$ ley**, ocurren solo en **una dirección**.
Esta observación reveló la existencia de una restricción más profunda — la **$2^{\text{a}}$ ley** — que gobierna la *direccionalidad* y la *degradación* de las transformaciones energéticas.

Una de las manifestaciones más claras de esta limitación aparece cuando se utiliza el **calor** como medio para producir **trabajo**.
Aunque el trabajo puede transformarse íntegramente en calor, la transformación inversa — la conversión completa de calor en trabajo — **nunca se observa**.
Para analizar cuantitativamente esta limitación, introducimos el concepto de **motores térmicos**, los dispositivos mediante los cuales dichas transformaciones tienen lugar de forma cíclica.

Es a través del estudio de estos motores que la **$2^{\text{a}}$ ley** se formalizó por primera vez, y que sus consecuencias prácticas — en particular, el **postulado de Kelvin–Planck** — se hicieron evidentes.

---

(subsec_heat_engines_definition)=
### Motores térmicos: transformar calor en trabajo

Es fácil transformar **trabajo en calor**.
Por ejemplo, agitar un vaso de agua con una cuchara lo calienta: el trabajo mecánico aplicado mediante la fricción se convierte en energía interna, elevando la temperatura del fluido.
Tales transformaciones — de trabajo a calor — son directas y completas.

Sin embargo, el **proceso inverso** no es posible en su totalidad: no se puede convertir **todo el calor absorbido** en **trabajo mecánico**.
Para transformar una parte del calor en trabajo de manera **cíclica y controlada**, se requieren dispositivos especiales conocidos como **motores térmicos**.

A pesar de sus muchas formas tecnológicas — motores de combustión interna, turbinas de vapor, turbinas de gas o centrales eléctricas — todos los motores térmicos comparten el mismo **esquema conceptual**:

1. **Absorben calor** de un **foco térmico a alta temperatura**. Denotaremos este calor como $Q_{H}$.
2. **Convierten parte de ese calor en trabajo mecánico**. Este trabajo corresponde al trabajo neto entregado por el sistema, es decir, $W_{\text{out}}$.
3. **Rechazan el calor restante** a un **foco a baja temperatura**. Lo simbolizaremos como $Q_L$ asignándole el valor positivo de $Q_L = |Q_\text{out}|$.
4. Operan de forma **cíclica**, devolviendo su fluido de trabajo al estado inicial tras cada ciclo.

:::{important}

**CONDICIÓN CÍCLICA**

Como un motor térmico regresa a su estado termodinámico inicial tras cada ciclo, su **cambio neto de energía** es nulo:

$$
\Delta E_{\text{ciclo}} = 0.
$$

Los únicos intercambios energéticos que tienen lugar en el sistema son $Q_{H}$, $Q_{L}$ y $W_{\text{out}}$. En consecuencia, por la **$1^{\text{a}}$ ley**:

(eq_energetic_balance_heat_engine_ver1)=
$$
\Delta E_{\text{ciclo}} = 0 = Q_{\text{neto}} - W_{\text{neto}}
$$

Como:

(eq_energetic_balance_heat_engine_ver2)=
$$
\begin{gather*}
Q_{\text{neto}} = Q_{\text{in}} + Q_{\text{out}} = Q_{H} - Q_{L} , \\[10pt]
W_{\text{neto}} = W_{\text{out}} + W_{\text{in}} , \\[10pt]
\end{gather*}
$$

se obtiene:

(eq_energetic_balance_heat_engine_ver3)=
$$
\boxed{Q_H - Q_L = W_{\text{out}}} \ .
$$

:::

---

(subsec_impossibility_of_total_conversion)=
### Por qué la conversión total de calor en trabajo es imposible

En la discusión anterior establecimos que un **motor térmico** opera cíclicamente, intercambiando energía con el entorno de tres maneras distintas:

* **absorbe calor** de un foco a alta temperatura,
* **produce trabajo**,
* y **rechaza calor** a un foco a menor temperatura.

Esta estructura cíclica es esencial, porque la sustancia de trabajo debe regresar a su estado termodinámico inicial tras cada ciclo.

Preguntémonos ahora si el rechazo de calor es realmente inevitable.

:::{epigraph}
¿Podría diseñarse, en principio, un proceso cíclico en el que *todo* el calor absorbido se transformase en trabajo, sin dejar remanente que deba expulsarse?
:::

Imaginemos un sistema idealizado que recibe una cantidad finita de calor $Q_H$ de una fuente a alta temperatura y entrega una cierta cantidad de trabajo $W_{\text{out}}$ al entorno — por ejemplo, elevando un peso o moviendo una carga. Si el proceso ha de ser **cíclico**, el sistema debe terminar exactamente como empezó: misma temperatura, misma energía interna, misma configuración. Por la **$1^{\text{a}}$ ley**, el balance energético total a lo largo de un ciclo completo es

$$
Q_{\text{neto}} = W_{\text{neto}},
$$

de modo que, para una hipotética conversión completa de calor en trabajo,

$$
Q_H = W_{\text{neto}}, \qquad Q_L = 0.
$$

Sin embargo, para retornar a su estado inicial, el sistema debe liberar cualquier energía interna adquirida durante la transformación. Esto requiere un **flujo de calor en sentido inverso** desde el sistema hacia el entorno. Si el entorno estuviese a la misma temperatura que la fuente, tal transferencia implicaría que el calor fluyera *espontáneamente de un cuerpo más frío a uno más caliente* — una violación del sentido observado de los procesos naturales.

Por tanto, es **imposible** que un dispositivo cíclico restaure su estado inicial convirtiendo la totalidad del calor absorbido en trabajo. Para cerrar el ciclo, una porción del calor de entrada debe ser **rechazada** hacia otro cuerpo a **menor temperatura**, garantizando que el calor fluya en la dirección natural (del caliente al frío). Esta fracción expulsada $Q_L$ constituye la parte de la energía que ha quedado **degradada** — sigue presente, pero ya no está disponible para producir trabajo.

:::{note}

**UN EJEMPLO SENCILLO CON UN SISTEMA PISTÓN–CILINDRO**

Un **conjunto pistón–cilindro** proporciona un ejemplo simple y tangible del razonamiento general expuesto.
Supongamos que el cilindro contiene un gas inicialmente a $30 \ ^{\circ}\mathrm{C}$ y se pone en contacto con un **foco caliente** a $100 \ ^{\circ}\mathrm{C}$.
Durante la expansión, el gas absorbe **$100 \ \text{kJ}$** de calor y realiza **$15 \ \text{kJ}$** de trabajo al elevar una masa.

Incluso si el proceso es ideal — sin fricción, cuasiestático y perfectamente reversible — el gas queda más caliente que al inicio: no todo el calor absorbido se convierte en trabajo; una parte incrementa su energía interna.
Para **cerrar el ciclo**, el gas debe enfriarse de nuevo hasta $30 \ ^{\circ}\mathrm{C}$, recuperando su estado inicial.
Pero esto requiere liberar el **exceso de $85 \ \text{kJ}$** de energía hacia un **foco más frío** (por debajo de $30 \ ^{\circ}\mathrm{C}$), puesto que el calor no puede fluir espontáneamente de un cuerpo más frío a otro más caliente.

Así, incluso en este caso idealizado, **una parte del calor absorbido debe ser rechazada** — precisamente como dicta la **$2^{\text{a}}$ ley**. El remanente $Q_L = 85 \ \text{kJ}$ representa **energía degradada**, no disponible para su conversión en trabajo.

$$
Q_H = 100~\text{kJ}, \quad W_{\text{out}} = 15~\text{kJ}, \quad Q_L = 85~\text{kJ}.
$$

Este ejemplo ilustra de forma concreta la **limitación general** recién discutida: ningún proceso cíclico — por ideal que sea — puede transformar todo el calor absorbido en trabajo mecánico.

:::

:::{important}

**$Q_{L}$ COMO NECESIDAD TERMODINÁMICA**

Todo motor térmico debe **rechazar una porción del calor absorbido** hacia un foco a menor temperatura. Este rechazo no es un fallo técnico, sino una **necesidad termodinámica fundamental**, que expresa la direccionalidad de las transformaciones energéticas y constituye la manifestación directa de la **$2^{\text{a}}$ ley**.
:::

---

(subsec_efficiency_heat_engines)=
### Rendimiento térmico

La noción de **rendimiento térmico** solo tiene sentido para sistemas que se comportan como **motores térmicos** — esto es, dispositivos que operan **cíclicamente** intercambiando calor con **dos focos térmicos** a distinta temperatura. Tales motores absorben energía en forma de calor de la **fuente a alta temperatura**, convierten parte de ella en **trabajo mecánico**, y rechazan el resto hacia el **sumidero a baja temperatura** para completar el ciclo. El **rendimiento térmico** ($\eta$ o $\eta_\text{th.}$) cuantifica esta **capacidad de conversión** comparando la salida útil (trabajo neto) con la entrada de energía (calor absorbido del foco caliente).

(eq_efficiency_def)=
$$
\eta_{\text{th.}} = \frac{W_{\text{neto}}}{Q_H}.
$$

A partir del **balance energético cíclico** de cualquier motor, el trabajo neto producido es igual a la diferencia entre el calor absorbido $(Q_H)$ y el calor rechazado $(Q_L)$, este último en valor absoluto:

(eq_efficiency_substitution)=
$$
\eta_{\text{th.}} = \frac{Q_H - Q_L}{Q_H} = 1 - \frac{Q_L}{Q_H}.
$$

Esta relación simple expresa una limitación fundamental: solo la fracción de calor que *no se rechaza* puede convertirse en trabajo. El rendimiento depende, por tanto, de la razón entre los calores intercambiados con los focos a alta y baja temperatura.

:::{important}

**LA NOCIÓN GENERALIZADA DE RENDIMIENTO**

El **rendimiento**, en su sentido más general, expresa la **razón entre lo que un proceso entrega y lo que consume** — esto es, el efecto útil obtenido frente a la energía (o recurso) requerida para producirlo.
Sirve como **medida de desempeño**: cuanto más próximo a la unidad sea este cociente, con mayor eficacia convierte el proceso su entrada en la salida deseada.

Esta noción abstracta aplica a cualquier transformación — mecánica, eléctrica, térmica o de otro tipo — y proporciona un lenguaje común para comparar cómo distintos sistemas usan la energía.

En el caso específico de los **motores térmicos**, este concepto general se vuelve el **rendimiento térmico**, donde la salida útil es el *trabajo producido* y el coste es el *calor absorbido* de la fuente a alta temperatura.
:::

---

(subsec_kelvin_planck_postulate)=
### El postulado de Kelvin–Planck

Las conclusiones alcanzadas — la necesidad de dos focos térmicos y la imposibilidad de transformar completamente el calor en trabajo — se expresan de manera concisa mediante el **postulado de Kelvin–Planck**, una de las formulaciones fundacionales de la **$2^{\text{a}}$ ley** de la termodinámica.

:::{epigraph}
**Es imposible construir un dispositivo que opere en ciclo y produzca como único efecto la extracción de calor de un solo foco térmico y su conversión completa en trabajo.**
:::

Esta afirmación formaliza la limitación inherente a todos los motores térmicos: un **dispositivo cíclico** no puede transformar en trabajo la totalidad del calor que absorbe de una única fuente.
Una parte de esa energía debe ser siempre rechazada como calor hacia un foco a menor temperatura.

:::{important}

**IMPLICACIONES DE LA FORMULACIÓN DE KELVIN–PLANCK**

El postulado de Kelvin–Planck establece varias consecuencias fundamentales:

* Aunque un proceso que convirtiese todo el calor absorbido en trabajo **podría cumplir la $1^{\text{a}}$ ley**, **violaría** la **$2^{\text{a}}$ ley**.
* Un verdadero motor térmico debe intercambiar calor con **dos focos** a diferentes temperaturas — uno del que se absorbe calor $(Q_H)$ y otro al que se rechaza una parte de esa energía $(Q_L)$.
* El **rendimiento térmico** de tal motor, $\eta_{\text{th.}} = 1 - Q_L/Q_H$, es por tanto siempre **menor que la unidad**, es decir, $\eta_{\text{th.}} < 1$.
* Cuanto menor es la diferencia de temperatura entre los focos, menor es el rendimiento alcanzable. Aumentar esa diferencia mejora el desempeño, pero **ninguna diferencia finita puede dar $\eta_\text{th.} = 1$**.
:::

---

(subsec_conceptual_closure_heat_engines)=
### Cierre conceptual

* Un **motor térmico** es un sistema cíclico que transforma parte del calor absorbido de un **foco caliente** en **trabajo útil**, rechazando el resto a un **foco frío** para cerrar el ciclo.
* El **rendimiento térmico** $\eta_{\text{th.}} = 1 - Q_L/Q_H$ expresa la fracción de la entrada de calor que se convierte en trabajo, fijando una **medida cuantitativa** del límite de conversión.
* El **postulado de Kelvin–Planck** expresa el **límite cualitativo**: la conversión total de calor en trabajo en un proceso cíclico es **imposible**.
* Esta limitación surge porque la **transferencia de calor es intrínsecamente direccional**, fluye de manera natural del caliente al frío.
* El calor rechazado $Q_L$ constituye **energía degradada**, consecuencia inevitable de la pérdida de calidad de la energía durante la transformación.

En esencia, la **$2^{\text{a}}$ ley** introduce una **jerarquía de calidad energética**: aunque todas las formas de energía son equivalentes en cantidad (según la **$1^{\text{a}}$ ley**), no todas son **igualmente convertibles**.
Establece un **límite fundamental al rendimiento de todos los procesos cíclicos**, definiendo la direccionalidad de las transformaciones termodinámicas reales.
