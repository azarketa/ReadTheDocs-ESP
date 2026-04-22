(sec_isoentropic_efficiency)=
## La eficiencia isoentrópica

El **rendimiento térmico** mide cuán eficazmente un sistema *cíclico* convierte calor en trabajo. Una vez que la **segunda ley** se extendió mediante la **desigualdad de Clausius**, el concepto de **irreversibilidad** pudo aplicarse a transformaciones individuales *no cíclicas*. Esto permitió definir la **eficiencia isoentrópica** — una medida de cuán cerca se encuentra un proceso real respecto al **límite ideal reversible (isoentrópico)**.

Mientras que el **rendimiento térmico** aplica a **ciclos completos entre focos térmicos**, la **eficiencia isoentrópica** aplica a **procesos individuales**, abiertos o cerrados, siempre que pueda definirse una **trayectoria isoentrópica de referencia** entre las mismas presiones de entrada y salida.

---

(subsec_isoentropic_irreversibility)=

### La eficiencia isoentrópica como medida de irreversibilidad

A partir de la **desigualdad de Clausius**, todo proceso satisface:

$$
s_2 - s_1 \ge \int_1^2 \frac{\delta q}{T},
$$

y la igualdad se cumple solo para procesos **reversibles**. Si, además, el proceso es **adiabático** ($\delta q = 0$), entonces

$$
\Delta s = 0,
$$

y la transformación es **isoentrópica**, definiendo el *límite ideal* de comportamiento.

Para cuantificar cuán lejos está un proceso real de este límite, comparamos dos transformaciones entre **las mismas presiones de entrada y salida**, una condición operativa habitual en dispositivos abiertos en flujo estacionario:

* El proceso **real (irreversible)**, subíndice **a**, termina en $(h_{2a}, s_{2a})$.
* El proceso **isoentrópico (ideal)**, subíndice **s**, termina en $(h_{2s}, s_{2s}=s_1)$.

Ambos parten de las mismas condiciones de entrada $(p_1, T_1, h_1, s_1)$, pero en el proceso real se cumple $s_{2a} > s_{2s}$ debido a la **generación de entropía**, lo cual exige (o entrega) un cambio de entalpía distinto.

La **eficiencia isoentrópica** $(\eta_{\text{s}})$ es por tanto el **cociente entre los cambios de entalpía (o trabajo) ideal y real** correspondientes a la misma variación de presión — un indicador normalizado de irreversibilidad (con valores típicos $0 < \eta_{\text{s}} < 1$).

---

(subsec_isoentropic_open_systems)=
### Aplicaciones a sistemas abiertos y el diagrama $h-s$

En dispositivos abiertos en flujo estacionario, como **compresores**, **turbinas** y **toberas**, el fluido de trabajo intercambia **entalpía** y **entropía** con su entorno. Para estos sistemas, el **diagrama $h-s$** es la representación natural para visualizar tanto los intercambios energéticos como la irreversibilidad:

* Los cambios de **entalpía ($h$)** representan **transferencias de energía** (trabajo de eje o energía cinética).
* Los cambios de **entropía ($s$)** cuantifican la **irreversibilidad** y la distancia respecto al límite isoentrópico.

Al comparar la transformación **real** e **isoentrópica**, ambas deben operar entre **las mismas presiones de entrada y salida**. Esto refleja las **restricciones operativas** típicas: el compresor debe entregar un aumento de presión prescrito, la turbina debe expandir hasta una presión de escape fija, y la tobera debe descargarse contra una presión ambiente dada. Imponer la misma variación de presión garantiza que ambos procesos cumplan la **misma función mecánica**, y que cualquier diferencia entre ellos se deba exclusivamente a **irreversibilidades internas**.

En este diagrama, un **proceso isoentrópico** aparece como una **línea vertical** $(\Delta s = 0)$, mientras que el **proceso real** se curva hacia la derecha $(\Delta s > 0)$, reflejando la generación interna de entropía.

:::{note}

**EL DIAGRAMA DE MOLLIER**

El **diagrama $h-s$** (o **diagrama de Mollier**) es una herramienta gráfica esencial en termodinámica. Permite comparar visualmente:

* **Líneas isoentrópicas** — verticales, $\Delta s = 0$ (ideal).  
* **Procesos reales** — curvados hacia la derecha, $\Delta s > 0$ (irreversible).  
* **Intercambios energéticos** — proporcionales a diferencias de entalpía.

Esto lo hace especialmente útil en turbinas, compresores y toberas, donde las **variaciones de entalpía** dominan la conversión energética.
:::

:::{note}

**ELECCIÓN DE LA RESTRICCIÓN OPERATIVA**

El **proceso isoentrópico de referencia** debe definirse siempre bajo las **mismas condiciones finales** que el proceso real. La restricción adecuada — como presión, volumen o temperatura finales — depende del sistema y su propósito:

