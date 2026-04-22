(sec_brayton_cycle_ideal)=
## El ciclo de gas ideal: el ciclo Brayton

La presente lección se centra en los **ciclos de gas de potencia**, es decir, ciclos termodinámicos diseñados para proporcionar una potencia mecánica neta de salida y cuyo fluido de trabajo opera, íntegramente, en fase gaseosa. Aun cuando el análisis se restringe a las llamadas **turbomáquinas térmicas receptoras**, sigue siendo posible concebir una variedad significativa de ciclos de gas distintos. Entre ellos, los ciclos **Ericsson** y **Stirling** constituyen ejemplos teóricos clásicos.

Sin embargo, por razones que se harán evidentes a lo largo de esta sección, estos ciclos tienen una relevancia práctica limitada en sistemas de potencia y propulsión a gran escala. En su lugar, el **ciclo Brayton** emerge como el ciclo de gas paradigmático y constituye la base de las turbinas de gas modernas y de los motores aeronáuticos.

---

(subsec_brayton_components)=
### Componentes y procesos ideales del ciclo Brayton

El **ciclo Brayton ideal simple** consta de tres componentes principales:

- un **compresor**,  
- una **cámara de combustión**,  
- una **turbina**.

El fluido de trabajo circula de manera continua a través de estos dispositivos, y el ciclo se define en términos de cuatro procesos termodinámicos idealizados:

- **Proceso $1 \rightarrow 2$ (compresión):**  
  El flujo entra en el compresor en el estado $1$ y se comprime hasta alcanzar el estado $2$. En el caso ideal, este proceso es **isentrópico**.

- **Proceso $2 \rightarrow 3$ (adición de calor):**  
  En el estado $2$, el flujo entra en la cámara de combustión, donde su entalpía aumenta debido a una reacción química. Idealmente, la adición de calor ocurre a **presión constante**,
  llevando al fluido hasta el estado $3$.

- **Proceso $3 \rightarrow 4$ (expansión):**  
  El gas de alta entalpía se expande a través de la turbina, produciendo trabajo mecánico y alcanzando el estado $4$. Idealmente, esta expansión es **isentrópica**.

- **Proceso $4 \rightarrow 1$ (expulsión de calor):**  
  Para cerrar el ciclo, el calor se expulsa a **presión constante**, devolviendo el fluido de trabajo a su estado termodinámico inicial.

:::{important}

**CICLO BRAYTON IDEAL**

El ciclo Brayton ideal consta de dos procesos isentrópicos (compresión y expansión) y dos procesos isobáricos (adición y expulsión de calor). Cada componente puede analizarse de forma independiente como un sistema abierto en régimen permanente.

:::

---

(subsec_brayton_diagrams)=
### Los diagramas $p–v$ y $T–s$ del ciclo Brayton ideal

La estructura del ciclo Brayton queda claramente ilustrada en los diagramas $p-v$ y
$T-s$:

- En el **diagrama $p-v$**:
  - los procesos $2 \rightarrow 3$ y $4 \rightarrow 1$ aparecen como **líneas rectas horizontales** (isobáricos),
  - los procesos $1 \rightarrow 2$ y $3 \rightarrow 4$ aparecen como **líneas curvas** (isentrópicos).

- En el **diagrama $T-s$**:
  - los procesos $1 \rightarrow 2$ y $3 \rightarrow 4$ aparecen como **líneas rectas verticales** (isentrópicos),
  - los procesos $2 \rightarrow 3$ y $4 \rightarrow 1$ aparecen como **líneas curvas** (isobáricos).

Estas representaciones ponen de manifiesto la simetría fundamental del ciclo.

---

(subsec_brayton_efficiency)=
### Rendimiento térmico del ciclo Brayton ideal

Para evaluar el rendimiento térmico del ciclo Brayton ideal, se supone que las variaciones de energía cinética y potencial son despreciables. Aplicando la **$1^{\text{a}}$ ley de la termodinámica** en su forma específica, se obtiene:

(eq_first_law_brayton)=
$$
(q_{\text{in}} - q_{\text{out}}) + (w_{\text{in}} - w_{\text{out}}) = h_{\text{in}} - h_{\text{out}} .
$$

La evaluación de los cambios de entalpía requiere especificar el modelo adoptado para el fluido de trabajo. En las turbinas de gas, el fluido de trabajo es predominantemente aire, y los productos de la combustión no alteran significativamente sus propiedades termodinámicas. Esto motiva el uso del **modelo de aire estándar**, que supone que:

- el aire se comporta como un **gas ideal**,
- todos los procesos son **internamente reversibles**,
- los calores específicos se evalúan a $25 \ ^{\circ}\text{C}$ y se consideran constantes (la **hipótesis estándar de aire frío**).

:::{note}

**HIPÓTESIS ESTÁNDAR DE AIRE FRÍO**

Bajo esta hipótesis, el aire se trata como un *gas perfecto* con calores específicos constantes. Aunque aproximado, este modelo proporciona una visión cualitativa precisa y resultados cuantitativos razonables para muchas aplicaciones de ingeniería.

