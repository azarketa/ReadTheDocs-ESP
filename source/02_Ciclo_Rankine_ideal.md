(sec_rankine_ideal_detailed)=
## El ciclo Rankine ideal

En el **ciclo Rankine ideal**, el análisis asume un flujo en **régimen estacionario**. Normalmente se desprecia cualquier contribución de la energía cinética y potencial del fluido, ya que por lo general son insignificantes en comparación con las transferencias de energía térmica y de trabajo que tienen lugar dentro del sistema.

Aplicando la **Primera Ley de la Termodinámica**, analizamos el balance de energía para cada componente. Procedemos sabiendo que:
1. No se realiza trabajo en los intercambiadores de calor (los evaporadores y condensadores).
2. Se asume que la turbomaquinaria (turbinas y bombas) es **isentrópica** (perfectamente reversible y adiabática).

Las variaciones de energía para cada proceso pueden escribirse como sigue:

* **Bomba ($q=0$):**
    La bomba incrementa la presión del líquido.

    $$w_{\text{pump,in}} = h_2 - h_1 \ ,$$

    donde $w$ representa el trabajo y $h$ representa la entalpía.

* **Evaporador ($w=0$):**
    Se añade calor al fluido a presión constante.

    $$q_{\text{in}} = h_3 - h_2$$

* **Turbina ($q=0$):**
    El fluido se expande, produciendo trabajo.

    $$w_{\text{turb,out}} = h_3 - h_4$$

* **Condensador ($w=0$):**
    El fluido cede calor al entorno.

    $$q_{\text{out}} = h_4 - h_1$$

La **eficiencia térmica** ($\eta_{\text{th}}$) del ciclo mantiene su definición termodinámica estándar:

$$\eta_{\text{th}} = \frac{w_{\text{net}}}{q_{\text{in}}} = 1 - \frac{q_{\text{out}}}{q_{\text{in}}}$$

---

(subsec_rankine_real_losses)=
### El ciclo Rankine real: comprensión de las irreversibilidades

El **ciclo Rankine real** difiere del modelo ideal debido a las **irreversibilidades** que aparecen en sus distintos componentes. Aunque el ciclo ideal es una referencia teórica útil, la ingeniería real debe tener en cuenta las pérdidas. Las dos fuentes principales de estas irreversibilidades son la **fricción del fluido** y las **pérdidas de calor** hacia el ambiente.

1. Fricción del fluido (caídas de presión):

    La fricción provoca que la presión del fluido disminuya a medida que este se mueve a través del evaporador, del condensador y de las tuberías que conectan dichos componentes (lo que se conoce como **pérdida de carga**).
    * **La consecuencia:** El vapor sale del evaporador a una presión ligeramente inferior a la de diseño. Después entra en la turbina a una presión todavía menor debido a la fricción en las tuberías de conexión.
    * **La compensación:** Aunque las caídas de presión en el condensador suelen ser pequeñas, las pérdidas globales del sistema implican que el agua debe bombearse a una **presión relativamente mayor** que la requerida en el caso ideal. Esto exige bombas de mayor tamaño y un mayor trabajo de entrada ($w_{\text{pump,in}}$).

2. Pérdidas de calor:

    A medida que el vapor circula por los componentes y las tuberías, inevitablemente transfiere calor al entorno más frío.

    * **La consecuencia:** Para mantener el mismo nivel de trabajo neto de salida, debe transferirse más calor al vapor en el evaporador para compensar estas pérdidas.
    * **El resultado:** Como $q_{\text{in}}$ aumenta para producir el mismo trabajo, la eficiencia térmica del ciclo disminuye.

3. Otras limitaciones del mundo real:

    Varios otros factores hacen que el ciclo real se desvíe del ideal:

    * **Subenfriamiento:** En casi todos los condensadores, el líquido se subenfría (se enfría por debajo de la temperatura de saturación) para evitar la **cavitación**: la rápida formación y colapso de burbujas de vapor en la línea de aspiración a baja presión de la bomba, lo que puede causar daños estructurales.
    * **Pérdidas mecánicas:** Los rodamientos y sellos están sometidos a fricción.
    * **Fugas:** Puede fugarse vapor fuera del ciclo y puede entrar aire en el condensador (rompiendo el vacío).
    * **Potencia auxiliar:** La energía consumida por dispositivos auxiliares, como los ventiladores que suministran aire al banco de combustión, representa una pérdida que debe computarse en el balance final de eficiencia.

:::{important}
**EFICIENCIAS DE LA BOMBA Y DE LA TURBINA**

Las desviaciones en la bomba y en la turbina son particularmente relevantes. Las bombas reales requieren mayor energía de entrada, y las turbinas reales producen menos trabajo de salida. Tenemos en cuenta este comportamiento no isentrópico mediante las **eficiencias isentrópicas**:

$$\eta_{\text{pump}} = \frac{w_s}{w_a} = \frac{h_{2s} - h_1}{h_{2a} - h_1}$$

$$\eta_{\text{turb}} = \frac{w_a}{w_s} = \frac{h_3 - h_{4a}}{h_3 - h_{4s}}$$

Aquí, los estados **$2a$** y **$4a$** corresponden a los procesos **reales**, mientras que **$2s$** y **$4s$** corresponden a los procesos **ideales** (isentrópicos).
:::

---

(subsec_rankine_efficiency_methods)=
### Métodos para mejorar la eficiencia del ciclo Rankine

Los ciclos de potencia de vapor son responsables de una gran parte de la producción mundial de electricidad. En consecuencia, cualquier mejora en la eficiencia térmica se traduce en un ahorro significativo de combustible (nuclear, fósil o de otro tipo).

