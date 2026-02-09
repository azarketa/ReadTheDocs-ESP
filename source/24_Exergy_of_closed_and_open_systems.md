(sec_exergy_closed_open)=
## Exergía en sistemas cerrados y abiertos

Una vez definidos los conceptos de **trabajo útil**, **trabajo reversible** e **irreversibilidad**, estamos preparados para formalizar la **noción de exergía**.  
La exergía representa el **máximo trabajo teórico** que puede obtenerse cuando un sistema evoluciona **reversiblemente** desde un estado inicial dado hasta el **estado muerto**, es decir, la condición de **equilibrio termodinámico** con el entorno. Por tanto, cuantifica en términos energéticos la **calidad** de la energía de un sistema y la **degradación** causada por las irreversibilidades.

---

(subsec_exergy_closed)=
### Definición de exergía para un sistema cerrado

Para ilustrar la derivación de la exergía del modo más directo y transparente, resulta conveniente examinar un **sistema pistón–cilindro**. Esta configuración proporciona la **representación más simple de las interacciones mecánicas y térmicas** entre un sistema y su entorno: trabajo presión–volumen en una frontera móvil y transferencia de calor hacia/desde el ambiente. Sirve, por tanto, como un **paradigma del intercambio energético reversible**, permitiendo derivar el concepto de exergía explícitamente a partir de la **primera** y la **segunda ley**, antes de extenderlo a sistemas más complejos.

Consideremos así un **sistema pistón–cilindro** actuando como **fuente** de un **motor térmico**, inicialmente en condiciones $(p > p_0, T > T_0)$. Al expandirse **reversiblemente** hasta el **estado muerto** $(p_f = p_0, T_f = T_0)$, el sistema:

* Realiza **trabajo de frontera** $\delta W_{\text{b.,useful}}$,
* Libera una **cantidad de calor** $\delta Q$ que acciona el motor térmico,
* Permite que el motor entregue un **trabajo adicional** $\delta W_{\text{HE}}$.

Aplicando la **primera ley** al sistema cerrado:

$$
\delta E_{\text{in}} - \delta E_{\text{out}} = \mathrm{d}E_{\text{sys.}} 
\quad \Rightarrow \quad 
\delta Q - \delta W = \mathrm{d}U
$$

El **trabajo diferencial** ejercido en la frontera puede descomponerse como:

$$
\delta W = p\,\mathrm{d}V = (p - p_0)\mathrm{d}V + p_0\mathrm{d}V 
= \delta W_{\text{b.,useful}} + \delta W_{\text{surr.}}
$$

El **trabajo entregado por el motor térmico** que opera entre el sistema (a $T$) y el ambiente (a $T_0$) es:

$$
\delta W_{\text{HE}} 
= \left(1 - \frac{T_0}{T}\right)\delta Q
= \delta Q - T_0\frac{\delta Q}{T} 
= \delta Q - T_0\,\mathrm{d}S
$$

Sustituyendo y reordenando se obtiene el **trabajo útil total diferencial** recuperable del conjunto sistema + motor térmico:

(eq_exergy_differential)=
$$
\delta W_{\text{total,useful}} = -\mathrm{d}U - p_0 \mathrm{d}V + T_0\, \mathrm{d}S
$$

Integrando entre el estado inicial y el **estado muerto**:

(eq_exergy_closed)=
$$
W_{\text{total,useful}} = (U - U_0) + p_0 (V - V_0) - T_0 (S - S_0).
$$

Esta cantidad representa el **máximo potencial de trabajo útil** del sistema, alcanzable únicamente mediante un **proceso reversible**.

Sin embargo, esta formulación solo incluye **modos microscópicos de energía** ($U$, $S$, $V$). Para obtener la **exergía total**, deben añadirse las contribuciones **macroscópicas** de energía — cinética y potencial:

(eq_exergy_closed_total)=
$$
\boxed{X = (U - U_0) + p_0 (V - V_0) - T_0 (S - S_0) + \frac{m c^2}{2} + m g z}
$$

De forma equivalente, agrupando las energías interna, cinética y potencial en el término específico $E$:

(eq_exergy_closed_total)=
$$
\boxed{X = (E - E_0) + p_0 (V - V_0) - T_0 (S - S_0)}
$$

La **exergía** cuantifica así el **máximo trabajo útil** extraíble cuando el sistema se desplaza reversiblemente hacia el equilibrio con el entorno.  
Si el sistema ya está en el estado muerto y no posee energía cinética ni potencial, $X = 0$: **no puede obtenerse trabajo útil adicional**.

