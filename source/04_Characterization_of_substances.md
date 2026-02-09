(sec_characterization_of_substances)=
## Caracterización de las sustancias

Una vez establecidos los conceptos básicos de {ref}`equilibrio, escalas de temperatura y procesos <sec_equilibrium_temperature_processes>`,
el siguiente paso es comprender cómo se aplican estas nociones a los **materiales reales** que conforman los sistemas termodinámicos.
Cada sistema está formado por *sustancias*, y la tarea de la Termodinámica es caracterizar sus estados y transformaciones.

Las preguntas clave son:

* ¿Qué entendemos por *sustancia*?
* ¿Cómo podemos describir los *cambios de estado* que experimentan las sustancias?

---

(subsec_classification_substances)=
### Clasificación de las sustancias

Las sustancias se clasifican según su **composición química** y **homogeneidad**.

* **Sustancias puras**: composición química uniforme e invariable.

  * *Simple*: compuesta por un solo elemento químico (p. ej., $\text{H}_2$, $\text{O}_2$).
  * *Compuesta*: formada por más de un elemento (p. ej., $\text{H}_2\text{O}$, $\text{CO}_2$).

* **Mezclas**: combinaciones físicas de dos o más sustancias puras.

  * *Mezclas homogéneas*: composición uniforme en todo el volumen (p. ej., aire, soluciones acuosas).
  * *Mezclas heterogéneas*: composición variable espacialmente (p. ej., aceite y agua).

La **fase** de una sustancia se refiere a una región espacial donde sus propiedades físicas son uniformes.
En termodinámica, los *cambios de fase* implican siempre *cambios de estado* — ambas nociones se consideran sinónimas.

:::{note}
**FASES COMO DOMINIOS TERMODINÁMICOS**

Una *fase* define una región de uniformidad física tanto en composición como en propiedades.
Cuando una sustancia cambia de fase, su estado termodinámico cambia de manera discontinua.
:::

Aunque la Termodinámica puede describir cualquier fase de cualquier sustancia, aquí se hará énfasis en los **fluidos** — en particular los **gases** — ya que constituyen el medio de trabajo de la mayoría de los sistemas térmicos.

---



(subsec_state_postulate)=
### Postulado del estado

El estudio de los sistemas termodinámicos tiene como objetivo describir sus estados de equilibrio mediante propiedades medibles.
La pregunta central es: **¿cuántas propiedades independientes se requieren para definir el estado de un sistema?** Esto se responde con el **postulado del estado**, formulado por Kline y Köenig en 1957:

:::{epigraph}
El estado de equilibrio de un sistema queda completamente especificado cuando se conocen $n + 1$ variables termodinámicas independientes,
donde $n$ es el número de formas independientes de realizar trabajo cuasiestático y reversible sobre el sistema.
:::

En la práctica:

* Para la mayoría de los **fluidos**, la forma relevante de trabajo reversible es el **trabajo de compresión o expansión**.
* Un **sistema simple** es aquel que permite trabajo reversible de **una sola forma** (por ejemplo, variando su volumen).
* Los sistemas capaces de múltiples tipos de trabajo (eléctrico, elástico, magnético, etc.) son **sistemas compuestos**, pero estos pueden dividirse en subsistemas simples cuyo único trabajo reversible es del tipo compresión/expansión.

:::{important}
**COROLARIO DEL POSTULADO DEL ESTADO**

Los **sistemas simples compresibles** — el enfoque principal de este curso — requieren solo **dos propiedades independientes** para definir su estado de equilibrio.
:::

:::{note}
**VARIABLES INDEPENDIENTES**

Las propiedades elegidas para describir un estado deben ser *intensivas* (independientes del tamaño y la geometría del sistema) y *mutuamente independientes*.
Para sistemas de fluidos, las variables principales son **presión** ($p$), **volumen específico** ($v = 1/\rho$) y **temperatura** ($T$).
:::

---



(subsec_equation_of_state)=
### Ecuación de estado

Si cualquiera de las tres variables fundamentales ($p$, $v$, $T$) puede expresarse como función de las otras dos, el sistema queda completamente caracterizado y se cumple el **postulado del estado**. Tal relación se conoce como **ecuación de estado**.

(eq_general_state_equation)=
$$
f(p, v, T) = 0
$$

Esta expresión general define cómo se interrelacionan las propiedades termodinámicas de una sustancia.
Formas específicas de esta función — como el **modelo de gases perfectos** — se explorarán a continuación.

:::{tip}
**POR QUÉ IMPORTAN LAS ECUACIONES DE ESTADO**

Las ecuaciones de estado proporcionan el puente entre la teoría y la realidad medible.
Permiten calcular una propiedad (por ejemplo, la presión) a partir de otras (por ejemplo, temperatura y volumen específico),
conectando así el marco abstracto de la Termodinámica con los datos experimentales.
:::

---

(subsec_conceptual_closure_characterization_substances)=
### Cierre conceptual

* Las sustancias definen la base física de los sistemas termodinámicos; su composición y fase determinan cómo se comportan y transforman.
* El **Postulado del Estado** especifica cuántas variables independientes se requieren para describir completamente un sistema.
* Para los **sistemas simples compresibles**, dos propiedades intensivas independientes (comúnmente $p$, $v$ y $T$) son suficientes.
* Expresar una de estas propiedades como función de las otras dos da la **ecuación de estado**, el vínculo matemático entre magnitudes medibles.
* Estos principios proporcionan la base para el estudio de {ref}`Modelos de Gases <sec_models_gases>`,
  donde se introducen formas funcionales específicas de la ecuación de estado.

