(sec_specific_heats_as_properties)=
## Calores específicos

Cuando un sistema recibe energía en forma de calor, su temperatura normalmente aumenta. La forma en que ocurre ese aumento depende de **cómo se condiciona el proceso** — por ejemplo, si el sistema puede expandirse o no. Algunos de estos procesos condicionados pueden reproducirse fácilmente de manera experimental, lo que permite **relacionar magnitudes medibles** como la energía añadida y el incremento de temperatura resultante. De estos experimentos controlados surgen las definiciones de los **calores específicos**, que conectan los cambios en energía interna y entalpía con las variaciones de temperatura.

En términos generales, el parámetro de **calor específico** se concibe como una constante de proporcionalidad entre el calor transferido en un proceso y la variación de temperatura experimentada por el sistema; como tal, la relación más general para un intercambio infinitesimal de energía en forma de calor adopta la expresión:

(eq_general_specific_heat_relation)=
$$
\delta q = c\,\mathrm{d}T.
$$

El propósito principal de esta sección es situar la expresión anterior sobre una base termodinámica sólida.

---

(subsec_heat_under_constraints)=
### Transferencia de calor derivada de la $1^{\text{a}}$ ley

Partiendo de la {ref}`forma diferencial <eq_first_law_reduced_diff>` de la $1^{\text{a}}$ ley para sistemas cerrados, pueden considerarse dos restricciones experimentales particularmente simples. Estos casos no solo son conceptualmente sencillos, sino también **fáciles de reproducir en condiciones de laboratorio**, ya que se basan en montajes físicos simples que aíslan un mecanismo de transferencia de energía a la vez:

* **Volumen constante (proceso isocórico):**

  Esta condición se logra encerrando la sustancia en un **recipiente rígido y sellado**, de modo que no pueda producirse cambio de volumen ($\mathrm{d}v = 0$). El sistema no puede realizar trabajo de frontera, y la expresión se reduce a:

  $$
  \mathrm{d}U = \delta Q.
  $$

  Así, el **calor transferido** (por unidad de masa, o en forma específica) equivale al **cambio en energía interna**:

  $$
  \boxed{\delta q|_{v=\text{const.}} = \delta q_v = \mathrm{d}u}.
  $$

* **Presión constante (proceso isobárico):**

  Esta configuración se obtiene permitiendo que el sistema se expanda o contraiga contra una **presión externa constante** — por ejemplo, mediante un **conjunto pistón–cilindro** abierto a la atmósfera. En esta condición ($\mathrm{d}p = 0$), podemos reescribir la $1^{\text{a}}$ ley en {ref}`términos de entalpía <eq_heat_enthalpy_relation1>` y obtener:

  $$
  \mathrm{d}H = \delta Q.
  $$

  Por tanto, a presión constante, la **transferencia de calor** (de nuevo, en términos específicos) equivale al **cambio de entalpía** (el subíndice ${p}$ indica que la presión se mantiene constante):

  $$
  \boxed{\delta q|_{p=\text{const.}} = \delta q_p = \mathrm{d}h}.
  $$

Estas dos situaciones — volumen constante y presión constante — son los montajes experimentales más fundamentales para estudiar la relación entre **aporte de calor** y **variación de temperatura**, ya que pueden realizarse con aparatos simples y bien controlados.

:::{note}

**POR QUÉ IMPORTA LA FACTIBILIDAD EXPERIMENTAL**

La relevancia de estas dos restricciones radica en que pueden lograrse prácticamente y controlarse con precisión. Un recipiente rígido impone naturalmente volumen constante, mientras que un pistón–cilindro expuesto a la atmósfera mantiene presión constante. Esta factibilidad experimental permite medir directamente cuánto calor se requiere para cambiar la temperatura de una sustancia bajo cada condición — haciendo que $c_v$ y $c_p$ sean propiedades medibles, reproducibles y físicamente significativas.
:::

---

