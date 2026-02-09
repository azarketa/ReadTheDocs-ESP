(sec_pvt_diagrams)=
## Diagramas $p-v-T$

Los estados termodinámicos de una sustancia pura pueden describirse mediante la **tríada de variables** $p$, $v$ y $T$. Estas magnitudes están vinculadas por la {ref}`relación de estado <eq_general_state_equation>`, que define la superficie termodinámica de la sustancia en un espacio tridimensional. Comprender cómo se comporta esta superficie es esencial para visualizar los **cambios de fase** y las **trayectorias de proceso** en sistemas reales.

Desde el punto de vista matemático, una función de una sola variable $y=f(x)$ se representa como una curva en el plano $x$–$y$. Si, en cambio, la función depende de dos variables independientes, $z=f(x, y)$, su representación gráfica es una **superficie** en el espacio tridimensional. De manera análoga, la relación $p-v-T$ define una superficie: cada punto sobre ella representa un estado de equilibrio de la sustancia.

Un **proceso cuasiestático** —una evolución lenta y reversible entre estados de equilibrio— traza una **curva continua** sobre esta superficie. La forma de la superficie y sus proyecciones sobre los planos coordenados proporcionan información sobre el comportamiento de las fases.

---

(subsec_tv_projection)=
### La proyección $T-v$

Analicemos un sistema simple y familiar: un **cilindro–pistón** lleno de agua líquida a presión atmosférica ($p \approx 101 \ \text{kPa}$) y a una temperatura inicial de $20 \ ^{\circ}\text{C}$. El sistema se calienta lentamente mediante una fuente térmica, como un pequeño quemador.

1. **Calentamiento del líquido:**

   A medida que se suministra calor, la temperatura del agua aumenta. El pistón permanece casi inmóvil, lo que indica que el **volumen específico** del líquido varía muy poco con la temperatura.

2. **Aproximación a la saturación:**

    Cuando la temperatura alcanza los $100 \ ^{\circ}\text{C}$ (a esta presión), el líquido se vuelve **saturado**. Cualquier aporte adicional de calor inicia un **cambio de fase**: la formación de vapor. El agua en este punto se denomina **líquido saturado**, mientras que el estado anterior (por debajo de $100 \ ^{\circ}\text{C}$) se llama **líquido subenfriado** o **comprimido**.

3. **Cambio de fase:**

   A medida que se forma vapor, el pistón comienza a desplazarse hacia arriba. La temperatura y la presión permanecen constantes durante el cambio, pero el **volumen específico** aumenta notablemente. Durante este proceso coexisten líquido y vapor: es la **mezcla saturada líquido–vapor**. Cada estado intermedio corresponde a una fracción determinada de masa vaporizada, cuantificada por la **calidad** $x$, que se definirá más adelante en esta sección.

4. **Vapor saturado:**

   Cuando la última gota de líquido se evapora, el sistema consiste únicamente en **vapor saturado**. Extraer calor de este estado invertiría el proceso, produciendo **condensación**.

5. **Vapor recalentado:**

   Si el calentamiento continúa más allá del estado de vapor saturado, la temperatura se eleva por encima de la temperatura de saturación. El vapor se expande, el pistón asciende aún más y el gas sigue aproximadamente {ref}`la ley de los gases ideales <eq_ideal_gas_specific_form>`. El fluido en esta región es el **vapor recalentado**.

:::{important}

**OBSERVACIONES CLAVE EN EL DIAGRAMA $T-v$**

* El **volumen específico** del agua líquida permanece casi constante hasta que comienza la ebullición.
* El **cambio de fase** aparece como una **línea horizontal** (constantes $T$ y $p$).
* La región de **vapor saturado** sigue un comportamiento similar al de un gas, donde $v$ aumenta notablemente con $T$.
:::

---


(subsec_completing_tv_projection)=
### Completando la proyección $T-v$

Repetir el experimento a diferentes presiones revela que:

* A **presiones más altas**, el **cambio de fase** ocurre a **temperaturas más elevadas**.
* La diferencia en volumen específico entre las fases líquida y vapor **disminuye** a medida que aumenta la presión.

Esto conduce a dos conclusiones importantes:

1. La **temperatura de saturación**, $T_{\text{sat}}$, **depende de la presión**.

   Presiones más altas corresponden a temperaturas de saturación más elevadas.

