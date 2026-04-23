(sec_nozzles_intro)=
## Toberas y difusores

El propósito de una **tobera** es transformar la entalpía de un gas en flujo en energía cinética mediante un conducto con una geometría adecuada. En los motores aeronáuticos, las toberas aceleran el flujo de escape y generan las elevadas velocidades de salida necesarias para producir empuje.

La contraparte funcional de una tobera es el **difusor**, que realiza la conversión inversa: desacelera un flujo con el fin de aumentar su presión estática y adaptarlo a los componentes posteriores (compresor, cámara de combustión, turbina) o, en el caso de motores de tipo estatorreactor, al propio proceso de combustión.

Aunque el principio básico es sencillo, el comportamiento de toberas y difusores depende en gran medida del régimen del flujo. En particular, los flujos **subsónicos** y **supersónicos** requieren variaciones de área fundamentalmente distintas para lograr aceleración o desaceleración.

---

(subsec_area_velocity_relation)=
### Relación área–velocidad para flujo estacionario y adiabático

Considérese una tobera unidimensional operando en régimen estacionario. La conservación de la masa implica:

(eq_nozzle_continuity)=
$$
\dot{m} = \rho A c = \text{const.}
$$

Tomando la diferencial y reordenando:

(eq_nozzle_continuity_diff)=
$$
\frac{d\rho}{\rho} + \frac{dA}{A} + \frac{dc}{c} = 0.
$$

Suponiendo flujo adiabático y modelando el aire como un gas ideal que experimenta un proceso internamente reversible, la relación isentrópica proporciona:

(eq_isentropic_dp_drho)=
$$
\frac{dp}{p} = \gamma \frac{d\rho}{\rho}.
$$

Para un gas ideal, $p = \rho R T$, por lo que:

(eq_ideal_gas_diff)=
$$
\frac{dp}{p} = \frac{d\rho}{\rho} + \frac{dT}{T}.
$$

Combinando las dos expresiones anteriores se obtiene:

(eq_dT_drho)=
$$
\frac{dT}{T} = (\gamma - 1)\frac{d\rho}{\rho}.
$$

A partir de la ecuación de la energía para flujo estacionario en una tobera adiabática (despreciando la energía potencial):

(eq_energy_nozzle_diff)=
$$
cdc + dh = 0,
$$

y, para un gas perfecto, $dh = c_p\,dT$, por tanto:

(eq_dT_dc)=
$$
c_p{}dT = -c{}dc \quad \Rightarrow \quad \frac{dT}{T} = -\frac{c{}dc}{c_p{}T}.
$$

Utilizando $c_p = \dfrac{\gamma R}{\gamma - 1}$ y $c_s^2 = \gamma R T$, se sigue que:

(eq_drho_dc)=
$$
\frac{d\rho}{\rho} = -\frac{c{}dc}{c_s^2}.
$$

Sustituyendo este resultado en la diferencial de continuidad se llega a la relación fundamental área–velocidad

(eq_area_velocity_mach)=
$$
\frac{dA}{A} = -\frac{dc}{c}{}(1 - Ma^2),
$$

donde el número de Mach es $Ma = \dfrac{c}{c_s}$ y la velocidad del sonido es $c_s = \sqrt{\gamma R T}$.

:::{important}

**LA GEOMETRÍA DEPENDE DEL RÉGIMEN DEL FLUJO**

El signo de $(1-Ma^2)$ determina si el área debe aumentar o disminuir para
acelerar o desacelerar un flujo.

{ref}`A partir de la evolución del área con la velocidad del flujo <eq_area_velocity_mach>`, se deducen cuatro casos de operación:

- **Tobera subsónica** ($Ma<1$, $dc>0$): $dA<0$ (un conducto convergente acelera el flujo).
- **Tobera supersónica** ($Ma>1$, $dc>0$): $dA>0$ (un conducto divergente acelera el flujo).
- **Difusor supersónico** ($Ma>1$, $dc<0$): $dA<0$ (un conducto convergente desacelera el flujo).
- **Difusor subsónico** ($Ma<1$, $dc<0$): $dA>0$ (un conducto divergente desacelera el flujo).

