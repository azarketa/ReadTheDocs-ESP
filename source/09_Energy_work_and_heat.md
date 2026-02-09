(sec_energy_work_heat)=
## Energía, trabajo y calor

Los sistemas termodinámicos no permanecen inmóviles; experimentan **procesos** que transforman o transfieren energía. Mientras que el análisis de equilibrio proporciona una instantánea del estado de un sistema, la **energía y sus modos de transferencia** describen cómo los sistemas evolucionan entre estados. Esta sección introduce las nociones fundamentales de **trabajo**, **calor** y **energía**: los pilares de la **$1^{\text{a}}$ ley de la termodinámica**, que establece que la energía no puede crearse ni destruirse, solo convertirse de una forma a otra.

---

(subsec_notion_of_energy)=
### Noción de energía

La termodinámica se construye en torno al concepto de **conservación de la energía**. La frase familiar — *«la energía no se crea ni se destruye, solo se transforma»* — captura la esencia de la $1^{\text{a}}$ ley, como se explica {ref}`más adelante <sec_first_law_closed_systems>`. Sin embargo, la energía no es un objeto tangible: es una **magnitud abstracta de contabilidad** que vincula diferentes formas de movimiento, interacción y transformación.

En cada proceso, la energía puede aparecer en diversas formas — mecánica, térmica, química, eléctrica — pero el **total** siempre permanece constante. Lo que cambia es su **distribución** entre esas formas.

La energía es una **propiedad de estado**. Una propiedad de estado es una magnitud cuyo valor está determinado por el estado termodinámico del sistema. En otras palabras: los estados termodinámicos se **describen** mediante propiedades de estado. Entre todas las magnitudes que pueden usarse en dicha descripción, la energía merece una consideración especial. Debido a su naturaleza conservativa, las variaciones de energía entre estados termodinámicos pueden relacionarse con las formas y procesos en que se producen dichas transferencias. Como veremos, la manera en que la termodinámica codifica los diferentes modos de transferencia de energía adopta su forma más simplificada en el enunciado de la $1^{\text{a}}$ ley.

:::{note}

**LA NOCIÓN ABSTRACTA DE LA $1^{\text{a}}$ LEY**

Aunque la $1^{\text{a}}$ ley se presentará en su forma matemática orientada a la aplicación en este curso, su concepción original es más abstracta. La conservación de la energía no es el enunciado formal de la $1^{\text{a}}$ ley; más bien, es **una de sus consecuencias**. En su concepción abstracta, la $1^{\text{a}}$ ley establece lo siguiente:
* Tomemos cualquier sistema termodinámico $S$.
* Dejémoslo evolucionar entre dos estados genéricos, $S_{1}$ y $S_{2}$.
* Siempre es posible definir una magnitud, llamada energía ($E$), tal que su diferencia $E_{2} - E_{1}$ no dependa de la forma en que se lleva a cabo la evolución entre los estados finales. En otras palabras: la variación de energía **es independiente de la trayectoria del proceso**.

Una magnitud física cuyos cambios entre estados dependen exclusivamente de los valores que adopta en dichos estados se denomina **propiedad física**. Así, el enunciado formal de la $1^{\text{a}}$ ley **establece la energía como una propiedad de estado**.
:::

---

(subsec_state_properties_process_magnitudes_and_reference_states)=
### Propiedades de estado, magnitudes de proceso y estados de referencia

El hecho de que la energía constituya una **propiedad de estado** significa que sus variaciones entre estados dependen solo de los valores que toma en esos estados, no de cómo se lleva a cabo el proceso. En cambio, una magnitud cuyo valor depende de la forma en que ocurre la transformación se denomina **magnitud de proceso**. Tales magnitudes cuantifican cómo un sistema intercambia energía con su entorno, en lugar de cuánta energía posee en un estado dado.

Las propiedades de estado y las magnitudes de proceso se refieren a cantidades físicas fundamentalmente diferentes. Por ello, es importante distinguirlas no solo conceptualmente, sino también de forma simbólica:

* Una **propiedad de estado** $\phi$:

  * Describe un **estado termodinámico** y tiene un valor bien definido en equilibrio.
  * Su cambio entre dos estados depende solo de esos estados y no de la trayectoria:

    * Para **cambios infinitesimales**, se utiliza el **operador diferencial**:

      * En el caso general, multivariable (si $\phi$ depende de un conjunto de parámetros $\left(x_1, x_2, \ldots\right)$):
        
        $$
        \mathrm{d}\phi =
        \left(\frac{\partial \phi}{\partial x_1}\right)\mathrm{d}x_1 +
        \left(\frac{\partial \phi}{\partial x_2}\right)\mathrm{d}x_2 + \cdots
        $$
        
      * Si $\phi = \phi(x)$, es decir, $\phi$ varía solo con un parámetro $x$, el diferencial se reduce a:
     
        $$
        \mathrm{d}\phi = \frac{\mathrm{d}\phi}{\mathrm{d}x}\mathrm{d}x.
        $$
     
        Integrando entre dos estados 1 y 2 se obtiene el cambio finito correspondiente:
     
        $$
        \Delta\phi_{1\to2} = \int_{x_1}^{x_2} \frac{\mathrm{d}\phi}{\mathrm{d}x}\mathrm{d}x = \phi_2 - \phi_1.
        $$
     
        Como $\phi$ es una **propiedad de estado**, $\mathrm{d}\phi$ es un **diferencial exacto**, y su integral depende solo de los extremos. Para dependencias unidimensionales, el **operador diferencial** expresa la tasa local de cambio de $\phi(x)$, mientras que la **integral** da la variación total entre estados.

