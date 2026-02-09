(sec_humid_air)=
## Aire húmedo

El aire húmedo es aire atmosférico ordinario que contiene una cantidad variable de vapor de agua. Para su análisis, resulta conveniente considerarlo como una **mezcla binaria** de **aire seco** (cuya composición es prácticamente constante) y **vapor de agua** (cuya cantidad varía según las condiciones ambientales). En los rangos atmosféricos típicos, ambos constituyentes pueden modelarse como **gases ideales**, lo que permite reutilizar las herramientas de mezcla introducidas anteriormente y mantener los cálculos simples y precisos.

La **psicrometría** se centra en unas pocas ideas clave: cuánta cantidad de vapor contiene el aire (su **contenido de humedad**), cómo se compara con la cantidad máxima que *podría* contener a la misma temperatura (su **humedad relativa**), cómo se reparte la **presión** entre el aire seco y el vapor (mediante presiones parciales) y cómo calcular la **entalpía** sobre una base de referencia clara (normalmente por unidad de masa de aire seco). Estos conceptos proporcionan un lenguaje compacto y práctico para problemas de confort, secado, refrigeración, deshumidificación y procesos atmosféricos.

(subsec_air_vapor_mixture_atmospheric_air)=
### Mezcla aire–vapor: aire atmosférico

El aire está compuesto principalmente por nitrógeno y oxígeno, y en menor medida por otros gases como argón y dióxido de carbono. Esta composición corresponde al **aire seco**, que no contiene vapor de agua.

En realidad, el **aire atmosférico** suele contener cierta cantidad de vapor de agua (humedad) que varía según la temperatura y las condiciones ambientales. Para la mayoría de los análisis prácticos, resulta conveniente modelar el aire atmosférico como una **mezcla de aire seco y vapor de agua**. La composición del aire seco permanece aproximadamente constante, mientras que la cantidad de vapor de agua fluctúa debido a fenómenos de **evaporación** y **condensación** en la atmósfera.

Por tanto, surge el desafío: *¿cómo caracterizar el aire atmosférico?* Si se supone que tanto el aire seco como el vapor de agua se comportan como **gases ideales**, los conceptos y relaciones previamente establecidos para mezclas de gases pueden aplicarse directamente al análisis del aire húmedo.

Este es, en esencia, el objetivo de la **psicrometría**: el estudio de las propiedades termodinámicas del **aire húmedo**.

---

(subsec_air_vapor_pressure_and_enthalpy)=
### Mezcla aire–vapor: presión y entalpía bajo hipótesis de gas ideal

En condiciones atmosféricas típicas, la temperatura del aire varía aproximadamente entre $-10 \ ^{\circ}\text{C}$ y $50 \ ^{\circ}\text{C}$. Dentro de este rango, el **aire seco** se comporta muy próximo a un **gas ideal**. Como veremos, esto significa que sus propiedades termodinámicas dependen casi exclusivamente de la temperatura. Esto permite introducir un vínculo simple y práctico entre temperatura y contenido energético mediante dos magnitudes relacionadas: el **calor específico** y la **entalpía**.

El **calor específico a presión constante**, $c_p$, actúa como un factor de proporcionalidad que conecta temperatura y energía: indica cuánta energía se requiere, por kilogramo de sustancia, para elevar su temperatura un kelvin manteniendo la presión constante.

(eq_cp_dry_air)=
$$c_p = 1{,}005 \ [\mathrm{kJ/(kg\cdot K)}]$$

En este contexto, la **entalpía específica** $h$ sirve como una medida conveniente del contenido energético específico del gas, combinando tanto su energía interna como la energía asociada a la presión que ejerce. Al igual que ocurre con el calor específico, la entalpía específica de un gas ideal depende únicamente de la temperatura, lo que facilita su cálculo.

Tomando como referencia una temperatura de $0 \ ^{\circ}\mathrm{C}$, la **entalpía específica** del aire seco puede expresarse como:

(eq_h_dry_air)=
$$h = c_p T$$

y la correspondiente **diferencia de entalpía** entre dos estados como:

(eq_delta_h_dry_air)=
$$\Delta h_{i\to f} = c_p \Delta T_{i\to f}.$$

