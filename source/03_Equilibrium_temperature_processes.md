(sec_equilibrium_temperature_processes)=
## Equilibrio, escalas de temperatura y procesos

Esta sección se basa en los fundamentos introducidos en {ref}`la sección anterior <sec_magnitudes_properties>` y formaliza cómo los sistemas alcanzan el **equilibrio**, cómo definimos y medimos la **temperatura**, y cómo caracterizamos los **estados** y **procesos**.
El equilibrio termodinámico sirve como puente conceptual entre las propiedades observables y las leyes que gobiernan sus transformaciones.

---

(subsec_thermodynamic_equilibrium)=
### Equilibrio termodinámico

Un sistema está en **equilibrio** cuando no ocurren cambios medibles en sus propiedades macroscópicas mientras permanece aislado de su entorno.
En tal estado, todo posible desequilibrio interno — mecánico, térmico o químico — ha sido eliminado.

:::{important}
**SIGNIFICADO DE EQUILIBRIO**

El equilibrio termodinámico significa que el sistema ha alcanzado una condición en la que no ocurre evolución interna espontánea.
Representa un estado de **máxima estabilidad** bajo las restricciones dadas.
:::

De manera intuitiva, todos los sistemas tienden al equilibrio cuando se dejan sin perturbaciones.
Matemáticamente, esta tendencia natural se describe mediante la **Segunda Ley de la Termodinámica**, que introduce la **entropía ($S$)** como la magnitud que cuantifica cómo los sistemas evolucionan hacia el equilibrio.

Para verificar si un sistema está en equilibrio, debemos examinar los siguientes aspectos:

* **Equilibrio mecánico:** ausencia de movimiento relativo o fuerzas no balanceadas.
  Dado que la presión es fuerza por unidad de área, el equilibrio mecánico requiere que las presiones sean uniformes en todo el sistema. Tomando dos puntos arbitrarios ($1$ y $2$) en el sistema, debe cumplirse que $p_1 = p_2$.

* **Equilibrio térmico:** temperatura uniforme en todo el sistema y entre sistemas que interactúan ($T_1 = T_2$).

* **Equilibrio químico:** composición uniforme; las concentraciones químicas permanecen constantes en el tiempo ($\mu_{1} = \mu_{2}$).

Un sistema en equilibrio completo satisface simultáneamente las tres condiciones.

---











(subsec_zeroth_law)=
### Ley cero de la Termodinámica y definición empírica de la temperatura

Cronológicamente, la **ley cero** se formuló después de las demás leyes, pero es **más fundamental** porque permite definir la temperatura como una propiedad medible.

Puede enunciarse así:

:::{epigraph}
**Si dos sistemas están cada uno en equilibrio térmico con un tercer sistema, entonces están en equilibrio térmico entre sí.**
:::

Formalmente, si el sistema $A$ (a temperatura $T_A$) está en equilibrio con el sistema $B$ ($T_B$), y $B$ está en equilibrio con $C$ ($T_C$), entonces:

(eq_zeroth_law_consequence)=
$$
T_A = T_B \quad \text{y} \quad T_B = T_C \ \Longrightarrow \ T_A = T_C
$$

Esta propiedad transitiva implica que la temperatura es una **propiedad bien definida**, independiente del tamaño o la composición del sistema.
La ley cero no define una *escala numérica* para la temperatura, pero demuestra que **la temperatura es una propiedad que puede medirse** — legitima el concepto de **termómetro**.

La ilustración esquemática siguiente pretende representar la ley cero tal como se explicó. Como se observa, la concepción de esta ley permite definir la noción de termómetros.

:::{figure} 1_fundamentals_figs/schematic_zeroth_law.svg
:name: zeroth_law
:width: %
:align: center

Representación esquemática de la ley cero
:::

:::{note}
**SIGNIFICADO EMPÍRICO DE LA TEMPERATURA**

La temperatura es la **propiedad de estado en equilibrio** que determina si dos sistemas están en **equilibrio térmico** $\implies$ si dos sistemas están en equilibrio térmico, **comparten la misma temperatura**.
:::

---


(subsec_temperature_scales)=
### Escalas de temperatura

Una vez establecida la ley cero, podemos construir **escalas de temperatura** como protocolos comparativos.
Cualquier fenómeno físico reproducible que varíe monótonamente con la temperatura (como el volumen de un líquido, la resistencia de un hilo o la presión de un gas) puede servir como base para una escala.

La elección de una escala es convencional — coexisten múltiples escalas de temperatura, aunque dos son dominantes en ingeniería y ciencia.
``


(subsubsec_celsius_scale)=
#### La escala Celsius

La **escala Celsius** (símbolo $[^\circ\text{C}]$) fue propuesta por Anders Celsius, tomando como puntos fijos:

* el **punto de fusión del agua**, $0\ [^\circ\text{C}]$, y
* el **punto de ebullición del agua**, $100\ [^\circ\text{C}]$,

