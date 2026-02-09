(sec_useful_work_reversibility_efficiency)=
## Trabajo útil, reversibilidad y eficiencia de la segunda ley

Una vez aclarados los conceptos de **estado muerto**, **entorno** y **potencial de trabajo**, podemos introducir las **magnitudes relacionadas con el trabajo** que sirven de puente hacia la **definición de exergía**. Estas magnitudes conectan los **intercambios de energía** de un sistema con la **calidad** de dichos intercambios, mostrando cómo las *irreversibilidades* reducen la cantidad de trabajo *útil* que puede obtenerse.

---

(subsec_surroundings_and_useful_work)=
### Trabajo del entorno y trabajo útil

Las nociones de **trabajo del entorno** y **trabajo útil** se introducen para separar el **trabajo mecánico total** ejercido en la frontera de un sistema de la **porción que representa energía aprovechable**. Siempre que un sistema interactúa mecánicamente con su ambiente, parte del trabajo de frontera simplemente contrarresta la **presión ambiente (atmosférica)**, manteniendo el equilibrio con el entorno. Solo la parte restante — el **trabajo útil** — contribuye efectivamente a modificar el estado energético del sistema y, por tanto, su **exergía** o **potencial de trabajo**.

Esta distinción se ilustra mejor mediante un **sistema pistón–cilindro**, la configuración más sencilla y representativa de la interacción mecánica. La **cara del pistón** está expuesta a la **atmósfera**, que actúa como **entorno** ejerciendo una presión constante $p_0$. Cuando el volumen del sistema cambia de $V_1$ a $V_2$, el entorno realiza **trabajo mecánico** sobre el sistema correspondiente a esta presión ambiental, expresado como

(eq_work_surr)=
$$
\boxed{W_{\text{surr.}} = p_0 (V_2 - V_1)} \ .
$$

Esta magnitud expresa la **acción mecánica de la presión ambiente** sobre la frontera.

El **trabajo útil** se define entonces como el **trabajo neto** obtenido tras restar esta contribución ambiental inevitable del trabajo total de frontera $W$:

(eq_work_useful)=
$$
\boxed{W_u = W - W_{\text{surr.}}} \ .
$$

Esta distinción aclara que:

* Para un sistema en **expansión**, el trabajo del entorno actúa como una **fuerza resistente** que debe superarse — **reduce** el trabajo útil obtenido.
* Para un sistema en **compresión**, el trabajo del entorno ayuda a la compresión — **reduce** el trabajo externo requerido.

Por tanto, $W_u$ representa la **energía mecánica efectiva** que queda disponible una vez descontados los efectos de la presión ambiental.

:::{note}

**TRABAJO DE FRONTERA EN SISTEMAS ABIERTOS**

En **sistemas abiertos**, donde la masa atraviesa la superficie de control, el concepto de trabajo de frontera aparece implícitamente como **trabajo de flujo**, definido por unidad de masa como $p v$.
Cada elemento de fluido debe “empujar” al fluido circundante al entrar o salir del volumen de control, y este efecto mecánico ya está incluido en el término **entalpía**, $h = u + p v$.
Así, la distinción entre trabajo **total** y **útil** sigue siendo válida — pero queda incorporada en la definición de entalpía en lugar de aparecer explícitamente como $p_0(V_2 - V_1)$.
:::

---

(subsec_reversible_work_and_irreversibility)=
### Trabajo reversible e irreversibilidad

Entre todas las transformaciones posibles entre dos estados dados, el **proceso reversible** proporciona el **máximo trabajo útil posible** (o requiere el **mínimo trabajo de entrada**). Esto define el **trabajo reversible**, $W_{\text{rev.,out}}$.

La **irreversibilidad**, $I$, cuantifica la **pérdida de potencial de trabajo útil** debida a la presencia de efectos disipativos. Se expresa, por tanto, como:

(eq_irreversibility)=
$$
\boxed{I = W_{\text{rev.,out}} - W_{u,\text{out}}} \ ,
$$

donde el subíndice **out** indica que las magnitudes se refieren a **trabajo de salida**.

En sistemas reales, $I > 0$, y solo en el **límite reversible ideal** se cumple $I = 0$, lo que indica ausencia de pérdida de potencial de trabajo.

:::{note}

**DISTINCIÓN EN EL USO DEL TÉRMINO *IRREVERSIBILIDAD***