* Una **magnitud de proceso** $\psi$:

  * Cuantifica cómo ocurre una transformación entre dos estados (el mecanismo por el cual el sistema cambia).
  * Su forma infinitesimal se representa mediante un **diferencial inexacto**, $\delta\psi$, porque su integral depende de la **trayectoria** seguida por el proceso:

    $$
    \Psi_{1\to2} = \int_{1}^{2} \delta\psi,
    $$
  
    donde el valor de $\Psi_{1\to2}$ cambia si cambia la trayectoria del proceso, incluso para los mismos estados inicial y final.

El propósito de introducir las notaciones para las diferencias de propiedades de estado y magnitudes de proceso es que la termodinámica no puede determinar **valores absolutos de energía**. La energía se define solo mediante **diferencias entre estados**, no por un cero absoluto que pueda medirse experimentalmente.

Para comparar y balancear energías (y otras propiedades) de manera coherente, se elige un **estado de referencia** — normalmente fijando $E=0$ en una condición definida. Esto simplifica los cálculos sin cambiar el significado físico; simplemente establece la escala numérica.

Los estados de referencia son **convencionales**, elegidos por **acuerdo** para simplificar los análisis. Por ejemplo:

* Fijar $h_f = 0$ para agua líquida saturada a $0 \ ^\circ\text{C}$ se adopta comúnmente como referencia de entalpía para el sistema agua–vapor.
* Asignar entalpías estándar de formación a $298 \ \text{K}$ y $1 \ \text{bar}$ es práctica habitual en termodinámica química.

Estas convenciones varían entre disciplinas, pero comparten el mismo objetivo: simplificar balances de energía y garantizar coherencia. No obstante, se pueden definir **estados de referencia personalizados** si un problema particular lo requiere, siempre que todas las magnitudes del análisis sean coherentes con la base elegida.


:::{important}

**RESUMEN DE PROPIEDADES DE ESTADO Y MAGNITUDES DE PROCESO**

La distinción entre **propiedades de estado** y **magnitudes de proceso** puede resumirse de forma compacta como sigue:

| **Tipo de magnitud** | **Símbolo(s)** | **Cambio infinitesimal** | **Cambio finito** | **Dependencia de la trayectoria** | **Tipo de diferencial** | **Significado físico**                                                                |
| :-------------------- | :--------: | :----------------------: | :---------------------------------------------------------------------------: | :-----------------: | :-------------------: | :---------------------------------------------------------------------------------- |
| **Propiedad de estado**    |   $\phi$   |     $\mathrm{d}\phi$     | $\Delta\phi_{1\to2} = \displaystyle\int_1^2 \mathrm{d}\phi = \phi_2 - \phi_1$ |   **Independiente**   |       **Exacto**       | Cuantifica el *estado* del sistema; depende solo de su condición de equilibrio.    |
| **Magnitud de proceso** |   $\psi$, $\Psi$   |       $\delta\psi$       |               $\Psi_{1\to2} = \displaystyle\int_1^2 \delta\psi$               |    **Dependiente**    |      **Inexacto**      | Cuantifica el *modo de cambio* entre estados; depende de la trayectoria de la transformación. |
:::

:::{note}

**LOS OPERADORES SIMPLIFICADOS**

Hasta ahora, los operadores de variación se han escrito con referencia explícita a sus extremos. Para un cambio de propiedad de estado, la expresión $\Delta\phi_{1\to2} = \phi_2 - \phi_1$ indica simplemente que estamos tomando la diferencia en la propiedad $\phi$ entre el estado 2 y el estado 1. Del mismo modo, el valor de una magnitud de proceso se ha escrito como $\Psi_{1\to2}$, haciendo explícitos los extremos del proceso.

En muchos problemas termodinámicos, sin embargo, los estados inicial y final son claros por el contexto, por lo que no es necesario especificarlos cada vez. En tales casos, los cambios finitos pueden escribirse más simplemente como $\Delta\phi$ o $\Psi$, con los extremos entendidos.
:::

---

(subsec_types_of_energy)=
### Tipos de energía

La **energía total** $E$ de un sistema se compone de varias contribuciones distintas:

(eq_energy_split)=
$$
E = U + E_k + E_p + E_f + \cdots
$$

donde:

* $U$ es la **energía interna**,
* $E_k$ es la **energía cinética**,
* $E_p$ es la **energía potencial**,
* y $E_f$ puede representar la **energía de flujo** o **energía de presión** en el análisis de volúmenes de control (sistemas abiertos).

En términos generales, distinguimos entre formas de energía **macroscópicas** (organizadas) y **microscópicas** (desorganizadas).

(subsubsec_macroscopic_energy)=
#### Energía macroscópica (organizada)

Las formas macroscópicas de energía dependen del movimiento global del sistema o de su posición relativa a un marco de referencia externo.

* **Energía cinética** debida a la velocidad del centro de masa ($c$):

(eq_Ek)=
$$
E_k = \frac{1}{2}mc^2.
$$

* **Energía potencial** asociada a la posición en un campo gravitatorio:

(eq_Ep)=
$$
E_p = m g (z - z_0).
$$

* **Energía de flujo (o trabajo de flujo)**, que cuantifica la energía necesaria para empujar una masa de fluido a través de una frontera:

(eq_Ef)=
$$
E_f = p V,
$$
donde $p$ es la presión y $V$ es el volumen del elemento de fluido en movimiento.

(subsubsec_microscopic_energy)=
#### Energía microscópica (desorganizada)

La **energía microscópica** o **energía interna** $U$ refleja los movimientos caóticos e interacciones de las moléculas: su traslación, rotación, vibración y enlaces. A diferencia de las formas macroscópicas de energía, las microscópicas no dependen (no son relativas) a un marco de referencia externo.

Como veremos, los cambios en $U$ adoptan formas relativamente simples en sistemas sin reacciones químicas ni cambios de fase. En tales sistemas, las variaciones en $U$ son principalmente **térmicas** y se correlacionan directamente con la temperatura. En resumen: cuanto mayor es la temperatura, mayor es el contenido de energía interna.

Sin embargo, no toda la energía interna es térmica: las energías química, nuclear y elástica también pueden contribuir a las fuentes de energía microscópica.

:::{note}

**ENERGÍA ORGANIZADA VS. DESORGANIZADA**

La energía “organizada” (como el movimiento macroscópico o el trabajo mecánico) puede **convertirse completamente** en energía desorganizada (movimiento molecular aleatorio o energía térmica).  
Como veremos, la transformación inversa está **limitada** por la $2^{\text{a}}$ ley de la termodinámica.

Por ello, convertir trabajo mecánico en calor es fácil (p. ej., fricción), pero convertir todo el calor en trabajo (como en los motores) es imposible.
:::



(subsec_physical_definition_of_work)=
### Definición física de trabajo

En su nivel más fundamental, el **trabajo** se define como la **transferencia de energía** que ocurre cuando una fuerza actúa a lo largo de un desplazamiento. Para un elemento infinitesimal de movimiento:

(eq_work_def)=
$$
\delta W = \vec{F} \cdot \mathrm{d}\vec{r}.
$$

La cantidad $\delta W$ es un **escalar** obtenido del producto escalar de dos vectores: la fuerza $\vec{F}$ y el desplazamiento $\mathrm{d}\vec{r}$. Su valor depende no solo de los extremos, sino también de la **trayectoria** seguida entre ellos.

La unidad de trabajo es el joule ($\text{J}$), definido como:

(eq_joule_unit)=
$$
1 \ \mathrm{J} = 1 \ \mathrm{N\cdot m}.
$$

Es decir, un joule equivale al trabajo realizado por una fuerza de un newton actuando a lo largo de un desplazamiento de un metro.

Para apreciar la escala de la unidad básica de energía (el joule), calculemos lo siguiente: la masa que nos haría gastar $1 \ \text{J}$ de energía al levantarla $1 \ \text{m}$ contra la fuerza de gravedad. Como $\delta W = 1 \ \text{J}$, $\mathrm{d}\vec{r} = 1 \vec{k}$ (suponiendo que $\vec{k}$ es el vector unitario en la dirección vertical) y $\vec{F} = -m{\cdot}\vec{a} = -m{\cdot}\vec{g} = m{\cdot}|g|\vec{k}$ (el signo negativo proviene del hecho de que, al levantar la masa, actuamos **contra** la fuerza de gravedad, que va en la dirección vertical negativa):

$$
1 \ [\text{J}] = m \ [\text{kg}] \ {\cdot} \ |g| \ [\frac{\text{m}}{\text{s}^{2}}] \ {\cdot} \ 1 \ [\text{m}] \ \Longrightarrow |g| \approx 10 \ [\frac{\text{m}}{\text{s}^{2}}] \ \Longrightarrow m \approx \frac{1}{10} \ \text{kg} = 100 \ \text{g},
$$

por lo que el cuerpo en cuestión sería una masa de 100 gramos — una cantidad pequeña comparada con los estándares cotidianos.

Como un joule es bastante pequeño para la mayoría de los problemas de ingeniería, es común usar sus múltiplos, como **kilojulios (kJ)** o **megajulios (MJ)**. Por ejemplo, un litro de gasolina libera aproximadamente $34 \ \text{MJ}$ de energía al quemarse, mientras que un cuerpo humano típico en reposo disipa alrededor de $100 \ \text{J}$ por segundo en trabajo metabólico y calor.