El concepto fundamental detrás de todas las modificaciones del ciclo Rankine es el mismo: **incrementar la eficiencia térmica**. Para ello, debemos obedecer una “regla de oro” termodinámica:
* Aumentar la **temperatura media** a la que se añade calor al fluido ($T_{\text{avg,in}}$).
* O disminuir la **temperatura media** a la que se rechaza calor ($T_{\text{avg,out}}$).

En la práctica, existen tres formas principales de lograrlo:

1. Disminuir la presión del condensador:

    Este método se centra en el lado del “rechazo de calor” de la ecuación.

    * **El mecanismo:** Dentro del condensador, el vapor existe como mezcla bifásica. Su temperatura queda fijada por su presión (estado de saturación). Por tanto, reducir la presión de operación reduce automáticamente la temperatura a la que se rechaza calor.
    * **El efecto:** Esto incrementa el **trabajo neto** (representado por el área encerrada en el diagrama $T-s$). Aunque los requerimientos de aporte de calor aumentan ligeramente, la eficiencia global se eleva.
    * **Limitaciones prácticas:**
        * **Límites de vacío:** Los condensadores suelen operar por debajo de la presión atmosférica. El límite inferior viene dictado por la temperatura del medio de enfriamiento (río, lago o aire ambiente).
        * **Infiltración de aire:** Presiones extremadamente bajas incrementan el riesgo de que entre aire en el condensador.
        * **Contenido de humedad:** Reducir la presión desplaza la línea de expansión hacia la izquierda. Esto aumenta la humedad (gotas) a la salida de la turbina (estado $4'$).

:::{note}
**EL PROBLEMA DE LA EROSIÓN**

La presencia de una humedad significativa en el escape de la turbina es perjudicial. Las gotas de agua erosionan los álabes de la turbina y reducen su rendimiento aerodinámico. Esta limitación física impide reducir indefinidamente la presión del condensador.
:::

2. Sobrecalentar el vapor:

    Este método se centra en el lado del “aporte de calor”.

    * **El mecanismo:** Se continúa calentando el vapor después de que se haya vaporizado, elevando su temperatura muy por encima del punto de saturación.
    * **El efecto:** Esto eleva la temperatura media de adición de calor sin modificar la presión del sistema. Tanto el trabajo neto como el calor aportado aumentan, pero la eficiencia mejora.
    * **Beneficio adicional:** El sobrecalentamiento desplaza la línea de expansión hacia la derecha, **disminuyendo significativamente el contenido de humedad** a la salida de la turbina, lo que protege los álabes.
    * **Limitaciones prácticas:** Estamos limitados por la metalurgia. La temperatura máxima que pueden soportar los materiales actuales de las turbinas es aproximadamente **$620 \ ^\circ\text{C}$**. Superar este valor requiere cerámicas avanzadas o nuevas innovaciones en aleaciones.

3. Incrementar la presión del evaporador:

    Este método también actúa sobre el lado del “aporte de calor”.

    * **El mecanismo:** Aumentar la presión eleva la temperatura de ebullición del agua.
    * **El efecto:** Esto incrementa automáticamente la temperatura media de adición de calor, mejorando la eficiencia térmica.
    * **El efecto secundario:** Como se observa en los diagramas $T\!-\!s$, una mayor presión desplaza el ciclo hacia la izquierda. Esto **aumenta el contenido de humedad** a la salida de la turbina.
    * **La solución:** Debido a este problema de humedad, los ciclos de alta presión casi siempre requieren **recalentamiento** del vapor (extrayéndolo, calentándolo de nuevo y expandiéndolo otra vez) para mantener protegidos los álabes de la turbina.

---

(subsec_rankine_supercritical)=
### El ciclo Rankine supercrítico

La búsqueda de una mayor eficiencia ha llevado a un incremento sostenido de las presiones de operación del evaporador. Muchas centrales modernas operan ya a **presiones supercríticas** (a menudo cercanas a **$30 \ \text{MPa}$**).

En estos ciclos:
* No existe un proceso de cambio de fase claramente distinguible (no aparecen burbujas de ebullición).
* El fluido pasa de manera continua de una densidad similar a la de un líquido a una densidad similar a la de un gas.
* Las eficiencias térmicas pueden alcanzar aproximadamente **$40\%$**.

---

(subsec_rankine_closure)=
### Cierre conceptual

* **Ideal frente a real:** El ciclo Rankine ideal se calcula mediante simples diferencias de entalpía, asumiendo componentes isentrópicos. El ciclo real debe tener en cuenta la **fricción** (caídas de presión) y las **pérdidas de calor**, utilizando eficiencias isentrópicas para cuantificar el rendimiento de los componentes.
* **El objetivo:** Todas las modificaciones buscan aumentar la eficiencia térmica para ahorrar recursos combustibles.
* **Las palancas:** La eficiencia mejora ampliando la diferencia de temperaturas:
    1. **Reduciendo la presión del condensador** (limitado por la erosión de los álabes debida a la humedad).
    2. **Sobrecalentando el vapor** (limitado por los puntos de fusión de los materiales, aprox. $620 \ ^\circ\text{C}$).
    3. **Incrementando la presión de la caldera** (limitado por la humedad, lo que a menudo requiere recalentamiento).
* **Estado del arte:** Los ciclos supercríticos operan a presiones muy elevadas ($>22 \ \text{MPa}$) para maximizar la temperatura media de adición de calor, alcanzando eficiencias superiores.

