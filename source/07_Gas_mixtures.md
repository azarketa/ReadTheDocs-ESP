(sec_gas_mixtures)=
## Mezclas de gases

Las mezclas de gases suelen actuar como fluido de trabajo en sistemas termodinámicos. A diferencia de las sustancias puras, que constan de una sola especie molecular, una mezcla gaseosa está compuesta por varios componentes puros. Cada uno de estos componentes contribuye a las propiedades globales de la mezcla, y su interacción debe describirse mediante definiciones específicas que amplían los conceptos usados para sustancias individuales.

Los dos descriptores de composición más fundamentales son la **fracción másica** y la **fracción molar**, ambos cuantifican cómo contribuye cada componente a la masa total y al número total de moles de la mezcla, respectivamente. Comprender estas definiciones es esencial para expresar propiedades de mezclas y formular la ecuación de estado que rige su comportamiento termodinámico.

---

(subsec_mass_and_molar_fractions)=
### Fracciones másicas y molares

Consideremos una mezcla gaseosa compuesta por $k$ sustancias diferentes (por ejemplo, oxígeno y monóxido de carbono). Dado que la **masa** y la **cantidad de sustancia** son propiedades *extensivas*, sus valores totales son la suma de las contribuciones de cada componente. Usando el subíndice $i$ para denotar un componente específico, podemos escribir:

(eq_total_moles_mass)=
$$N_{\text{total}}{}={} \sum_{i=1}^{k} N_i \qquad\text{y}\qquad m_{\text{total}}{}={} \sum_{i=1}^{k} m_i$$

Cada componente de la mezcla se caracteriza por dos fracciones:

* La **fracción másica** $x_i$, que representa la proporción de la masa total que corresponde al componente $i$.
* La **fracción molar** $y_i$, que representa la proporción del número total de moles correspondiente a ese mismo componente.

Se definen como sigue:

(eq_mass_molar_fractions)=
$$x_i{}={} \frac{m_i}{m_{\text{total}}} \qquad\text{y}\qquad y_i{}={} \frac{N_i}{N_{\text{total}}}$$

Dado que son fracciones, deben cumplir la condición de normalización:

(eq_normalization_mass_molar)=
$${\sum_{i=1}^{k} x_i}{}={}1 \qquad\text{y}\qquad {\sum_{i=1}^{k} y_i}{}={}1$$

:::{note}

**INTERPRETACIÓN FÍSICA**

La fracción másica expresa cuánto de la masa total de la mezcla corresponde a cada especie, mientras que la fracción molar indica cuántos moles de esa especie están presentes en relación con el total. Ambas son fundamentales para convertir entre magnitudes basadas en moles y en masa en cálculos de mezclas.
:::

---

(subsec_pvt_behaviour_ideal_mixtures)=
### Comportamiento $p-v-T$ de mezclas de gases ideales

Las definiciones de $x_i$ y $y_i$ adquieren especial relevancia al describir el comportamiento presión–volumen–temperatura ($p–v–T$) de mezclas que obedecen la **ley de gas ideal**. Cuando los gases se comportan idealmente, dos relaciones empíricas —**ley de Dalton** y **ley de Amagat**— conectan las propiedades globales de la mezcla con las de sus componentes individuales.

(eq_dalton_law)=
$$p_{\text{total}}{}={} \sum_{i=1}^{k} p_i(T_{\text{total}}, V_{\text{total}})$$

Según la ley de Dalton, la **presión total** de una mezcla es igual a la suma de las **presiones parciales** ejercidas por cada componente. Cada presión parcial $p_i$ se calcula a la temperatura y volumen totales de la mezcla, es decir, el estado termodinámico compartido por todas las especies.

De forma análoga, la **ley de Amagat** aplica el mismo principio aditivo a los volúmenes:

(eq_amagat_law)=
$$V_{\text{total}}{}={} \sum_{i=1}^{k} V_i(T_{\text{total}}, p_{\text{total}})$$

La afirmación de Amagat refleja que el **volumen también es una propiedad extensiva**, al igual que la masa o los moles. Se deduce que el volumen total de la mezcla es igual a la suma de los volúmenes parciales que ocuparía cada componente si existiera solo a la presión y temperatura totales de la mezcla.