---

(subsec_work_simple_compressible_systems)=
### Noción de trabajo en sistemas compresibles simples

En un **proceso cuasiestático (reversible)**, el sistema evoluciona a través de una serie ininterrumpida de **estados de equilibrio**. Esto significa que todas las propiedades intensivas (como presión y temperatura) permanecen bien definidas en cada instante. Como $p$ puede asignarse un valor definido en cada paso infinitesimal, el producto $p\mathrm{d}V$ es una cantidad significativa, lo que permite expresar el trabajo en **forma diferencial** como:

(eq_flow_work_diff)=
$$
\delta W = p\mathrm{d}V,
$$

o, en forma específica,

(eq_flow_work_diff_spec)=
$$
\delta w = p\mathrm{d}v.
$$

Una manera sencilla de interpretar la {ref}`expresión anterior <eq_flow_work_diff>` es imaginar el límite del sistema como una pared móvil de área $A$ sobre la cual actúa una fuerza $\vec{F}$. Si la pared se desplaza una cantidad infinitesimal $\mathrm{d}\vec{x}$, el **trabajo elemental** es el producto punto $\vec{F}{\cdot}\mathrm{d}\vec{x}$.  
Como la **presión** es {ref}`la fuerza por unidad de área <eq_pressure_def>`, $p = F/A$, el trabajo infinitesimal puede escribirse como:

$$
\delta W = \pm pA\mathrm{d}x,
$$

y, como $\pm{}A\mathrm{d}x = \pm\mathrm{d}V$, {ref}`se obtiene la ecuación genérica del trabajo <eq_flow_work_diff>`. La interpretación de los signos positivo y negativo, según la convención adoptada en este curso, se da {ref}`en una sección posterior <subsec_the_sign_convention_work_heat>`. Integrando la expresión anterior entre dos estados de equilibrio 1 y 2 se obtiene el **trabajo total, finito, adscrito al proceso**:

(eq_flow_work_int)=
$$
W_{1\to2} = \int_{1}^{2} p\mathrm{d}V.
$$

Gráficamente, esto representa el **área bajo la curva del proceso** en un diagrama $p–V$. La forma de $p(V)$ determina cómo se evalúa esta integral.



(subsec_typical_process_cases)=
### Casos típicos de procesos

* **Proceso isocórico** ($V = \text{constante}$):

  Como $\mathrm{d}V = 0$,

  $$
  W_{1\to2} = \int_{1}^{2} p\mathrm{d}V = 0.
  $$

  No se realiza trabajo de frontera — el proceso ocurre a volumen constante.

* **Proceso isobárico** ($p = \text{constante}$):

  La presión puede sacarse fuera de la integral:

  $$
  W_{1\to2} = p \int_{V_1}^{V_2} \mathrm{d}V = p(V_2 - V_1).
  $$

* **Proceso isotérmico de gas ideal** ($T = \text{constante}$, $p V = n R T$):

  Sustituyendo $p = nRT/V$,

  $$
  W_{1\to2} = nRT \int_{V_1}^{V_2} \frac{\mathrm{d}V}{V}
  = nRT \ln\left(\frac{V_2}{V_1}\right).
  $$

* **Proceso adiabático de gas ideal**:

  En un proceso adiabático, no cruza calor la frontera del sistema — toda la transferencia de energía ocurre como trabajo.  
  La presión y el volumen están relacionados por la expresión $p V^{\gamma} = \text{constante}$, donde $\gamma = c_p / c_v$ es la razón de calores específicos.  
  Sustituyendo $p = \text{C}/V^{\gamma}$,

  $$
  W_{1\to2} = \int_{V_1}^{V_2} \text{C} V^{-\gamma}\mathrm{d}V
  = \frac{\text{C}}{1 - \gamma}\left(V_2^{1 - \gamma} - V_1^{1 - \gamma}\right)
  = \frac{p_2 V_2 - p_1 V_1}{1 - \gamma}.
  $$

