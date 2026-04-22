(sec_carnot_cycles_temperature_scale_postulates)=
## Ciclo de Carnot, escala termodinámica de temperaturas y postulados de Carnot

La discusión anterior distinguió los procesos **reversibles** de los **irreversibles**, mostrando que los primeros representan los **límites ideales** del comportamiento real. Nos centramos ahora en el **ciclo de Carnot**, una construcción teórica que encarna un motor térmico *perfectamente reversible* y establece la **máxima eficiencia** que puede alcanzar cualquier motor real.

Este modelo ideal permite introducir los **postulados de Carnot** y la **escala termodinámica de temperaturas**, ambos derivados directamente de los principios de la **$2^{\text{a}}$ ley**.

---

(subsec_carnot_cycle)=
### El ciclo de Carnot

El **ciclo de Carnot** es el **ciclo reversible idealizado** de un motor térmico. Consta de cuatro procesos reversibles — **dos isotermos** y **dos adiabáticos** — ejecutados de tal manera que la sustancia de trabajo (por ejemplo, un gas ideal) atraviese una secuencia de **estados de equilibrio**.

1. **Expansión isotérmica (1–2):**  
   El sistema está en contacto con un **foco caliente** a temperatura $T_H$. Se expande lentamente mientras absorbe un calor $Q_H$, manteniendo su temperatura constante. Cualquier enfriamiento infinitesimal debido a la expansión se compensa con una entrada equivalente de calor, garantizando la reversibilidad.

2. **Expansión adiabática (2–3):**  
   El sistema se aísla del foco caliente y continúa expandiéndose **sin intercambio de calor**. Su temperatura desciende de $T_H$ a $T_L$ al realizar trabajo sobre los alrededores.

3. **Compresión isotérmica (3–4):**  
   El sistema se pone en contacto con un **foco frío** a temperatura $T_L$ y se comprime lentamente. Rechaza un calor $Q_L$ mientras permanece a temperatura constante.

4. **Compresión adiabática (4–1):**  
   De nuevo aislado, el sistema continúa comprimiéndose **adiabáticamente** hasta que la temperatura asciende de nuevo a $T_H$, recuperando el estado inicial.

Durante un ciclo completo, el sistema absorbe $Q_H$ del foco caliente, rechaza $Q_L$ al foco frío y entrega un **trabajo neto**

$$
W_{\text{neto}} = Q_H - Q_L.
$$

Aunque cada etapa es reversible, la **$2^{\text{a}}$ ley** se respeta plenamente:
siempre debe rechazarse parte de la energía como calor, por lo que la conversión total de $Q_H$ en trabajo es imposible.

:::{important}

**EL IDEAL REVERSIBLE**

Un ciclo de Carnot representa el **límite reversible** de un motor térmico — un proceso que ocurre sin efectos disipativos. Define la **máxima eficiencia teórica** alcanzable entre dos temperaturas $T_H$ y $T_L$. Todos los motores reales son **irreversibles** y, por lo tanto, sus eficiencias son **menores** que las de un motor de Carnot operando entre los mismos focos.

:::

---

(subsec_inverse_carnot_cycle)=
### Ciclo de Carnot inverso

Dado que el ciclo de Carnot es **reversible**, puede **operarse en sentido inverso**. Cuando se invierte la secuencia de procesos, el resultado es un **ciclo de Carnot inverso**, que representa un **refrigerador** o **una bomba de calor ideal**.

* El sistema **recibe un trabajo** $W_{\text{in}}$.
* **Absorbe calor** $Q_L$ de un foco frío.
* **Rechaza calor** $Q_H$ a un foco caliente.

El proceso cumple el **postulado de Clausius**: el calor solo puede fluir del frío al caliente **si se suministra trabajo externo**.

:::{note}

**RELACIÓN ENTRE EL CICLO DIRECTO Y EL INVERSO**

Tanto el **ciclo directo** como el **ciclo inverso** de Carnot operan entre los mismos dos focos, $T_H$ y $T_L$. Solo difieren en la **dirección del flujo energético**: el ciclo directo produce trabajo aprovechando el flujo natural de calor (caliente → frío), mientras que el inverso consume trabajo para invertir dicho flujo (frío → caliente).

:::

---

(subsec_carnot_postulates)=
### Los postulados de Carnot

El análisis de los ciclos de Carnot conduce a dos proposiciones fundamentales que sustentan la **$2^{\text{a}}$ ley**:

* **Primer postulado de Carnot:**

   :::{epigraph}
   Ningún motor térmico real (irreversible) que opere entre dos focos térmicos puede ser más eficiente que uno reversible que opere entre los mismos focos.
   :::

* **Segundo postulado de Carnot:**

   :::{epigraph}
   Todos los motores térmicos reversibles que operan entre los mismos dos focos tienen la misma eficiencia, independientemente del fluido de trabajo o de los detalles constructivos.
   :::