* En **sistemas abiertos en flujo estacionario**, lo habitual es fijar la **presión de salida**.
* En **sistemas cerrados**, pueden aplicarse otras restricciones (por ejemplo, un cambio fijado de **volumen** o **temperatura**).

Al imponer condiciones finales idénticas, la **eficiencia isoentrópica** aísla el efecto de las **irreversibilidades**, garantizando que cualquier desviación respecto al ideal se deba únicamente a la **generación de entropía**, y no a diferentes objetivos operativos

:::

<br/>

(subsubsec_eta_compressor)=
#### Compresores

Un **compresor** con una sola entrada y salida incrementa la presión de un gas mediante el **aporte de trabajo**. Neglectando efectos de energía cinética y potencial, y escribiendo la ecuación de balance de energía en régimen estacionario en términos específicos:

$$
w_{\text{in}} = h_2 - h_1.
$$

La **eficiencia isoentrópica de un compresor** se define como:

:::{epigraph}
El cociente entre el *trabajo que sería necesario para elevar la presión de un gas de manera isoentrópica* y el *trabajo real suministrado*.
:::

(eq_eta_comp)=
$$
\boxed{\eta_{\text{s, comp.}} = \frac{h_{2s} - h_1}{h_{2a} - h_1}} \ .
$$

Aquí, el numerador representa la aportación energética *ideal* (mínima), y el denominador la aportación *real*. La diferencia de signos y el orden de los límites de integración siguen del hecho de que tanto la energía como la entropía **aumentan** durante la compresión. Por tanto, las diferencias de entalpía son **positivas** en la expresión anterior.

Para modelos específicos de sustancia:

* **Sustancias genéricas (tabuladas):** entalpías obtenidas de $h(p,T)$ o $h(p,s)$.

* **Gases ideales:**

  $$
  \begin{gather*}
  h_{2s} - h_1 = \int_{T_1}^{T_{2s}} c_p(T)\,\mathrm{d}T, \\[10pt]
  h_{2a} - h_1 = \int_{T_1}^{T_{2a}} c_p(T)\,\mathrm{d}T,
  \end{gather*}
  $$

  de modo que

  $$
  \boxed{\eta_{\text{s, comp.}} = 
  \frac{\int_{T_1}^{T_{2s}} c_p(T)\mathrm{d}T}
       {\int_{T_1}^{T_{2a}} c_p(T)\mathrm{d}T}} \ .
  $$

* **Gases perfectos ($c_p = \text{const.}$):**

  $$
  \boxed{\eta_{\text{s, comp.}} = \frac{T_{2s} - T_1}{T_{2a} - T_1}} \ .
  $$

<br/>

(subsubsec_eta_turbine)=

#### Turbinas

Una **turbina** de una única entrada y salida expande un gas de alta presión hacia una presión menor, produciendo **trabajo de eje**. Despreciando los cambios de energía cinética y potencial y aplicando el balance de energía en régimen estacionario:

$$
w_{\text{out}} = h_1 - h_2.
$$

La **eficiencia isoentrópica de una turbina** se define como:

:::{epigraph}
El cociente entre el *trabajo real producido* por la turbina y el *trabajo que produciría si el proceso entre el mismo estado de entrada y la misma presión de salida fuese isoentrópico*.
:::

(eq_eta_turb)=
$$
\boxed{\eta_{\text{s, turb.}} = \frac{h_1 - h_{2a}}{h_1 - h_{2s}}} \ .
$$

En expansiones, la energía y la entalpía **disminuyen**, por lo que los signos y los límites de integración se invierten respecto a la compresión, asegurando diferencias de entalpía **positivas**.

* **Gases ideales:**

  $$
  \begin{gather*}
  h_{2a} - h_1 = \int_{T_1}^{T_{2a}} c_p(T)\,\mathrm{d}T, \\[10pt]
  h_{2s} - h_1 = \int_{T_1}^{T_{2s}} c_p(T)\,\mathrm{d}T,
  \end{gather*}
  $$

  lo que da

  $$
  \boxed{\eta_{\text{s, turb.}} = 
  \frac{\int_{T_{1}}^{T_{2a}} c_p(T)\mathrm{d}T}
       {\int_{T_{1}}^{T_{2s}} c_p(T)\mathrm{d}T}} \ .
  $$

* **Gases perfectos ($c_p = \text{const.}$):**

  $$
  \boxed{\eta_{\text{s, turb.}} = \frac{T_1 - T_{2a}}{T_1 - T_{2s}}} \ .
  $$

<br/>

(subsubsec_eta_nozzle)=
#### Toberas

Una **tobera** convierte **entalpía** en **energía cinética** de un chorro fluido. La ecuación de energía en flujo estacionario (omitiendo calor y energía potencial) da:

$$
h_1 + \frac{c_1^2}{2} = h_2 + \frac{c_2^2}{2}.
$$