(subsec_experimental_basis_specific_heats)=
### Origen experimental de los calores específicos

En ambos experimentos — **volumen constante** y **presión constante** — la energía añadida como calor produce un **aumento de temperatura** que puede medirse. La proporcionalidad entre el incremento de temperatura y la energía suministrada conduce naturalmente a la introducción de los **calores específicos**.

Dado que la **energía interna** $u$ y la **entalpía** $h$ son **propiedades de estado** — cada una dependiente de variables medibles como temperatura y presión o volumen — sus cambios pueden expresarse mediante **derivadas parciales**, donde se mantiene fijo un parámetro mientras varía el otro.

{ref}`Por el postulado de estado <subsec_state_postulate>`, sabemos que dos variables intensivas independientes bastan para determinar el estado termodinámico de un sistema compresible simple. Mantener una de ellas (ya sea presión o volumen específico) constante mientras se varía la temperatura aísla cómo cambia la energía con $T$ bajo esa condición específica.

* A **volumen constante**:

  $$
  \left(\frac{\partial u}{\partial T}\right)_v = c_v \ [\text{kJ}/(\text{kg}{\cdot}\text{K})].
  $$

* A **presión constante**:

  $$
  \left(\frac{\partial h}{\partial T}\right)_p = c_p \ [\text{kJ}/(\text{kg}{\cdot}\text{K})].
  $$

Estas relaciones muestran cómo **energía interna** y **entalpía** responden a cambios de temperatura para una sustancia dada, definiendo los **calores específicos** $c_v$ y $c_p$ como **coeficientes basados en propiedades** — característicos de la sustancia y su estado termodinámico, igual que $u$ o $h$.

En la práctica, cuando estos experimentos se repiten en intervalos de temperatura más amplios, se observa que la proporcionalidad entre el calor suministrado y el cambio de temperatura **no permanece estrictamente lineal**. Esta desviación indica que la cantidad de energía necesaria para elevar la temperatura de una sustancia en un grado depende de cuánta parte de su estructura interna (modos traslacionales, rotacionales, vibracionales) está energéticamente activa a esa temperatura. Por ello, los calores específicos deben considerarse como **magnitudes dependientes de la temperatura**:

$$
c_v = c_v(T), \qquad c_p = c_p(T),
$$

ya que los mecanismos microscópicos que gobiernan el almacenamiento de energía evolucionan con la temperatura.

:::{important}

**EL CALOR NO ES UNA PROPIEDAD DE ESTADO**

Aunque las expresiones $\delta q_v = c_v\mathrm{d}T$ y $\delta q_p = c_p\mathrm{d}T$ puedan parecer indicar que el calor ($Q$) es una propiedad de estado, esto **no es así**.

El calor es una **magnitud de proceso**, no una propiedad del estado. Depende de la **trayectoria** seguida entre dos estados — incluso si, bajo ciertas restricciones, su cambio infinitesimal parece tener una forma diferencial simple. Solo las magnitudes relacionadas con la energía ($u$, $h$) son **funciones de estado**; el calor $q$ es simplemente el **modo de transferencia** mediante el cual cambian esas propiedades.

| **Magnitud**                | **Expresión (forma infinitesimal)** | **¿Siempre válida?** | **¿Requiere restricción?** | **Tipo de restricción**              |
| :-------------------------- | :---------------------------------- | :-------------------: | :-------------------------: | :----------------------------------- |
| Variación de energía interna | $\mathrm{d}u = c_v\mathrm{d}T$     |          Sí           |             No             | Definición siempre válida de $c_v$  |
| Variación de entalpía        | $\mathrm{d}h = c_p\mathrm{d}T$     |          Sí           |             No             | Definición siempre válida de $c_p$  |
| Transferencia de calor (isocórico) | $\delta q_v = c_v\mathrm{d}T$ |          No           |             Sí             | $v = \text{constante}$              |
| Transferencia de calor (isobárico)  | $\delta q_p = c_p\mathrm{d}T$ |          No           |             Sí             | $p = \text{constante}$              |
:::



