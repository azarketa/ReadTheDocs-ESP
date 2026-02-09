(sec_models_gases)=
## Gases ideales y reales

Modelar gases es uno de los aspectos clave de la Termodinámica. Los gases difieren por su composición y estructura molecular — aire, monóxido de carbono, hidrógeno, metano, butano o vapor de etanol se comportan de manera distinta.
Sin embargo, bajo condiciones adecuadas, todos los gases muestran patrones comparables que pueden capturarse mediante modelos matemáticos.

Esta sección desarrolla primero el **modelo de gas ideal**, válido a bajas presiones y altas temperaturas, y luego introduce **modelos de gases reales** que amplían la precisión predictiva en condiciones densas o frías. Un ejemplo cuantitativo ilustra sus diferencias. Las variables intensivas utilizadas aquí se conectan directamente con {ref}`la sección anterior <sec_characterization_substances>`, y las formas finales satisfacen {ref}`the general state relation <eq_general_state_equation>`.

---

(subsec_ideal_gas_assumptions)=
### Supuestos del modelo de gas ideal

El **modelo de gas ideal** se basa en dos postulados simplificadores:

1. **Volumen molecular despreciable:** las moléculas ocupan una porción insignificante del volumen total. Esta aproximación es válida a **bajas presiones**.

2. **Fuerzas intermoleculares despreciables:** se ignoran las atracciones y repulsiones intermoleculares. Esto es razonable a **altas temperaturas**, donde domina la energía cinética.

:::{important}
**VALIDEZ DE LA APROXIMACIÓN DE GAS IDEAL**

El modelo de gas ideal describe gases en el límite de baja densidad y alta temperatura, donde las interacciones moleculares *desaparecen*.
En este régimen, todos los gases se comportan de manera similar, independientemente de su naturaleza química.
:::

---



(subsec_ideal_gas_equation)=
### La ecuación del gas ideal

La relación entre presión, volumen, temperatura y cantidad de sustancia se expresa mediante la **ley del gas ideal**.

(eq_ideal_gas_molar_form)=
$$
p{}V = n{}\text{R}_{\text{u}}{}T
$$

donde:

* $p$ es la presión absoluta ($\text{Pa}$),
* $V$ es el volumen ($\text{m}^3$),
* $n$ es la cantidad de sustancia ($\text{mol}$),
* $T$ es la temperatura absoluta ($\text{K}$), y
* $\text{R}_{\text{u}} = 8{,}314 \ [\text{J}/(\text{mol}\cdot\text{K})]$ es la constante universal de los gases.

La **constante específica del gas** $R$ se define como:

(eq_specific_gas_constant)=
$$
R = \frac{\text{R}_{\text{u}}}{\text{M}}
$$

donde $\text{M}$ es la masa molar ($\text{kg}/\text{mol}$). Como $\text{M} = m/n$, se obtiene la **forma en masa**:

(eq_ideal_gas_mass_form)=
$$
p{}V = m{}R{}T
$$

Dividiendo por la masa $m$ se obtiene la **forma específica**:

(eq_ideal_gas_specific_form)=
$$
p{}v = R{}T
$$

donde $v = V/m$ es el volumen específico ($\text{m}^3/\text{kg}$).

:::{note}
**RELACIÓN CON EL POSTULADO DEL ESTADO**

La relación $p{}v = R{}T$ conecta las tres variables intensivas introducidas en {ref}`la sección anterior <sec_characterization_substances>` y constituye una realización particular de {ref}`la relación general de estado <eq_general_state_equation>`.
:::

---



(subsec_real_gases)=
### Gases reales y desviaciones del comportamiento ideal

Cuando los gases se comprimen o se enfrían, su comportamiento se aparta del predicho por la ley del gas ideal. Estas desviaciones ocurren porque las moléculas reales **ocupan un espacio finito** y **ejercen fuerzas** entre sí — efectos que el modelo ideal desprecia. Para cuantificar estas diferencias, introducimos el **factor de compresibilidad**:

(eq_compressibility_factor)=
$$
Z = \frac{p{}v}{R{}T}
$$

Para un gas ideal, $Z = 1$. Si $Z < 1$, dominan las interacciones atractivas; si $Z > 1$, prevalecen los efectos repulsivos. El factor de compresibilidad proporciona así una medida compacta y adimensional de la desviación respecto al comportamiento ideal.

:::{note}
**SIGNIFICADO DE $Z$**

El factor de compresibilidad $Z$ cuantifica cuánto se desvía un gas real de la ley ideal bajo una combinación dada de $p$ y $T$.
Al representar $Z$ frente a $p$ para varios gases a distintas temperaturas se observa una tendencia común:
todos se aproximan a $Z = 1$ a baja presión, mostrando que el comportamiento de gas ideal es el caso límite de los gases reales.
:::