Si tanto el **aire** como el **vapor de agua** se tratan como gases ideales, entonces, según la **ley de Dalton de presiones parciales**, la presión total es la suma de las presiones parciales individuales:

(eq_dalton_air_vapor)=
$$p{}={}p_a{}+{}p_{\text{v}}$$

En el diagrama $T$–$s$ del agua, las líneas de entalpía constante y temperatura constante se superponen por debajo de $50 \ ^{\circ}\mathrm{C}$, lo que confirma que la entalpía depende principalmente de la temperatura en este rango. Por tanto, la entalpía del vapor de agua en el aire puede tomarse como la del **vapor saturado a la misma temperatura**:

(eq_hv_hg_relation)=
$$h_{\text{v}}(T, \text{baja }p) \simeq h_g(T)$$

Dado que la entalpía del vapor saturado a $0 \ ^{\circ}\mathrm{C}$ es $2500{,}9\ \mathrm{kJ/kg}$ y que su calor específico medio es $c_p{}={}1{,}82\ \mathrm{kJ/kg\cdot K}$, se puede escribir:

(eq_hg_approximation)=
$$h_g(T) \simeq h_g(0 \ ^{\circ}\mathrm{C}){}+{}1{,}82T{}={}2500{,}9{}+{}1{,}82{}T \ [\mathrm{kJ/kg}]$$

:::{note}

**HIPÓTESIS DE GAS IDEAL PARA EL VAPOR DE AGUA**

Tratar el vapor de agua como gas ideal implica una pequeña pérdida de precisión, pero es despreciable en condiciones atmosféricas típicas. A $50 \ ^{\circ}\mathrm{C}$, la presión de saturación del agua es $12{,}3 \ \mathrm{kPa}$. Por debajo de esta presión, el vapor de agua se comporta como un **gas ideal** con un error inferior al $0{,}2 \ \%$, incluso en estados saturados. Así, la entalpía del vapor de agua depende **solo de la temperatura**, $h_{\text{v}}{}={}h(T)$.
:::

:::{note}

**REFERENCIA DE TEMPERATURA PARA EL CÁLCULO DE ENTALPÍA**

La expresión para {ref}`la variación de entalpía del aire seco <eq_h_dry_air>` muestra, aparentemente, que la entalpía en un estado termodinámico dado puede calcularse **en términos absolutos**. La termodinámica, sin embargo, no proporciona medios para calcular valores energéticos absolutos, sino **diferencias de energía** (o entalpía, o entropía). De hecho, como la temperatura de referencia se fija en $0 \ ^{\circ}\text{C}$, y existe una **relación lineal** entre $^{\circ}\text{C}$ y $K$ (una diferencia de temperatura de $X \ ^{\circ}\text{C}$ equivale a una diferencia de $X \ \text{K}$), es posible **eliminar el término de referencia** de la expresión. Formalmente, no obstante, la expresión debería haber sido:

$$\Delta{}h_{0\to{}i}={}c_p{}(T_{i} - T_{0})\left[^{\circ}\text{C}\right]$$

Entonces, la expresión rigurosa para el {ref}`cambio de entalpía entre estados inicial y final arbitrarios <eq_delta_h_dry_air>` sería:

$$\Delta{}h_{i\to{}f} = c_p{}\left(\Delta{}T_{0\to{}f} - \Delta{}T_{0\to{}i}\right) = c_p{}\left(T_{f} - T_{0} - \left(T_{i} - T_{0}\right)\right) = c_p\left(T_{f} - T_{i}\right) = c_p\Delta{}T_{i\to{}f}$$
:::



:::{tip}

**EVALUACIÓN APROXIMADA DE LA ENTALPÍA DEL AIRE HÚMEDO**

Al realizar cálculos psicrométricos, utiliza la {ref}`entalpía del aire seco <eq_h_dry_air>` para la porción seca y la {ref}`entalpía del vapor de agua <eq_hg_approximation>` para la porción de vapor. Ambas pueden combinarse posteriormente para expresar la entalpía total del aire húmedo por unidad de masa de aire seco.
:::

