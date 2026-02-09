(sec_clausius_inequality_entropy)=
## La desigualdad de Clausius y la definición de entropía

Hasta este punto, la **$2^{\text{a}}$ ley** se ha formulado para **dispositivos cíclicos** — motores térmicos, refrigeradores y bombas de calor — donde el intercambio de energía ocurre repetidamente entre focos térmicos. Sin embargo, la termodinámica se aplica no solo a ciclos, sino a **cualquier transformación de estado**. Del mismo modo que la **$1^{\text{a}}$ ley** expresa la conservación de la energía para **todos** los procesos, la **$2^{\text{a}}$ ley** debe poder expresarse en una forma general, basada en procesos — que valga incluso para **transformaciones no cíclicas**.

---

(subsec_clausius_inequality)=
### La desigualdad de Clausius

Para generalizar la **$2^{\text{a}}$ ley**, **Rudolf Clausius** propuso una configuración particularmente esclarecedora: consideró un **motor térmico reversible** y un **sistema auxiliar** separado que absorbe el calor rechazado por el motor y lo utiliza para producir trabajo adicional.

Consideremos, entonces, un **motor reversible** que absorbe una cantidad infinitesimal de calor $\delta Q_R$ de un **foco térmico** a temperatura $T_R$ y produce una pequeña cantidad de **trabajo** $\delta W_{\text{rev}}$. El calor que rechaza, $\delta Q$, se envía a un **conjunto pistón–cilindro** que contiene un gas a temperatura $T$. Al expandirse cuasiestáticamente mientras absorbe ese calor, el gas realiza un trabajo $\delta W_{\text{sys}}$.

El **trabajo total** del sistema combinado es, por tanto,

$$
\delta W_{\text{neto}} = \delta W_{\text{rev}} + \delta W_{\text{sys}}.
$$

Aplicando la **$1^{\text{a}}$ ley** al sistema completo (motor + cilindro) se obtiene

$$
\mathrm{d}E_{\text{neto}} = \delta Q_R - \delta W_{\text{neto}}.
$$

Para un proceso **cíclico** combinado, el cambio total de energía es nulo $(\mathrm{d}E_{\text{neto}} = 0)$, y por tanto

$$
\delta W_{\text{neto}} = \delta Q_R.
$$

Dado que el motor es **reversible**, se aplica la relación de Carnot a los calores y temperaturas implicados:

$$
\frac{\delta Q}{\delta Q_R} = \frac{T}{T_R}.
$$

Sustituyendo en la relación anterior e integrando sobre un ciclo completo se llega a

(eq_clausius_intermediate)=
$$
W_{\text{neto}} = T_R \oint \frac{\delta Q}{T}.
$$

Esta ecuación **parece** describir un sistema que toma calor de un único foco (a $T_R$) y lo convierte íntegramente en trabajo — una **violación** del postulado de Kelvin–Planck. Puesto que tal proceso no puede ocurrir, el integral no puede corresponder a un trabajo positivo; por consiguiente, debe cumplirse

(eq_clausius_inequality)=
$$
\boxed{\oint \frac{\delta Q}{T} \leq 0.}
$$

Esta es la **desigualdad de Clausius**, una formulación general de la **$2^{\text{a}}$ ley** aplicable a cualquier **proceso cíclico**.

:::{important}

**INTERPRETACIÓN FÍSICA DE LA DESIGUALDAD**

* Para un **ciclo reversible**, $\displaystyle \oint \frac{\delta Q}{T} = 0$.
* Para un **ciclo irreversible**, $\displaystyle \oint \frac{\delta Q}{T} < 0$.

La igualdad señala el límite ideal, cuasiestático, sin efectos disipativos; la desigualdad marca la **irreversibilidad** inherente a todos los procesos reales.
:::

:::{note}

**POR QUÉ IMPORTA LA CONSTRUCCIÓN DE CLAUSIUS**

Esta configuración conceptual no es arbitraria — es un **experimento mental** diseñado para poner a prueba la coherencia de la **$2^{\text{a}}$ ley**. Al acoplar un motor reversible con otro sistema que reutiliza su calor rechazado, Clausius examinó si sería posible, *en principio*, construir un dispositivo que tomase calor de un único foco y lo convirtiese íntegramente en trabajo — precisamente la situación prohibida por el **postulado de Kelvin–Planck**.