ambos medidos a presión atmosférica estándar ($1\ \text{atm} = 101325\ \text{Pa}$).

Su principal ventaja radica en su rango práctico: proporciona valores convenientes para fenómenos cotidianos.

---

(subsubsec_Kelvin_scale)=
#### La escala Kelvin

La **escala Kelvin** es la **escala termodinámica de temperatura**, que forma parte del Sistema Internacional (SI).
Está directamente relacionada con la escala Celsius mediante:

(eq_C_to_K)=
$$
T\left(\text{K}\right) = T\left(^\circ\text{C}\right) + 273.15
$$

William Thomson (Lord Kelvin) dedujo el concepto de **cero absoluto**, la temperatura a la cual el movimiento molecular cesaría teóricamente.
Este límite inferior, $0\ \text{K}$, corresponde a $-273.15\ [^\circ\text{C}]$.
Aunque el cero absoluto no puede alcanzarse (prohibido por la mecánica cuántica y la Tercera Ley), proporciona una referencia universal.

:::{important}
**TEMPERATURA ABSOLUTA**

La escala de temperatura absoluta es independiente de las propiedades del material.
El cero Kelvin representa el límite conceptual de reposo molecular completo, aunque la incertidumbre cuántica impide su realización.
Esta universalidad convierte a la escala Kelvin en la base para aplicaciones científicas e ingenieriles.
:::

:::{tip}
**UNIDADES Y NOTACIÓN**

La unidad de temperatura termodinámica es el **Kelvin** ($[\text{K}]$), no “grado Kelvin”.
El símbolo $^\circ$ se utiliza solo para la escala Celsius.
:::

---

(subsec_states_processes)=
### Estados y procesos

Tras haber introducido las magnitudes medibles básicas y la noción de equilibrio, podemos definir los conceptos fundamentales finales de la Termodinámica: **estados** y **procesos**.

Un **estado** representa el conjunto de condiciones físicas que describen un sistema en un momento dado — cada propiedad tiene un valor definido ($p$, $T$, $V$, etc.).
El estado de un sistema puede cambiar con el tiempo o permanecer constante:

* **Estado estacionario:** las propiedades no varían con el tiempo, $\frac{dX}{dt}=0$.
* **Estado transitorio:** las propiedades evolucionan con el tiempo, $\frac{dX}{dt}\neq0$.

Un **proceso** representa la *transición entre dos estados*.
Puede considerarse como una trayectoria que conecta un estado inicial $(1)$ y un estado final $(2)$.

:::{important}
**DEFINICIÓN DE PROCESO**

Un proceso termodinámico es cualquier transformación que lleva un sistema de un estado de equilibrio a otro.
La **trayectoria** seguida y el **tiempo** requerido para alcanzar el estado final definen el tipo de proceso.
:::

---

(subsubsec_relaxation_time)=
#### Tiempo de relajación

Cuando un sistema se perturba, necesita cierto tiempo para alcanzar un nuevo equilibrio.
Esta duración característica se conoce como **tiempo de relajación** ($\tau$).

Empíricamente:

* $\tau$ aumenta con el **volumen** del sistema ($V$); los sistemas más grandes tardan más en equilibrarse.
* $\tau$ disminuye con el **área de la superficie límite** ($A$); superficies mayores permiten un intercambio más rápido.

:::{tip}
**INTERPRETACIÓN DEL TIEMPO DE RELAJACIÓN**

Una bañera grande tarda más en calentarse debido a su mayor volumen,
pero aumentar la superficie de calentamiento reduce el tiempo necesario para alcanzar el equilibrio.
:::

---



(subsec_typical_processes)=
### Procesos termodinámicos típicos

Aunque existen innumerables procesos, solo unos pocos casos idealizados tienen importancia analítica:

1. **Procesos cíclicos (ciclos):**
   Transformaciones repetitivas que comienzan y terminan en el mismo estado.
   Ejemplos: ciclos de potencia y de refrigeración.

2. **Procesos cuasiestáticos (reversibles):**
   Transformaciones infinitamente lentas en las que el sistema permanece infinitesimalmente cerca del equilibrio en todo momento.
   En la práctica, ningún proceso es verdaderamente cuasiestático, pero esta idealización permite derivar relaciones fundamentales entre las variables de estado.

:::{important}
**CUASIESTÁTICO COMO LÍMITE IDEAL**

Un proceso cuasiestático no es real, pero sirve como **modelo de referencia**.
Como el equilibrio se mantiene en cada etapa, el sistema pasa por una serie continua de estados de equilibrio,
lo que hace posible definir e integrar sus propiedades termodinámicas.
:::

---

(subsec_equilibrium_temperature_processes_conceptual_closure)=
### Cierre conceptual

* El equilibrio significa ausencia de cambios macroscópicos.
* La ley cero define la temperatura como la propiedad que indica el equilibrio térmico.
* Las escalas de temperatura traducen este concepto en magnitudes medibles.

