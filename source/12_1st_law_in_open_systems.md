(sec_open_systems)=
## $1^{\text{a}}$ ley en sistemas abiertos

Mientras que la $1^{\text{a}}$ ley para **sistemas cerrados** expresa el balance entre la transferencia de energía como calor y trabajo ($\Delta E = Q - W$), los dispositivos de ingeniería reales rara vez operan de forma aislada.
**Turbinas**, **compresores**, **bombas**, **toberas** y **intercambiadores de calor** son todos ejemplos de **sistemas abiertos**, en los que **masa** y **energía** cruzan continuamente las fronteras del sistema.

El objetivo de esta sección es extender la $1^{\text{a}}$ ley a estos **sistemas de flujo**, comenzando con el principio de **conservación de la masa**, introduciendo el concepto de **trabajo de flujo**, y finalmente derivando la **ecuación de energía para flujo estacionario** expresada en términos de **entalpía**.

---

(subsec_mass_conservation_open_systems)=
### Conservación de la masa

El punto de partida en cualquier análisis de sistemas abiertos es la **ecuación de continuidad**, que expresa que la **tasa de cambio de masa** dentro de un volumen de control (VC) es igual a la **diferencia entre las tasas de masa que entran y salen**:

(eq_continuity_equation)=
$$
\frac{\mathrm{d}m_{\text{vc}}}{\mathrm{d}t} = \frac{\mathrm{d}m}{\mathrm{d}t}
= \sum_{\text{in}} \dot{m} - \sum_{\text{out}} \dot{m}.
$$

Esta ecuación es la formulación formal de la **conservación de la masa**. Como trabajaremos con volúmenes de control a lo largo de la formulación de ecuaciones que corresponden a sistemas abiertos, omitiremos el subíndice VC en adelante para mayor claridad, tal como se hace después de la primera igualdad {ref}`en la expresión anterior <eq_continuity_equation>`.

Si las propiedades del volumen de control **no cambian con el tiempo**, se dice que el sistema opera bajo **condiciones de estado estacionario**:

(eq_continuity_steady_state)=
$$
\frac{\mathrm{d}m}{\mathrm{d}t} = 0
\quad\Longrightarrow\quad
\sum_{\text{in}} \dot{m} = \sum_{\text{out}} \dot{m}.
$$

Un **sistema estacionario** es, por tanto, aquel en el que la **masa dentro del volumen de control permanece constante**, aunque las partículas individuales de fluido entren y salgan continuamente.
Esta suposición es válida para la mayoría de los dispositivos de ingeniería que trabajan bajo condiciones de diseño, donde los caudales de entrada y salida permanecen estables en el tiempo.

:::{important}

**UNA ENTRADA-UNA SALIDA (ESTACIONARIO)**

Con una entrada (1) y una salida (2) en estado estacionario,

(eq_continuity_single_inlet_outlet)=
$$
\boxed{\dot m_1 = \dot m_2 \equiv \dot m} \ ,
$$

lo que significa que **todo el flujo de masa que entra** por la entrada **debe salir** por la salida.
:::

:::{note}

**SIGNIFICADO DE ESTADO ESTACIONARIO**

Un estado estacionario no implica que el **flujo sea estático** — solo significa que, cuando se observa en el tiempo, las **propiedades promedio** (masa, presión, temperatura, etc.) dentro del volumen de control permanecen constantes.
:::

---

(subsec_flujo_work_notion)=
### La noción de trabajo de flujo

En sistemas cerrados, el trabajo se asocia con el movimiento de la frontera ($p\mathrm{d}V$). En sistemas abiertos, sin embargo, la masa cruza la superficie de control, y debe actuar una **fuerza de presión** para empujarla a través. Este esfuerzo mecánico requerido se denomina **trabajo de flujo** (o **energía de flujo**).

Considera un pistón imaginario empujando fluido hacia el sistema.
Si la cara del pistón tiene área $A$, la presión sobre el fluido es $p$, y la velocidad normal a la superficie es $V_\perp=c$, la fuerza y la potencia asociadas con la entrada son:

(eq_flujo_work)=
$$
F = p A,
\qquad
\dot{W}_\text{flujo} = Fc = pAc = \dot{m}(pv),
$$

donde $\dot{m} = \rho{}A{}c$ y $v = 1/\rho$ es el volumen específico.

Así, cada flujo de masa que cruza la frontera lleva una **tasa asociada de trabajo mecánico** igual a $pv$.

:::{important}

**SIGNIFICADO FÍSICO DEL TRABAJO DE FLUJO**

El trabajo de flujo representa el **esfuerzo de presión necesario para impulsar el fluido** a través de una frontera de control.
No es una forma independiente de energía, sino parte del **trabajo mecánico** involucrado en mantener el flujo estacionario a través del dispositivo.
:::