:::

---

(subsec_back_pressure_effect)=
### Efecto de la presión de descarga y estrangulamiento

En flujo compresible, el comportamiento de la tobera está fuertemente influido por la presión de descarga (o contrapresión). A medida que la presión de descarga disminuye con respecto a la presión de entrada, el caudal másico aumenta, pero solo hasta un cierto límite.

Cuando la presión de descarga alcanza un **valor crítico**, el flujo se **estrangula** en la sección de área mínima (la garganta). En condiciones de estrangulamiento:

- el número de Mach en la garganta pasa a ser $Ma=1$,
- el caudal másico alcanza un valor máximo,
- reducciones adicionales de la presión de descarga no incrementan $\dot{m}$.

Este efecto de saturación es particularmente relevante en las toberas convergente–divergentes (de Laval).

:::{note}

**POR QUÉ IMPORTA EL ESTRANGULAMIENTO**

Una vez que la garganta está estrangulada, el flujo aguas arriba queda efectivamente desacoplado de cambios adicionales en la presión aguas abajo. Los ajustes posteriores ocurren principalmente en la parte divergente y/o fuera de la tobera mediante estructuras de ondas compresibles.

:::

---

(subsec_laval_nozzle_regimes)=
### Regímenes de operación de una tobera de Laval

Considérese una tobera convergente–divergente diseñada para operar con expansión supersónica. A medida que la presión de descarga se reduce progresivamente:

- Inicialmente, el flujo permanece enteramente **subsónico** y la sección divergente actúa como un difusor.
- En la contrapresión crítica, la garganta se estrangula ($Ma=1$).
- Para presiones de descarga menores, el flujo se vuelve **supersónico** en parte de la sección divergente, pero puede aparecer un **choque normal** dentro de la tobera. Aguas abajo del choque, el flujo vuelve a ser subsónico y el resto del conducto divergente se comporta como un difusor.
- A medida que la presión de descarga disminuye aún más, el choque se desplaza aguas abajo y puede llegar eventualmente a la salida de la tobera.

Una vez que el flujo interno alcanza su patrón isentrópico totalmente expandido, reducciones adicionales de la presión de descarga se compensan fuera de la tobera. Esto conduce a tres regímenes clásicos:

- **Tobera sobreexpandida:** $p_e < p_{\text{amb}}$; se forman choques oblicuos fuera de la tobera para comprimir el chorro. Típico a baja altitud (alta presión ambiente).
- **Tobera idealmente expandida:** $p_e = p_{\text{amb}}$; no se necesita ninguna estructura de choque externa.
- **Tobera subexpandida:** $p_e > p_{\text{amb}}$; la expansión continúa fuera de la tobera mediante abanicos de expansión y celdas de choque. Típico a gran altitud (baja presión ambiente).

---

(subsec_isentropic_stagnation_relations)=
### Relaciones isentrópicas de remanso y condiciones en la garganta

Para una tobera adiabática e isentrópica con gas perfecto, la ecuación de la energía en flujo estacionario da:

(eq_stagnation_energy)=
$$
c_p T_0 = \frac{c^2}{2} + c_p T.
$$

Reordenando y utilizando $c_s^2=\gamma R{}T$ se llega a la relación estándar entre temperatura de remanso y estática:

(eq_T0_T)=
$$
\frac{T_0}{T} = 1 + \frac{\gamma - 1}{2}Ma^2.
$$

Las razones correspondientes de presión y densidad para flujo isentrópico son:

(eq_p0_p)=
$$
\frac{p_0}{p} = \left(1+\frac{\gamma - 1}{2}Ma^2\right)^{\gamma/(\gamma - 1)},
$$

(eq_rho0_rho)=
$$
\frac{\rho_0}{\rho} = \left(1+\frac{\gamma - 1}{2}Ma^2\right)^{1/(\gamma - 1)}.
$$

En la garganta de una tobera de Laval, donde $Ma=1$, las razones críticas pasan a ser:

(eq_critical_T_ratio)=
$$
\frac{T_*}{T_0} = \frac{2}{\gamma+1},
$$

(eq_critical_P_ratio)=
$$
\frac{p_*}{p_0} = \left(\frac{2}{\gamma+1}\right)^{\gamma/(\gamma-1)},
$$

(eq_critical_rho_ratio)=
$$
\frac{\rho_*}{\rho_0} = \left(\frac{2}{\gamma+1}\right)^{1/(\gamma-1)}.
$$

La velocidad crítica en la garganta es $c_* = c_{s,*}$ y puede escribirse como

(eq_throat_velocity)=
$$
c_* = \sqrt{\gamma{}R{}T_*} = \sqrt{\frac{2\gamma}{\gamma+1}}{}\sqrt{R T_0}.
$$

Cuando la velocidad de entrada es pequeña en comparación con la velocidad de salida, la velocidad de salida puede aproximarse a partir de la caída de entalpía como

(eq_exit_velocity_approx)=
$$
c_2 \approx \sqrt{2{}(h_1 - h_2)}.
$$

:::{note}

**RELACIÓN ÁREA–NÚMERO DE MACH**

La razón de áreas de la tobera puede expresarse como función del número de Mach:

(eq_area_mach)=
$$
\frac{A}{A_*} = \frac{1}{Ma} \left[\frac{2}{\gamma+1}\left(1+\frac{\gamma-1}{2}Ma^2\right)\right]^{\frac{\gamma+1}{2(\gamma-1)}}.
$$

Esta relación se obtiene combinando la continuidad con las relaciones isentrópicas entre magnitudes de remanso y estáticas, y expresando el caudal másico tanto en una sección genérica como en la garganta.

:::

---

(subsec_polytropic_nozzle)=
### Modelo de tobera no isentrópica (politrópica)

Si la tobera no es internamente reversible, puede emplearse una aproximación politrópica, escrita como $p v^n = \text{const.}$ En tal caso, las razones críticas adoptan formas análogas al caso isentrópico, sustituyendo $\gamma$ por $n$ donde corresponda:

- $T_*/T_0 = 2/(n+1)$,
- $p_*/p_0 = \left(2/(n+1)\right)^{n/(n-1)}$,
- $\rho_*/\rho_0 = \left(2/(n+1)\right)^{1/(n-1)}$.

La velocidad en la garganta pasa a ser:

(eq_throat_velocity_polytropic)=
$$
c_* = \sqrt{\frac{2\gamma}{n+1}{}\frac{n-1}{\gamma-1}}{}\sqrt{R T_0}.
$$

Una forma práctica de tener en cuenta las pérdidas es relacionar la velocidad real de salida con la isentrópica mediante un factor de eficiencia $\eta$:

(eq_exit_velocity_eta)=
$$
c_2 \approx \sqrt{\eta}c_{2,\text{iso}}.
$$

El exponente politrópico puede vincularse con la eficiencia mediante:

(eq_polytropic_n_eta)=
$$
n = \frac{\gamma+1+\eta(\gamma-1)}{\gamma+1-\eta(\gamma-1)}.
$$

---

(subsec_nozzles_conceptual_closure)=
### Cierre conceptual
- Las toberas convierten entalpía en energía cinética; los difusores realizan la conversión inversa.
- La variación de área necesaria para acelerar o desacelerar un flujo depende del número de Mach.
- La relación clave es $\dfrac{dA}{A} = -\dfrac{dc}{c}(1-Ma^2)$.
- El estrangulamiento ocurre cuando la garganta alcanza $M=1$, limitando el caudal másico.
- En las toberas de Laval, la presión de descarga controla si aparecen choques dentro o fuera de la tobera.
- Las relaciones isentrópicas de remanso proporcionan $T_0/T$, $p_0/p$ y $\rho_0/\rho$ como funciones de $Ma$.
- Las toberas reales pueden modelarse politrópicamente o mediante correcciones de velocidad/eficiencia.