:::

Con estas hipótesis, las interacciones de calor son

(eq_brayton_qin)=
$$
q_{\text{in}} = h_3 - h_2 = c_p (T_3 - T_2),
$$

(eq_brayton_qout)=
$$
q_{\text{out}} = h_4 - h_1 = c_p (T_4 - T_1).
$$

El rendimiento térmico resulta

(eq_eta_brayton_general)=
$$
\eta_{\text{th,Brayton}} = 1 - \frac{q_{\text{out}}}{q_{\text{in}}} = 1 - \frac{T_4 - T_1}{T_3 - T_2}.
$$

Dado que los procesos $1 \rightarrow 2$ y $3 \rightarrow 4$ son isentrópicos y $p_2 = p_3$, $p_4 = p_1$, se sigue que:

(eq_brayton_isentropic_relations)=
$$
\frac{T_2}{T_1} = \left( \frac{p_2}{p_1} \right)^{\frac{\gamma - 1}{\gamma}} = \frac{T_3}{T_4}.
$$

Introduciendo la **relación de presiones**:

(eq_pressure_ratio)=
$$
r_p = \frac{p_2}{p_1},
$$

el rendimiento térmico del ciclo Brayton ideal resulta:

(eq_eta_brayton_final)=
$$
\eta_{\text{th,Brayton}} = 1 - \frac{1}{r_p^{(\gamma - 1)/\gamma}} .
$$

Esta expresión muestra que el rendimiento térmico aumenta tanto con la relación de presiones como con la relación de calores específicos.


:::{note}

**COMPROMISO ENTRE RENDIMIENTO TÉRMICO Y POTENCIA NETA DE SALIDA**

En las turbinas de gas reales, la temperatura máxima del ciclo se produce en la entrada de la turbina (estado $3$) y está limitada por la resistencia térmica de los álabes y de los materiales de la turbina. Para una temperatura de entrada a turbina fija, aumentar la relación de presiones incrementa inicialmente la potencia neta de salida, pero más allá de cierto punto la potencia neta empieza a disminuir.

Como resultado, el **máximo rendimiento térmico** y la **máxima potencia neta de salida** no se alcanzan para la misma relación de presiones, lo que conduce a un compromiso de diseño inevitable.

Un menor trabajo específico neto requiere un mayor caudal másico para alcanzar una determinada potencia de salida, lo cual puede ser económicamente indeseable. En ciclos Brayton reales, las
relaciones de presión típicas se sitúan en el intervalo $11 \le r_p \le 16$.

:::

:::{tip}

**EL PAPEL DEL AIRE EN LAS TURBINAS DE GAS**

En las turbinas de gas, el aire cumple dos funciones esenciales:

- proporciona el comburente necesario para la combustión del combustible,
- actúa como **medio de refrigeración** para mantener temperaturas admisibles en componentes críticos.

Para cumplir la segunda función, las turbinas de gas operan con relaciones másicas aire–combustible muy superiores a la estequiométrica, superando a menudo valores de 50. Esto justifica modelar los productos de la combustión como aire con un error mínimo.

Dado que el combustible se añade aguas abajo del compresor, el caudal másico a través de la turbina es ligeramente mayor que el que atraviesa el compresor. Suponer un caudal másico constante a lo largo de todo el ciclo constituye, por tanto, una aproximación conservadora.

:::

---

(subsec_back_work_ratio)=
### Relación de trabajo de retroceso

En los ciclos de potencia de gas, una fracción significativa del trabajo de la turbina es necesaria para accionar el compresor. La relación entre el trabajo del compresor y el trabajo de la turbina se conoce como **relación de trabajo de retroceso** (*back-work ratio*), y suele ser elevada en las turbinas de gas, acercándose con frecuencia al $50 \ \%$.

Bajas eficiencias isentrópicas en el compresor o en la turbina incrementan aún más esta relación.

Por el contrario, en las centrales de vapor la relación de trabajo de retroceso es mucho menor (típicamente $1–5 \ \%$), ya que comprimir un líquido requiere mucho menos trabajo que comprimir un gas.
Como consecuencia, para una misma potencia neta de salida, las turbinas de gas deben ser, en general, mayores que las turbinas de vapor.

---

(subsec_brayton_conceptual_closure)=
### Cierre conceptual

- El ciclo Brayton es el ciclo fundamental de potencia de gas.
- Consta de dos procesos isentrópicos y dos procesos isobáricos.
- Bajo la hipótesis estándar de aire frío, su rendimiento depende solo de la
  relación de presiones y de $\gamma$.
- Aumentar la relación de presiones mejora el rendimiento, pero no incrementa
  indefinidamente la potencia neta.
- El aire actúa tanto como reactivo como medio de refrigeración en las turbinas de gas.
- Las turbinas de gas presentan una elevada relación de trabajo de retroceso en comparación con las centrales de vapor.

