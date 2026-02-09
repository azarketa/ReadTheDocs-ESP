(sec_entropy_variations_Tds_relations)=
## Cálculo de variaciones de entropía y las relaciones $T\mathrm{d}s$

Habiendo establecido la **definición de entropía** como $\mathrm{d}S = (\delta Q/T)_{\text{int.,rev.}}$, pasamos ahora a analizar cómo varía esta propiedad **entre dos estados de equilibrio**. Cuantificar variaciones de entropía es fundamental porque nos permite:

* identificar la **irreversibilidad** en procesos reales,
* medir la **degradación energética** asociada a la transferencia de calor, y
* evaluar **límites de eficiencia** para motores y refrigeradores.

Para ello, necesitamos relaciones que vinculen $\delta Q$ y $T$ con propiedades medibles del sistema. Estas son las **relaciones $T\mathrm{d}s$**, que expresan la **$2^{\text{a}}$ ley** en una forma diferencial y calculable.

---

(subsec_Tds_relations)=
### Derivación de las relaciones $T\mathrm{d}s$

Comenzamos con un **sistema cerrado, estable e internamente reversible**. Esta configuración permite aislar los mecanismos termodinámicos esenciales: como la masa permanece constante, solo **calor** y **trabajo de frontera** cruzan la frontera del sistema.

Para tal sistema, la **$1^{\text{a}}$ ley** da

$$
\mathrm{d}E = \delta Q_{\text{int.,rev.}} - \delta W_{\text{int.,rev.}}.
$$

Despreciando cambios macroscópicos de energía cinética y potencial, $\mathrm{d}E = \mathrm{d}U$, y por tanto

$$
\mathrm{d}U = \delta Q_{\text{int.,rev.}} - \delta W_{\text{int.,rev.}}.
$$

Dado que el proceso es internamente reversible, podemos sustituir $\delta Q_{\text{int.,rev.}} = T\mathrm{d}S$ y $\delta W_{\text{int.,rev.}} = p\mathrm{d}V$, obteniendo

(eq_Tds_internal_energy)=
$$
\begin{gather*}
\mathrm{d}U = T{}\mathrm{d}S - p{}\mathrm{d}V, \\[10pt]
\mathrm{d}u = T{}\mathrm{d}s - p{}\mathrm{d}v.
\end{gather*}
$$

Esta es la **primera relación $T\mathrm{d}s$**, en forma extensiva y específica.

Introduciendo la **entalpía**, $h = u + Pv$, derivando, y sustituyendo $\mathrm{d}U = T{}\mathrm{d}S - p{}\mathrm{d}V$, se obtiene

(eq_Tds_enthalpy)=
$$
\begin{gather*}
T{}\mathrm{d}S = \mathrm{d}H - V{}\mathrm{d}p, \\[10pt]
T{}\mathrm{d}s = \mathrm{d}h - v{}\mathrm{d}p.
\end{gather*}
$$

Juntas, estas expresiones dan las **relaciones fundamentales $T\mathrm{d}s$**, que normalmente se escriben en forma específica:

(eq_Tds_relations)=
$$
\boxed{
\begin{gather*}
T\mathrm{d}s = \mathrm{d}u + p\mathrm{d}v, \\[10pt]
T\mathrm{d}s = \mathrm{d}h - v\mathrm{d}p.
\end{gather*}
}
$$

:::{important}

**ALCANCE DE LA FORMULACIÓN PARA SISTEMAS CERRADOS**

La formulación para sistemas cerrados aísla la relación entre **energía** y **entropía** en su forma más sencilla. Para **sistemas abiertos**, las mismas relaciones $T\mathrm{d}s$ se aplican **localmente**, pero debe añadirse un término adicional que contabilice la **entropía transportada por el flujo de masa**. Esta extensión conduce a las **ecuaciones de energía y entropía en régimen estacionario**, usadas en turbomáquinas e intercambiadores de calor.
:::

---

(subsec_entropy_variation_model)=
### Variaciones de entropía según el modelo de sustancia

La evaluación de variaciones de entropía depende del comportamiento de la **sustancia de trabajo**. Aunque las relaciones $T\mathrm{d}s$ son generales, su uso práctico exige especificar el **modelo de sustancia** — ya sea un **gas ideal**, un **gas perfecto**, o una **sustancia real (pura)**. Cada caso implica una relación distinta entre $p$, $v$ y $T$, y por tanto una expresión diferente para la variación de entropía.