2. El **cambio de volumen** durante la vaporización se hace menor a altas $p$ y $T$, desapareciendo finalmente en un punto único conocido como **punto crítico**.

    En el **punto crítico**, los estados de líquido saturado y vapor saturado coinciden. Más allá de este punto, no existe una distinción clara entre líquido y gas: la sustancia se convierte en un **fluido supercrítico**.
    
    Para el agua:

    (eq_critical_magnitudes_water)=
    $$
    T_{\text{cr}} = 373,95 \ ^{\circ}\text{C}, \quad p_{\text{cr}} = 22,06\text{MPa}
    $$
    
    Los fluidos supercríticos presentan propiedades intermedias entre las de los gases y los líquidos y se emplean en aplicaciones especializadas como la extracción con disolventes y el secado supercrítico.

:::{note}

**OLLAS A PRESIÓN Y EBULLICIÓN EN ALTURA**

* En una **olla a presión**, la presión interna supera la presión atmosférica, lo que permite que el agua permanezca líquida por encima de $100 \ ^{\circ}\text{C}$ y, por tanto, cocinar los alimentos más rápido.
* Por otro lado, en la cima del **Monte Everest**, donde $p_{\text{atm}} \approx 34 \ \text{kPa}$, el agua hierve aproximadamente a $86 \ ^{\circ}\text{C}$.
* A unos $19{.}000 \ \text{m}$ (la **línea de Armstrong**), donde la presión atmosférica iguala la presión de vapor del agua a la temperatura corporal ($36 \ ^{\circ}\text{C}$), los líquidos del cuerpo humano comenzarían a hervir sin presurización.

:::

---

(subsec_simplified_tv_projection)=
### La proyección $T-v$ simplificada

Si trazamos todos los puntos de saturación tanto para el líquido como para el vapor y los conectamos, obtenemos la **línea de saturación**, que forma una **campana invertida**. El diagrama $T-v$ puede dividirse entonces en regiones distintas:

* **Dentro de la campana:** la **región bifásica** (mezcla líquido–vapor).
* **A la izquierda:** la región de **líquido subenfriado**.
* **A la derecha:** la región de **vapor recalentado**.
* **Por encima de la campana:** la **región supercrítica**.

Este diagrama $T-v$ simplificado es una piedra angular en la visualización termodinámica: un mapa compacto que muestra cómo la materia transita entre sus fases principales.

---

(subsec_pv_projection)=
### La proyección $p-v$

Para complementar la vista $T-v$, consideremos el mismo sistema cilindro–pistón, pero ahora **manteniendo la temperatura constante** mientras se varía la presión.

Aplicando o retirando pesos sobre el pistón, se modifica la presión externa, mientras el intercambio de calor con el baño térmico mantiene la temperatura fija.  
El **diagrama $p-v$** resultante muestra características similares a la proyección $T-v$:

* A medida que la presión disminuye a temperatura constante, el líquido comienza a vaporizarse cuando se alcanza $p_{\text{sat}}$.
* A presiones más altas, ocurre la condensación.
* Ambas transformaciones trazan una **línea horizontal de cambio de fase** en el diagrama $p-v$.

La envolvente en forma de campana vuelve a separar las regiones monofásicas de la mezcla bifásica.

:::{note}

**COMPARACIÓN ENTRE LOS DIAGRAMAS $T-v$ Y $p-v$**

* En la **región líquida**, el volumen específico varía muy poco con $T$ o $p$.
* En la **región de vapor**, $p$ es inversamente proporcional a $v$ (ley de Boyle–Mariotte).
* El cambio de fase aparece como una línea horizontal en ambas proyecciones.
:::

---


    
(subsec_extending_pv_projection)=
### Ampliando la proyección $p-v$

Cuando se extiende para incluir la fase sólida, el diagrama $p-v$ muestra características adicionales:

* **Sustancias que se contraen al solidificarse** (la mayoría de los materiales) presentan una línea de transición sólido–líquido vertical, ya que $v$ disminuye bruscamente al solidificarse.
* **Sustancias que se expanden al congelarse** (como el agua) exhiben una línea inclinada: la fase sólida tiene un volumen específico ligeramente mayor que el líquido.

A presiones aún más bajas, aparecen otras transiciones:

* El **punto triple**, donde sólido, líquido y vapor coexisten en equilibrio. Para el agua:

  (eq_triple_point_values_water)=
  $$
  T_{\text{tr}} = 0{,}01{\ ^\circ}\text{C}, \quad p_{\text{tr}} = 0{,}6117 \ \text{kPa}
  $$

* El **proceso de sublimación**, una transición directa de sólido a vapor (o viceversa) a presiones inferiores a $p_{\text{tr}}$.

---

(subsec_pt_projection)=
### La proyección $p-T$ (diagrama de fases)

El **diagrama $p-T$**, o **diagrama de fases**, presenta los límites de fase de manera más compacta. Muestra las tres líneas fundamentales:

* **Línea de sublimación** (equilibrio sólido–vapor),
* **Línea de fusión** (equilibrio sólido–líquido), y
* **Línea de vaporización** (equilibrio líquido–vapor).

Estas tres líneas convergen en el **punto triple**, que aparece como un único punto en esta proyección.

La pendiente de la **línea de fusión** revela si una sustancia **se expande** o **se contrae** al congelarse:

* Pendiente positiva: el volumen disminuye al solidificarse (la mayoría de las sustancias).
* Pendiente negativa: el volumen aumenta (agua).

:::{note}

**INTERPRETACIÓN DE LAS LÍNEAS DE PROCESO**

* Las **líneas verticales** corresponden a procesos isotérmicos (temperatura constante).
* Las **líneas horizontales** corresponden a procesos isobáricos (presión constante).
* Por ejemplo:

  * Línea I′: sublimación isotérmica,
  * Línea I″: fusión isotérmica,
  * Línea I‴: evaporación isotérmica,
  * Línea I: sublimación isobárica,
  * Línea II: fusión isobárica,
  * Línea III: evaporación isobárica.
:::

---

(subsec_evaporation_process)=
### El proceso de evaporación y la calidad del vapor

La evaporación desempeña un papel central en muchos sistemas de ingeniería —desde **calderas** y **intercambiadores de calor** hasta **centrales termoeléctricas**. Durante la evaporación, la mezcla líquido–vapor se modela a menudo como **homogénea**, lo que simplifica enormemente el análisis.

El grado de vaporización se cuantifica mediante la **calidad del vapor**, $x$, definida como:

(eq_quality_definition)=
$$
x = \frac{m_{\text{vapor}}}{m_{\text{líquido}} + m_{\text{vapor}}}
$$

Este parámetro intensivo varía desde $x=0$ (líquido saturado) hasta $x=1$ (vapor saturado). En la región bifásica, todas las demás propiedades pueden expresarse como promedios ponderados por masa de sus valores en líquido saturado y vapor saturado.



::::{important}

**EJEMPLO RESUELTO — LOCALIZACIÓN DE ESTADOS DEL AGUA EN EL DIAGRAMA $p–v–T$**

**Enunciado del problema**

Para cada estado termodinámico del **agua**, determina las propiedades solicitadas localizando el estado en la superficie $p–v–T$ mediante datos tabulados{cite}`2015Cengel`:

1. $p=150~\mathrm{bar}$, $T=693~\mathrm{K}$ ($=420\ ^\circ\mathrm{C}$). Hallar $v$.
2. $p=0{,}5~\mathrm{bar}$, $u=340{,}49~\text{kJ}/\text{kg}$. Hallar $v$ y $T$.
3. $p=6~\mathrm{bar}$, $x=0{,}65$. Hallar $v$ y $T$.
4. $p=25~\mathrm{bar}$, $v=0{,}095~\text{m}^{3}/\text{kg}$. Hallar $T$.

---

**Síntesis**

| Caso | Datos dados                                           | A determinar |
| :--- | :---------------------------------------------------- | :----------- |
| 1    | $p=150~\mathrm{bar}$, $T=420\ ^\circ\mathrm{C}$      | $v$          |
| 2    | $p=0{,}5~\mathrm{bar}$, $u=340{,}49~\text{kJ}/\text{kg}$ | $v$, $T$     |
| 3    | $p=6~\mathrm{bar}$, $x=0{,}65$                         | $v$, $T$     |
| 4    | $p=25~\mathrm{bar}$, $v=0{,}095~\text{m}^{3}/\text{kg}$| $T$          |

---

**Estrategia de solución**