Ahora, introduciendo la **ley de gas ideal** para cada componente, podemos establecer el vínculo entre las razones de cantidades parciales y totales y las fracciones molares. Para cualquier componente $i$:

(eq_partial_pressure_ratio)=
$$\frac{p_i(T_{\text{total}}, V_{\text{total}})}{p_{\text{total}}}{}={} \frac{\left(\frac{N_i R_u T_{\text{total}}}{V_{\text{total}}}\right)}{\left(\frac{N_{\text{total}} R_u T_{\text{total}}}{V_{\text{total}}}\right)}{}={} \frac{N_i}{N_{\text{total}}}{}={}y_i$$

(eq_partial_volume_ratio)=
$$\frac{V_i(T_{\text{total}}, p_{\text{total}})}{V_{\text{total}}}{}={} \frac{\left(\frac{N_i R_u T_{\text{total}}}{p_{\text{total}}}\right)}{\left(\frac{N_{\text{total}} R_u T_{\text{total}}}{p_{\text{total}}}\right)}{}={} \frac{N_i}{N_{\text{total}}}{}={}y_i$$

Así, las razones entre la presión parcial y el volumen parcial de cada componente respecto a los valores totales de la mezcla coinciden con la **fracción molar** del componente:

(eq_y_relation)=
$$\frac{p_i}{p_{\text{total}}}{}={} \frac{V_i}{V_{\text{total}}}{}={} \frac{N_i}{N_{\text{total}}}{}={}y_i$$

:::{tip}

**IMPORTANCIA DE LA FRACCIÓN MOLAR**

La fracción molar expresa directamente cómo contribuye cada especie a la presión y volumen globales de la mezcla gaseosa. Actúa como el factor de ponderación natural para muchas otras propiedades de la mezcla y simplifica la formulación de ecuaciones de estado y energía.
:::

---



(subsec_properties_ideal_mixtures)=
### Propiedades de mezclas de gases ideales

Una vez establecidas las relaciones $p$–$v$–$T$ para mezclas ideales, las mismas definiciones de fracciones molares y másicas pueden emplearse para describir otras propiedades termodinámicas. El **principio de aditividad** de las propiedades extensivas se extiende naturalmente a la energía interna, entalpía, entropía y calores específicos.

Para los **calores específicos molares** (expresados en $[\mathrm{J/mol\cdot K}]$), cada propiedad de la mezcla es la suma ponderada por fracción molar de las propiedades correspondientes de los gases individuales:

(eq_molar_specific_heats)=
$$\overline{c_{p}}_{\text{mezcla}}{}={} \sum_{i=1}^{k} y_i{}\overline{c_{p}}_{i} \qquad\text{y}\qquad \overline{c_{v}}_{\text{mezcla}}{}={} \sum_{i=1}^{k} y_i{}\overline{c_{v}}_{i}$$

Cuando los calores específicos se expresan en **base másica** (en $[\mathrm{J/kg\cdot K}]$), la ponderación debe realizarse con las **fracciones másicas**:

(eq_mass_specific_heats)=
$$c_{p_{\text{mezcla}}}{}={} \sum_{i=1}^{k} x_i{}c_{p_{i}} \qquad\text{y}\qquad c_{v_{\text{mezcla}}}{}={} \sum_{i=1}^{k} x_i{}c_{v_{i}}$$

De manera similar, la **masa molar** de la mezcla —que representa la masa equivalente por kilomol de mezcla— se obtiene mediante la suma ponderada por fracción molar de las masas molares de los componentes:

(eq_mixture_molar_mass)=
$$\text{M}_{\text{mezcla}}{}={} \sum_{i=1}^{k} y_i{}\text{M}_i$$

Finalmente, la **constante de gas de la mezcla** se obtiene realizando una suma ponderada por fracción másica de las constantes individuales:

(eq_mixture_gas_constant)=
$$R_{\text{mezcla}}{}={} \sum_{i=1}^{k} x_i{}R_i$$

Por último, las **propiedades extensivas** de una mezcla pueden expresarse como sumas ponderadas por moles o por masa de las propiedades molares/específicas de cada componente:

\begin{equation}
    \Phi_{\text{mezcla}}
    \begin{cases}
         = \sum_{i=1}^{k} N_i\overline{\phi}_i \ \ \text{(base molar)}\\[3ex]
         = \sum_{i=1}^{k} m_i\phi_i \ \ \text{(base másica)}
    \end{cases}
\end{equation}

donde:

* $\Phi_{\text{mezcla}}$ es la propiedad total (extensiva) de la mezcla,
* $\overline{\phi}_i$ y $\phi_i$ son las propiedades **molares** y **específicas**, respectivamente, del componente $i$,
* $N_i$ y $m_i$ son los **moles** y la **masa** de dicho componente, y
* $k$ es el número total de componentes en la mezcla.

Esta formulación se aplica a cualquier **magnitud extensiva** —como el volumen total— y garantiza que la propiedad de la mezcla refleje la contribución colectiva de todos los componentes, cada uno ponderado por su fracción másica.

:::{note}

**VALIDEZ DE LA ADITIVIDAD**

Todas las relaciones anteriores se basan en la **hipótesis de mezcla ideal**, donde se desprecia la interacción entre especies diferentes. Para mezclas reales —especialmente a alta presión, baja temperatura o cuando ocurren reacciones químicas— estas reglas deben sustituirse por modelos no ideales (por ejemplo, ecuaciones de estado con reglas de mezcla o coeficientes de actividad).
:::

:::{important}

**COHERENCIA DE UNIDADES EN PROPIEDADES DE MEZCLAS**

Cada propiedad de una mezcla de gases ideal —ya sea expresada por mol o por masa— resulta de un **promedio ponderado** de las propiedades de los componentes. El factor de ponderación depende de la base de referencia:

* **Fracción molar $y_i$** para propiedades molares.
* **Fracción másica $x_i$** para propiedades en base másica.

Esta distinción asegura la coherencia dimensional y predicciones precisas de propiedades. Obsérvese que las cantidades molares y másicas presentan una nomenclatura diferente. Si $\phi$ es una magnitud genérica (por ejemplo, un calor específico o una masa molar):
* Las **cantidades molares** se expresan con **barra superior**, es decir, $\overline{\phi}$ (p. ej., $\overline{c}_{p,\text{mezcla}}$). Cuando se emplea una fórmula de suma ponderada, las cantidades molares se acompañan de las **fracciones molares $y_{i}$**.
* Las **cantidades másicas** se expresan con símbolos **sin barra**, es decir, $\phi$ (p. ej., $c_{p,\text{mezcla}}$). Cuando se emplea una fórmula de suma ponderada, las cantidades másicas se acompañan de las **fracciones másicas $x_{i}$**.
:::



::::{important}

**EJEMPLO RESUELTO — PROPIEDADES DE MEZCLA DEL AIRE ESTÁNDAR**

**Enunciado del problema**

El aire es una mezcla común que suele describirse con una composición volumétrica de $21 \ \%$ $\text{O}_{2}$ y $79 \ \%$ $\text{N}_{2}$. Las masas molares de esos componentes pueden obtenerse de tablas químicas estándar, así como los valores de la constante universal de los gases ($\text{R}_{\text{u}}$) y las constantes de calor específico de los componentes a temperaturas particulares. Suponiendo que el sistema analizado está compuesto por aire estándar a una temperatura de $25 \ ^{\circ}\text{C}$, calcula su masa molar efectiva, así como sus constantes de calor específico, y compáralas con los valores tabulados estándar.

**Síntesis**

El “aire estándar” se modela como una mezcla de gas ideal con **fracciones molares** $y_{\mathrm{O_2}} = 0{,}21$, $y_{\mathrm{N_2}}=0{,}79$ a $T=25 \ ^\circ\text{C}$, y se calculan las siguientes magnitudes:

* **Masa molar efectiva**, $\text{M}_{\text{aire}}$,
* **Mezcla** $\overline{c_{p}}_{\text{aire}}$ y $\overline{c_{v}}_{\text{aire}}$ (base molar), luego en **base másica** $c_{p_{\text{aire}}}$, $c_{v_{\text{aire}}}$, $R_{\text{aire}}$, y $\gamma_{\text{aire}}=c_{p_{\text{aire}}}/c_{v_{\text{aire}}}$,
* Comparación con valores **tabulados de “aire estándar”** a $\approx 300 \ \text{K}$.

