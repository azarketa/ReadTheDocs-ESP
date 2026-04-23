(sec_refrigeration_cycles_COP_clausius)=
## Ciclos de refrigeración, COP y el postulado de Clausius

La **$2^{\text{a}}$ ley** muestra que los **motores térmicos** solo pueden convertir en trabajo una parte del calor que reciben, rechazando el resto hacia un foco más frío.
Si este principio se **invierte**, obtenemos dispositivos que utilizan trabajo externo para forzar que el calor fluya *en contra* de su dirección natural — es decir, de una región más fría hacia una más caliente.
Tales **sistemas de refrigeración** y **bombas de calor** representan la operación complementaria de los motores térmicos: no producen trabajo a partir de calor, sino que **consumen trabajo** para inducir una transferencia de calor no espontánea.

---

(subsec_refrigeration_cycles_definition)=
### Ciclos de refrigeración y bombas de calor

Un **ciclo de motor térmico invertido** constituye la base tanto de los refrigeradores como de las bombas de calor.
Su funcionamiento puede resumirse del siguiente modo:

1. **Extracción de calor:** el dispositivo absorbe calor $Q_L$ desde una **región a baja temperatura**.
2. **Aporte de trabajo:** se suministra un trabajo externo $W_{\text{neto,in}}$ (mediante un compresor o motor).
3. **Rechazo de calor:** el dispositivo expulsa calor $Q_H$ hacia una **región a alta temperatura**.
4. **Operación cíclica:** el fluido de trabajo regresa a su estado inicial al final de cada ciclo.

La diferencia entre ambos dispositivos radica únicamente en su propósito:

* un **refrigerador** extrae calor de un espacio a baja temperatura,
* una **bomba de calor** entrega calor a un espacio cálido.

:::{important}

**OPERACIÓN EN DIRECCIÓN INVERSA**

Mientras un **motor térmico** convierte parte del flujo natural de calor (caliente → frío) en trabajo,
un **motor térmico invertido** consume trabajo para hacer que el calor fluya en dirección **frío → caliente**.
Esta constituye la diferencia esencial entre ambas clases de dispositivos cíclicos.

:::

---

(subsec_COP_definition)=
### Coeficiente de operación (COP)

El coeficiente de operación (COP, del inglés ***Coefficient Of Performance***) desempeña para los dispositivos de refrigeración el mismo papel conceptual que el **rendimiento** para los motores térmicos: mide la razón entre el **efecto útil obtenido** y la **energía requerida** para lograrlo.

Sin embargo, mientras un motor térmico produce trabajo y su salida útil es el *trabajo neto entregado* $(W_{\text{neto,out}})$, un **dispositivo invertido** (refrigerador o bomba de calor) **consume** trabajo. En motores térmicos pueden producirse múltiples interacciones de trabajo a lo largo del ciclo, de modo que el **trabajo neto** representa el balance global. En ciclos invertidos suele haber un **único trabajo dominante** (el del compresor), que se denota simplemente como $W_{\text{in}}$.

* **Ciclo de refrigeración:**

    Para un **refrigerador**, el efecto útil es el **calor absorbido** de la región fría $(Q_L)$. A partir del **balance energético** de un ciclo invertido y tratando todos los términos como valores positivos:

    (eq_energy_balance_reversed_cycle)=
    $$
    Q_H = Q_L + W_{\text{in}},
    \qquad \text{de modo que} \qquad W_{\text{in}} = Q_H - Q_L.
    $$

    Por definición:

    (eq_COP_refrigerator)=
    $$
    \text{COP}_{\text{R}} = \frac{Q_L}{W_{\text{in}}} = \frac{Q_L}{Q_H - Q_L} \implies \boxed{\text{COP}_{\text{R}} = \frac{1}{Q_H/Q_L - 1}} \ .
    $$

* **Ciclo de bomba de calor:**

    Para una **bomba de calor**, el efecto útil es el **calor entregado** a la región caliente $(Q_H)$. Siguiendo el mismo razonamiento:

    (eq_COP_heatpump)=
    $$
    \text{COP}_{\text{HP}} = \frac{Q_H}{W_{\text{in}}} = \frac{Q_H}{Q_H - Q_L} \implies \boxed{\text{COP}_{\text{HP}} = \frac{1}{1 - Q_L/Q_H}} \ .
    $$

Ambos valores de $\text{COP}$ están relacionados:

$$
\text{COP}_{\text{HP}}=\frac{Q_H}{Q_H-Q_L} = \frac{Q_L}{Q_H-Q_L} + 1 = \text{COP}_{\text{R}} + 1 \implies \boxed{\text{COP}_{\text{HP}} = \text{COP}_{\text{R}} + 1} \ .
$$

:::{important}

**INTERPRETACIÓN FÍSICA DE LOS VALORES DE COP**

El **coeficiente de operación** sigue la *misma lógica conceptual* que el **rendimiento**: ambos expresan la **razón entre lo que se obtiene y lo que cuesta** obtenerlo. En el caso del $\text{COP}$, esta razón indica cuánta transferencia de calor se logra por unidad de trabajo suministrado:

* $\text{COP} > 1$ — la **condición habitual** en dispositivos reales.  
  Significa que cada unidad de trabajo suministrado permite transferir *más de una unidad* de calor entre los focos. Por ejemplo, $\text{COP}_{\text{R}} = 4$ implica que $1$ unidad de trabajo eléctrico remueve cuatro unidades de calor del espacio frío.