---

(subsubsec_entropy_variation_ideal_gas)=
### Variación de entropía en gases ideales

Para un **gas ideal**,

$$
\begin{gather*}
pv = RT, \\[10pt]
\mathrm{d}u = c_v(T)\mathrm{d}T, \\[10pt]
\mathrm{d}h = c_p(T)\mathrm{d}T.
\end{gather*}
$$

Sustituyendo estas expresiones en las relaciones $Tds$ se obtiene:

$$
\begin{gather*}
\mathrm{d}s = c_v(T)\frac{\mathrm{d}T}{T} + R\frac{\mathrm{d}v}{v}, \\[10pt]
\mathrm{d}s = c_p(T)\frac{\mathrm{d}T}{T} - R\frac{\mathrm{d}p}{p}.
\end{gather*}
$$

Integrando entre dos estados $(1)$ y $(2)$:

(eq_entropy_ideal_gas)=
$$
\boxed{
\begin{gather*}
s_2 - s_1 = \int_{T_1}^{T_2}\frac{c_v(T)}{T}\mathrm{d}T + R\ln\frac{v_2}{v_1}, \\[10pt]
s_2 - s_1 = \int_{T_1}^{T_2}\frac{c_p(T)}{T}\mathrm{d}T - R\ln\frac{p_2}{p_1}.
\end{gather*}
}
$$

La primera forma se usa cuando se conocen los volúmenes específicos; la segunda, cuando se conocen las presiones. Ambas son equivalentes gracias a la ecuación de estado del gas ideal.

:::{note}

**INTERPRETACIÓN DEL INTEGRAL**

El término $\displaystyle \int \frac{c(T)}{T}\mathrm{d}T$ representa la **variación de entropía debida a cambios de temperatura**, mientras que el término logarítmico describe el **efecto de expansión o compresión**.
:::

---

(subsubsec_entropy_variation_perfect_gas)=
#### Variación de entropía en gases perfectos

Si los calores específicos son constantes ($c_p$, $c_v = \text{const.}$), las integrales se vuelven analíticas:

(eq_entropy_perfect_gas)=
$$
\boxed{
\begin{gather*}
s_2 - s_1 = c_v \ln\frac{T_2}{T_1} + R\ln\frac{v_2}{v_1}, \\[10pt]
s_2 - s_1 = c_p \ln\frac{T_2}{T_1} - R\ln\frac{p_2}{p_1}.
\end{gather*}
}
$$

Estas **formas logarítmicas** se emplean ampliamente para el aire y los gases de combustión bajo condiciones moderadas.

---

(subsubsec_entropy_variation_pure_substances)=
#### Variación de entropía en sustancias puras

Cuando la sustancia de trabajo **no se comporta como un gas ideal**, las formas analíticas anteriores dejan de ser válidas. Para **sustancias puras** como agua o refrigerantes, los valores de entropía deben obtenerse de **tablas de propiedades termodinámicas** o **correlaciones experimentales**.

Como $s$ es una **propiedad de estado**, su valor queda determinado de manera única una vez que se fijan **dos variables intensivas independientes** (por ejemplo, $T$ y $p$), según el **postulado del estado**. En consecuencia, $s$ puede tabularse igual que $u$, $h$ o $v$.

Por ello, para sustancias reales, las variaciones de entropía se evalúan leyendo directamente $s_1$ y $s_2$ de tablas o interpolando entre estados próximos.

:::{important}

**RESUMEN DE LOS CÁLCULOS DE VARIACIÓN DE ENTROPÍA**

| **Modelo / Tipo de sustancia** | **Comportamiento de $c_p$, $c_v$** | **Expresión de la entropía**       | **Fuente de datos / Integración**       |
| :----------------------------- | :--------------------------------- | :---------------------------------- | :---------------------------------------- |
| **Gas ideal**                  | $c_p(T)$, $c_v(T)$                 | Forma integral                      | Requiere correlaciones $c(T)$             |
| **Gas perfecto**               | $c_p$, $c_v$ constantes            | Forma logarítmica                   | Integración analítica directa             |
| **Sustancia pura**             | No ideal / tabulada                | $s(T,p)$ o $s(T,v)$ de tablas        | Datos experimentales / interpolación      |

:::

---