---

(subsec_reduced_variables)=
### Propiedades críticas y variables reducidas

Los estudios experimentales muestran que toda sustancia presenta un **punto crítico** más allá del cual desaparece la distinción entre líquido y vapor. Este punto se define por tres magnitudes características: la **presión crítica** $p_c$, la **temperatura crítica** $T_c$ y el **volumen específico crítico** $v_c$.

Estos valores son medibles experimentalmente y proporcionan un marco de referencia natural para comparar sustancias.
Aunque el significado detallado de “punto crítico” se abordará más adelante,
ya podemos definir las **variables reducidas**:

(eq_reduced_variables)=
$$
T_r = \frac{T}{T_c}, \qquad p_r = \frac{p}{p_c}, \qquad v_r = \frac{v}{v_c}
$$

Expresar las relaciones termodinámicas en términos de $(T_r, p_r, v_r)$ hace que el comportamiento de diferentes gases sea **comparable en una base universal**, lo que constituye la esencia de la **ley de los estados correspondientes**.

:::{tip}
**LEY DE LOS ESTADOS CORRESPONDIENTES**

Cuando los datos de varios gases se representan en función de las variables reducidas $(T_r, p_r, v_r)$, sus curvas de compresibilidad se superponen sobre la misma superficie. Esta observación empírica implica que el comportamiento termodinámico de los gases está gobernado fundamentalmente por relaciones adimensionales, no por sus propiedades absolutas.
:::

---



(subsec_cubic_models)=
### Modelos clásicos y modernos de gases reales

Aunque $Z$ es un excelente descriptor del comportamiento de los gases reales, aún necesitamos **ecuaciones explícitas** que vinculen $p$, $v$ y $T$ para calcular estados y procesos.
Con este fin, se han desarrollado varias **ecuaciones de estado semiempríricas**. Estas ecuaciones modifican la ley del gas ideal incluyendo términos correctivos para el **volumen molecular finito** y las **fuerzas intermoleculares**.

:::{note}
**POR QUÉ APARECEN LAS ECUACIONES CÚBICAS**

Cuando la ley del gas ideal se corrige con un término proporcional a $1/v^2$ (para modelar atracciones) y otro que resta un volumen finito $b$ (para modelar repulsiones),
la expresión resultante se vuelve **cúbica en el volumen específico** $v$. Por eso la mayoría de las ecuaciones de estado clásicas — van der Waals, Redlich–Kwong, Peng–Robinson —
pertenecen a la familia de **ecuaciones cúbicas**. Son las formas algebraicas más simples capaces de reproducir las curvas $p$–$v$ con forma de S observadas experimentalmente
cerca de las transiciones de fase, manteniendo la posibilidad de resolverse en forma cerrada.
:::

* **Ecuación de van der Waals**

  La primera ecuación que introduce ambos tipos de correcciones moleculares:

  (eq_vanderwaals)=
  $$
  \bigl(p + a{}\tfrac{n^{2}}{V^{2}}\bigr)\bigl(V - n{}b\bigr) = n{}\text{R}_{\text{u}}{}T
  $$

  donde:

  * $a$ corrige las *atracciones intermoleculares*,
  * $b$ corrige el *tamaño molecular finito*.

  Cuando $a = b = 0$, se recupera la ley del gas ideal.

* **Ecuación de Redlich–Kwong**

  Una mejora que introduce un término de atracción dependiente de la temperatura:

  (eq_redlich_kwong)=
  $$
  p = \frac{\text{R}_{\text{u}}{}T}{V_m - b} - \frac{a}{T^{1/2}{}V_m{}(V_m + b)}
  $$

  Este modelo funciona bien para presiones moderadas y altas temperaturas,
  y sigue siendo algebraicamente simple.

* **Ecuación de Peng–Robinson**

  Desarrollada para mejorar la precisión cerca de las regiones crítica y líquida:

  (eq_peng_robinson)=
  $$
  p = \frac{\text{R}_{\text{u}}{}T}{V_m - b} - \frac{a\alpha(T)}{V_m(V_m + b) + b(V_m - b)}
  $$

  con:
  * $\alpha(T) = [1 + \kappa(1 - \sqrt{T/T_c})]^2$,
  * $\kappa = 0{,}37464 + 1{,}54226\omega - 0{,}26992\omega^2$,
  * y $\omega$ el **factor acéntrico** del gas (medida de la no esfericidad o acentricidad de las moléculas).

  El modelo Peng–Robinson es particularmente eficaz para calcular equilibrios vapor–líquido
  y se utiliza ampliamente en la termodinámica aplicada.

