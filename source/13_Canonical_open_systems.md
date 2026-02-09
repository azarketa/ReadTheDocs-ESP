(sec_canonical_open_systems)=
## Sistemas abiertos canónicos

Los sistemas abiertos canónicos presentados a continuación son dispositivos estándar de **flujo estacionario** en los que la **$1^{\text{a}}$ ley para sistemas abiertos** — {ref}`en su forma específica basada en entalpía <eq_1st_law_open_systems_enthalpy_terms_single_inlet_outlet>` — se aplica directamente:

Cada uno de estos sistemas realiza un tipo característico de **conversión** o **transferencia de energía** entre calor, trabajo y flujo de masa, dependiendo de la configuración física y las condiciones del proceso.

---

(subsec_turbines_compressors)=
### Turbinas y compresores

Las **turbinas** y los **compresores** son dispositivos mecánicos en los que se interconvierte la **entalpía** y el **trabajo de eje**.

* En una **turbina**, el fluido se expande, su entalpía disminuye y parte de esta energía se extrae como **potencia de eje**.
* En un **compresor**, ocurre lo contrario: se suministra trabajo externo al sistema para aumentar la entalpía del fluido (y por tanto su presión y temperatura).

En ambos dispositivos, la **transferencia de calor** hacia el entorno es pequeña en comparación con el intercambio de energía mecánica, y los **cambios en energía cinética y potencial** son despreciables.

Partiendo de la expresión de flujo estacionario de la $1^{\text{a}}$ ley bajo estas suposiciones ($q \simeq 0$, $\Delta c^2 \simeq 0$, $\Delta z \simeq 0$):

(eq_turbine_compressor)=
$$
0 - w_{\text{eje}} = (h_2 - h_1)
\quad\Longrightarrow\quad
\boxed{h_2 - h_1 = -w_{\text{eje}}} \ .
$$

Esto indica que el **cambio de entalpía específica** es igual al **negativo del trabajo de eje por unidad de masa**.

:::{important}

**INTERPRETACIÓN FÍSICA**

* Para una **turbina**, $w_{\text{eje}} > 0$, lo que significa que **se produce trabajo**, por lo que $h_2 < h_1$.
* Para un **compresor**, $w_{\text{eje}} < 0$, lo que significa que **se consume trabajo**, por lo que $h_2 > h_1$.
  En ambos casos, la operación adiabática hace que el cambio de entalpía represente directamente el intercambio de trabajo.
:::

---

(subsec_nozzles_diffusers)=
### Toberas y difusores

Las **toberas** y los **difusores** son dispositivos aerodinámicos que convierten energía entre **entalpía** y **energía cinética**.

* En una **tobera**, la entalpía disminuye a medida que el fluido se acelera (aumentando su velocidad $c$).
* En un **difusor**, la energía cinética disminuye y la entalpía aumenta a medida que el fluido se desacelera.

Suponiendo **operación adiabática** ($q \simeq 0$), **sin trabajo de eje** ($w_{\text{eje}} = 0$) y **cambio de elevación despreciable** ($\Delta z \simeq 0$), el balance de energía en flujo estacionario se convierte en:

(eq_nozzle_diffuser)=
$$
\boxed{(h_2 - h_1) + \frac{c_2^2 - c_1^2}{2} = 0} \ .
$$

Esta expresión muestra que la **disminución o aumento de entalpía** se convierte completamente en **energía cinética** (o viceversa).

:::{tip}

**SOBRE LA GEOMETRÍA DEL FLUJO**

La relación detallada entre **geometría** (convergente o divergente) y **régimen de flujo** (subsónico o supersónico) depende de los efectos de compresibilidad.
Estas condiciones —cruciales en el diseño de **toberas aerodinámicas** y **difusores**— se analizarán más adelante en el estudio del **flujo compresible**.
:::

---

(subsec_heaters)=
### Calentadores

Los **calentadores** son dispositivos donde la temperatura del fluido (y por tanto su entalpía) aumenta mediante **adición de calor**.
Ejemplos típicos incluyen **calentadores eléctricos**, **calderas** y **sobrecalentadores**.

Estos sistemas generalmente operan **sin trabajo de eje** ($w_{\text{eje}} = 0$) y con **cambios despreciables en energía cinética** y **potencial**.
Bajo estas suposiciones, la $1^{\text{a}}$ ley se simplifica a:

(eq_heater)=
$$
\boxed{h_2 - h_1 = q} \ .
$$

Esto significa que el **calor suministrado al volumen de control** aumenta directamente la **entalpía** del fluido en flujo, principalmente como un incremento en **energía interna** y **temperatura**.

:::{note}

**SIGNIFICADO PRÁCTICO**

