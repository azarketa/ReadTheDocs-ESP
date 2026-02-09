(sec_first_law_closed_systems)=
## $1^{\text{a}}$ Ley en sistemas cerrados

Hasta ahora, hemos establecido que la termodinámica describe cómo la energía se mueve y cambia de forma dentro y entre sistemas. Cuando tratamos con un **sistema cerrado**, la **masa permanece constante** — ninguna sustancia cruza la frontera del sistema. Sin embargo, la energía aún puede transferirse en forma de **trabajo** o **calor**. Esta sección formula la **$1^{\text{a}}$ ley de la termodinámica** para tales sistemas, expresando el balance entre almacenamiento de energía y transferencia de energía.

---

(subsec_energy_balance_closed_system)=
### Balance de energía para un sistema cerrado

Un **sistema cerrado** intercambia **energía**, pero no **masa**, con su entorno. O, mejor dicho: como ninguna masa puede cruzar la frontera de un sistema cerrado por definición, los únicos intercambios energéticos que pueden tener lugar son aquellos asociados a transferencias no másicas. Si, {ref}`como se indicó anteriormente <sec_energy_work_heat>`, la energía no se crea ni se destruye — solo se transforma — y los **únicos modos de transferencia no másica** son calor y trabajo, el balance total de energía se escribe como:

(eq_first_law_basic)=
$$
\Delta{}E{}={}Q{}-{}W,
$$

donde:

* $Q$ es el **calor neto** transferido *al* sistema,
* $W$ es el **trabajo neto** realizado *por* el sistema,
* $\Delta{}E$ es el **cambio total de energía** del sistema.

:::{note}

**SUPOSICIONES IMPLÍCITAS EN LA FORMULACIÓN DE LA $1^{\text{a}}$ LEY**

{ref}`La expresión anterior <eq_first_law_basic>` también asume, implícitamente, que:
* El cambio finito de energía, $\Delta{}E$, ocurre entre dos estados extremos $(1)$ y $(2)$. Formalmente, esto significa que la ecuación debería leerse como $\Delta{}E_{1\to2} = Q_{1\to2} - W_{1\to2}$, como se mencionó al {ref}`introducir el <subsec_state_properties_process_magnitudes_and_reference_states>` operador $\Delta$. Sin embargo, considerando que toda la formulación que sigue se refiere a diferencias entre dos estados extremos, esos subíndices se omitirán por claridad.
* La convención de signos {ref}`adoptada en este curso <subsec_the_sign_convention_work_heat>` es coherente con la forma en que las contribuciones de calor y trabajo aparecen en la ecuación.

| **Tipo de intercambio energético** | **Descripción** | **Signo de $Q$ o $W$** | **Efecto sobre la energía del sistema ($\Delta E$)** |
| :---------------------------------- | :----------------------------------- | :--------------------: | :--------------------------------------: |
| **Calor añadido al sistema**       | El sistema recibe calor (entrada de energía) |         $Q > 0$        |              $\Delta E > 0$              |
| **Calor liberado por el sistema**  | El sistema pierde calor (salida de energía)   |         $Q < 0$        |              $\Delta E < 0$              |
| **Trabajo realizado por el sistema** | El sistema realiza trabajo sobre el entorno |         $W > 0$        |              $\Delta E < 0$              |
| **Trabajo realizado sobre el sistema** | El entorno realiza trabajo sobre el sistema  |         $W < 0$        |              $\Delta E > 0$              |

:::

La variación total de energía del sistema puede descomponerse en sus componentes **macroscópicos** y **microscópicos**:

(eq_first_law_components)=
$$
\Delta{}E{}={} \Delta{}E_k{}+{}\Delta{}E_p{}+{}\Delta{}U{}={}Q{}-{}W,
$$

donde:

* $\Delta E_k$ corresponde al **cambio de energía cinética**,
* $\Delta E_p$ al **cambio de energía potencial**,
* $\Delta U$ al **cambio de energía interna**.

En ausencia de reacciones **químicas** o **nucleares**, $\Delta U$ representa únicamente **efectos térmicos** — es decir, variaciones en la temperatura del sistema.

:::{note}

**ENERGÍA DE FLUJO Y TRABAJO**