---

(subsec_humidities)=
### Mezcla aire–vapor: humedades

La **cantidad de vapor de agua** en el aire puede cuantificarse de varias maneras. La más intuitiva es la **humedad específica** $\omega$, que representa la masa de vapor de agua por unidad de masa de aire seco:

(eq_specific_humidity)=
$$
\omega{}={} \frac{m_{\text{v}}}{m_a}{}={}
\frac{\left(p_{\text{v}} V / R_{\text{v}} T\right)}{\left(p_a V / R_a T\right)}{}={}
\frac{(p_{\text{v}}/R_{\text{v}})}{(p_a/R_a)}{}={}
0{,}622\frac{p_{\text{v}}}{p_a}
\quad\left[\frac{\text{kg vapor de agua}}{\text{kg aire seco}}\right]
$$

Para aire perfectamente seco ($m_{\text{v}}{}={}0$), $\omega{}={}0$. A medida que se añade más vapor, $\omega$ aumenta hasta que el aire alcanza la **saturación**, condición en la que no puede contener más humedad.

En saturación, cualquier exceso de vapor de agua se condensa. La humedad específica del **aire saturado** a una temperatura y presión dadas puede calcularse sustituyendo $p_{\text{v}}$ en la {ref}`relación de humedad específica <eq_specific_humidity>` por la **presión de saturación** $p_g$ del agua a esa temperatura.

La **humedad relativa** $\phi$ compara el contenido real de vapor con el máximo posible a la misma temperatura:

(eq_relative_humidity)=
$$
\phi{}={} \frac{m_{\text{v}}}{m_g}{}={}
\frac{(p_{\text{v}} V / R_{\text{v}} T)}{(p_g V / R_{\text{v}} T)}{}={}
\frac{p_{\text{v}}}{p_g}
\quad[-]
$$

donde $p_g{}={}p_{\text{sat @ }T}$ es la presión de saturación del agua a la temperatura $T$.

Para una mezcla aire–vapor, la **entalpía** por unidad de masa de aire seco combina las contribuciones de ambos componentes:

(eq_total_enthalpy_mixture)=
$$H{}={}H_a{}+{}H_{\text{v}}{}={}m_a h_a{}+{}m_{\text{v}} h_{\text{v}}$$

y, dividiendo por $m_a$:

(eq_specific_enthalpy_humid_air)=
$$h{}={}h_a{}+{}\frac{m_{\text{v}}}{m_a}{}h_{\text{v}}{}={}h_a{}+{}\omega{}h_{\text{v}} \quad [\mathrm{kJ/kg_{aire\ seco}}]$$

:::{note}

**BASE DE REFERENCIA PARA PROPIEDADES DEL AIRE HÚMEDO**

En cálculos psicrométricos, las propiedades se expresan comúnmente **por kilogramo de aire seco** en lugar de por kilogramo de mezcla total.  
Esto simplifica las comparaciones, ya que $m_a$ permanece constante mientras que $m_{\text{v}}$ varía con la humedad y la temperatura.
:::

:::{important}

**SIGNIFICADO FÍSICO DE LA HUMEDAD RELATIVA**

La humedad relativa $\phi$ varía de 0 (aire seco) a 1 (aire saturado). A medida que aumenta la temperatura, la capacidad del aire para contener vapor de agua crece, por lo que $\phi$ cambia incluso cuando $\omega$ (el contenido real de vapor) permanece constante.
:::

---

(subsec_dew_point_temperature)=
### Temperatura de rocío

Los ambientes húmedos suelen dar lugar a la **formación de rocío**, como cuando se encuentra hierba mojada en las mañanas de verano aunque no haya llovido. Este fenómeno ocurre cuando el **aire húmedo** se enfría hasta que su capacidad para contener vapor de agua iguala su contenido real de vapor.

Durante el día, la evaporación aumenta el contenido de vapor del aire. A medida que la temperatura desciende por la noche, la **capacidad de retención de humedad** disminuye. Finalmente, el aire se vuelve **saturado**, lo que significa que su **humedad relativa** alcanza el $100\ \%$. Cualquier descenso adicional de temperatura provoca condensación: este es el inicio de la formación de rocío.