---

(subsec_thermodynamic_temperature_scale)=
### La escala termodinámica de temperaturas

Los **postulados de Carnot** permiten definir una **escala de temperaturas** que depende únicamente de las **leyes de la termodinámica**, y no de las propiedades de ninguna sustancia particular.

Consideremos tres **motores térmicos reversibles**, denominados A, B y C, dispuestos en cascada entre tres focos térmicos a temperaturas $T_1$, $T_2$ y $T_3$, con $T_1 > T_2 > T_3$. El motor A opera entre $T_1$ y $T_2$, el motor B entre $T_2$ y $T_3$, y el motor C entre $T_1$ y $T_3$.

Para cualquier motor reversible, el rendimiento térmico se expresa como

$$
\eta_{\text{th.}} = 1 - \frac{Q_L}{Q_H},
$$

donde $Q_H$ y $Q_L$ son los calores absorbido y rechazado en los focos caliente y frío, respectivamente. Como los postulados de Carnot afirman que el rendimiento depende **solo** de las temperaturas de los focos, podemos expresar la razón de calores como

$$
\frac{Q_L}{Q_H} = f(T_L, T_H),
$$

donde $f$ es una función todavía desconocida que refleja la dependencia entre las temperaturas de ambos focos.

Para cada uno de los tres motores, el rendimiento se escribe entonces como:

$$
\begin{gather*}
\eta_{\text{th.},A} = 1 - \frac{Q_2}{Q_1} = 1 - f(T_2, T_1), \\[10pt]
\eta_{\text{th.},B} = 1 - \frac{Q_3}{Q_2} = 1 - f(T_3, T_2), \\[10pt]
\eta_{\text{th.},C} = 1 - \frac{Q_3}{Q_1} = 1 - f(T_3, T_1).
\end{gather*}
$$

Ahora bien, si los motores A y B operan **en serie**, el calor rechazado por A ($Q_2$) se convierte en el calor absorbido por B. A partir de la conservación de la energía aplicada al sistema combinado (A+B), la razón global de calores entre los focos extremos ($T_1$ y $T_3$) satisface

(eq_carnot_combined_ratio)=
$$
\frac{Q_3}{Q_1} = \frac{Q_3}{Q_2} \cdot \frac{Q_2}{Q_1}.
$$

Sustituyendo las expresiones funcionales para cada término se obtiene

(eq_carnot_functional_relation)=
$$
f(T_1, T_3) = f(T_1, T_2)\, f(T_2, T_3).
$$

Esta condición — que la razón global de calores sea el **producto** de las razones intermedias — debe cumplirse para cualquier temperatura intermedia $T_2$. El único tipo de función que satisface este requisito para valores arbitrarios de temperatura es aquella que puede **separarse** en el cociente de dos funciones de una sola variable:

(eq_carnot_functional_form)=
$$
\boxed{f(T_L, T_H) = \frac{\phi(T_L)}{\phi(T_H)}.}
$$

En efecto, si $f$ adopta esta forma, la relación multiplicativa se verifica automáticamente:

$$
\frac{\phi(T_3)}{\phi(T_1)} = \frac{\phi(T_3)}{\phi(T_2)} \cdot \frac{\phi(T_2)}{\phi(T_1)}.
$$

Este resultado implica que la razón de calores entre dos focos en un ciclo reversible depende únicamente de una **propiedad monótona** de la temperatura, $\phi(T)$, asegurando que el calor fluya naturalmente desde valores más altos hacia valores más bajos de temperatura.

La elección más simple y directa para $\phi(T)$, propuesta por **Lord Kelvin**, es hacerla **proporcional a la propia temperatura absoluta**:

(eq_carnot_kelvin_choice)=
$$
\phi(T) = T.
$$

Con esta elección, la razón de calores resulta ser

(eq_carnot_temperature_relation)=
$$
\boxed{\frac{Q_L}{Q_H} = \frac{T_L}{T_H}.}
$$

Esta ecuación define la **escala termodinámica de temperaturas**, también conocida como **escala Kelvin**, donde la razón entre las temperaturas de dos focos es igual a la razón entre los calores intercambiados en un ciclo reversible.

:::{important}

**CARACTERÍSTICAS DE LA ESCALA TERMODINÁMICA**

* La escala termodinámica de temperaturas surge **directamente de la $2^{\text{a}}$ ley**, independientemente de cualquier sustancia de trabajo. Su naturaleza universal proviene de que conecta la temperatura con un proceso físico relacionado con la energía (intercambio de calor), eliminando la dependencia operativa respecto a escalas basadas en dispositivos o materiales concretos.
* En ciclos reversibles, las **razones de temperatura** son iguales a las **razones de calor**.
* La forma más simple, $\phi(T)=T$, define una escala **lineal y absoluta**, cuya unidad es el **kelvin (K)**.
* El cero kelvin $(0 \ \text{K})$ corresponde al límite teórico donde toda actividad termodinámica cesa.
:::