{ref}`Al presentar las formas de energía macroscópica <subsubsec_macroscopic_energy>`, uno de los tipos especificados fue la llamada **energía de flujo** $(pV)$. En sistemas cerrados, la energía de flujo no se almacena como parte del sistema; representa **trabajo de frontera** y, por tanto, aparece en $W$. Las formas de energía que permanecen *contenidas* dentro del sistema son la cinética, la potencial y la interna.
:::

---

(subsec_first_law_simplified)=
### Forma simplificada: cambios cinéticos y potenciales despreciables

Para la mayoría de los sistemas estacionarios (sin movimiento significativo ni cambio de altura), las variaciones de energía cinética y potencial son despreciables:

(eq_first_law_reduced)=
$$
\boxed{\Delta{}U{}={}Q{}-{}W} \ .
$$

Esta forma reducida — ampliamente utilizada en termodinámica — expresa que **todas las transferencias de energía como calor o trabajo** se manifiestan como **cambios en la energía interna**.  
Así, si un sistema cerrado recibe calor o realiza trabajo, su **temperatura** (y, por tanto, su energía interna) cambiará en consecuencia. Su forma diferencial es igualmente relevante:

(eq_first_law_reduced_diff)=
$$
\mathrm{d}U = \delta Q - \delta W \ \Rightarrow \ \boxed{\mathrm{d}U = \delta Q - p\mathrm{d}V} \ .
$$



:::{tip}

**INTERPRETACIÓN DE $\Delta U = Q - W$**

* Cuando $Q > W$, la **energía interna del sistema aumenta** (se calienta). El calor recibido supera el trabajo realizado por el sistema.
* Cuando $|-Q| > |-W|$, la **energía interna del sistema disminuye** (se enfría). La pérdida de calor supera el trabajo realizado sobre el sistema.
* Cuando $W > Q$, la **energía interna del sistema disminuye** (se enfría). El trabajo realizado por el sistema supera el calor recibido.
* Cuando $|-W| > |-Q|$, la **energía interna del sistema aumenta** (se calienta). El trabajo realizado sobre el sistema supera la pérdida de calor.

Este balance intuitivo ayuda a identificar la dirección del flujo de energía en procesos simples.
:::

---

(subsec_first_law_enthalpy)=
### $1^{\text{a}}$ ley: particularización con entalpía

La combinación de energía interna y el término de flujo, $pV$, aparece con tanta frecuencia que se define como una propiedad termodinámica separada: la **entalpía**:

(eq_enthalpy_def)=
$$
\boxed{H{}={}U{}+{}pV} \ .
$$

La **entalpía**, $H$, representa la **energía útil total** de un fluido, combinando la *capacidad térmica para realizar trabajo* (a través de $U$) y la *capacidad de flujo* ($pV$). Mientras que la energía interna $U$ refleja efectos relacionados con la temperatura, la entalpía incorpora tanto **temperatura** como **presión**, lo que la convierte en una medida más práctica en procesos que involucran fluidos y flujo.

Diferenciando la definición de $H$:

(eq_differential_enthalpy)=
$$
\mathrm{d}H{}={} \mathrm{d}U{}+{}p\mathrm{d}V{}+{}V\mathrm{d}p.
$$

Sustituyendo la **$1^{\text{a}}$ ley en su forma diferencial**, $\mathrm{d}U{}={} \delta Q{}-{}p\mathrm{d}V$, en esta expresión se obtiene:

(eq_heat_enthalpy_relation1)=
$$
\mathrm{d}H = \delta{}Q - p\mathrm{d}V + p\mathrm{d}V + V\mathrm{d}p \ \Rightarrow \ \boxed{\delta Q{}={} \mathrm{d}H{}-{}V\mathrm{d}p} \ .
$$

Esta relación proporciona un vínculo directo entre la **transferencia de calor** y el **cambio de entalpía**, destacando cómo las variaciones de $p$ y $V$ afectan el intercambio total de calor.

:::{note}

**POR QUÉ TIENE SENTIDO DEFINIR LA ENTALPÍA EN SISTEMAS CERRADOS**

En un **sistema cerrado**, no cruza masa la frontera, por lo que el término $pV$ **no** representa energía almacenada dentro del sistema — pertenece al término de **trabajo de frontera** en la expresión diferencial de la $1^{\text{a}}$ ley:

$$
\mathrm{d}U = \delta Q - \delta W = \delta Q - p\mathrm{d}V.
$$