La **temperatura de rocío**, $T_{\text{rocío}}$, se define como la temperatura a la que comienza la condensación cuando el aire se enfría a presión constante.  
En términos termodinámicos, es la **temperatura de saturación** del agua correspondiente a la **presión actual de vapor** $p_{\text{v}}$ de la mezcla:

(eq_dew_point_definition)=
$$T_{\text{rocío}}{}={}T_{\text{sat. @ }p_{\text{v}}}$$

:::{note}

**SIGNIFICADO DE LA TEMPERATURA DE ROCÍO**

El punto de rocío refleja el **contenido real de humedad** del aire: valores altos de $T_{\text{rocío}}$ implican mayor contenido de vapor. Cuando el aire se enfría hasta su punto de rocío, comienza la condensación, marcando la transición de condiciones insaturadas a saturadas.
:::

::::{important}

**EJEMPLO RESUELTO - CONTENIDO DE AGUA Y AIRE EN UNA SAUNA**

**Enunciado del problema**

Una sauna tiene $5 \ \text{m}$ de ancho, $3 \ \text{m}$ de fondo y $2 \ \text{m}$ de alto. En su interior hay un dispositivo transmisor de condiciones ambientales que proporciona la lectura combinada de presión absoluta, temperatura y humedad relativa. Bajo condiciones nominales de operación de la sauna, el dispositivo indica una presión absoluta de $1 \ \text{atm}$, una temperatura de $70 \ ^{\circ}\text{C}$ y una humedad relativa del $75\ \%$. Calcula la humedad específica, así como el contenido total de aire y agua en la sala. Compara dichos valores con el caso en que la sauna está apagada y su temperatura desciende (manteniendo las otras variables constantes) hasta alcanzar el equilibrio con el ambiente en reposo, que está a $20 \ ^{\circ}\text{C}$. Asimismo, calcula y compara las temperaturas de rocío del sistema en ambas condiciones de operación. Discute los resultados.

**Síntesis**

Se evaluarán dos condiciones para la misma sala de volumen $5\times3\times2\ \text{m}^3$:

* **Operación nominal:** $p=1 \ \text{atm}$, $T=70 \ ^\circ\text{C}$, $\phi=75 \ \%$.
* **Sauna apagada (equilibrio con el ambiente):** $p=1\ \text{atm}$, $T=20 \ ^\circ\text{C}$, $\phi=75 \ \%$.

---

**Datos del problema**{cite}`2015Cengel`

| Magnitud                        |           Símbolo           | Valor                                                                      |
| :----------------------------- | :------------------------: | :------------------------------------------------------------------------- |
| Volumen de la sala             |             $V$            | $30 \ \text{m}^3$                                                           |
| Presión absoluta               |             $p$            | $101{,}325 \ \text{kPa}$                                                     |
| Humedad relativa (ambos casos) |           $\phi$           | $0{,}75$                                                                     |
| Temperaturas                   |         $\left(T_1, \ T_2\right)$         | $\left(70 \ ^\circ\text{C}=343{,}15 \ \text{K}, \ 20 \ ^\circ\text{C}=293{,}15 \ \text{K}\right)$ |
| Presión de saturación del vapor| $p_{\text{g}}(70^\circ\text{C})$ | $\approx 31{,}2 \ \text{kPa}$                                                 |
| Presión de saturación del vapor| $p_{\text{g}}(20^\circ\text{C})$ | $\approx 2{,}339 \ \text{kPa}$                                                |
| Constantes de gas              |        $\left(R_{\text{a}}, \ R_{\text{v}}\right)$       | $\left(287{,}058, \ 461{,}5\right) \ \text{J}{}\text{kg}^{-1}\text{K}^{-1}$                    |

---




**Estrategia de solución**

Tratamos el aire húmedo como una mezcla binaria ideal (aire seco + vapor de agua). Para cada estado, calcular:

1. **Presiones parciales**

$$
p_{\text{v}}=\phi{}p_{\text{g}}, \qquad p_{\text{a}}=p-p_{\text{v}} .
$$

2. **Relación de humedad**