Para gases perfectos, $h \approx c_p (T - T_{0})$ con $c_{p} = \text{const.} \neq f(T)$, por lo que este balance se convierte en $q = c_p (T_{2} - T_{1})$, mostrando que el aumento de temperatura es proporcional al calor suministrado.
:::

---


(subsec_throttling_valves)=

### Válvulas de estrangulamiento (expansión)

Las **válvulas de estrangulamiento** — también llamadas **válvulas de expansión** o **válvulas de control** — reducen la presión de un fluido en flujo mediante una restricción brusca.
Estos procesos se modelan como **adiabáticos** ($q \simeq 0$), **sin trabajo de eje** y con **cambios despreciables en energía cinética y potencial**.

Aplicando estas suposiciones a la forma de flujo estacionario se obtiene:

(eq_throttling_valve)=
$$
0 = (h_2 - h_1) \implies \boxed{h_2 = h_1} \ .
$$

Por tanto, el estrangulamiento es un **proceso isoentálpico**: la entalpía total permanece constante aunque sus dos componentes — **energía interna** ($u$) y **trabajo de flujo** ($Pv$) — cambien en direcciones opuestas.

Podemos expresarlo explícitamente como:

(eq_throttling_valve_decomposition)=
$$
h = u + pv \implies u_2 - u_1 = -(p_2v_2 - p_1v_1).
$$

Esto significa que una **disminución de la energía de flujo** (caída en $Pv$) debe compensarse con un **aumento en la energía interna** ($u$), o viceversa.
En la práctica, la caída de presión suele causar una **disminución de temperatura**, ya que parte de la energía interna se emplea para realizar el trabajo presión-volumen.

:::{note}

**INTERPRETACIÓN FÍSICA**

La **condición isoentálpica** no siempre implica temperatura constante. En fluidos reales donde $u=u(T,p)$, reducir la presión durante el estrangulamiento puede causar enfriamiento (efecto Joule–Thomson), ampliamente aprovechado en procesos de **refrigeración** y **licuefacción**.
Por el contrario, en gases ideales, $u$ depende solo de $T$, por lo que la temperatura permanece invariable durante el estrangulamiento.
:::

---

(subsec_heat_exchangers)=
### Intercambiadores de calor

Los **intercambiadores de calor** transfieren calor entre dos o más fluidos en flujo separados por una pared sólida, sin mezcla directa. Se modelan como **adiabáticos respecto al entorno** y **sin trabajo de eje**. Observa que:
* A diferencia de los dispositivos anteriores, el paradigma de una entrada/una salida no es aplicable en un intercambiador de calor. Por definición, estos dispositivos hacen interactuar dos fluidos, por lo que la **configuración más simple** concebible debe considerar **dos entradas y dos salidas**. Para los fines de esta exposición, esas dos corrientes se subscriptarán como $a$ y $b$.
* Por supuesto, la **ecuación de continuidad** se cumplirá igualmente.
    * La **masa total** que entra al sistema debe ser igual a la masa total que sale de él $\implies (\dot{m}_{a} + \dot{m}_{b})_{\text{in}} = (\dot{m}_{a} + \dot{m}_{b})_{\text{out}}$
    * Cada una de las corrientes individuales cumplirá también la ecuación de continuidad $\implies \dot{m}_{a_{\text{in}}} = \dot{m}_{a_{\text{out}}}, \quad \dot{m}_{b_{\text{in}}} = \dot{m}_{b_{\text{out}}}$.
    * La condición adiabática del dispositivo respecto al entorno significa que, considerando el sistema como un todo, **no se observa flujo de calor hacia o desde el dispositivo** $\implies q=0$.

Para cada corriente de fluido, aplicando la ecuación de energía en flujo estacionario se obtiene:

(eq_heat_exchanger_energy_balance)=
$$
\dot m_a (h_{a_{\text{out}}} - h_{a_{\text{in}}}) + \dot m_b (h_{b_{\text{out}}} - h_{b_{\text{in}}}) = 0
\implies
\boxed{\dot m_a \Delta h_a = -\dot m_b \Delta h_b} \ .
$$

Por tanto, el **aumento de entalpía de un fluido** es igual a la **disminución de entalpía del otro**.

:::{note}

**EJEMPLOS PRÁCTICOS**

Esta idealización se aplica a condensadores, economizadores, evaporadores y otros intercambiadores de calor industriales.
En sistemas reales, las pérdidas térmicas, la conducción en la pared y el contraflujo imperfecto modifican ligeramente este balance.
:::

---



(subsec_mixing_chambers)=
### Cámaras de mezcla