1. **Comprobación del estado**: para un $p$ o $T$ dado, comparar con propiedades de saturación $(T_\text{sat}(p)$, $p_\text{sat}(T)$; $v_f,v_g$; $u_f,u_g$) para decidir la **región**: líquido subenfriado/comprimido, mezcla saturada o vapor recalentado.
2. **Mezcla**: si está saturada, $T=T_\text{sat}(p)$ y $v=v_f+x(v_g-v_f)$, $u=u_f+x(u_g-u_f)$.
3. **Recalentado / subenfriado**: interpolar en las tablas correspondientes:

   $$y(T)=y(T_1)+\dfrac{y_2-y_1}{T_2-T_1}(T-T_1)\quad\text{a presión fija}.$$

---

**Cálculos**

1. **$p=150~\mathrm{bar},\ T=420\ ^\circ\mathrm{C}$:**

   * **Comprobación del estado:**

        $T_\text{sat}(150~\mathrm{bar})\approx 349\ ^\circ\mathrm{C}<420\ ^\circ\mathrm{C}\Rightarrow \boxed{\text{vapor sobrecalentado}}$ .

   * **Interpolación:**

        * A $p=150~\mathrm{bar}$ entre:
  
            * $T_1 = 400\ ^\circ\mathrm{C}$ ,
            * $v_1 = 0{,}015671 \ \text{m}^{3}/\text{kg}$ ,
            * $T_2=450\ ^\circ\mathrm{C}$ ,
            * $v_2 = 0{,}01847 \ \text{m}^{3}/\text{kg}$.

        $$
        v(T)=v_1+\frac{v_2-v_1}{T_2-T_1}(T-T_1)
        \quad\Rightarrow\quad
        v=\boxed{0{,}01679~\text{m}^{3}/\text{kg}} \ (16{,}79~\text{dm}^{3}/\text{kg}).
        $$

2. **$p=0{,}5~\mathrm{bar},\ u=340{,}49~\text{kJ}/\text{kg}$:**

   * **Comprobación del estado:**

     $T_\text{sat}(0{,}5~\mathrm{bar})=81{,}32\ ^\circ\mathrm{C}$ y $u_f\simeq340{,}49~\text{kJ}/\text{kg}$.  
     Como $u\approx u_f \Rightarrow \boxed{\text{líquido saturado}}$.

   * **Evaluación:**

     $$T=\boxed{81{,}32\ ^\circ\mathrm{C}} \ ,\quad v=v_f(p=0{,}5~\mathrm{bar})=\boxed{0{,}00103~\text{m}^3/\text{kg}}\ (1{,}03~\text{dm}^{3}/\text{kg}).$$

3. **$p=6~\mathrm{bar},\ x=0{,}65$**

   * **Comprobación del estado:**

     Dada la calidad $x$, el estado está en la campana de saturación $\Rightarrow \boxed{\text{mezcla saturada}}$ :
  
    $$\text{mezcla saturada} \implies T=T_\text{sat}(6~\mathrm{bar})=\boxed{158{,}83\ ^\circ\mathrm{C}} \ .$$

   * **Relación de mezcla:**

     Usando $v=v_f+x(v_g-v_f)$ a $p=6~\mathrm{bar}$ con $v_f=0{,}001091$ y $v_g=0{,}3156\ \text{m}^{3}/\text{kg}$,
   
     $$
     v=0{,}001091+0{,}65(0{,}3156-0{,}001091) = \boxed{0{,}20553~\text{m}^{3}/\text{kg}}\ (205{,}53~\text{dm}^{3}/\text{kg}).
     $$

4. **$p=25~\mathrm{bar} \ v=0{,}095~\text{m}^{3}/\text{kg}$**

   * **Comprobación del estado:**

     A $25~\mathrm{bar}$, $v_g(p)\approx0{,}0795~\text{m}^{3}/\text{kg}$.  
     Como $v=0{,}095>v_g \Rightarrow \boxed{\text{vapor sobrecalentado}}$ .

   * **Interpolación (a presión fija $p=25~\mathrm{bar}$):**
  
        * Entre:
  
            * $T_1 = 250\ ^\circ\mathrm{C}$ ,
            * $v_1 = 0{,}08705 \ \text{m}^{3}/\text{kg}$ ,
            * $T_2=300\ ^\circ\mathrm{C}$ ,
            * $v_2 = 0{,}09894 \ \text{m}^{3}/\text{kg}$.     
  
        $$
        T=T_1+\frac{v-v_1}{v_2-v_1}(T_2-T_1) \Rightarrow T = \boxed{283{,}43\ ^\circ\mathrm{C}}.
        $$