* **Proceso politrópico**:

    Una forma de generalizar los casos anteriores es mediante la **relación politrópica**, $p V^n = \text{constante}$.  
    Dicha relación describe una amplia clase de procesos donde la relación presión–volumen sigue una ley de potencia. El exponente $n$ indica cómo el gas intercambia energía durante la transformación:
    
    * Para **$n$ pequeño**, la presión disminuye lentamente con el volumen, lo que significa que se produce más trabajo (similar a una expansión isobárica o isotérmica).
    * Para **$n$ grande**, la presión cae rápidamente y se realiza menos trabajo (aproximándose al comportamiento isocórico).
    
    Así, $n$ controla la “trayectoria” en el plano $p$–$V$, unificando diferentes tipos de procesos (isotérmico, adiabático, etc.) en un único modelo general.

  Sustituyendo $p = \text{C}/V^n$,

  $$
  W_{1\to2} = \int_{V_1}^{V_2} \text{C}V^{-n}\mathrm{d}V
  = \frac{\text{C}}{1-n}\left(V_2^{1-n} - V_1^{1-n}\right)
  = \frac{p_2 V_2 - p_1 V_1}{1 - n}.
  $$

  {ref}`Como se mencionó anteriormente <subsec_work_simple_compressible_systems>`, el trabajo realizado por un sistema compresible simple puede representarse mediante el área bajo la curva $p-V$ que describe el proceso $p(V)$.  
  La relación general $pV^n = \text{constante}$ describe una familia particular de curvas posibles en el diagrama $p-V$ para sustancias que siguen el modelo de gas ideal.  
  De hecho, dicha familia es el conjunto de **curvas hiperbólicas**, donde la curvatura y la pendiente están determinadas por el **índice politrópico $n$**:
    
  * Cuando $n = 1$, la curva es una **hipérbola equilátera**, correspondiente a un proceso **isotérmico** para un gas ideal $(pV = \text{constante})$.
  * Cuando $n = \gamma$, la curva representa un proceso **adiabático**, más pronunciado que el isotérmico porque no hay intercambio de calor.
  * Otros valores de $n$ describen casos intermedios o límites (p. ej., $n = 0$ para isobárico, $n \to \infty$ para isocórico).
  
  Así, el **modelo politrópico** unifica todas las trayectorias termodinámicas comunes bajo una sola expresión matemática, con las transformaciones isotérmica y adiabática apareciendo como **hipérbolas particulares** de esta familia general.

Estos casos muestran que el trabajo realizado depende de **cómo** el sistema se mueve entre estados — es decir, de la **trayectoria** — y no solo de los estados en sí.

:::{important}

**EXPRESIONES DE TRABAJO PARA CASOS DE GAS IDEAL**

| **Proceso** | **Restricción / Condición** | **Expresión del trabajo** | **Interpretación** | **Índice politrópico** | Forma de la curva en el diagrama $p-V$ |
| :- | :- | :- | :- | :-: | :-: |
| **Isocórico** | $V = \text{const.}$ | $W_{1\to2} = 0$ | Sin cambio de volumen $\rightarrow$ no hay trabajo de frontera. | $n \to \infty$ | Línea vertical |
| **Isobárico** | $p = \text{const.}$ | $W_{1\to2} = p(V_2 - V_1)$ | Presión constante $\rightarrow$ trabajo igual a presión × cambio de volumen. | $n = 0$ | Línea horizontal |
| **Isotérmico (gas ideal)** | $T = \text{const.}$ | $W_{1\to2} = nRT\ln(V_2/V_1)$ | Temperatura fija $\rightarrow$ el trabajo proviene totalmente del intercambio de calor. | $n = 1$ | Hipérbola equilátera |
| **Adiabático (gas ideal)**  | $Q = 0$ | $W_{1\to2} = \dfrac{p_2V_2 - p_1V_1}{1 - \gamma}$, donde $\gamma = c_p/c_v$ | Sin transferencia de calor $\rightarrow$ el trabajo equivale al cambio en energía interna. | $n = \gamma$ | Hipérbola (más pronunciada que la equilátera) |
| **Politrópico** | $p V^n = \text{const.}$ $\text{ } n \neq 1$ | $W_{1\to2} = \dfrac{p_2V_2 - p_1V_1}{1 - n}$ | Proceso generalizado que describe muchas trayectorias posibles entre estados. |   $n = n$ | Hipérbola modulada por $n$ |

:::

:::{note} 

**ETIMOLOGÍA DE “POLITRÓPICO”**

La palabra **“politrópico”** proviene del griego *poly* (πολύ, “muchos”) y *tropos* (τρόπος, “modo” o “manera”). Significa literalmente “muchas maneras”, reflejando que un proceso politrópico puede ocurrir de **muchas formas posibles** según el exponente $n$, cada una representando un modo distinto de intercambio de energía entre presión y volumen.
:::



(subsec_heat)=
### Noción de calor

Mientras que el trabajo resulta de **movimiento organizado** o **fuerzas actuando a través de desplazamientos**, el **calor** resulta de **interacciones microscópicas aleatorias** impulsadas por diferencias de temperatura.

La transferencia de energía por calor siempre procede **de mayor a menor temperatura**. Para una transferencia diferencial:

(eq_heat_direction)=
$$
T_\text{caliente} > T_\text{frío} \quad \Longrightarrow \quad Q_{\text{caliente}\to\text{frío}} > 0.
$$

El calor, al igual que el trabajo, es **dependiente de la trayectoria** y se mide en julios. Se simboliza por $\delta Q$ para una transferencia infinitesimal y por $Q$ para un proceso finito. Es una forma de transferencia de energía o energía *en tránsito* a través de la frontera (igual que el trabajo), no la energía almacenada dentro del sistema. Una vez absorbido, contribuye a la **energía interna** $U$ de un sistema cerrado o, como veremos, a la **entalpía** $H$ del fluido en un sistema abierto.