$$
\omega = 0{,}62198{}\frac{p_{\text{v}}}{p-p_{\text{v}}}\quad [\text{kg}_{\text{v}}/\text{kg}_{\text{a}}].
$$

3. **Masas en la sala**

$$
m_{\text{a}}=\frac{p_{\text{a}}V}{R_{\text{a}}T}, \qquad m_{\text{v}}=\frac{p_{\text{v}} V}{R_{\text{v}} T}, \qquad m_{\text{tot}} = m_{\text{a}} + m_{\text{v}} .
$$

---

1. **Operación nominal**

    * **Presiones parciales**

        $$
        p_{\text{v}} = 0{,}75\times 31{,}2 \ \text{kPa} = 23{,}4 \ \text{kPa},
        $$
        
        $$
        p_{\text{a}} = 101{,}325 - 23{,}4 = 77{,}925 \ \text{kPa}.
        $$
        
        $$
        \boxed{p_{\text{v}} = 23{,}4 \ \text{kPa}}, \qquad \boxed{p_{\text{a}}=77{,}925 \ \text{kPa}}.
        $$

    * **Relación de humedad:**

        $$
        \omega = 0{,}62198{}\frac{23{,}4}{101{,}325-23{,}4} =
        $$

        $$
        = 0{,}62198{}\frac{23{,}4}{77{,}925} = 0{,}62198\times 0{,}3004 = 0{,}1868.
        $$
        
        $$
        \boxed{\omega_{70} = 0{,}1868 \ \text{kg}_{\text{v}}/\text{kg}_{\text{a}}}.
        $$

    * **Masas en la sala:**

        $$
        m_{\text{a}}=\frac{77{,}925{\cdot}10^{3} \times 30}{287{,}058 \times 343{,}15}
        = \frac{2{,}338{\cdot}10^{6}}{98{,}45{\cdot}10^{3}} \approx 23{,}73 \ \text{kg},
        $$
        
        $$
        m_{\text{v}}=\frac{23{,}4{\cdot}10^{3} \times 30}{461{,}5\times 343{,}15}
        = \frac{7{,}02{\cdot}10^{5}}{1{,}58{\cdot}10^{5}} \approx 4{,}433 \ \text{kg},
        $$
        
        $$
        m_{\text{tot}}= 23{,}73 + 4{,}433 \approx 28{,}17\ \text{kg}.
        $$
        
        $$
        \boxed{m_{\text{a},70} = 23{,}73 \ \text{kg}},\quad
        \boxed{m_{\text{v},70} = 4{,}433 \ \text{kg}},\quad
        \boxed{m_{\text{tot},70} = 28{,}17 \ \text{kg}}.
        $$
  
    * **Temperatura de rocío:**

        El **punto de rocío** es la temperatura a la que la *presión de saturación* iguala esta presión de vapor:

        $$
        p_{\text{g}}(T_{\text{rocío}}) = p_{\text{v}} = 23{,}4\ \text{kPa}.
        $$

        De tablas de vapor estándar{cite}`2015Cengel`:
        
        | $T$ $[^{\circ}\text{C}]$ | $p_{\text{g}}$ $[\text{kPa}]$ |
        | :------: | :------------: |
        |    $60$    |      $19{,}94$     |
        |    $65$    |      $25{,}04$     |
        |    $70$    |      $31{,}15$     |

        Interpolando entre $60 \ {^\circ}\text{C}$ y $65 \ {^\circ}\text{C}$:
  
        $$
        T_{\text{rocío},70} = 60 + (23{,}4 - 19{,}94)\frac{65 - 60}{25{,}04 - 19{,}94} =        
        $$

        $$
        = 60 + 3{,}46\times 0{,}98 \approx 63{,}4 \ ^\circ\text{C}.
        $$

        $$
        \boxed{T_{\text{rocío},70} \approx 63{,}4 \ ^\circ\text{C}}.
        $$
  
---