:::{note}

**SOBRE LAS UNIDADES DE LOS CALORES ESPECÍFICOS**

Obsérvese que tanto $c_v$ como $c_p$ se miden en $[\text{kJ}/(\text{kg}{\cdot}\text{K})]$, lo que significa que los calores específicos expresan la **cantidad de energía necesaria para elevar la temperatura de un kilogramo de sustancia en un kelvin**, bajo la restricción especificada (volumen constante o presión constante).
:::

---

(subsec_three_models_real_ideal_perfect_gases)=
### Tres modelos: gases reales, ideales y perfectos

Hasta ahora, hemos reconocido dos enfoques principales para describir el comportamiento de los gases: {ref}`gases reales e ideales <subsec_equation_of_state_gases>`. En los **gases reales**, las fuerzas intermoleculares desempeñan un papel importante, y su influencia debe considerarse en la ecuación de estado, que puede volverse bastante compleja. En contraste, los **gases ideales** son aquellos en los que dichas fuerzas se desprecia y las moléculas se comportan como partículas independientes. Su comportamiento está gobernado por la ley simple $pv = RT$.

Al considerar la dependencia de los calores específicos, esta distinción se vuelve aún más clara. Para **gases reales**, los calores específicos varían tanto con la **temperatura** como con la **presión (o volumen)**, reflejando los efectos de las interacciones moleculares:

$$
c_v = c_v(T, p), \qquad c_p = c_p(T, p).
$$

Para **gases ideales**, donde los efectos intermoleculares están ausentes, la **energía interna** ($u$) y la **entalpía** ($h$) dependen **solo de la temperatura**, y lo mismo ocurre con sus derivadas:

$$
c_v = c_v(T), \qquad c_p = c_p(T).
$$

Esta simplificación hace que los gases ideales sean particularmente convenientes para el modelado analítico, ya que desacopla los efectos térmicos de las variaciones de presión o volumen.

Aún más, una simplificación adicional define el **gas perfecto**, un caso especial del gas ideal en el que se **suponen constantes** $c_v$ y $c_p$ en el intervalo de temperatura considerado.

:::{important}

**RESUMEN DE LOS TRES MODELOS DE GAS**

| **Tipo de gas**    | **Dependencia de $c_v$, $c_p$**               | **Interacciones**                         |            **Ecuación de estado**            |
| :----------------- | :------------------------------------------- | :--------------------------------------- | :-------------------------------------------: |
| **Gas real**       | $c_v = c_v(T,p)$, $c_p = c_p(T,p)$           | Fuerzas intermoleculares significativas  | No ideal (p. ej., van der Waals, forma virial) |
| **Gas ideal**      | $c_v = c_v(T)$, $c_p = c_p(T)$               | Sin interacciones; solo colisiones elásticas |                  $pv = RT$                  |
| **Gas perfecto**   | $c_v = \text{const.}$, $c_p = \text{const.}$ | Mismas suposiciones que el gas ideal     |                  $pv = RT$                  |
:::

Así, todo gas perfecto es un gas ideal, pero no todo gas ideal es perfecto — y ningún gas real es ideal. Para cálculos energéticos, estas distinciones conducen a las siguientes expresiones generales:

$$
\Delta u = \int_{T_1}^{T_2} c_v(T)\mathrm{d}T,
\qquad
\Delta h = \int_{T_1}^{T_2} c_p(T)\mathrm{d}T,
$$

que, en la **aproximación de gas perfecto**, se simplifican a:

$$
\boxed{\Delta u = c_v\Delta T, \qquad \Delta h = c_p\Delta T.}
$$

::::{important}

**EL EXPERIMENTO DE EXPANSIÓN LIBRE DE JOULE**