---

(subsec_rates_specifics)=
### Tasas y formas específicas

Para uso práctico, los términos de transferencia de energía se expresan a menudo en base **específica** (por unidad de masa) o como **tasas** (por unidad de tiempo). Como se ha hecho hasta ahora, las cantidades específicas se simbolizarán con las versiones en minúscula de sus contrapartes extensivas:

$$
\delta w = \frac{\delta W}{m}, \quad
\delta q = \frac{\delta Q}{m}, \qquad \text{medido en } [\text{J}/\text{kg}]
$$

mientras que las tasas se simbolizan con variables punteadas:

$$
\dot{W} = \frac{\mathrm{d}W}{\mathrm{d}t}, \quad
\dot{Q} = \frac{\mathrm{d}Q}{\mathrm{d}t}, \qquad \text{medido en } [\text{J}/\text{s}]\equiv[\text{W}].
$$

Estas formas son esenciales para sistemas de flujo estable, procesos cíclicos y sistemas abiertos, donde la transferencia de energía por unidad de masa o por unidad de tiempo suele ser más informativa que las cantidades totales.

:::{note}

**WATT, LA UNIDAD BÁSICA DE POTENCIA**

Obsérvese que la unidad Watt $[\text{W}]$ corresponde a la **tasa de energía**, es decir, al flujo de energía por unidad de tiempo (por segundo).
:::

---

(subsec_the_sign_convention_work_heat)=
### Convención de signos para trabajo y calor

{ref}`Como se mencionó antes <subsec_work_simple_compressible_systems>`, la {ref}`expresión infinitesimal para el trabajo <eq_flow_work_diff>` es una **relación general** que puede tomar valores **positivos** o **negativos** dependiendo del **signo del cambio de volumen** (es decir, $\pm\mathrm{d}V$):

* Si $\mathrm{d}V > 0$, el sistema **se expande** y realiza **trabajo positivo** sobre el entorno — la energía sale del sistema como salida mecánica.
* Si $\mathrm{d}V < 0$, el sistema **se comprime**, y se realiza **trabajo negativo** *por* el entorno — equivalente a trabajo realizado *sobre* el sistema, lo que significa que entra energía mecánica.

En un diagrama $p$–$V$, esto corresponde al **área bajo la curva del proceso**:

* **Expansión** $(W > 0)$: trabajo realizado *por* el sistema $\rightarrow$ el sistema **pierde** energía.
* **Compresión** $(W < 0)$: trabajo realizado *sobre* el sistema $\rightarrow$ el sistema **gana** energía.

Del mismo modo, el calor también es una **magnitud de proceso** cuyo signo depende de la **dirección del flujo de energía**. Por convención, definimos:

* **Calor positivo** $(Q > 0)$: la energía entra al sistema como calor $\rightarrow$ el sistema **gana** energía.
* **Calor negativo** $(Q < 0)$: la energía sale del sistema como calor $\rightarrow$ el sistema **pierde** energía.

En esta convención, **$Q$ positivo** indica *calentamiento* (energía recibida por el sistema), mientras que **$Q$ negativo** indica *enfriamiento* (energía liberada al entorno).

:::{warning} Importante: resumen de la convención de signos
| **Tipo de interacción**   | **Significado físico**            | **Dirección del flujo de energía**  | **Convención de signo** |
| :--------------------- | :------------------------------ | :------------------------- | :-----------------: |
| **Trabajo (por el sistema)**   | Expansión o salida mecánica  | Del sistema → entorno |      $W > 0$      |
| **Trabajo (sobre el sistema)**   | Compresión o entrada mecánica | Del entorno → sistema |      $W < 0$      |
| **Calor (hacia el sistema)**   | Calentamiento                         | Del entorno → sistema |      $Q > 0$      |
| **Calor (desde el sistema)** | Enfriamiento                         | Del sistema → entorno |      $Q < 0$      |
:::

:::{note}

**COHERENCIA DE LAS CONVENCIONES DE SIGNO**

La convención $W > 0$ para trabajo realizado **por** el sistema y $Q > 0$ para calor **añadido al** sistema es estándar en **termodinámica de ingeniería**.  
En textos de **física**, sin embargo, a veces se usa el signo opuesto para el trabajo ($W > 0$) para trabajo realizado **sobre** el sistema.  
Confirma siempre la convención de signos utilizada antes de comparar ecuaciones o resultados de diferentes fuentes.
:::

(worked_example_boundary_work)=
::::{important}

**EJEMPLO RESUELTO — TRABAJO DE FRONTERA DEL $\text{N}_2$ EN DIFERENTES PROCESOS**

**Enunciado del problema**

Un sistema cerrado contiene **1 kg de gas nitrógeno ($\text{N}_2$)** inicialmente a una presión de $p_1 = 100 \ \text{kPa}$ y una temperatura de $T_1 = 300 \ \text{K}$.  
Siempre que el proceso considerado lo permita, el gas se expande **cuasiestáticamente** hasta que su **volumen final se duplica** ($V_2 = 2V_1$).