2. **Sauna apagada**

    * **Presiones parciales (sustituir números primero):**

        $$
        p_{\text{v}}=0{,}75\times 2{,}339 \ \text{kPa} = 1{,}75425 \ \text{kPa},
        $$

        $$
        p_{\text{a}}=101{,}325 - 1{,}75425 = 99{,}57075 \ \text{kPa}.
        $$
        
        $$
        \boxed{p_{\text{v}} = 1{,}754 \ \text{kPa}}, \qquad \boxed{p_{\text{a}}=99{,}57075 \ \text{kPa}}.
        $$

    * **Relación de humedad:**

        $$
        \omega = 0{,}62198{}\frac{1{,}754}{101{,}325 - 1{,}754} =        
        $$

        $$
        = 0{,}62198{}\frac{1{,}754}{99{,}57075} = 0{,}62198 \times 0{,}01762 = 0{,}01096.
        $$
        
        $$
        \boxed{\omega_{20} = 0{,}01096\ \text{kg}_{\text{v}}/\text{kg}_{\text{a}}}.
        $$

    * **Masas en la sala:**

        $$
        m_{\text{a}} = \frac{99{,}57075{\cdot}10^{3} \times 30}{287{,}058\times 293{,}15}
        = \frac{2{,}99{\cdot}10^{6}}{84{,}16{\cdot}10^{3}} \approx 35{,}50 \ \text{kg},
        $$
        
        $$
        m_{\text{v}}=\frac{1{,}754{\cdot}10^{3} \times 30}{461{,}5 \times 293{,}15}
        = \frac{5{,}26{\cdot}10^{4}}{1{,}35{\cdot}10^{5}}\approx 0{,}389 \ \text{kg},
        $$
        
        $$
        m_{\text{tot}} = 35{,}50 + 0{,}389\approx 35{,}89\ \text{kg}.
        $$
        
        $$
        \boxed{m_{\text{a},20} = 35{,}50 \ \text{kg}},\quad
        \boxed{m_{\text{v},20} = 0{,}389 \ \text{kg}},\quad
        \boxed{m_{\text{tot},20} = 35{,}89 \ \text{kg}}.
        $$

    * **Temperatura de rocío:**

        Aquí,
  
        $$p_{\text{v}} = 0{,}75 \times p_{\text{g}}(20^\circ\text{C}) = 1{,}754\ \text{kPa}.$$
        
        De tablas{cite}`2015Cengel`:

        | $T$ $[^{\circ}\text{C}]$ | $p_{\text{g}}$ $[\text{kPa}]$ |
        | :------: | :------------: |
        |    $15$    |      $1{,}705$     |
        |    $20$    |      $2{,}339$     |

        Interpolando entre $15 \ ^{\circ}\text{C}$ y $20 \ ^{\circ}\text{C}$:
  
        $$
        T_{\text{rocío},20} = 15 + (1{,}754 - 1{,}705)\frac{20 - 15}{2{,}339 - 1{,}705} =        
        $$

        $$
        = 15 + 0{,}049\times 7{,}87 \approx 15{,}4 \ ^\circ\text{C}.
        $$

        $$
        \boxed{T_{\text{rocío},20} \approx 15{,}4 \ ^\circ\text{C}}.
        $$

---

3. **Tabla comparativa**

| Caso | $T$ $[^{\circ}\text{C}]$ | $\phi$ $[–]$ | $p_{\text{v}}$ $[\text{kPa}]$ | $p_{\text{a}}$ $[\text{kPa}]$ | $\omega$ $[\text{kg}_{\text{v}}/\text{kg}_{\text{a}}]$ | $m_{\text{a}}$ $[\text{kg}]$ | $m_{\text{v}}$ $[\text{kg}]$ | $m_{\text{tot}}$ $[\text{kg}]$ | $T_{\text{rocío}}$ $[^{\circ}\text{C}]$ |
| :------------------------------------ | :------: | :--------: | :---------: | :------------: | :--------------------: | ------------: | ---------: | ----------------------: | :------: |
| **Operación nominal** | $70$ | $0{,}75$ | $23{,}4$  | $77{,}93$ | $0{,}1868$ | $23{,}73$ | $4{,}433$ | $28{,}17$ | $63{,}4$ |
| **Sauna apagada** | $20$ | $0{,}75$ | $1{,}754$ | $99{,}57$ | $0{,}01096$ | $35{,}50$ | $0{,}389$ | $35{,}89$ | $15{,}4$ |
| **Cambio relativo**<br/>*(vs. nominal)* | $-71{,}4 \ \%$ | — | $−92{,}5 \ \%$ | $+27{,}8 \ \%$ | $−94{,}1 \ \%$ | $+49{,}6 \ \%$ | $−91{,}2 \ \%$ | $+27{,}4 \ \%$ | $-75{,}7 \ \%$ |