:::{note}
**PRECISIÓN COMPARATIVA**

* **Van der Waals** — cualitativa pero demasiado simplificada.
* **Redlich–Kwong** — mejora el comportamiento con la temperatura, precisión moderada.
* **Peng–Robinson** — alta precisión en regiones vapor–líquido y cerca del punto crítico.

Cada una de estas ecuaciones puede expresarse posteriormente en términos del factor de compresibilidad $Z$
para comparaciones cruzadas y conexión con expansiones teóricas.
:::

---



(subsec_virial_equation)=
### La ecuación de estado virial

Aunque los modelos cúbicos ofrecen correlaciones prácticas para ingeniería, un enfoque teórico más fundamental surge de la **mecánica estadística**, donde la presión de un gas se expande en potencias de la densidad. Esto conduce a la **ecuación de estado virial**, expresada en términos del factor de compresibilidad:

(eq_virial_expansion)=
$$
Z = 1 + \frac{B(T)}{v} + \frac{C(T)}{v^{2}} + \frac{D(T)}{v^{3}} + \cdots
$$

Los coeficientes $B(T)$, $C(T)$ y $D(T)$ se conocen como **coeficientes viriales**,
cada uno correspondiente a interacciones moleculares de complejidad creciente:

* $B(T)$ — interacciones de pares,
* $C(T)$ — interacciones de tres cuerpos,
* $D(T)$ — efectos de cuatro cuerpos y superiores.

A grandes valores de $v$ (baja densidad), los términos de orden superior desaparecen y se recupera la ley del gas ideal. A densidades moderadas, bastan los primeros términos para capturar las desviaciones de los gases reales.

:::{note}
**CONEXIÓN CON LAS ECUACIONES CÚBICAS**

Expandir cualquier ecuación de estado cúbica — van der Waals, Redlich–Kwong o Peng–Robinson — para presiones pequeñas ($p_r \ll 1$) o volúmenes específicos grandes produce una **serie tipo virial**. En ese límite, las constantes $a$ y $b$ de esos modelos cúbicos pueden expresarse en términos de los coeficientes viriales $B(T)$ y $C(T)$. Por tanto, la ecuación de estado virial representa el **límite universal a baja presión** de todos los modelos de gases reales.

En la práctica ingenieril, la serie suele truncarse tras el primer término correctivo:

(eq_virial_first_order)=
$$
Z \approx 1 + \frac{B(T)}{v}
$$

Sustituyendo en la ley del gas ideal se obtiene:

(eq_virial_pressure_correction)=
$$
p \approx \frac{R{}T}{v}\left(1 + \frac{B(T)}{v}\right)
$$

Esta **aproximación virial de primer orden** proporciona una corrección conveniente para efectos de gas real a presiones moderadas, manteniendo la simplicidad computacional.

La expansión virial truncada es precisa a **presiones bajas o moderadas**, donde las interacciones intermoleculares se limitan a efectos de corto alcance.

A presiones altas o cerca del punto crítico, las ecuaciones cúbicas como Peng–Robinson ofrecen mejor precisión y consistencia termodinámica.
:::

:::{note}
**SIGNIFICADO Y ORIGEN DE LA PALABRA *VIRIAL***

La palabra **“virial”** proviene del término latino *vis*, que significa *fuerza* o *energía*. Fue introducida por el físico alemán **Rudolf Clausius** en 1870 en el contexto de sus estudios sobre la teoría mecánica del calor. Clausius utilizó la expresión *“virialis”* para denotar la *energía asociada a las fuerzas moleculares*, y a partir de ella formuló lo que hoy se conoce como el **Teorema de Virial**.

En esencia, el teorema de Virial relaciona la **energía cinética promedio** de las moléculas en un sistema con la **energía potencial promedio** derivada de sus interacciones mutuas. A partir de esta relación mecánica, Clausius estableció un vínculo entre las fuerzas microscópicas y la presión macroscópica — conexión que dio origen a la **ecuación virial**, que expresa la presión de un gas como una serie en potencias de la densidad.

Así, el término *virial* se refiere al “contenido de energía-fuerza” (*vis*) de un sistema, no a la varianza ni a la expansión de series. Cada coeficiente en la ecuación de virial representa el efecto acumulado de las fuerzas moleculares: interacciones de dos cuerpos, tres cuerpos y superiores. El nombre enfatiza el origen mecánico de la ecuación — es, fundamentalmente, una expresión de estado derivada de las fuerzas.
:::