El **experimento de expansión libre de Joule** proporciona evidencia experimental directa de que, para un **gas ideal**, tanto la **energía interna** como la **entalpía** dependen únicamente de la temperatura.

En el montaje clásico de Joule, se permitió que un gas **se expandiera libremente** hacia el vacío desde un recipiente rígido a otro, ambos aislados térmicamente (una **expansión libre adiabática**). Las observaciones clave fueron:

1. **No hubo intercambio de calor** con el entorno ($Q = 0$).
2. **No se realizó trabajo** por parte del gas ($W = 0$), ya que la expansión ocurrió contra el vacío.

A partir de la $1^{\text{a}}$ ley para un sistema cerrado:

$$
\Delta U = Q - W,
$$

se deduce que:

$$
\Delta U = 0.
$$

Sin embargo, después de la expansión, se observó que el gas tenía la **misma temperatura** que antes. Así, dado que $\Delta U = 0$ y $\Delta T = 0$, Joule concluyó que, para tales gases:

$$
U = U(T),
$$

es decir, **la energía interna de un gas ideal depende solo de la temperatura**, no del volumen ni de la presión.

Extendiendo este resultado a la entalpía:

$$
h = u + pv,
$$

y usando la ley del gas ideal $pv = RT \implies pv=f(T)$, se sigue que:

$$
h = h(T),
$$

porque tanto $u$ como $RT$ son funciones únicamente de la temperatura.

Este experimento estableció, por tanto, una propiedad fundamental de los gases ideales:



:::{epigraph}
**Para un gas ideal, tanto $u$ como $h$ son funciones únicamente de la temperatura — independientes de la presión y el volumen.**
:::

:::{note}

**SIGNIFICADO DEL RESULTADO DE JOULE**

El hallazgo de Joule no solo confirmó la validez del modelo de gas ideal, sino que también proporcionó la base física para usar calores específicos dependientes de la temperatura $c_v(T)$ y $c_p(T)$, ya que:

$$
\mathrm{d}u = c_v(T)\mathrm{d}T, \qquad \mathrm{d}h = c_p(T)\mathrm{d}T.
$$

Estas relaciones son válidas para todos los gases ideales y constituyen la base de la mayoría de los análisis termodinámicos que implican cambios de temperatura.
:::

::::

---

(subsec_relation_between_specific_heats)=
### Relación entre $c_p$ y $c_v$

Reconocer que tanto $c_v$ como $c_p$ describen cómo varían la energía interna y la entalpía con la temperatura permite explorar cómo están **interrelacionados**. Para un gas ideal (o perfecto), la relación entre $c_p$ y $c_v$ se deduce directamente de la {ref}`definición de entalpía <eq_enthalpy_def>`:

$$
h = u + RT \ \Rightarrow \ \mathrm{d}h = \mathrm{d}u + R\mathrm{d}T.
$$

Sustituyendo las formas diferenciales $\mathrm{d}u = c_v\mathrm{d}T$ y $\mathrm{d}h = c_p\mathrm{d}T$ se obtiene la **relación de Mayer**:

(eq_mayer_relation)=
$$
\boxed{c_p - c_v = R} \ .
$$

Esta expresión simple vincula ambos calores específicos mediante la constante del gas y revela cuánta energía adicional debe suministrarse a presión constante para compensar el trabajo de expansión.

:::{note}

**EL PAPEL DE $R$ EN LOS PROCESOS ISOTÉRMICOS**

De forma análoga a cómo aparecen $c_v$ y $c_p$ bajo sus respectivas restricciones (isocórica e isobárica), la **constante del gas** $R$ desempeña un papel similar en los procesos **isotérmicos** de **gases ideales**, donde la temperatura permanece constante pero **presión** y **volumen** varían.

En tales casos, a partir de la **relación de Mayer**:

$$
R = c_p - c_v,
$$