---



(subsec_first_law_open_systems)=
### Derivación de la $1^{\text{a}}$ ley para sistemas abiertos

Comenzamos con el **principio de balance**: la **tasa de cambio de energía en el volumen de control** es igual a la **tasa de energía que entra** menos la **tasa de energía que sale** (todas las tasas extensivas):

(eq_1st_law_open_systems_general)=
$$
\frac{\mathrm{d}E}{\mathrm{d}t} = \Big(\dot Q_{\text{in}} - \dot W_{\text{in}} + \sum_{\text{in}} \dot m e \Big) - \Big(\dot Q_{\text{out}} - \dot W_{\text{out}} + \sum_{\text{out}} \dot m e\Big),
$$

donde la **energía total específica** de una corriente de flujo es

(eq_total_energy_specific)=
$$
e = u + \frac{c^2}{2} + g z.
$$

Es conveniente definir las tasas de calor y trabajo **netas** para el volumen de control:

(eq_definitions_heat_work_rates_open_systems)=
$$
\dot Q \equiv \dot Q_{\text{in}} - \dot Q_{\text{out}}, \qquad \dot W \equiv \dot W_{\text{out}} - \dot W_{\text{in}}
$$

de modo que, siendo positivo el calor **hacia** el VC y el trabajo **desde** el VC:

(eq_1st_law_open_systems_simplified_ver1)=
$$
\frac{\mathrm{d}E}{\mathrm{d}t} = \dot Q - \dot W + \sum_{\text{in}} \dot m e - \sum_{\text{out}} \dot m e.
$$

---

(subsec_steady_state_open_systems_internal_energy)=
### Formulación en estado estacionario (basada en energía interna)

En un **proceso de flujo estacionario**, el contenido energético del volumen de control permanece constante en el tiempo:

(eq_condition_steady_state)=
$$
\frac{\mathrm{d}E}{\mathrm{d}t} = 0.
$$

Por tanto,

(eq_1st_law_open_systems_simplified_energy_terms)=
$$
\boxed{\dot{Q} - \dot{W} = \sum_{\text{out}} \dot{m} \left(u + \frac{c^2}{2} + g z\right) + \sum_{\text{in}} \dot{m} \left(u + \frac{c^2}{2} + g z\right)} \ .
$$

:::{important}

**UNA ENTRADA-UNA SALIDA (FORMA ESPECÍFICA, BASADA EN ENERGÍA)**

Con $\dot m_1=\dot m_2=\dot m$ y dividiendo por $\dot m$,

(eq_1st_law_open_systems_simplified_energy_terms_single_inlet_outlet)=
$$
\boxed{q - w = \big(u_2 - u_1\big) + \frac{c_2^2 - c_1^2}{2} + g(z_2 - z_1)} \ .
$$

:::

---

(subsec_steady_state_open_systems_enthalpy)=
### Formulación en estado estacionario (basada en entalpía)

En la mayoría de los dispositivos de sistemas abiertos, no todo el trabajo mecánico resulta de empujar el fluido a través de las fronteras. Parte aparece como **potencia mecánica útil** transmitida mediante un eje giratorio, como en **turbinas**, **compresores** o **bombas**. Este componente se denomina **trabajo de eje**, y junto con el **trabajo de flujo** constituye la interacción mecánica total a través de la frontera del sistema. Así, la tasa total de trabajo contiene partes de **eje** y **flujo**:

(eq_decomposition_work_contributions_open_systems)=
$$
\dot W = \dot W_{\text{eje}} + \dot W_{\text{flujo}}, \qquad \dot W_{\text{flujo}} = \sum \dot m pv.
$$

Sustituyendo y reagrupando (moviendo el trabajo de flujo a las energías de las corrientes) se obtiene la **forma general no estacionaria** en variables de energía interna:

(eq_1st_law_open_systems_simplified_ver2)=
$$
\frac{\mathrm{d}E}{\mathrm{d}t} =\dot Q - \dot W_{\text{eje}} +\sum_{\text{in}}\dot m\left(u + pv + \frac{c^2}{2}+g z\right)
-\sum_{\text{out}}\dot m\left(u + pv + \frac{c^2}{2}+g z\right).
$$

Como $h \equiv u + p v$, el balance estacionario se convierte en

(eq_1st_law_open_systems_enthalpy_terms)=
$$
\boxed{\dot Q - \dot W_{\text{eje}} = \sum_{\text{out}} \dot m \left(h + \frac{c^2}{2} + g z\right) + \sum_{\text{in}} \dot m \left(h + \frac{c^2}{2} + g z\right)} \ .
$$



:::{important}

**UNA ENTRADA-UNA SALIDA (FORMA ESPECÍFICA, BASADA EN ENTALPÍA)**