---

**Datos del problema**{cite}`2015Cengel`

| Magnitud                                    |                  Símbolo                  | Valor                                                                                                  |
| :------------------------------------------ | :--------------------------------------: | :----------------------------------------------------------------------------------------------------- |
| Fracciones molares                          |   $\left(y_{\mathrm{O_2}}, \ y_{\mathrm{N_2}}\right)$   | $\left(0{,}21, \ 0{,}79\right)$                                                                                          |
| Masas molares                               |   $\left(\text{M}_{\mathrm{O_2}}, \ \text{M}_{\mathrm{N_2}}\right)$   | $\left(31{,}998, \ 28{,}0134\right) \ \text{g/mol}$                                                                       |
| Constante universal de los gases            |                   $R_u$                  | $8{,}314462618 \ \text{J mol}^{-1}\text{K}^{-1}$                                                          |
| Componentes $\overline{c_{p}}$ a $25^\circ\text{C}$ | $\left(\overline{c_{p}}_{\mathrm{O_2}}, \ \overline{c_{p}}_{\mathrm{N_2}}\right)$ | $\left(29{,}355, \ 29{,}124\right) \ \text{J mol}^{-1}\text{K}^{-1}$                                                      |
| Aire estándar (tabulado) | $\left(\text{M}_{\text{aire}_{\text{tb}}}, \ R_{\text{aire}_{\text{tb}}}, \ c_{p_{\text{aire}_{\text{tb}}}}, \ c_{v_{\text{aire}_{\text{tb}}}}, \ \gamma_{\text{aire}_{\text{tb}}}\right)$ | $\left(28{,}965, \ 287{,}058, \ 1005, \ 718, \ 1{,}400\right)$ |

---

**Cálculos**

1. **Masa molar efectiva (mezcla ideal):**

    $$
    \text{M}_{\text{aire}} = \sum_i y_i M_i = 0{,}21(31{,}998) + 0{,}79(28{,}0134) = 28{,}850166\ \text{g/mol}.
    $$
    
    $$
    \boxed{\text{M}_{\text{aire}} = 28{,}850 \ \text{g/mol}}
    $$

2. **Calores molares de la mezcla (mezcla de gas ideal, regla de Lewis):**

    $$
    \overline{c_{p}}_{\text{aire}}=\sum_i y_i \overline{c_{p}}_{i} = 0{,}21(29{,}355) + 0{,}79(29{,}124) = 29{,}17251 \ \text{J mol}^{-1}\text{K}^{-1},
    $$
    
    $$
    \overline{c_{v}}_{\text{aire}} = \overline{c_{p}}_{\text{aire}} - R_u = 29{,}17251 - 8{,}314462618 = 20{,}85805 \ \text{J mol}^{-1}\text{K}^{-1}.
    $$
    
    $$
    \boxed{\overline{c_{p}}_{\text{aire}} = 29{,}173\ \text{J mol}^{-1}\text{K}^{-1}}, \qquad \boxed{\overline{c_{v}}_{\text{aire}} = 20{,}858\ \text{J mol}^{-1}\text{K}^{-1}}
    $$

3. **Propiedades en base másica** (usando $\text{M}_{\text{aire}}$ en $\text{kg/mol}$):

    Convertir $\text{M}_{\text{aire}}$ a $\text{kg/mol}$: $ \ \text{M}_{\text{aire}} = 28{,}850166\times10^{-3}\ \text{kg/mol}$.

   * Constante específica de gas:

        $$
        R_{\text{aire}} = \frac{R_u}{\text{M}_{\text{aire}}} = \frac{8{,}314462618}{28{,}850166\times10^{-3}} = 288{,}1946\ \text{J kg}^{-1}\text{K}^{-1}.
        $$

    * Calores específicos en base másica:
    
        $$
        c_{p_{\text{aire}}}=\frac{\overline{c_{p}}_{\text{aire}}}{\text{M}_{\text{aire}}} = \frac{29{,}17251}{28{,}850166\times10^{-3}} = 1{,}011 \ \text{kJ kg}^{-1}\text{K}^{-1},
        $$
    
        $$
        c_{v_{\text{aire}}}=\frac{\overline{c_{v}}_{\text{aire}}}{\text{M}_{\text{aire}}} = \frac{20{,}85805}{28{,}850166\times10^{-3}} = 0{,}723 \ \text{kJ kg}^{-1}\text{K}^{-1}.
        $$

    * Exponente isentrópico:

        $$
        \gamma_{\text{aire}}=\frac{c_{p_{\text{aire}}}}{c_{v_{\text{aire}}}} = \frac{1{,}011}{0{,}723} = 1{,}39862.
        $$

    $$
    \boxed{R_{\text{aire}} = 288{,}195\ \text{J kg}^{-1}\text{K}^{-1}},\quad
    \boxed{c_{p_{\text{aire}}} = 1{,}011 \ \text{kJ kg}^{-1}\text{K}^{-1}},
    $$

    $$
    \boxed{c_{v_{\text{aire}}} = 0{,}723 \ \text{kJ kg}^{-1}\text{K}^{-1}},\quad
    \boxed{\gamma_{\text{aire}} = 1{,}3986}
    $$