El proceso se analiza bajo diferentes condiciones — **isocórico**, **isobárico**, **isotérmico**, **adiabático** y **politrópico** — para determinar el **trabajo de frontera** realizado por el gas en cada caso. Para el caso más genérico, se asume un índice politrópico de $n = 1{,}2$.

Se supone comportamiento de gas ideal en todo momento y se comparan las magnitudes de trabajo resultantes.



**Síntesis**

El trabajo de frontera se define como:

$$
W_{1\to2} = \int_{V_1}^{V_2} p \mathrm{d}V.
$$

Para un gas ideal, $pV = mRT$, y la forma funcional de $p(V)$ depende del **tipo de proceso**.  
Aplicamos las relaciones apropiadas para cada proceso y evaluamos los valores correspondientes de $W_{1\to2}$.

---

**Datos del problema**{cite}`2015Cengel`

| Magnitud                             |       Símbolo       |                     Valor |
| :----------------------------------- | :------------------: | ------------------------: |
| Gas                                  |          —           |   Nitrógeno ($\text{N}_2$) |
| Constante del gas                   |         $R$          | $0{,}2968 \ \text{kJ}/\text{kg}{\cdot}\text{K}$ |
| Razón de calores específicos         | $\gamma = c_p/c_v$   |                     $1{,}4$ |
| Masa                                 |         $m$          |           $1 \ \text{kg}$ |
| Presión inicial                      |        $p_1$         |        $100 \ \text{kPa}$ |
| Temperatura inicial                  |        $T_1$         |          $300 \ \text{K}$ |
| Relación de volúmenes                |      $V_2/V_1$       |                       $2$ |
| Exponente politrópico                |         $n$          |                     $1{,}2$ |

---

**Cálculos**

Para el estado inicial:

$$
p_1 V_1 = mRT_1 = (1)(0{,}2968)(300) = 89{,}04 \ \text{kJ} = 89{,}04 \ \text{kPa}{\cdot}\text{m}^3.
$$

Por tanto:

$$
\boxed{V_1 = \dfrac{mRT_1}{p_1} = \dfrac{89{,}04}{100} = 0{,}8904 \ \text{m}^3} \ .
$$

---

1. **Proceso isocórico** ($V = \text{constante}$)

Sin cambio de volumen $\Rightarrow \mathrm{d}V = 0$:

$$
W_{1\to2} = W_{\text{isocórico}} = \int_{V_1}^{V_2} p\mathrm{d}V = 0.
$$

$$
\boxed{W_{\text{isocórico}} = 0 \ \text{kJ}}
$$

---

2. **Proceso isobárico** ($p = \text{constante}$)

$$
W_{1\to2} = W_{\text{isobárico}} = p(V_2 - V_1) = 100(0{,}8904) = 89{,}0 \ \text{kJ}.
$$

$$
\boxed{W_{\text{isobárico}} = 89{,}0 \ \text{kJ}}
$$

---

3. **Proceso isotérmico** ($T = \text{constante}$)

$$
W_{1\to2} = W_{\text{isotérmico}} = mRT \ln\left(\frac{V_2}{V_1}\right) = (1)(0{,}2968)(300)\ln(2) = 61{,}7 \ \text{kJ}.
$$

$$
\boxed{W_{\text{isotérmico}} = 61{,}7 \ \text{kJ}}
$$

---

4. **Proceso adiabático** ($Q = 0$, reversible)

$$
W_{1\to2} = W_{\text{adiabático}} = \frac{p_2V_2 - p_1V_1}{1 - \gamma}.
$$

De $pV^\gamma = \text{constante}$:

$$
\frac{T_2}{T_1} = \left(\frac{V_1}{V_2}\right)^{\gamma-1} = (0{,}5)^{0{,}4} = 0{,}758,
\quad T_2 = 0{,}758(300) = 227{,}4 \ \text{K}.
$$

Entonces:

$$
W_{\text{adiabático}} = \frac{mR(T_2 - T_1)}{1 - \gamma}
= \frac{(1)(0{,}2968)(227{,}4 - 300)}{1 - 1{,}4} = 53{,}9 \ \text{kJ}.
$$

$$
\boxed{W_{\text{adiabático}} = 53{,}9 \ \text{kJ}}
$$

---

5. **Proceso politrópico** ($pV^n = \text{constante}$, $n = 1{,}2$)

$$
W_{1\to2} = W_{\text{politrópico}} = \frac{p_2V_2 - p_1V_1}{1 - n}.
$$

De la relación politrópica:

$$
\frac{p_2}{p_1} = \left(\frac{V_1}{V_2}\right)^n = (0{,}5)^{1{,}2} = 0{,}435.
$$

Por tanto, $p_2 = 43{,}5 \ \text{kPa}$, y

$$
W_{\text{politrópico}} = \frac{(43{,}5)(2V_1) - (100)(V_1)}{1 - 1{,}2} = \frac{(87{,}0 - 100)V_1}{-0{,}2} = 65{,}0 \ \text{kJ}.
$$