* $\text{COP} = 1$ — caso límite en el que el sistema simplemente **convierte trabajo en una cantidad equivalente de transferencia de calor**; deja de ser ventajoso.

* $\text{COP} < 1$ — indica un proceso **ineficiente o defectuoso**, donde se consume más trabajo que el calor que se transfiere; el dispositivo no sería práctico como refrigerador o bomba de calor.

A diferencia del rendimiento de los motores térmicos (limitado por 1), el $\text{COP}$ puede superar la unidad porque los sistemas de refrigeración y bombas de calor **no crean energía** — **la redistribuyen**, usando el trabajo mecánico para forzar una transferencia de calor.

:::

---

(subsec_clausius_postulate)=
### El postulado de Clausius

Los ciclos de refrigeración se basan en **forzar que el calor se desplace del frío al caliente**, un proceso que solo puede ocurrir si se suministra **trabajo externo**.
Esta restricción queda expresada en el **postulado de Clausius**, la formulación complementaria de la **$2^{\text{a}}$ ley**:

:::{epigraph}
**Ningún proceso cíclico puede transferir calor de un cuerpo más frío a uno más caliente sin consumir trabajo externo.**
:::

El postulado de Clausius expresa la misma limitación física que la formulación de **Kelvin–Planck**, pero desde la perspectiva opuesta:
esta última prohíbe la conversión total de calor en trabajo, mientras que la primera prohíbe la transferencia espontánea de calor del frío al caliente.

---

(subsec_complementarity_postulates)=
### Complementariedad de ambos postulados

Las formulaciones de **Kelvin–Planck** y **Clausius** describen la misma restricción fundamental sobre los procesos cíclicos: una se refiere a la **producción de trabajo** y la otra a la **transferencia de calor**.
Su equivalencia puede demostrarse mediante el razonamiento siguiente.

Supongamos un **motor térmico** capaz de violar el postulado de Kelvin–Planck, convirtiendo todo el calor absorbido $Q_H$ íntegramente en trabajo $(Q_L = 0)$.
Si este trabajo alimenta un **ciclo de refrigeración** operando entre los mismos dos focos, dicho ciclo absorbería $Q_L$ del foco frío y expulsaría $Q_H + Q_L$ al foco caliente.
El efecto global sería una **transferencia neta de $Q_L$ del frío al caliente sin aporte de trabajo externo** — una violación directa del **postulado de Clausius**. El argumento inverso conduce a la misma conclusión, demostrando que ambos postulados son **lógicamente equivalentes** e imponen restricciones idénticas a los ciclos termodinámicos.

:::{important}

**RESUMEN DE LA COMPLEMENTARIEDAD DE LOS POSTULADOS**

| **Aspecto**                | **Kelvin–Planck (Motores térmicos)**         | **Clausius (Refrigeradores / Bombas de calor)**                                            |
| :------------------------ | :-------------------------------------------- | :------------------------------------------------------------------------------------------ |
| **Tipo de ciclo**         | Directo (produce trabajo)                     | Invertido (consume trabajo)                                                                 |
| **Flujo de calor**        | Natural: caliente → frío                      | Forzado: frío → caliente                                                                    |
| **Interacción de trabajo**| Salida $(W_{\text{neto,out}})$                | Entrada $(W_{\text{in}})$                                                                   |
| **Medida de desempeño**   | $\eta_{\text{th.}} = W_{\text{neto,out}}/Q_H = 1 - Q_L/Q_H$             | $\text{COP}_{\text{R}} = Q_L/W_{\text{in}}$, $\text{COP}_{\text{HP}} = Q_H/W_{\text{in}}$   |
| **Limitación**            | Imposible conversión total **calor → trabajo**    | Imposible transferencia **frío → caliente** sin trabajo                                         |
| **Requisito energético**  | Parte del calor debe rechazarse               | Debe suministrarse trabajo externo                                                          |
| **Significado físico**    | Direccionalidad de la degradación energética  | Direccionalidad de la recuperación energética                                               |

:::

Ambos postulados expresan una misma verdad: **ningún proceso cíclico puede ocurrir sin un coste energético**.
En los motores térmicos, este coste es el **rechazo inevitable de calor**; en los ciclos de refrigeración, es el **trabajo requerido** para invertir el flujo de calor.
Juntos revelan una **asimetría inherente en las transformaciones energéticas**: el trabajo puede degradarse siempre en calor, pero invertir esa transformación requiere compensación.

Esta equivalencia prepara el terreno para la siguiente pregunta fundamental:

:::{epigraph}
**¿Cuál es el máximo rendimiento que puede alcanzar un ciclo termodinámico sin violar la $2^{\text{a}}$ ley?**
:::

Responderla exige distinguir entre procesos **reversibles** e **irreversibles**.

---

(subsec_conceptual_closure_refrigeration)=
### Cierre conceptual

* Los **refrigeradores** y **bombas de calor** son motores térmicos invertidos que emplean trabajo para desplazar calor *en contra* de su dirección natural.
* Su desempeño se mide mediante el **coeficiente de operación (COP)** — el calor útil transferido por unidad de trabajo suministrado.
* El **postulado de Clausius** establece que dicho desplazamiento invertido no puede ocurrir espontáneamente.
* Las formulaciones de **Kelvin–Planck** y **Clausius** son expresiones complementarias de la misma restricción impuesta por la **$2^{\text{a}}$ ley**.
* En conjunto, definen la **direccionalidad y los límites** de todas las transformaciones cíclicas de energía: todo proceso tiene un coste energético, y la conversión perfecta es físicamente inalcanzable.