---

**Comparación con valores tabulados de “aire estándar”**

| Propiedad  | Cálculo actual | Tabulado |  Dif. rel. |
| :-------------------------- | --------: | --------: | ---------: |
| $\text{M} \ [\text{g}/\text{mol}]$                    |  $28{,}850$ |  $28{,}965$ | $-0{,}40 \ \%$ |
| $R_{\text{aire}} \ [\text{J kg}^{-1}K^{-1}]$            | $288{,}195$ | $287{,}058$ | $+0{,}40 \ \%$ |
| $c_{p_{\text{aire}}} \ [\text{kJ kg}^{-1}K^{-1}]$       | $1{,}011$ |    $1{,}005$ | $+0{,}61 \ \%$ |
| $c_{v_{\text{aire}}} \ [\text{kJ kg}^{-1}K^{-1}]$       |  $0{,}723$ |     $0{,}718$ | $+0{,}69 \ \%$ |
| $\gamma_{\text{aire}} \ [–]$                            |  $1{,}3986$ |   $1{,}400$ | $-0{,}10 \ \%$ |

---

:::{tip}

**INTERPRETACIÓN**

Las diferencias son **inferiores al 1 %** y se deben a:
1. La composición binaria simplificada (sin $\text{Ar}$, $\text{CO}_{2}$, etc.; el argón por sí solo aumenta la $\text{M}_{\text{aire}}$).
2. Dependencias suaves de $c_{p}$ con la temperatura para gases reales alrededor de $300\ \text{K}$.

Incluir especies menores (p. ej., $\sim0{,}93 \ \% \ \text{Ar}$) y usar polinomios $c_p(T)$ de alta precisión acercaría los resultados a los valores tabulados de “aire estándar”.
:::

::::

---

(subsec_conceptual_closure_gas_mixtures)=
### Cierre conceptual

* Las {ref}`fracciones másicas y molares <eq_mass_molar_fractions>` son la base del análisis de mezclas. Su {ref}`condición de normalización <eq_normalization_mass_molar>` garantiza una descripción completa de la composición.
* La {ref}`ley de Dalton de presiones <eq_dalton_law>` y la {ref}`ley de Amagat de volúmenes <eq_amagat_law>` establecen el comportamiento aditivo de las mezclas ideales para presión y volumen.
* Tanto las **presiones parciales** como los **volúmenes parciales** {ref}`se escalan con la fracción molar <eq_y_relation>`, lo que explica su papel central en las formulaciones de mezclas.
* La **evaluación de propiedades** sigue la misma lógica aditiva: calores específicos (en sus formulaciones {ref}`molares <eq_molar_specific_heats>` y {ref}`másicas <eq_mass_specific_heats>`), {ref}`masa molar <eq_mixture_molar_mass>` y {ref}`constante de gas <eq_mixture_gas_constant>` son todos promedios ponderados.
* Las **variaciones de propiedades de estado** como {ref}`energía interna <eq_state_property_changes>`, {ref}`entalpía <eq_enthalpy_change_mixture>` y {ref}`entropía <eq_entropy_change_mixture>` son sumas ponderadas por masa, extendiendo el mismo principio al análisis de energía y entropía.