(subsec_the_isoentropic_condition)=
### La condición isoentrópica

Antes de explorar la forma matemática de las relaciones isoentrópicas, es esencial aclarar el significado físico de la **condición isoentrópica**. Un proceso es *isoentrópico* cuando se desarrolla sin **ningún cambio de entropía**.

Estas transformaciones representan el **límite ideal de referencia** para compresiones y expansiones reales, especialmente en gases, turbinas, compresores o toberas. Aplicando las relaciones $T\mathrm{d}s$ a un **gas perfecto**, la condición isoentrópica produce relaciones analíticas entre presión, temperatura y volumen específico. Más adelante constituirán la base para evaluar el rendimiento de dispositivos donde el comportamiento adiabático casi reversible es una buena aproximación.

Un proceso es **isoentrópico** cuando el **cambio neto de entropía del sistema es cero**:

$$
\Delta S_{\text{sys.}} = 0.
$$

Esto simplemente significa que, entre los estados inicial y final, el **contenido total de entropía** del sistema permanece invariable — aunque la energía pueda intercambiarse en distintas formas.

La entropía de un sistema puede cambiar por dos motivos distintos:

1. **Transferencia de entropía** debida a **intercambio de calor** a través de la frontera.
2. **Generación de entropía** debida a **irreversibilidades internas** (fricción, mezclado, diferencias finitas de temperatura, etc.).

Matemáticamente:

$$
\Delta S_{\text{sys.}} = \Delta S = \int \frac{Q}{T} + S_{\text{gen.}} = \Delta S_{\text{transf.}} + S_{\text{gen.}},
$$

donde $S_{\text{gen.}} \ge 0$ es la entropía generada internamente.

La **manera más simple** de cumplir $\Delta S = 0$ es imponer **adiabaticidad** ($Q = 0$) *y* **reversibilidad** ($S_{\text{gen.}} = 0$). Así, no cruza calor por la frontera ni se genera entropía internamente: el proceso es realmente isoentrópico. Esta combinación define el **proceso isoentrópico ideal**, usado típicamente en el análisis de turbinas, compresores y toberas.

Sin embargo, un proceso **adiabático y reversible** es solo **una** forma de lograr isoentropía, no la única. Otras combinaciones pueden también resultar en $\Delta S = 0$ bajo circunstancias especiales:

* Un proceso **no adiabático e irreversible** puede ser isoentrópico si el aumento de entropía por irreversibilidad se **compensa exactamente** con una pérdida de entropía vía transferencia de calor.
* Un proceso **no adiabático y reversible** generalmente **no** es isoentrópico, pues hay intercambio de entropía con los alrededores.

:::{important}

**RUTAS HACIA LA ISOENTROPÍA**

| **Tipo de proceso**                     | **¿Adiabático?** | **¿Reversible?** | **¿isoentrópico?**        | **Comentarios**                                                        |
| :-------------------------------------- | :-------------- | :-------------- | :----------------------- | :--------------------------------------------------------------------- |
| Adiabático + Reversible                 | Sí              | Sí              | Sí                       | isoentrópico ideal (sin calor, sin generación).                         |
| No adiabático + Irreversible            | No              | No              | Puede (caso especial)       | Posible si $\Delta S_{\text{transf.}} + S_{\text{gen.}} = 0$.          |
| Adiabático + Irreversible               | Sí              | No              | No                       | Se genera entropía internamente.                                      |
| No adiabático + Reversible              | No              | Sí              | No                       | Se intercambia entropía con los alrededores.                           |
| No adiabático + Irreversible (general)  | No              | No              | No                       | La mayoría de procesos reales.                             |

:::

Por lo tanto, **isoentrópico $\neq$ adiabático + reversible**, aunque esa sea la vía **más directa e idealizada**. Un proceso isoentrópico es, en esencia, aquel donde **el balance total de entropía es cero**, independientemente del mecanismo que lo permita.

---

(subsec_closed_form_relations_ideal_gases)=
### Relaciones en forma cerrada para gases ideales