---



::::{important}
**EJEMPLO RESUELTO — PRESIÓN Y FACTOR DE COMPRESIBILIDAD DEL $\text{CO}_2$ A $300 \ \text{K}$**

**Enunciado del problema**

Determinar la **presión** y el **factor de compresibilidad** $Z$ para el **dióxido de carbono** bajo condiciones termodinámicas especificadas, utilizando tanto **modelos ideales** como **modelos de gas real**. El gas ocupa un **volumen molar** de $V_m = 0{,}01 \ \text{m}^3/\text{mol}$ y se mantiene a una **temperatura** de $T = 300 \ \text{K}$. Esto corresponde a una condición cercana al punto crítico del $\text{CO}_2$, lo que lo convierte en un caso significativo para evaluar la fidelidad de los modelos.

Los modelos considerados son:

1. Gas ideal  
2. Van der Waals  
3. Redlich–Kwong  
4. Peng–Robinson  
5. Virial (aproximación de primer orden)  
6. Virial (aproximación de segundo orden)  

**Síntesis**

Se aplican diferentes modelos de gas para calcular la presión de un mol de $\text{CO}_{2}$ que ocupa un volumen de $0{,}01 \ \text{m}^{3}$ a una temperatura de $T = 300 \ \text{K}$.

---

**Datos del problema**{cite}`weast1972handbook, mit_virial`

| Magnitud                | Símbolo | Valor |
| :---------------------- | :------: | :---: |
| Temperatura             | $T$ | $300 \ \text{K}$ |
| Volumen molar           | $V_m$ | $0{,}01 \ \text{m}^3/\text{mol}$ |
| Constante universal de los gases | $\text{R}_{\text{u}}$ | $8{,}314 \ \text{J}/(\text{mol}\cdot\text{K})$ |
| $a$ (vdW–RK–PR)         | $a$ | $0{,}364 \ \text{Pa}{\cdot}\text{m}^6/\text{mol}^2$ |
| $b$ (vdW–RK–PR)         | $b$ | $4{,}27\times10^{-5} \ \text{m}^3/\text{mol}$ |
| Temperatura crítica     | $T_c$ | $304{,}2 \ \text{K}$ |
| Presión crítica         | $p_c$ | $7{,}38\times10^6 \ \text{Pa}$ |
| Factor acéntrico        | $\omega$ | $0{,}225$ |
| **2º coeficiente de Virial** (a $300 \ \text{K}$) | $B$ | $-121{,}5\times10^{-6} \ \text{m}^3/\text{mol}$ |
| **3º coeficiente de Virial** (a $300 \ \text{K}$) | $C$ | $5{,}2\times10^{-9} \ \text{m}^6/\text{mol}^2$ |

---

1. **Cálculo de propiedades reducidas**

(eq_example_reduced_props)=
$$
T_r = \frac{T}{T_c} = 0{,}986,
\qquad
p_r = \frac{p}{p_c}.
$$

Como $p$ debe determinarse, $p_r$ se evaluará por separado para cada modelo.

---

2. **Predicciones de los modelos**

* **Modelo de gas ideal**

$$
\boxed{p = \frac{\text{R}_{\text{u}}{}T}{V_m} = 2{,}49\times10^{5} \ \text{Pa}} \ ,
$$

$$
\boxed{Z = \frac{p{}V_m}{\text{R}_{\text{u}}{}T} = 1{,}000} \ .
$$

---

* **Ecuación de van der Waals**

$$
\boxed{p = \frac{\text{R}_{\text{u}}{}T}{V_m - b} - a{}\frac{1}{V_m^2}
= 2{,}13\times10^{5} \ \text{Pa}} \ ,
$$

$$
\boxed{Z = \frac{p{}V_m}{\text{R}_{\text{u}}{}T} = 0{,}857} \ .
$$

---

* **Ecuación de Redlich–Kwong**

$$
\boxed{p = \frac{\text{R}_{\text{u}}{}T}{V_m - b} - \frac{a}{T^{1/2}{}V_m(V_m + b)} = 2{,}20\times10^{5} \ \text{Pa}} \ ,
$$

$$
\boxed{Z = 0{,}885} \ .
$$

---

* **Ecuación de Peng–Robinson**

$$
p =
\frac{\text{R}_{\text{u}}{}T}{V_m - b} - \frac{a\alpha(T)}{V_m(V_m + b) + b(V_m - b)},
$$

donde:

$$
\alpha(T) = [1 + \kappa(1 - \sqrt{T/T_c})]^2,
\qquad
\kappa = 0{,}37464 + 1{,}54226\omega - 0{,}26992\omega^2.
$$