Esta construcción actúa, por tanto, como una **prueba de consistencia**: si el sistema combinado llegase a producir un trabajo neto positivo intercambiando calor con un solo foco, el postulado quedaría violado. Así, la configuración proporciona una vía rigurosa y didáctica para derivar una **restricción cuantitativa** sobre todos los ciclos — la **desigualdad de Clausius**.
:::

---

(subsec_entropy_definition)=
### De la forma cíclica al proceso general: la definición de entropía

La **desigualdad de Clausius** se obtuvo primero para transformaciones cíclicas, pero sus implicaciones alcanzan mucho más lejos. Si para un ciclo reversible se cumple

$$
\oint \frac{\delta Q}{T} = 0,
$$

entonces el integral de $\frac{\delta Q}{T}$ entre dos estados dados — *siempre que el proceso sea reversible* — debe depender **solo de esos estados**, no del camino seguido entre ellos.
En términos matemáticos, esto significa que el integral define una **función de estado**.

La **forma diferencial** de esa función de estado es, por tanto,

(eq_entropy_differential)=
$$
\boxed{\mathrm{d}S = \left(\frac{\delta Q}{T}\right)_{\text{rev}}.}
$$

Esta nueva magnitud, introducida por Clausius, se denomina **entropía** $(S)$. Constituye un puente entre las formulaciones de la **$2^{\text{a}}$ ley** basadas en **ciclos** y las basadas en **procesos**. La entropía mide tanto el **estado termodinámico** de un sistema como el **grado de irreversibilidad** de un proceso.

Para un proceso real (irreversible), la desigualdad de Clausius puede escribirse en forma general como

(eq_entropy_inequality)=
$$
\boxed{\Delta S \ge \int \frac{\delta Q}{T}},
$$

donde la igualdad solo se cumple para transformaciones **reversibles**.

:::{important}

**SIGNIFICADO DE LA ENTROPÍA Y GENERALIZACIÓN DE LA $2^{\text{a}}$ LEY**

* La entropía es una **propiedad de estado**, lo que permite expresar la **$2^{\text{a}}$ ley** para **procesos no cíclicos**.
* Para cualquier **proceso reversible**, $\Delta S = \int \frac{\delta Q_{\text{rev}}}{T}$.
* Para cualquier **proceso irreversible**, $\Delta S > \int \frac{\delta Q_{\text{irrev}}}{T}$ — lo que significa que la **entropía del universo aumenta**.
:::

:::{note}

**UNIDADES DE ENTROPÍA**

Ten en cuenta que, según la {ref}`ecuación anterior <eq_entropy_inequality>`, la entropía (y la entropía específica, i.e., entropía por unidad de masa) comparte la misma **estructura dimensional** que el cociente entre calor y temperatura:

$$
\begin{gather*}
[S] = \frac{\text{kJ}}{\text{K}}, \\[10pt]
[s] = \frac{\text{kJ}}{\text{kg}{\cdot}\text{K}}.
\end{gather*}
$$

Las unidades de $s$ coinciden con las de $c_p$ o $c_v$ — reflejando que todas describen **energía por unidad de masa y por unidad de temperatura**.
:::

---

(subsec_principle_increasing_entropy)=
### El principio de aumento de la entropía

Una vez establecida la **entropía** como propiedad que cuantifica la transferencia de calor reversible, podemos extender su uso a **todos los procesos reales**. La **desigualdad de Clausius** proporciona la clave: permite comparar cualquier transformación real (irreversible) con una reversible entre los mismos dos estados. Mediante esta comparación, la **$2^{\text{a}}$ ley** revela una regla universal que gobierna la evolución de la entropía en la naturaleza — el **principio de aumento de la entropía**.

Considera un **proceso genérico** entre dos estados, $(1)$ y $(2)$, que puede ser reversible o irreversible. Si le añadimos un **camino de retorno internamente reversible** $(2) \rightarrow (1)$, se forma un ciclo completo y se aplica la **desigualdad de Clausius**:

$$
\oint \frac{\delta Q}{T} \le 0.
$$

Desarrollando el integral cíclico se obtiene

$$
\int_1^2 \frac{\delta Q}{T} + \int_2^1 \left( \frac{\delta Q}{T} \right)_{\text{rev.}} \le 0,
$$