Con la **condición isoentrópica** establecida ($\Delta S_{\text{sys}} = 0$), la vía más práctica para obtener fórmulas analíticas es el caso **adiabático + reversible**. Para gases ideales, esto conduce — a través de las relaciones $T\mathrm{d}s$ — a **leyes potenciales** que vinculan $T$, $p$ y $v$. Estas expresiones son valiosísimas para el dimensionamiento y análisis de **turbinas, compresores y toberas**, pues permiten calcular cambios de estado sin integrar caminos, siempre que el gas pueda modelarse como **perfecto** (constantes $c_p$, $c_v$, y por tanto $\gamma$). Cuando $c_p(T)$ y $c_v(T)$ varían (gas ideal no perfecto), la condición sigue siendo válida, pero las relaciones requieren **integrales de temperatura**.

Para derivar estas relaciones de forma cerrada, partimos de las ecuaciones diferenciales del **gas perfecto** ($c_p$, $c_v$ constantes; $R = c_p - c_v$) y de cualquiera de las relaciones $T\mathrm{d}s$:

1. Con las variables $(T,v)$:

    $$
    \mathrm{d}s = c_v\frac{\mathrm{d}T}{T} + R\frac{\mathrm{d}v}{v}.
    $$

    Condición isoentrópica $\mathrm{d}s = 0$:

    $$
    c_v\frac{\mathrm{d}T}{T} = -R\frac{\mathrm{d}v}{v}.
    $$

    Integramos entre $(1)$ y $(2)$:

    $$
    c_v\ln\frac{T_2}{T_1} = -R\ln\frac{v_2}{v_1}.
    $$

    Usando $\displaystyle \frac{R}{c_v} = \gamma - 1$ (con $\gamma = c_p/c_v$):

    $$
    \ln\frac{T_2}{T_1} = -(\gamma-1)\ln\frac{v_2}{v_1}
    \implies
    \frac{T_2}{T_1} = \Big(\frac{v_1}{v_2}\Big)^{\gamma-1}.
    $$

    Relación de estado:

    $$
    \boxed{T v^{\gamma-1} = \text{const.}}
    $$

3. Con las variables $(T,p)$:

    $$
    \mathrm{d}s = c_p\frac{\mathrm{d}T}{T} - R\frac{\mathrm{d}p}{p}.
    $$

    De nuevo, $\mathrm{d}s = 0$:

    $$
    c_p\frac{\mathrm{d}T}{T} = R\frac{\mathrm{d}p}{p}
    \implies
    \ln\frac{T_2}{T_1} = \frac{R}{c_p}\ln\frac{p_2}{p_1}.
    $$

    Como $\displaystyle \frac{R}{c_p} = \frac{\gamma-1}{\gamma}$:

    $$
    \frac{T_2}{T_1} = \Big(\frac{p_2}{p_1}\Big)^{(\gamma-1)/\gamma}
    \implies
    \boxed{T p^{(1-\gamma)/\gamma} = \text{const.}}
    $$

4. Para obtener la forma $(p,v)$:

    Partimos de:

    $$
    \begin{gather*}
    Tv^{\gamma-1}=\text{const.}, \\[10pt]
    Tp^{(1-\gamma)/\gamma}=\text{const.}.
    \end{gather*}
    $$

    Expresando $T$:

    $$
    \begin{gather*}
    T = C_1 v^{1-\gamma}, \\[10pt]
    T = C_2 p^{(\gamma-1)/\gamma}.
    \end{gather*}
    $$

    Igualamos:

    $$
    C_1 v^{1-\gamma} = C_2 p^{(\gamma-1)/\gamma}
    \implies
    p^{(\gamma-1)/\gamma} v^{\gamma-1} = \text{const.}
    $$

    Elevando a la potencia $\gamma/(\gamma-1)$:

    $$
    \boxed{p v^{\gamma} = \text{const.}}.
    $$

Por tanto, la condición isoentrópica para **gases perfectos** se expresa mediante tres relaciones equivalentes:

(eq_isoentropic_relations)=
$$
\boxed{
\begin{gather*}
T v^{\gamma-1} = \text{const.}, \\[10pt]
T p^{(1-\gamma)/\gamma} = \text{const.}, \\[10pt]
p v^{\gamma} = \text{const.}
\end{gather*}
}
$$

:::{important}

**POR QUÉ LA CONDICIÓN ISOENTRÓPICA IMPONE $pv^{\gamma}=\text{const.}$**

Observa que la relación $pv^{\gamma}=\text{const.}$ se ha derivado a partir de la condición isoentrópica aplicada a un gas perfecto. Esa misma expresión se había utilizado con anterioridad al calcular el trabajo de un gas perfecto en un sistema simple compresible **bajo la restricción de un proceso adiabático**.