Con $\dot m_1=\dot m_2=\dot m$ y dividiendo por $\dot m$,

(eq_1st_law_open_systems_enthalpy_terms_single_inlet_outlet)=
$$
\boxed{q - w_{\text{eje}} = (h_2 - h_1) + \frac{c_2^2 - c_1^2}{2} + g(z_2 - z_1)} \ .
$$

:::

::::{important}

**FORMULACIÓN COMPARATIVA DE SISTEMAS CERRADOS Y ABIERTOS**

| **Formulación** | **Sistema cerrado** | **Sistema abierto en flujo estacionario (una entrada-una salida cuando aplica)** |
| :-  | :-  | :- |
| **Forma general de la $1^{\text{a}}$ ley** | $\displaystyle \Delta{}E = \Delta{U} + \Delta{E_{\text{k}}} + \Delta{E_{\text{p}}} = Q - W$ | $\displaystyle \dot{Q} - \dot{W} = \sum_{\text{out}} \dot{m} \left(u + \frac{c^2}{2} + g z\right) + \sum_{\text{in}} \dot{m} \left(u + \frac{c^2}{2} + g z\right)$ <br/> $\displaystyle \dot{Q} - \dot{W}_{\text{eje}} = \sum_{\text{out}} \dot{m} \left(h + \frac{c^2}{2} + g z\right) + \sum_{\text{in}} \dot{m} \left(h + \frac{c^2}{2} + g z\right)$ |
| **Componentes del trabajo** | Solo trabajo de frontera $\displaystyle \int p\mathrm{d}v$ | Trabajo de eje $\displaystyle \left(-\int v\mathrm{d}p \right)$ + trabajo de flujo $(\Delta(pv))$|
| **Forma específica** | $\displaystyle \Delta{u} + \Delta{e_{\text{k}}} + \Delta{e_{\text{p}}} = q - w$ | $\displaystyle q - w = (u_2 - u_1) + \tfrac{c_2^2 - c_1^2}{2} + g(z_2 - z_1)$ <br/> $q - w_{\text{eje}} = (h_2 - h_1) + \tfrac{c_2^2 - c_1^2}{2} + g(z_2 - z_1)$ |
| **Ejemplos típicos**  | Pistón–cilindro, tanque rígido | Compresor, turbina, difusor, tobera, intercambiador de calor, mezclador, válvula|


:::{note}

**FORMA DIFERENCIAL DEL TRABAJO DE EJE**

Debido a la {ref}`relación de descomposición del trabajo <eq_decomposition_work_contributions_open_systems>`, dicha relación puede escribirse para transferencias diferenciales de energía tipo trabajo. Como $\delta{}w=p\mathrm{d}v$ en sistemas compresibles simples, y $\delta{}w_{\text{flujo}}=\mathrm{d}(pv)$

(eq_eje_work_expression)=
$$
\delta{}w = \delta{}w_{\text{eje}} + \delta{}w_{\text{flujo}} \implies p\mathrm{d}v = \delta{}w_{\text{eje}} + \mathrm{d}(pv) = \delta{}w_{\text{eje}} + p\mathrm{d}v + v\mathrm{d}p \implies
$$

$$
\implies \boxed{\delta{}w_{\text{eje}} = -v(p)\mathrm{d}p} \ , \qquad \boxed{w_{\text{eje}} = -\int_{p_1}^{p_2} v(p)\mathrm{d}p} \ .
$$

:::

::::

---

(subsec_conceptual_closure_open_systems)=
### Cierre conceptual

La $1^{\text{a}}$ ley para sistemas abiertos muestra cómo se aplica la conservación de la energía cuando **masa** y **energía** cruzan las fronteras del sistema. Sus ideas clave pueden resumirse así:

* **Conservación de la masa** — En estado estacionario, la masa que entra y sale del volumen de control es la misma, asegurando que no haya acumulación neta.
* **Trabajo de flujo** — Debe actuar una fuerza de presión para impulsar el fluido a través de cada frontera; este esfuerzo mecánico acompaña a cada flujo de masa.
* **Tipos de trabajo** — El trabajo total se divide en **trabajo de eje**, que representa potencia mecánica útil, y **trabajo de flujo**, que representa la energía transportada con el flujo de masa.
* **Operación estacionaria** — En condiciones estacionarias, las interacciones de calor y trabajo de eje equilibran exactamente los cambios de energía entre las corrientes de entrada y salida.
* **Rol de la entalpía** — Combinar energía interna y trabajo de flujo en **entalpía** simplifica el análisis de sistemas abiertos, facilitando la expresión de balances energéticos.

En resumen, la energía sigue conservándose, pero en sistemas abiertos se mueve no solo como calor o trabajo, sino también **con la masa** que fluye continuamente a través del volumen de control.