$$
\boxed{W_{\text{politrópico}} = 65{,}0 \ \text{kJ}}
$$



**Resumen de resultados**

| Proceso                | Relación                   | $W$ [kJ] | Trabajo relativo                    | Comentarios                                           |
| :--------------------- | :------------------------- | -------: | :---------------------------------- | :---------------------------------------------------- |
| Isocórico              | $V = \text{const.}$        |      $0{,}0$ | —                                   | Sin movimiento de frontera → sin trabajo.            |
| Isobárico              | $p = \text{const.}$        |     $89{,}0$ | Mayor                                | Mayor área $p$–$V$; presión externa constante.       |
| Isotérmico             | $T = \text{const.}$        |     $61{,}7$ | Moderado                             | El calor compensa totalmente el trabajo para mantener $T$ constante. |
| Adiabático             | $Q = 0$                    |     $53{,}9$ | Menor (no nulo)                      | Trabajo realizado a expensas de la energía interna (enfriamiento). |
| Politrópico ($n = 1{,}2$) | $pV^{1{,}2} = \text{const.}$ |     $65{,}0$ | Entre isotérmico y adiabático         | Intercambio parcial de calor suaviza la caída de presión. |

---

**Visualización**

Para el sistema actual, los procesos anteriores se representan así en un diagrama $p$–$V$. Como se observa, los comentarios anteriores se correlacionan con las formas de las curvas. En particular, se hace evidente que los diferentes procesos se representan mediante una curva que adopta una forma específica en el diagrama:

* El proceso **isocórico** se representa como una **línea vertical**.
* El proceso **isobárico** se representa como una **línea horizontal**.
* El proceso **isotérmico** se convierte en una **hipérbola equilátera**.
* El proceso **adiabático** también es una hipérbola, pero con una **pendiente y curvatura más pronunciadas** que la isotérmica, debido a que $\gamma = 1{,}4 > 1$.
* El proceso **politrópico** se representa como una hipérbola cuya pendiente y curvatura están entre las de los procesos isotérmico y adiabático ($\gamma > n > 1$). Estos tres casos muestran que la inclinación y curvatura de las hipérbolas están moduladas por el índice politrópico $n$.

![PV_diagram](1_fundamentals_figs/PV_diagram_worked_example_mod.svg)

---

:::{tip}

**INTERPRETACIÓN**

Una interpretación detallada en términos de energía, trabajo y calor puede desarrollarse al introducir formalmente la $1^{\text{a}}$ ley. Sin embargo, se pueden dar algunas pistas preliminares. Para la misma relación de expansión ($V_2/V_1 = 2$), la **salida de trabajo** depende de cómo el sistema intercambia calor:

* En la expansión **isobárica**, la presión constante produce la mayor área bajo la curva $p$–$V$.
* En la expansión **isotérmica**, la presión cae como $1/V$, dando un trabajo moderado.
* En la expansión **politrópica**, un intercambio limitado de calor produce una trayectoria intermedia entre isotérmica y adiabática.
* En la expansión **adiabática**, no entra calor — el gas se enfría y la caída de presión es más pronunciada, produciendo el menor trabajo no nulo de todos los procesos particulares analizados en el ejemplo.
* En los procesos **isocóricos**, no hay movimiento de frontera y no se realiza trabajo.

Este ejemplo muestra cómo la **trayectoria del proceso** — no solo los estados extremos — dicta el trabajo mecánico en las transformaciones termodinámicas.
:::

::::

---

(subsec_conceptual_closure_energy_work_heat)=
### Cierre conceptual

La **energía** es una *propiedad de estado*: caracteriza la condición de un sistema y sus variaciones dependen solo de los estados inicial y final. El **trabajo** y el **calor**, en cambio, son *magnitudes de proceso*: describen **cómo** la energía cruza la frontera del sistema — ya sea como acción mecánica organizada (trabajo) o como transferencia molecular desordenada debida a una diferencia de temperatura (calor).

Por tanto, trabajo y calor son **complementarios**: ningún sistema puede intercambiar energía sin uno o ambos. Su dirección y magnitud dependen de la trayectoria del proceso, no únicamente de los estados.

Para relacionar estas transferencias de manera coherente, la termodinámica adopta **convenciones de signo** claras:

* $W > 0$ cuando el trabajo lo realiza **el sistema** (expansión), y $W < 0$ cuando se realiza **sobre** él (compresión).
* $Q > 0$ cuando el calor se **añade** al sistema (calentamiento), y $Q < 0$ cuando se **libera** (enfriamiento).

En el **diagrama $p$–$V$**, las áreas representan **trabajo**, mientras que en el **diagrama $T$–$s$**, representan **calor** para procesos reversibles. Ambas vistas se complementan: una expresa el intercambio de energía **mecánica**, la otra el intercambio **térmico**, ofreciendo una imagen completa de la transferencia de energía entre un sistema y su entorno.