Sin embargo, la {ref}`definición de entalpía <eq_enthalpy_def>` sigue siendo útil incluso para sistemas cerrados. Esto se debe a que, al diferenciar $H$, la derivada del producto $pV$ {ref}`introduce dos contribuciones <eq_differential_enthalpy>` que muestran que, aunque $p\mathrm{d}V$ ya aparece en el balance de energía, el término adicional $V\mathrm{d}p$ permite expresar la dependencia de la energía con la presión de forma más compacta.

Definir $H$ como $U + pV$ es, por tanto, una **conveniencia formal**: reorganiza los términos energéticos en una sola propiedad que simplifica formulaciones posteriores — especialmente cuando la presión se convierte en variable independiente — sin implicar la existencia de un nuevo almacenamiento de energía en el sistema.
:::

:::{note}

**SOBRE LA ENTALPÍA COMO PROPIEDAD TERMODINÁMICA**

Dado que la **entalpía** se define como una combinación específica de {ref}`dos propiedades de estado <eq_enthalpy_def>`, ella misma es una **propiedad de estado**. Tanto la energía interna $U$ como el producto $pV$ dependen únicamente del **estado termodinámico** — es decir, de variables medibles como presión, volumen y temperatura — no de la trayectoria seguida entre estados.

En consecuencia, la {ref}`diferencial de la entalpía <eq_differential_enthalpy>` es un **diferencial exacto**, lo que significa que los cambios en $H$ entre dos estados dependen únicamente de los extremos y no del proceso intermedio.

Esta naturaleza basada en propiedades es lo que permite que la entalpía, al igual que la energía interna, aparezca directamente en ecuaciones de estado y tablas termodinámicas.
:::

(worked_example_energy_balance)=
::::{important}

**EJEMPLO RESUELTO — BALANCE DE ENERGÍA EN DIFERENTES PROCESOS**

**Enunciado del problema**

Supongamos el mismo sistema y procesos analizados en {ref}`el ejemplo anterior <worked_example_boundary_work>`. Consideremos que, aunque cada trayectoria de proceso difiere, el **cambio neto en la energía almacenada** del sistema es igual al **trabajo realizado en el proceso adiabático**, es decir:

$$
\Delta E = -W_{\text{adiabático}} = -53{,}9\ \text{kJ}.
$$

El signo negativo indica que el sistema **pierde energía** por trabajo de expansión. Usando la **$1^{\text{a}}$ ley de la termodinámica** para un sistema cerrado:

$$
\Delta E = Q - W,
$$

determina la **transferencia de calor** $Q$ correspondiente para cada proceso a partir del trabajo conocido $W$.



**Síntesis**

Si $\Delta E$ se fija en $-53{,}9\ \text{kJ}$, entonces:

$$
Q = \Delta E + W = -53{,}9 + W.
$$

Como el sistema se expande en todos los casos ($W > 0$), parte de su energía almacenada se utiliza como trabajo mecánico.  
Para alcanzar la misma pérdida de energía en todos los procesos, la **transferencia de calor** requerida debe ajustarse en consecuencia.

---

**Datos del problema**

| Proceso               |          Relación          | $W$ [kJ] |
| :-------------------- | :------------------------: | -------: |
| Isocórico             |     $V = \text{const.}$    |     $+0{,}0$ |
| Isobárico             |     $p = \text{const.}$    |    $+89{,}0$ |
| Isotérmico            |     $T = \text{const.}$    |    $+61{,}7$ |
| Adiabático            |           $Q = 0$          |    $+53{,}9$ |
| Politrópico ($n=1{,}2$)  | $pV^{1{,}2} = \text{const.}$ |    $+65{,}0$ |

---

**Cálculos**

Para cada proceso,

$$
Q = \Delta E + W = -53{,}9 + W.
$$