Ten en cuenta que la adiabaticidad ya impide la transferencia de entropía mediante intercambio de calor (es decir, $Q = 0 \implies \Delta S_{\text{transf.}} = 0$). Además, el cálculo del trabajo se llevó a cabo bajo la condición adicional de que el proceso fuera **cuasiestático**, lo cual implica que es **reversible**. Por tanto, de forma implícita, la relación $pv^{\gamma}=\text{const.}$ utilizada antes estaba imponiendo una condición isoentrópica.

Un proceso **adiabático y cuasiestático** es también un proceso **isoentrópico**.

:::

---

(subsec_Ts_diagram)=
### El diagrama $T\!-\!s$ y su interpretación gráfica

Una vez definidas las variaciones de entropía (mediante las relaciones $T\mathrm{d}s$), evaluadas para distintos **modelos de sustancia** (gases ideales/perfectos y sustancias reales), y aclarada la **condición isoentrópica** (incluyendo su especialización adiabática–reversible), introducimos ahora el **diagrama $T\!-\!s$**. Este diagrama es el complemento natural del **diagrama $p\!-\!v$**: así como el **trabajo** se representa por áreas en el plano $p\!-\!v$, el **calor reversible** se representa por áreas en el plano $T\!-\!s$. Ambos planos proporcionan un registro geométrico claro de las dos magnitudes fundamentales de proceso.

* **Complementariedad gráfica: $p-v$ (trabajo) vs. $T-s$ (calor reversible)**  

    Para cualquier interacción de **trabajo cuasiestático** (de frontera):

    $$
    \delta W_{\text{rev.}} = p\mathrm{d}V \implies W_{\text{rev.}} = \int p\,\mathrm{d}V,
    $$

    de modo que el **área bajo la curva** en un diagrama $p-v$ representa el **trabajo reversible** (y el área encerrada por un ciclo representa el **trabajo neto**). Para cualquier interacción de **calor internamente reversible**:

    $$
    \delta Q_{\text{rev.}} = T\mathrm{d}S \implies Q_{\text{rev.}} = \int T\,\mathrm{d}S,
    $$

    de modo que el **área bajo la curva** en un diagrama $T-s$ representa el **calor reversible** (y el área encerrada por un ciclo equivale al **calor neto reversible**). Estas dos integrales constituyen las expresiones diferenciales de la **$1^{\text{a}}$** y **$2^{\text{a}}$** ley en sus formas más útiles para integración de trayectoria.

* **Formas explícitas $T-s$ para gases perfectos (constantes $c_p$, $c_v$)**  

   Para un **gas perfecto** ($c_p, c_v = \text{const.}$; $R = c_p - c_v$), las relaciones $T\mathrm{d}s$ se integran en las formas logarítmicas:

    $$
    \mathrm{d}s = c_v\frac{\mathrm{d}T}{T} + R\frac{\mathrm{d}v}{v}
    \implies
    s - s_0 = c_v\ln\frac{T}{T_0} + R\ln\frac{v}{v_0},
    $$

    $$
    \mathrm{d}s = c_p\frac{\mathrm{d}T}{T} - R\frac{\mathrm{d}p}{p}
    \implies
    s - s_0 = c_p\ln\frac{T}{T_0} - R\ln\frac{p}{p_0}.
    $$

    De aquí se obtienen **formas explícitas exponenciales**, muy útiles para representar procesos en el plano $T-s$:

    * **Forma $(T,v,s)$:**

        $$
        T = T_0 e^{\frac{s-s_0}{c_v}}
        \Big(\frac{v_0}{v}\Big)^{R/c_v}
        $$

    * **Forma $(T,p,s)$:**

        $$
        T = T_0 e^{\frac{s-s_0}{c_p}}
        \Big(\frac{p}{p_0}\Big)^{R/c_p}
        $$

    * **Casos especiales útiles** (gas perfecto):
        * **Isocórico** ($v=$ const.):  
          $s-s_0 = c_v\ln(T/T_0) \implies T = T_0 e^{(s-s_0)/c_v}$.
        * **Isobárico** ($p=$ const.):  
          $s-s_0 = c_p\ln(T/T_0) \implies T = T_0 e^{(s-s_0)/c_p}$.
        * **Isotermo** ($T=$ const.): línea horizontal.
        * **isoentrópico** ($s=$ const.): línea vertical.