---

(subsec_carnot_efficiency_and_COP)=
### Rendimiento de Carnot y sus implicaciones

Para un motor térmico reversible que opere entre $T_H$ y $T_L$, el **rendimiento de Carnot** es

(eq_carnot_efficiency)=
$$
\boxed{\eta_{\text{th,rev}} = \eta_{\text{Carnot}} = 1 - \frac{T_L}{T_H}}.
$$

Ningún motor real puede superar este valor. Del mismo modo, para el **ciclo de Carnot inverso**, los **coeficientes de operación (COP)** vienen dados por

(eq_carnot_COPs)=
$$
\boxed{\text{COP}_{\text{R,rev}} = \text{COP}_{\text{R,Carnot}} = \frac{T_L}{T_H - T_L}}, \qquad
\boxed{\text{COP}_{\text{HP,rev}} = \text{COP}_{\text{HP,Carnot}} = \frac{T_H}{T_H - T_L}}.
$$

Estos valores representan los **máximos teóricos** alcanzables por cualquier sistema de refrigeración o bomba de calor que opere entre las mismas temperaturas.

:::{important}

**LOS CICLOS DE CARNOT COMO LÍMITES DE REFERENCIA**

La comparación entre dispositivos reales e ideales es inmediata:

| **Tipo de dispositivo**     | **Criterio**                                | **Interpretación**                        |
| :-------------------------- | :------------------------------------------ | :---------------------------------------- |
| **Motor térmico**           | $\eta_{\text{th}} < \eta_{\text{Carnot}}$   | Motor irreversible (real)                 |
|                             | $\eta_{\text{th}} = \eta_{\text{Carnot}}$   | Motor reversible (ideal)                  |
|                             | $\eta_{\text{th}} > \eta_{\text{Carnot}}$   | Imposible (viola la $2^{\text{a}}$ ley)   |
| **Refrigerador / bomba de calor** | $\text{COP} < \text{COP}_{\text{Carnot}}$ | Irreversible (real)                       |
|                             | $\text{COP} = \text{COP}_{\text{Carnot}}$   | Reversible (ideal)                        |
|                             | $\text{COP} > \text{COP}_{\text{Carnot}}$   | Imposible (viola la $2^{\text{a}}$ ley)   |

Así, los límites de Carnot distinguen **tres regímenes** de operación:

1. Los **dispositivos reales** son siempre menos eficientes que el ideal de Carnot.
2. Los **dispositivos reversibles** alcanzan la eficiencia de Carnot, pero son únicamente conceptuales.
3. Los **dispositivos hipotéticos** que superasen los valores de Carnot violarían la **$2^{\text{a}}$ ley**, por lo que son imposibles.

:::

El análisis de los **ciclos de Carnot** muestra que la eficiencia de cualquier proceso reversible depende únicamente de la **razón de temperaturas** entre los focos.  
Esta observación suscita una cuestión más profunda:

:::{epigraph}
¿Existe alguna propiedad intrínseca de un sistema que gobierne la dirección y la limitación de estas transferencias de energía? En caso afirmativo: ¿cuál es esa propiedad?
:::

Para responder, debemos introducir una nueva magnitud termodinámica — la **entropía** — que proporciona una medida universal de la **dispersión de energía** y de la **irreversibilidad de los procesos**. La siguiente sección desarrollará el concepto de **entropía** y derivará su fundamento matemático a través de la **desigualdad de Clausius**.

---

(subsec_conceptual_closure_carnot)=
### Cierre conceptual

* El **ciclo de Carnot** representa el *modelo reversible ideal* de un motor térmico y establece el **límite superior** del desempeño termodinámico.
* Su **ciclo inverso** define el **refrigerador o bomba de calor ideal**, ambos en pleno acuerdo con la **$2^{\text{a}}$ ley**.
* Los **postulados de Carnot** demuestran que la eficiencia depende **exclusivamente** de las temperaturas de los focos, conduciendo de manera natural a la **escala termodinámica de temperaturas**.
* La **escala Kelvin** surge de este razonamiento, conectando las razones entre temperaturas con las razones entre calores en ciclos reversibles.
* El **rendimiento de Carnot** y los **COP de Carnot** establecen límites absolutos de rendimiento: ningún proceso real puede superarlos.

En resumen, los ciclos de Carnot revelan el **límite cuantitativo** de la **$2^{\text{a}}$ ley**: definen qué es *termodinámicamente posible* y, por contraste, ponen de manifiesto lo que la irreversibilidad de la realidad prohíbe.