---

4. **Discusión de resultados**

* **Colapso acusado de la presión de vapor y de la relación de humedad:** al enfriar de $70 \ ^{\circ}\text{C}$ a $20  \ ^{\circ}\text{C}$ (manteniendo $\phi = 75 \ \%$), la presión parcial de vapor $p_{\text{v}}$ cae en más de **$90 \ \%$**, y la humedad específica $\omega$ disminuye aproximadamente **$94 \ \%$** $\Longrightarrow$ La capacidad del aire para retener vapor de agua decrece drásticamente a baja temperatura.
    
* **Reducción sustancial de la masa de vapor.**  
  La masa de vapor de agua en la sala desciende de **$4{,}43 \ \text{kg}$** a **$0{,}39 \ \text{kg}$** ($\approx -91 \ \%$). La condición de aire caliente contiene así más de diez veces más humedad por kg de aire seco que la condición fría.
    
* **Aumento de la masa total y del aire seco.**  
  El enfriamiento a presión y volumen constantes incrementa la densidad del gas, de modo que $m_{\text{a}}$ sube en **$\approx 50 \ \%$**, y la masa total de aire húmedo en **$\approx 27 \ \%$**.
    
* **Descenso de la temperatura de rocío.**  
  En la **sauna caliente**, el punto de rocío es muy elevado ($\approx 63{,}4 \ ^{\circ}\text{C}$), lo que implica que la condensación se producirá sobre cualquier superficie por debajo de esa temperatura — prácticamente todos los elementos metálicos o de vidrio cerca de los límites de la sala. En la **condición enfriada**, el punto de rocío baja hasta $\approx 15{,}4 \ ^{\circ}\text{C}$, coherente con niveles típicos de humedad interior. La diferencia de $48 \ ^{\circ}\text{C}$ en los puntos de rocío refleja la **fuerte dependencia exponencial** de la presión de vapor con la temperatura — la esencia de por qué las saunas mantienen atmósferas tan densas y ricas en humedad.




:::{tip}

**IMPLICACIÓN FÍSICA DE UN ENFRIAMIENTO REAL**

En la práctica, si el aire a $70 \ ^{\circ}\text{C}$ se enfriara en un volumen cerrado sin deshumidificación, la mayor parte del vapor de agua no podría permanecer en fase gaseosa; aproximadamente **$4 \ \text{kg}$** de agua líquida se **condensarían** sobre paredes y bancos para restablecer la saturación a baja temperatura.
:::

::::

---

(subsec_conceptual_closure_humid_air)=
### Cierre conceptual

* El **aire atmosférico** se modela como una **mezcla de aire seco y vapor de agua**, donde la composición del aire seco permanece constante pero el contenido de vapor varía.
* Suponer **comportamiento de gas ideal** permite usar la {ref}`ley de Dalton <eq_dalton_air_vapor>` y relaciones simples para la {ref}`entalpía del aire seco <eq_h_dry_air>` y la {ref}`entalpía del aire húmedo <eq_hg_approximation>`.
* La {ref}`humedad específica <eq_specific_humidity>` ($\omega$) cuantifica la masa de vapor por unidad de aire seco, mientras que la {ref}`humedad relativa <eq_relative_humidity>` ($\phi$) expresa la relación entre el contenido actual y el máximo posible de vapor.
* La {ref}`entalpía del aire húmedo <eq_specific_enthalpy_humid_air>` se calcula por unidad de masa de aire seco, combinando las contribuciones del aire seco y del vapor.
* La {ref}`temperatura de rocío <eq_dew_point_definition>` indica cuándo comienza la condensación y sirve como medida clave de la humedad real del aire.