* **Uso práctico del diagrama $T-s$**

    * Para **gases ideales/perfectos**, las relaciones anteriores permiten **parametrizar la trayectoria** en el plano $T-s$ y calcular  
      $Q_{\text{rev.}} = \int T\,\mathrm{d}S$ directamente como el área bajo la curva.
    
    * Para **sustancias puras (no ideales)**, $s(T,p)$ o $s(T,v)$ proviene de **tablas**, pero la **regla del área sigue siendo válida**:
      $Q_{\text{rev.}} = \int T\,\mathrm{d}S$.  
      El diagrama $T-s$ incluye la **campana de saturación** (líquido subenfriado, región bifásica, vapor recalentado). A lo largo de la **vaporización**, $s$ **aumenta**; a lo largo de la **condensación**, $s$ **disminuye** — las áreas rectangulares/curvilíneas correspondientes cuantifican el calor reversible.

:::{note}

**AUMENTO DE ENTROPÍA EN PROCESOS ISOCÓRICOS E ISOBÁRICOS**

Según las expresiones derivadas arriba, en procesos isocóricos e isobáricos la temperatura evoluciona como $\propto e^{s/c_v}$ y $\propto e^{s/c_p}$, respectivamente. Como ya se ha demostrado que $c_p > c_v$, se tiene $1/c_v > 1/c_p$ y, en consecuencia, la relación $T(s)$ es más **empinada** en el caso isócoro. Para una misma diferencia de temperatura $\Delta T$, el incremento de entropía $\Delta S$ será **mayor** en el proceso isobárico que en el isócoro.

Esta deducción, basada únicamente en la relación funcional $T(s)$, también puede obtenerse desde la noción del calor como mecanismo de transferencia de entropía:

* En un sistema cerrado sometido a un proceso isócoro (recipiente rígido), el calor requerido incrementa solo la energía interna.
* En un sistema cerrado sometido a un proceso isobárico (pistón–cilindro), el calor requerido incrementa la entalpía.
* El aumento de entalpía **siempre requiere más calor** que el aumento de energía interna. En el proceso isobárico, parte del calor se convierte en el trabajo mecánico para elevar el pistón; en el isócoro, todo el calor va a aumentar la energía interna.
* Al requerirse más calor en el caso isobárico, la **transferencia de energía asociada** a un mismo aumento de temperatura es mayor.
:::

---

(subsec_conceptual_closure_entropy_Tds)=
### Cierre conceptual

* Las **relaciones $T\mathrm{d}s$** son la expresión diferencial de la **$2^{\text{a}}$ ley** para una sustancia simple compresible.

* Estas relaciones son **locales** y se extienden a **sistemas abiertos** añadiendo el **transporte de entropía por flujo de masa**; constituyen la base de las ecuaciones de energía/entropía en régimen estacionario usadas en turbomáquinas, compresores, toberas e intercambiadores de calor.

* Calcular **variaciones de entropía** requiere un **modelo de sustancia**:

  * **Gas ideal** $(c_p(T), c_v(T))$: formas integrales con  
    $\displaystyle \int \frac{c(T)}{T}\,\mathrm{d}T$ más términos logarítmicos.
  * **Gas perfecto** ($c_p$, $c_v$ constantes): expresiones **logarítmicas cerradas** (analíticas).
  * **Sustancia pura (real)**: valores tabulados; $s$ queda fijada por dos propiedades intensivas independientes.

* La **condición isoentrópica** significa **cambio neto nulo de entropía** ($\Delta S = 0$). La ruta más sencilla es **adiabática + reversible** ($Q = 0$, $S_{\text{gen}} = 0$), pero otros balances especiales (no adiabático + irreversible) también pueden llevar a $\Delta S = 0$.

* Para **gases perfectos**, la especialización adiabático–reversible da las clásicas **leyes potenciales**:  
  * $T v^{\gamma-1}=\text{const.}$  
  * $T p^{(1-\gamma)/\gamma}=\text{const.}$  
  * $p v^{\gamma}=\text{const.}$

* Los planos **$p-v$** y **$T-s$** son **complementarios**: trabajo ↔ área en $p-v$; calor reversible ↔ área en $T-s$. Esta dualidad proporciona un registro geométrico claro de **trabajo** y **calor reversible** en procesos y ciclos.