Expresando la exergía por unidad de masa se obtiene su forma **específica**:

(eq_exergy_specific_simplified)=
$$
\boxed{\phi = (e - e_0) + p_0 (v - v_0) - T_0 (s - s_0)}
$$

El **cambio de exergía específica** entre dos estados arbitrarios $(1)$ y $(2)$ es:

(eq_exergy_change_specific)=
$$
\boxed{\Delta \phi = \phi_2 - \phi_1 = (e_2 - e_1) + p_0 (v_2 - v_1) - T_0 (s_2 - s_1)}
$$

---

(subsec_exergy_open)=
### Definición de exergía para un sistema abierto

Al tratar con **sistemas abiertos**, la formulación adecuada debe incluir el **trabajo de flujo** — el trabajo requerido para empujar masa hacia dentro o fuera del sistema.

Si un fluido en movimiento ejerce presión $p$ al cruzar la frontera, la **exergía de flujo** es:

(eq_flow_exergy)=
$$
x_{\text{flow}} = (p - p_0)\,v
$$

Este término representa el **trabajo necesario para desplazar** el volumen de aire atmosférico ocupado por el fluido en movimiento.  
Desempeña aquí el mismo papel que el término $p_0(v - v_0)$ en la expresión para sistemas cerrados.

Sumando el término de flujo a la exergía del sistema cerrado se obtiene la **exergía específica para sistemas abiertos**:

(eq_exergy_open)=
$$
\boxed{\psi = (h - h_0) - T_0 (s - s_0) + \frac{c^2}{2} + g z}
$$

donde $h = u + pv$ es la entalpía específica. El **cambio de exergía específica** correspondiente es:

(eq_exergy_change_open)=
$$
\boxed{\Delta \psi = \psi_2 - \psi_1 = (h_2 - h_1) - T_0 (s_2 - s_1) + \frac{c_2^2 - c_1^2}{2} + g (z_2 - z_1)}
$$

---

(subsec_exergy_transfer_terms)=
### Mecanismos de transferencia de exergía

Dado que la exergía es una **cantidad transferible**, puede atravesar fronteras de sistema mediante **calor**, **trabajo** o **masa**.  
Los términos correspondientes son:

(eq_exergy_heat_work_mass)=
$$
\begin{aligned}
X_{\text{calor}} &= \left(1 - \frac{T_0}{T}\right) Q, \\[10pt]
X_{\text{trabajo}} &=
\begin{cases}
W - W_{\text{surr}}, & \text{para trabajo de frontera}, \\[6pt]
W, & \text{para otros modos de trabajo},
\end{cases} \\[10pt]
X_{\text{masa}} &= \dot{m}\,\psi.
\end{aligned}
$$

:::{important}

**INTERPRETACIÓN DE LOS MECANISMOS DE TRANSFERENCIA DE EXERGÍA**

Cada mecanismo de transferencia corresponde a un **potencial de trabajo útil**:

* La **exergía térmica** disminuye con el nivel de temperatura de la fuente.  
* La **exergía de trabajo** equivale a la parte *útil* del trabajo realizado.  
* La **exergía de masa** refleja el *estado energético y entrópico* transportado por la materia en movimiento.

:::

---

(subsec_conceptual_closure_exergy_closed_open)=
### Cierre conceptual

* La **exergía** representa el **máximo trabajo útil** que un sistema puede entregar al avanzar **reversiblemente** hacia el equilibrio con su **entorno** — el **estado muerto**.
* En **sistemas cerrados**, la exergía depende de las energías interna, cinética y potencial, así como de los términos $p_0V$ y $T_0S$ que expresan la desviación energética respecto al ambiente.
* En **sistemas abiertos**, la inclusión del **trabajo de flujo** y la **entalpía** refleja la capacidad de la **materia en movimiento** para transportar energía útil.
* La exergía transferida mediante **calor**, **trabajo** o **masa** representa el flujo de *potencial de trabajo* a través de las fronteras.
* Cuando un sistema alcanza el **estado muerto**, su exergía — y por tanto su capacidad de producir trabajo útil — **desaparece**.

En esencia, la exergía proporciona una **medida cuantitativa de la distancia entre un sistema y el equilibrio completo**. El siguiente paso es formalizar cómo este potencial disminuye en todos los procesos reales — conduciendo al **principio de la disminución de la exergía** y a la definición de **destrucción de exergía**.