la constante del gas representa la **energía necesaria para que una unidad de masa (o mol) de gas se expanda por unidad de cambio de temperatura a presión constante**, en comparación con volumen constante — es decir, la *energía por unidad de temperatura que se destina al trabajo de expansión ($p\Delta{}v$)* en lugar de a la energía interna.

Durante los **procesos isotérmicos**, $\Delta T = 0 \Rightarrow \Delta u = \Delta h = 0$, por lo que la transferencia de calor $Q$ se convierte totalmente en **trabajo de frontera** $W$. Usando la ley del gas ideal $pv = RT$, tenemos:

$$
w = q = \int_{v_1}^{v_2} p\mathrm{d}v = RT \ln\frac{v_2}{v_1}.
$$

Así, mientras que $c_v$ y $c_p$ conectan los cambios de temperatura con las variaciones de energía interna y entalpía bajo restricciones fijas, **$R$ gobierna el intercambio de energía durante transformaciones isotérmicas** — cuantificando cuánta energía (por unidad de masa o mol) se transfiere como trabajo cuando un gas ideal se expande o comprime *sin cambiar su temperatura*.

En resumen:

| Tipo de proceso | Restricción          | Relación gobernante         | Significado físico                                        |
| :-------------- | :------------------- | :-------------------------- | :-------------------------------------------------------- |
| Isocórico       | $v = \text{const.}$ | $\Delta u = c_v \Delta T$  | El calor cambia solo la energía interna                  |
| Isobárico       | $p = \text{const.}$ | $\Delta h = c_p \Delta T$  | El calor cambia energía interna y trabajo $pv$           |
| Isotérmico      | $T = \text{const.}$ | $q = w = RT \ln(v_2/v_1)$  | El calor se convierte totalmente en trabajo (sin $\Delta u$, $\Delta h$) |
:::

La razón entre los dos calores específicos,

(eq_gamma_def)=
$$
\boxed{\gamma = \frac{c_p}{c_v}} \ ,
$$

es adimensional y depende de la **estructura molecular** del gas — específicamente del número de grados de libertad activos (traslación, rotación, vibración). Para la mayoría de los gases reales, $\gamma$ disminuye ligeramente con la temperatura a medida que se activan los modos vibracionales.

| **Tipo de gas**               | **Ejemplos moleculares** | **Grados de libertad (aprox.)**                               | $\gamma = c_p/c_v$ (típico) {cite}`2015Cengel` |
| :---------------------------- | :----------------------- | :------------------------------------------------------------: | :---------------------------------------------: |
| **Monoatómico**               | $\text{He}$, $\text{Ne}$, $\text{Ar}$             | 3 traslacionales                                              | $1{,}66–1{,}67$ |
| **Diatómico**                 | $\text{N}_{2}$, $\text{O}_{2}$, $\text{H}_{2}$, Aire | 3 traslacionales + 2 rotacionales                             | $1{,}38–1{,}41$ |
| **Triatómico (lineal)**       | $\text{CO}_{2}$, $\text{N}_{2}\text{O}$             | 3 traslacionales + 2 rotacionales + (1 vibracional a alta $T$) | $1{,}30–1{,}33$ |
| **Triatómico (no lineal)**    | $\text{H}_{2}\text{O}$, $\text{SO}_{2}$             | 3 traslacionales + 3 rotacionales + (vibracionales)           | $1{,}25–1{,}29$ |
| **Poliatómico (≥ 4 átomos)**  | $\text{CH}_{4}$, $\text{C}_{2}\text{H}_{6}$, $\text{NH}_{3}$ | 3 traslacionales + 3 rotacionales + varios vibracionales      | $1{,}10–1{,}20$ |

Dado que $c_p$, $c_v$ y $\gamma$ son **propiedades termodinámicas**, sus valores dependen del tipo de gas y de la temperatura, y por tanto están **tabulados** en manuales de ingeniería y fuentes de referencia para uso práctico {cite}`2015Cengel`.


:::{note}