| Proceso                   |         Relación         | $W$ [kJ] | $\Delta E$ [kJ] | $Q$ [kJ] | Interpretación                                            |
| :------------------------ | :----------------------: | -------: | --------------: | -------: | :-------------------------------------------------------- |
| Isocórico                 |     $V=\text{const.}$    |     $+0{,}0$ |           $–53{,}9$ |    $–53{,}9$ | Sin trabajo; toda la pérdida de energía como rechazo de calor. |
| Isobárico                 |     $p=\text{const.}$    |    $+89{,}0$ |           $–53{,}9$ |    $+35{,}1$ | El trabajo supera la pérdida de energía; requiere aporte de calor. |
| Isotérmico                |     $T=\text{const.}$    |    $+61{,}7$ |           $–53{,}9$ |     $+7{,}8$ | Pequeño aporte de calor compensa el trabajo mecánico.        |
| Adiabático                |           $Q=0$          |    $+53{,}9$ |           $–53{,}9$ |      $0{,}0$ | Caso de referencia: toda la pérdida de energía como trabajo de expansión. |
| Politrópico ${(n=1{,}2)}$     | $pV^{1{,}2}=\text{const.}$ |    $+65{,}0$ |           $–53{,}9$ |    $+11{,}1$ | Caso intermedio entre adiabático e isotérmico.       |

---

**Interpretación**

En este ejemplo, el **caso adiabático** sirve como referencia: toda la pérdida de energía del sistema se manifiesta como **trabajo**, sin transferencia de calor ($Q=0$). Para los otros procesos, lograr la misma disminución neta de energía ($\Delta E = -53{,}9\ \text{kJ}$) requiere diferentes intercambios de calor:

* En procesos con **mayor trabajo** (p. ej., isobárico), debe entrar calor al sistema para mantener el mismo cambio global de energía.
* En procesos sin trabajo (isocórico), toda la pérdida de energía ocurre como **rechazo de calor**.

Esto ilustra cómo la $1^{\text{a}}$ ley garantiza la coherencia entre transferencias de energía independientemente de la trayectoria del proceso.

---

**Visualización**

El gráfico de barras siguiente compara, para cada proceso, las contribuciones de **trabajo** $W$ y **calor** $Q$ que, en conjunto, producen la misma pérdida total de energía $\Delta E = -53{,}9\ \mathrm{kJ}$. Una línea discontinua horizontal marca $\Delta E$. Las barras por encima de la línea indican **aporte de calor**, mientras que las barras por debajo indican **rechazo de calor**.

![deltaE-diagram](1_fundamentals_figs/deltaE_diagram_worked_example_mod_.svg)

---

:::{tip}

**CONEXIÓN CON LOS CALORES ESPECÍFICOS**

Más adelante, cuando se introduzcan los **calores específicos**, veremos que $\Delta U$ y $\Delta H$ se relacionan directamente con los cambios de temperatura bajo condiciones de volumen y presión constantes. Esto hará que los diferentes requerimientos de calor en cada proceso sean previsibles a partir de propiedades térmicas medibles.

Sin embargo, dos casos límite en este ejemplo anticipan la lógica detrás de los calores específicos:

* En procesos **isocóricos**, el volumen del sistema es fijo ($\mathrm{d}V=0$), por lo que no se realiza trabajo ($\delta W=0$).  
  Todo el intercambio de energía ocurre como calor, $\delta Q = \mathrm{d}U$.  
  Esta es la base física para definir el **calor específico a volumen constante**, $c_v$.

* En procesos **adiabáticos**, el sistema está perfectamente aislado ($\delta Q=0$), por lo que no se intercambia calor. Cualquier variación de energía se manifiesta exclusivamente como **trabajo**, $\mathrm{d}U = -\delta W$. Aunque la adiabaticidad **no define** una capacidad calorífica, muestra el otro extremo: un proceso en el que un modo de transferencia se suprime por completo.

Juntas, estas dos restricciones — una eliminando el trabajo, la otra eliminando el calor — aclaran por qué los calores específicos se definen bajo condiciones *controladas e idealizadas*. Aíslan el efecto del cambio de temperatura sobre un único mecanismo de intercambio de energía, haciendo que el comportamiento térmico sea medible y comparable entre sistemas.
:::

::::

---

(subsec_conceptual_closure_firstlaw_closed)=
### Cierre conceptual
* Un **sistema cerrado** intercambia energía pero **no masa** con su entorno.
* La **$1^{\text{a}}$ ley** expresa el **balance de energía** entre almacenamiento interno y transferencia:
  $\Delta E{}={}Q{}-{}W$.
* Cuando los efectos cinéticos y potenciales son despreciables, basta con la forma simplificada $\Delta U{}={}Q{}-{}W$.
* La **entalpía**, $H{}={}U{}+{}pV$, surge de manera natural al tratar procesos a presión constante o en extensiones a sistemas abiertos.