La palabra **irreversibilidad** se usa en dos sentidos relacionados:

* Cualitativamente, se refiere a la **presencia de efectos disipativos** (como fricción, diferencias de temperatura finitas o mezclado) que impiden que un proceso sea reversible.
* Cuantitativamente, designa la **magnitud $I$**, que mide el **equivalente energético** de dichos efectos — el *potencial de trabajo destruido* debido a la generación de entropía.

Aunque ambos significados están conectados, el primero es descriptivo, mientras que el segundo es **numérico** y **medible** en julios.
:::

---

(subsec_second_law_efficiency)=
### Eficiencia de la segunda ley y la medida de la calidad de la energía

La **eficiencia de la segunda ley**, también llamada **eficiencia racional**, complementa la **eficiencia térmica** al considerar no solo la **cantidad**, sino también la **calidad** de la energía intercambiada. Mientras que la **primera ley** se ocupa de la conservación de la energía, la **segunda ley** evalúa *cuán eficazmente* puede transformarse esa energía en trabajo útil.

Para comprender esta idea, imaginemos dos motores térmicos que operan bajo distintos rangos de temperatura pero que presentan la **misma eficiencia térmica**. Aunque sus relaciones energéticas $(W/Q_H)$ sean iguales, sus **contextos termodinámicos** difieren: el motor que opera con una diferencia de temperatura menor trabaja en condiciones menos favorables. Al compararlos con el **límite reversible (Carnot)** correspondiente a cada rango de temperaturas, el motor que funciona eficazmente bajo la diferencia de temperatura más restrictiva muestra una **eficiencia de la segunda ley mayor**, ya que se encuentra **más cerca de su propio límite ideal**.

Así, la eficiencia de la segunda ley expresa cuán eficazmente un dispositivo se aproxima a su **referencia reversible**, independientemente de los niveles absolutos de temperatura involucrados. Formalmente, para un motor térmico:

(eq_eta_II_engines)=
$$
\boxed{\eta_{II} = \frac{\eta_{\text{th.}}}{\eta_{\text{th.,rev.}}}} \ .
$$

Para ilustrarlo cuantitativamente, consideremos dos motores térmicos, **A** y **B**, cada uno con una **eficiencia térmica** de $\eta_{\text{th.}} = 0{,}30$. El motor **A** opera entre $T_H = 600\ \text{K}$ y $T_L = 300\ \text{K}$, mientras que el motor **B** opera entre $T_H = 1000\ \text{K}$ y $T_L = 300\ \text{K}$.

Sus **eficiencias reversibles (Carnot)** son:

$$
\eta_{\text{th.,rev.,A}} = 1 - \frac{300}{600} = 0{,}50,
$$

$$
\eta_{\text{th.,rev.,B}} = 1 - \frac{300}{1000} = 0{,}70.
$$

En consecuencia, sus **eficiencias de la segunda ley** son:

$$
\eta_{II,\text{A}} = \frac{0{,}30}{0{,}50} = 0{,}60,
$$

$$
\eta_{II,\text{B}} = \frac{0{,}30}{0{,}70} \approx 0{,}43.
$$

Aunque ambos motores transforman la misma *fracción* del calor en trabajo, el motor **A** alcanza su rendimiento **en condiciones menos favorables**, y por tanto opera **más cerca de su límite reversible**. Esto muestra que $\eta_{II}$ mide no solo *cuánta* energía se convierte, sino *qué tan bien* se desempeña el sistema respecto a su potencial teórico.

En general, y dependiendo del propósito del sistema, esta eficiencia puede expresarse como:

:::{important}

**DEFINICIONES GENERALES DE EFICIENCIA DE LA SEGUNDA LEY**

| **Tipo de dispositivo** | **Definición** | **Interpretación** |
| :- | :- | :- |
| **Dispositivo productor de trabajo** | $\displaystyle \eta_{II} = \frac{\eta_{\text{th.}}}{\eta_{\text{th.,rev.}}} = \frac{W_u}{W_{\text{rev.}}}$ | Fracción del trabajo máximo que realmente se obtiene |
| **Dispositivo consumidor de trabajo** | $\displaystyle \eta_{II} = \frac{\eta_{\text{th.}}}{\eta_{\text{th.,rev.}}} = \frac{W_{\text{rev.}}}{W_u}$ | Cercanía fraccional al mínimo reversible de entrada |
| **Refrigerador / bomba de calor** | $\displaystyle \eta_{II} = \frac{\text{COP}}{\text{COP}_{\text{rev.}}}$ | Fracción del rendimiento ideal alcanzado |
:::