**SOBRE LA RELACIÓN ENTRE $\gamma$ Y LA ESTRUCTURA MOLECULAR**

La disminución de los valores de $\gamma$ con el aumento de la complejidad molecular ilustra cómo dicha complejidad amplía el número de modos de almacenamiento de energía, haciendo que el gas sea más “flexible” o “adaptable” térmicamente. Esta “mayor capacidad de adaptación” térmica significa que el gas puede **absorber más energía para un mismo incremento de temperatura** — en otras palabras, tiene más formas de almacenar energía internamente (a través de modos rotacionales y vibracionales). A medida que aumenta la complejidad molecular, la energía se distribuye entre más grados de libertad, por lo que la temperatura aumenta menos para la misma entrada de energía, resultando en un valor **menor** de $\gamma$.
:::

---

Más allá de la razón $\gamma = c_p / c_v$, a menudo resulta conveniente introducir un **calor específico generalizado** $c$ para describir **procesos politrópicos**, donde presión y volumen cumplen $p v^n = \text{constante}$. En tales procesos, la capacidad calorífica efectiva $c$ se vincula directamente con el exponente politrópico $n$ mediante la relación:

(eq_polytropic_exponent_relation)=
$$
\boxed{n = \frac{c_p - c}{c_v - c}}.
$$

Esta expresión muestra que el valor de $n$ — y, por tanto, el carácter termodinámico del proceso — depende de la posición relativa del calor específico del proceso $c$ entre $c_v$ y $c_p$. Cuando $c$ se aproxima a $c_v$, el proceso tiende a ser isocórico ($n \to \infty$); cuando $c$ se aproxima a $c_p$, el proceso se vuelve isobárico ($n \to 0$). Los valores intermedios de $c$ corresponden a **procesos politrópicos** con intercambio parcial de calor entre el sistema y su entorno.

| **Tipo de proceso** | **Condición**       | **Índice politrópico** $n$ | **Calor específico efectivo** $c$ |
| :------------------- | :------------------ | :-------------------------: | :--------------------------------: |
| **Isocórico**        | $v = \text{const.}$ |      $n \to \infty$        |             $c = c_v$             |
| **Isobárico**        | $p = \text{const.}$ |          $n = 0$           |             $c = c_p$             |
| **Isotérmico**       | $T = \text{const.}$ |          $n = 1$           | $c \to \pm \infty$ (indefinido)       |
| **Adiabático**       | $Q = 0$             |       $n = \gamma$         |              $c = 0$              |

:::{note}

**SOBRE LA DEDUCCIÓN DE $n=(c_{p} - c)/(c_{v} - c)$**

Para un **sistema compresible simple**, la forma infinitesimal de la primera ley es:

$$
\delta q = \mathrm{d}u + p\mathrm{d}v.
$$

Para un **gas ideal**, $\mathrm{d}u = c_v\mathrm{d}T$, y dado que $p v = R T$, el diferencial del volumen puede expresarse como:

$$
\mathrm{d}v = \frac{R}{p}\mathrm{d}T - \frac{R T}{p^2}\mathrm{d}p.
$$

Sustituyendo de nuevo:

$$
\delta q = c_v\mathrm{d}T + p\left(\frac{R}{p}\mathrm{d}T - \frac{R T}{p^2}\mathrm{d}p\right)
= (c_v + R)\mathrm{d}T - \frac{R T}{p}\mathrm{d}p.
$$

Usando la relación de Mayer $c_p = c_v + R$, esto se convierte en:

$$
\delta q = c_p\mathrm{d}T - \frac{R T}{p}\mathrm{d}p.
$$

En un **proceso politrópico**, presión y volumen se relacionan por:

$$
p v^n = \text{constante}.
$$

Diferenciando logarítmicamente:

$$
\frac{\mathrm{d}p}{p} = -n\frac{\mathrm{d}v}{v}.
$$