La **eficiencia isoentrópica de una tobera** se define como:

:::{epigraph}
El cociente entre la diferencia de *energía cinética real* del fluido a la salida y de la diferencia de la *energía cinética* que se obtendría si el proceso (mismo estado de entrada y misma presión de salida) fuera isoentrópico.
:::

(eq_eta_noz)=
$$
\boxed{\eta_{\text{s, tob.}} = \frac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2}
= \frac{h_1 - h_{2a}}{h_1 - h_{2s}}} \ .
$$

Para un **gas ideal**:

$$
\begin{gather*}
h_1 - h_{2a} = \int_{T_{2a}}^{T_1} c_p(T)\,\mathrm{d}T, \\[10pt]
h_1 - h_{2s} = \int_{T_{2s}}^{T_1} c_p(T)\,\mathrm{d}T,
\end{gather*}
$$

lo que conduce a

$$
\boxed{\eta_{\text{s, tob.}} = 
\frac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2} =
\frac{\int_{T_{2a}}^{T_1} c_p(T)\mathrm{d}T}
     {\int_{T_{2s}}^{T_1} c_p(T)\mathrm{d}T}} \ .
$$

Para **gases perfectos ($c_p = \text{const.}$):**

$$
\boxed{\eta_{\text{s, tob.}} = 
\frac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2} =
\frac{T_1 - T_{2a}}{T_1 - T_{2s}}} \ .
$$

<br/>

:::{important}

**RESUMEN DE LAS EXPRESIONES DE EFICIENCIA isoentrÓPICA**

| **Dispositivo** | **Sustancias genéricas / tabuladas** | **Gases ideales ($c_p(T)$)** | **Gases perfectos ($c_p$ const.)** | **Interpretación** |
| :- | :- | :- | :- | :- |
| **Compresor** | $\dfrac{h_{2s}-h_1}{h_{2a}-h_1}$ | $\dfrac{\int_{T_1}^{T_{2s}} c_p(T)\mathrm{d}T}{\int_{T_1}^{T_{2a}} c_p(T)\mathrm{d}T}$ | $\dfrac{T_{2s}-T_1}{T_{2a}-T_1}$ | Fracción del trabajo ideal de compresión que se logra realmente |
| **Turbina** | $\dfrac{h_1-h_{2a}}{h_1-h_{2s}}$ | $\dfrac{\int_{T_{2a}}^{T_1} c_p(T)\mathrm{d}T}{\int_{T_{2s}}^{T_1} c_p(T)\mathrm{d}T}$ | $\dfrac{T_1-T_{2a}}{T_1-T_{2s}}$ | Fracción del trabajo ideal de expansión realmente entregado |
| **Tobera** | $\dfrac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2}=\dfrac{h_1-h_{2a}}{h_1-h_{2s}}$ | $\dfrac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2}=\dfrac{\int_{T_{2a}}^{T_1} c_p(T)\mathrm{d}T}{\int_{T_{2s}}^{T_1} c_p(T)\mathrm{d}T}$ | $\dfrac{c_{2a}^2 - c_1^2}{c_{2s}^2 - c_1^2}=\dfrac{T_1-T_{2a}}{T_1-T_{2s}}$ | Fracción de variación de energía cinética real respecto a la ideal |
:::

---

(subsec_conceptual_closure_isoentropic_eff)=
### Cierre conceptual

* La **eficiencia isoentrópica** generaliza la **segunda ley** desde los ciclos completos hasta los **procesos individuales**, cuantificando la **distancia respecto a la reversibilidad**.
* Mide cuán cerca se encuentra una transformación real de su contraparte **isoentrópica ideal** (adiabática y reversible).
* Ambos procesos — real e ideal — se comparan bajo la **misma restricción operativa** (por ejemplo, la misma presión de salida en sistemas abiertos).
* La **generación de entropía** aumenta el trabajo requerido (compresores) o reduce el trabajo útil entregado (turbinas) o la variacion de energía cinética producida (toberas), disminuyendo $\eta_{\text{s}}$.
* Para **sustancias tabuladas**, la eficiencia se obtiene de **diferencias de entalpía**; para **gases ideales**, mediante **integrales de $c_p(T)$**; y para **gases perfectos**, mediante **relaciones de temperatura**.
* El **diagrama $h-s$ (Mollier)** ofrece una representación intuitiva: la línea vertical marca el **límite isoentrópico**, mientras que la desviación hacia la derecha refleja la **irreversibilidad**.
* Todas las eficiencias isoentrópicas cumplen $0 < \eta_{\text{s}} < 1$, siendo $\eta_{\text{s}}=1$ el **límite reversible adiabático**.
* En esencia, $\eta_{\text{s}}$ une el análisis de **energía** con el de **entropía**, relacionando **trabajo útil** e **irreversibilidad** en una sola medida adimensional del desempeño.