---

**Resumen y conclusiones**

| Caso | Región de fase       | Resultados                                                                                           |
| :--: | :------------------- | :--------------------------------------------------------------------------------------------------- |
| 1    | Vapor recalentado    | $v = 0{,}01679~\text{m}^{3}/\text{kg}\ (16{,}79~\text{dm}^{3}/\text{kg})$                              |
| 2    | Líquido saturado     | $T = 81{,}32~^\circ\text{C},\quad v = 0{,}00103~\text{m}^{3}/\text{kg}\ (1{,}03~\text{dm}^{3}/\text{kg})$|
| 3    | Mezcla saturada      | $T = 158{,}83~^\circ\text{C},\quad v = 0{,}20553~\text{m}^{3}/\text{kg}\ (205{,}53~\text{dm}^{3}/\text{kg})$|
| 4    | Vapor recalentado    | $T = 283{,}43~^\circ\text{C}$                                                                        |

* Comparar los estados dados con las **propiedades de saturación** permite identificar la fase de inmediato.
* Los estados de mezcla (caso 3) están **dentro de la campana**; los estados subenfriados y recalentados (1, 2 y 4) están **fuera** de ella.
* La interpolación lineal en tablas proporciona valores intermedios precisos para $v$ y $T$.

---

:::{tip}
 
**LECTURA DE LA SUPERFICIE $p-v-T$**

* Fijar $p$ y $T$ (caso 1) selecciona un punto **isóbaro–isotermo**; comparar $T$ con $T_\text{sat}(p)$ indica si el estado está **dentro** (mezcla) o **fuera** (recalentado/subenfriado) de la campana.
* Fijar $p$ y $u$ (caso 2) cerca de $u_f$ sitúa el estado en la línea de **líquido saturado** a $T_\text{sat}(p)$, por lo que $v=v_f(p)$.
* Especificar $p$ y $x$ (caso 3) coloca el estado **en la campana** a $T_\text{sat}(p)$, con $v$ como combinación lineal de $v_f$ y $v_g$.
* Fijar $p$ y un $v$ grande (caso 4) indica típicamente **vapor recalentado**; interpolar en tablas de vapor recalentado para obtener $T$.  
  Estos patrones muestran cómo simples comprobaciones contra propiedades de saturación permiten navegar la superficie $p–v–T$ de forma rápida y precisa.
:::

::::

---

(subsec_error_tv_diagram)=
### Desviación respecto al comportamiento de gas ideal

En el **diagrama $T-v$**, la desviación del comportamiento real del vapor respecto a la ley de gas ideal aumenta al aproximarse al **punto crítico**. A bajas presiones y altas temperaturas, los gases se comportan casi idealmente porque su volumen específico es grande, haciendo despreciables las fuerzas intermoleculares. Sin embargo, cerca de las condiciones de saturación o condensación, las desviaciones se vuelven significativas y el uso de **modelos de gas real** se vuelve esencial.

:::{warning} Importante: región de validez del modelo de gas ideal
La **hipótesis de gas ideal** solo es válida cuando la distancia entre moléculas es grande (baja $p$, alta $T$). Cerca de las fronteras de fase, las atracciones intermoleculares dominan y el modelo de gas ideal falla. Este es el régimen donde se requieren **factores de compresibilidad** y **ecuaciones de estado cúbicas**.
:::

---

(subsec_conceptual_closure_pvt)=
### Cierre conceptual

* La **superficie $p-v-T$** representa el espacio completo de estados de una sustancia.
* Las **proyecciones** sobre los planos coordenados ($T-v$, $p-v$, $p-T$) revelan los mecanismos de cambio de fase y comportamiento crítico.
* La **línea de saturación** forma una campana invertida que delimita las regiones subenfriada, bifásica y recalentada.
* Los **puntos crítico y triple** definen los límites de coexistencia entre las fases líquida y gas.
* Comprender estos diagramas es fundamental para interpretar ciclos termodinámicos y procesos de conversión de energía.