y, dado que el segundo término vale $S_1 - S_2$, resulta

$$
S_2 - S_1 \ge \int_1^2 \frac{\delta Q}{T},
\qquad \text{o, de forma equivalente,} \qquad
\mathrm{d}S \ge \frac{\delta Q}{T}.
$$

Esta desigualdad expresa que, para cualquier proceso real (irreversible), el **aumento de entropía del sistema** es mayor que la **entropía transferida** únicamente mediante calor. El cambio total de entropía puede escribirse entonces como

(eq_entropy_generation)=
$$
\boxed{\Delta S_{\text{sys.}} = \int_1^2 \frac{\delta Q}{T} + S_{\text{gen.}}},
\qquad S_{\text{gen.}} \ge 0,
$$

donde $S_{\text{gen.}}$ representa la **entropía generada internamente** debido a las irreversibilidades. Para un proceso reversible, $S_{\text{gen.}} = 0$; para uno irreversible, $S_{\text{gen.}} > 0$.

En un **sistema aislado**, no cruza la frontera ni calor ni masa ($\delta Q = 0$), de modo que

$$
\Delta S_{\text{aislado}} = S_{\text{gen.}} \ge 0.
$$

Así, la entropía solo puede **permanecer constante** (para procesos reversibles) o **aumentar** (para procesos irreversibles). Extendiendo esta idea al **universo termodinámico** — el sistema y sus alrededores conjuntamente — se obtiene

(eq_entropy_universe)=
$$
\boxed{\Delta S_{\text{univ.}} = \Delta S_{\text{sys.}} + \Delta S_{\text{surr.}} = S_{\text{gen.,univ.}} \ge 0.}
$$

Son posibles disminuciones locales de entropía dentro de subsistemas, pero siempre deben compensarse con aumentos mayores en otros lugares, asegurando que la **entropía total del universo no disminuye jamás**.

:::{important}

**SIGNIFICADO FÍSICO**

* La entropía se **conserva** solo en procesos reversibles y se **crea** en los irreversibles.
* El aumento de entropía define la **dirección natural de los procesos** y establece la **flecha termodinámica del tiempo**.
* Aunque la entropía puede disminuir localmente, el **balance global** (sistema + alrededores) siempre satisface $\Delta S_{\text{univ.}} \ge 0$.
:::

---

(subsec_conceptual_closure_clausius_entropy)=
### Cierre conceptual

* La **construcción de Clausius** transforma la **$2^{\text{a}}$ ley** de una limitación cualitativa sobre dispositivos cíclicos en un **principio cuantitativo** válido para todos los procesos.
* Al acoplar un motor reversible con otro sistema, Clausius mostró que la conversión completa de calor en trabajo **violaría** la **$2^{\text{a}}$ ley**, conduciendo a la **desigualdad de Clausius**
  
  $$
  \oint \frac{\delta Q}{T} \le 0.
  $$
  
* Esta relación distingue los ciclos **reversibles** ($=$) de los **irreversibles** ($<$) y revela que el integral reversible define una nueva **propiedad de estado** — la **entropía**:
  
  $$
  \mathrm{d}S = \left( \frac{\delta Q}{T} \right)_{\text{rev.}}.
  $$
  
* La entropía extiende la **$2^{\text{a}}$ ley** a **cualquier proceso**, midiendo tanto la **distribución de energía** dentro de un sistema como la **irreversibilidad** de las transformaciones reales.
* El **balance de entropía**,
  
  $$
  \Delta S_{\text{sys.}} = \int \frac{\delta Q}{T} + S_{\text{gen.}},
  $$
  
  distingue la **transferencia** de entropía (vía calor) de la **generación** de entropía (vía irreversibilidad).
* El **principio de aumento de la entropía** establece que, para cualquier sistema aislado o para el universo en su conjunto,
  
  $$
  \Delta S_{\text{univ.}} \ge 0,
  $$
  
  expresando la dirección natural de todos los procesos.
* Las transformaciones reversibles conservan entropía, mientras que las irreversibles la crean — definiendo simultáneamente el **límite de desempeño ideal** y la **flecha termodinámica del tiempo**.

En resumen, la **$2^{\text{a}}$ ley** alcanza su forma más general: la energía sigue conservándose, pero su **calidad** — medida por la entropía — **se degrada inevitablemente** en todo proceso real.