Como $v = R T / p$, también podemos relacionar $\mathrm{d}p/p$ con $\mathrm{d}T/T$:

$$
\frac{\mathrm{d}p}{p} = \frac{n}{n - 1}\frac{\mathrm{d}T}{T}.
$$

Reemplazando $\mathrm{d}p$ en la expresión anterior para $\delta q$:

$$
\delta q = c_p\mathrm{d}T - \frac{R T}{p}\left(\frac{p n}{(n - 1)T}\mathrm{d}T\right)
= \left[c_p - \frac{n R}{n - 1}\right]\mathrm{d}T.
$$

Por tanto, para un proceso politrópico, el calor intercambiado por unidad de cambio de temperatura es:

$$
\delta q = c\mathrm{d}T, \quad \text{con} \quad c = c_p - \frac{n R}{n - 1}.
$$

Sustituyendo $R = c_p - c_v$ finalmente se obtiene:

$$
c = \frac{n c_v - c_p}{n - 1},
$$

y reordenando:

$$
n = \frac{c_p - c}{c_v - c}.
$$

Esta expresión indica **cuán “politrópico” es el proceso**, es decir, cuánto del cambio de energía interna proviene del intercambio de calor frente al trabajo:

* $c$ representa el **calor específico efectivo** — la cantidad de calor por unidad de cambio de temperatura para el proceso real.
* $c_p$ y $c_v$ son los dos **valores límite**:

  * $c_p$ corresponde al caso en que la presión permanece constante, donde una parte del calor suministrado se destina a realizar trabajo, y la parte restante se emplea en incrementar la energía interna.
  * $c_v$ corresponde a ausencia de trabajo de expansión (volumen constante), donde todo el calor se destina a aumentar la energía interna.

Entre esos extremos, el proceso se comporta *parcialmente como ambos*, dependiendo de cuánto de la energía suministrada (o extraída) se destina al trabajo de expansión/compresión.

El exponente $n$ actúa así como un **selector termodinámico** entre estos límites:

* Cuando $c = c_p$ → $n = 0$: presión constante.
* Cuando $c = c_v$ → $n \to \infty$: volumen constante.
* Cuando $c = 0$ → $n = \gamma$: adiabático (sin intercambio de calor).
* Cuando $c$ tiende a infinito → $n = 1$: isotérmico (el calor compensa totalmente el trabajo realizado).
:::

---

(subsec_conceptual_closure_specific_heats)=
### Cierre conceptual

* Los **calores específicos**, $c_v$ y $c_p$, vinculan los cambios medibles de temperatura con las variaciones subyacentes en **energía interna** y **entalpía**.
* Sus definiciones surgen de **procesos realizables experimentalmente** —volumen constante y presión constante— que aíslan un mecanismo de transferencia de energía a la vez.
* Como $u$ y $h$ son **propiedades de estado**, las cantidades $c_v$ y $c_p$ son **propiedades termodinámicas bien definidas**, aunque el **calor** intercambiado ($\delta q$) siga siendo una variable de proceso **dependiente de la trayectoria**.
* La dependencia de $c_v$ y $c_p$ con la **temperatura** (y, para gases reales, con la **presión o el volumen**) conecta la termodinámica macroscópica con la estructura microscópica de la materia.
* Para **gases ideales**, donde $u$ y $h$ dependen solo de la temperatura, la **relación de Mayer** $(c_p - c_v = R)$ y la **relación de calores específicos** ($\gamma = c_p / c_v$) proporcionan vínculos compactos entre estas propiedades y el comportamiento molecular.
* Aumentar la complejidad molecular amplía el número de modos de almacenamiento de energía, reduciendo $\gamma$ y haciendo que el gas sea más “adaptable térmicamente”.

En conjunto, estas ideas forman el puente entre los **efectos térmicos medibles** y las **propiedades termodinámicas intrínsecas**, estableciendo la base para análisis posteriores de **transformaciones energéticas** y **procesos de flujo**.