:::{note}

**INTERPRETACIÓN DE LA EFICIENCIA DE LA SEGUNDA LEY**

La **eficiencia de la segunda ley** también puede entenderse como una medida del **margen de mejora** de un sistema real. Un valor de $\eta_{II}$ cercano a 1 indica que el proceso ya opera **cerca de su límite reversible**, dejando poco potencial de mejora. Por el contrario, una $\eta_{II}$ baja revela una **gran diferencia** entre el rendimiento real y el ideal, cuantificando el **potencial para reducir irreversibilidades** y **mejorar la calidad energética** del dispositivo.

:::

---

(subsec_efficiency_comparison)=
### Comparación de las eficiencias definidas hasta ahora

A este punto se han introducido varias **medidas de eficiencia**, cada una abordando una **dimensión distinta del rendimiento** y basada en principios diferentes:

* La **eficiencia térmica**, $\eta_{\text{th.}}$, cuantifica la **fracción de calor de entrada convertida en trabajo**: la perspectiva de la primera ley (balance energético) para motores térmicos.
* La **eficiencia de Carnot**, $\eta_{\text{Carnot}}=\eta_{\text{th.,rev.}}$, es la **eficiencia térmica de un motor reversible**; representa la **máxima eficiencia posible** entre $T_H$ y $T_L$, siendo así un **caso particular (reversible)** de eficiencia térmica.
* La **eficiencia isentrópica**, $\eta_{\text{s}}$, compara un **proceso real** con su contraparte **adiabática + reversible** (isentrópica): una medida **específica del dispositivo** para compresores, turbinas y toberas.
* La **eficiencia de la segunda ley**, $\eta_{II}$, compara el **rendimiento real** con el **límite reversible** (Carnot o equivalente), combinando **cantidad** y **calidad** de energía en un único indicador adimensional.

:::{important}

**RESUMEN Y COMPARACIÓN DE LOS TIPOS DE EFICIENCIA**

| **Tipo de eficiencia** | **Definición / relación** | **Referencia ideal** | **Significado físico** |
| :- | :- | :- | :- |
| **Eficiencia térmica** | $\displaystyle \eta_{\text{th.}} = \frac{W_{\text{out}}}{Q_{\text{in}}} = 1 - \frac{Q_L}{Q_H}$ | Ninguna (basada en balance energético) | Mide conversión de energía según la primera ley (cantidad) |
| **Eficiencia de Carnot** | $\displaystyle \eta_{\text{Carnot}}=\eta_{\text{th.,rev.}} = 1 - \frac{T_L}{T_H}$ | Ella misma | Mide la conversión máxima posible según la primera ley |
| **Eficiencia isentrópica** | $\displaystyle \eta_{\text{s}} = \frac{(\Delta h)_{\text{s}}}{(\Delta h)_{\text{a}}}$ u otra equivalente según el proceso | Proceso adiabático + reversible (isentrópico) | Comparación específica entre proceso real e isentrópico |
| **Eficiencia de la segunda ley** | $\displaystyle \eta_{II} = \frac{\eta_{\text{th.}}}{\eta_{\text{th.,rev.}}}$ | Límite reversible (Carnot o general) | Considera cantidad y calidad — cercanía al límite reversible |
:::

---

(subsec_conceptual_closure_useful_work)=
### Cierre conceptual

* El **trabajo del entorno** aísla el efecto mecánico de la presión ambiente.
* El **trabajo útil** mide la contribución mecánica efectiva tras descontar dicho efecto ambiental.
* El **trabajo reversible** representa el límite teórico máximo; la **irreversibilidad** cuantifica la pérdida de ese potencial.
* La **eficiencia de la segunda ley** generaliza este concepto en un indicador adimensional, enlazando la primera y la segunda ley.
* En conjunto, estos conceptos establecen la base para el siguiente paso: la definición de **exergía** como la medida unificada de *energía útil* — el máximo trabajo útil que un sistema puede entregar al alcanzar el equilibrio con su entorno.