Numéricamente:

$$
\boxed{p = 2{,}25\times10^{5} \ \text{Pa}} \ ,
$$

$$
\boxed{Z = 0{,}905} \ .
$$

---

* **Ecuación de Virial (aproximación de primer orden)**

$$
\boxed{p = \frac{\text{R}_{\text{u}}{}T}{V_m}{}\left(1 + \frac{B}{V_m}\right) = 2{,}47\times10^{5}{} \ \text{Pa}} \ ,
$$

$$
\boxed{Z = 1 + \frac{B}{V_m} = 0{,}994} \ .
$$

---

* **Ecuación de Virial (aproximación de segundo orden)**

$$
\frac{C}{V_m^{2}} = \frac{5{,}2\times10^{-9}}{(0{,}01)^2} = 5{,}2\times10^{-5},
$$

$$
\boxed{Z = 1 - 0{,}01215 + 5{,}2\times10^{-5} = 0{,}98790} \ ,
$$

$$
\boxed{p = \frac{\text{R}_{\text{u}}{}T}{V_m}{}Z \approx 2{,}4642\times10^{5}{}\text{Pa}} \ .
$$

---

3. **Evaluación de presión reducida**

(eq_example_reduced_pressure)=
$$
p_r = \frac{p}{p_c}.
$$

| Modelo           | $p$ [$\text{Pa}$] | $Z$ | $p_r$ | $\Delta{}p$ [%] vs Peng–Robinson |
| :-------------- | :----------------: | :---: | :----: | :----------: |
| Gas ideal       | $2{,}49{\times}10^5$ | $1{,}000$ | $0{,}0337$ | $+10{,}7$ |
| van der Waals   | $2{,}13{\times}10^5$ | $0{,}857$ | $0{,}0288$ | $−5{,}3$ |
| Redlich–Kwong   | $2{,}20{\times}10^5$ | $0{,}885$ | $0{,}0298$ | $−2{,}2$ |
| Peng–Robinson   | $2{,}25{\times}10^5$ | $0{,}905$ | $0{,}0305$ | $0{,}0$ |
| Virial (1 término) | $2{,}47{\times}10^5$ | $0{,}994$ | $0{,}0335$ | $+9{,}8$ |
| Virial (2 términos) | $2{,}4642{\times}10^5$ | $0{,}988$ | $0{,}0334$ | $+9{,}5$ |

---

:::{tip}
**INTERPRETACIÓN**

A $T_r \approx 0{,}99$, el $\text{CO}_2$ se encuentra cerca de su región crítica.

* El **modelo de gas ideal** sobreestima la presión en ~10 %, ya que ignora las atracciones moleculares.
* El **modelo de van der Waals** la subestima ligeramente, al sobrecorregir por cohesión.
* **Redlich–Kwong** y **Peng–Robinson** capturan repulsión y atracción con mayor precisión, siendo este último el más exacto.
* El **modelo virial** reproduce casi la predicción del gas ideal — señal clara de que es fiable principalmente a bajas presiones.
* La aproximación de un término reduce la presión ideal solo ligeramente ($Z{}\approx{}0{,}988$), aún **sobreestimando** ~$9{,}5$ % frente a **Peng–Robinson**. Añadir el **tercer término virial** cambia $Z$ solo en $5{,}2\times10^{-5}$, por lo que la aproximación de dos términos es prácticamente idéntica.
* La curvatura cerca del punto crítico en la superficie $p$–$v$–$T$ se captura mucho mejor con **ecuaciones de estado cúbicas** (Redlich–Kwong/Peng–Robinson) que con truncamientos viriales de bajo orden.
:::

::::

---

(subsec_conceptual_closure_gases)=
### Cierre conceptual

* La **ley del gas ideal** $(p{}v = R{}T)$, para *bajas* presiones y *altas* temperaturas, satisface {ref}`la relación general de estado <eq_general_state_equation>`.
* El comportamiento de **gases reales** requiere correcciones por tamaño finito e interacciones — mediante {ref}`van der Waals <eq_vanderwaals>`, {ref}`Redlich–Kwong <eq_redlich_kwong>`, {ref}`Virial <eq_virial_equation>` y {ref}`Peng–Robinson <eq_peng_robinson>`.
* Para condiciones amplias en ingeniería, **Peng–Robinson** ofrece el mejor equilibrio entre precisión y simplicidad; **Redlich–Kwong** es una alternativa más ligera.
* Las formas truncadas de **Virial** siguen siendo útiles para gases diluidos, pero no son las más precisas a densidades moderadas o cerca de límites de fase.