Las **cámaras de mezcla** combinan múltiples corrientes en una única corriente de salida homogénea. Normalmente son **adiabáticas**, **sin trabajo de eje** y presentan **cambios despreciables en energía cinética y potencial**. Como ocurre con los intercambiadores de calor, el paradigma de una entrada/una salida no es aplicable aquí. La **configuración más simple** concebible es aquella en la que dos corrientes de entrada se mezclan en una sola corriente de salida. Denominando las corrientes, respectivamente, como $(1, 2)$ (entradas) y $3$ (salida):

A partir de la **conservación de la masa**:

(eq_mixing_chamber_mass_conservation)=
$$
\dot m_1 + \dot m_2 = \dot m_3.
$$

y de la **conservación de la energía**:

(eq_mixing_chamber_energy_balance)=
$$
\dot m_1 h_1 + \dot m_2 h_2 = \dot m_3 h_3
\implies
\boxed{h_3 = \frac{\dot m_1 h_1 + \dot m_2 h_2}{\dot m_1 + \dot m_2}} \ .
$$

La entalpía de salida $h_3$ representa un **promedio ponderado por masa** de las entalpías de entrada.

:::{tip}

**APLICACIONES**

Los dispositivos de mezcla se encuentran en **cámaras de combustión**, **humidificadores** e **inyectores de vapor**, donde la uniformidad energética en la corriente de salida es esencial.
:::

---

(subsec_summary_table_canonical_systems)=

### Resumen de sistemas canónicos de flujo estacionario

| **Dispositivo**       | **Interacción energética principal** | **Forma simplificada de la $1^{\text{a}}$ ley** | **Suposiciones típicas**                                           | **Efecto físico principal**                                  |
| :-------------------- | :----------------------------------- | :---------------------------------------------- | :---------------------------------------------------------------- | :----------------------------------------------------------- |
| **Turbina**           | Trabajo de eje (salida)             | $h_2 - h_1 = -w_{\text{eje}}$                | Adiabático, $\Delta c^2$ y $\Delta z \simeq 0$             | Convierte la caída de entalpía en potencia mecánica          |
| **Compresor / Bomba** | Trabajo de eje (entrada)            | $h_2 - h_1 = -w_{\text{eje}}$                | Adiabático, $\Delta c^2$ y $\Delta z \simeq 0$             | Aumenta la entalpía (y presión) mediante trabajo mecánico    |
| **Tobera / Difusor**| Intercambio de energía cinética     | $(h_2 - h_1) + \tfrac{c_2^2 - c_1^2}{2} = 0$   | Adiabático, $w_{\text{eje}}=0$, $\Delta z \simeq 0$              | Convierte entalpía ↔ energía cinética                        |
| **Calentador**        | Adición de calor                   | $h_2 - h_1 = q$                                | $w_{\text{eje}}=0$, $\Delta c^2$ y $\Delta z \simeq 0$             | Eleva la temperatura del fluido mediante transferencia de calor |
| **Válvula de estrangulamiento** | Flujo isoentálpico        | $h_2 = h_1$                                    | Adiabático, $w_{\text{eje}}=0$, $\Delta c^2$ y $\Delta z \simeq 0$  | La caída de presión induce redistribución entre energía interna y trabajo de flujo |
| **Intercambiador de calor** | Intercambio térmico entre corrientes | $\dot m_a \Delta h_a = -\dot m_b \Delta h_b$   | Adiabático global, sin $w_{\text{eje}}$                          | Transferencia de calor entre dos fluidos sin mezcla          |
| **Cámara de mezcla**  | Promedio de entalpía               | $\dot m_1 h_1 + \dot m_2 h_2 = \dot m_3 h_3$   | Adiabático, $w_{\text{eje}}=0$, $\Delta c^2$ y $\Delta z \simeq 0$ | Produce una mezcla uniforme de corrientes entrantes          |

---

(subsec_conceptual_closure_canonical)=

### Cierre conceptual

Los sistemas abiertos canónicos presentados anteriormente son todas **aplicaciones en flujo estacionario** de la misma ley física.
Sus diferencias radican en el **mecanismo energético dominante** y en las **simplificaciones** que hacen que un término de la $1^{\text{a}}$ ley sea más relevante que otros.

* **Turbinas** y **compresores** intercambian entalpía con trabajo mecánico.
* **Toberas** y **difusores** convierten energía entre entalpía y forma cinética.
* **Calentadores** e **intercambiadores de calor** modifican la entalpía mediante transferencia de calor.
* **Válvulas de estrangulamiento** son isoentálpicas pero muestran acoplamiento presión–temperatura mediante redistribución entre energía interna y trabajo de flujo.
* **Cámaras de mezcla** combinan múltiples flujos, conservando tanto la masa como la entalpía total.

Cada tipo de dispositivo ejemplifica una forma en que el **mismo principio de conservación** se manifiesta en ingeniería:
**la energía no puede crearse ni destruirse — solo cambia de forma a medida que la masa fluye a través de las fronteras del sistema.**


