(sec_steam_cycles_intro)=
## Concibiendo un ciclo de vapor realizable

Hasta este punto, los ciclos de potencia discutidos (Brayton, Otto, Diesel) han sido **ciclos de potencia de gas**: el fluido de trabajo permanece en fase gaseosa durante todo el recorrido. En muchas situaciones prácticas, sin embargo, resulta ventajoso permitir que el fluido de trabajo **cambie de fase**, o que opere como una **mezcla bifásica** (líquido–vapor) durante parte del ciclo. Los ciclos de este tipo se conocen como **ciclos de potencia de vapor**.

El fluido de trabajo prototípico de un ciclo de vapor es el **agua/vapor**. Las razones no son estéticas; son razones de ingeniería:

- el agua es **económica** y ampliamente disponible,
- es segura y fácil de manejar a gran escala (en comparación con muchas alternativas),
- y posee un **alto calor latente de vaporización**, lo que permite grandes transferencias de energía a temperatura casi constante durante la ebullición y la condensación.

En la práctica, las centrales de ciclo de vapor suelen denominarse según su **fuente de calor** —carbón, nuclear, gas natural, solar térmica— porque el equipo encargado del aporte de calor varía. Sin embargo, desde el punto de vista del análisis termodinámico, el propio lazo de vapor suele seguir la **misma estructura cíclica básica** con independencia de cómo se suministre el calor. Por eso muchas centrales aparentemente distintas pueden estudiarse con las mismas herramientas conceptuales.

Entre todos los ciclos de potencia de vapor, la referencia más extendida y didáctica es el **ciclo Rankine**, que será el foco del presente tema. Otras configuraciones se mencionarán más adelante —como los **ciclos combinados**, el **ciclo Rankine orgánico (ORC)**, los **ciclos binarios** y la **cogeneración**—, pero el ciclo Rankine proporciona la base esencial.

:::{important}

**POR QUÉ IMPORTA EL CAMBIO DE FASE**

Permitir que el fluido de trabajo hierva y condense crea una poderosa palanca de diseño: el calor puede absorberse y rechazarse intercambiando grandes cantidades de energía a temperatura casi constante (durante el cambio de fase), lo cual puede ser beneficioso tanto desde el punto de vista de la eficiencia como para el diseño práctico de intercambiadores de calor.

:::

---

(subsec_steam_carnot)=
### El ciclo de Carnot de vapor: una idea natural que fracasa en la práctica

El **ciclo de Carnot** es, teóricamente, el ciclo más eficiente que opera entre dos focos térmicos a temperaturas $T_\mathrm{H}$ y $T_\mathrm{C}$. Por tanto, resulta tentador plantearse:

:::{epigraph}
Si Carnot es el ciclo más eficiente, ¿por qué no diseñar centrales de vapor que operen con un **ciclo de Carnot de vapor**?
:::

La respuesta es que, aunque un ciclo de Carnot de vapor puede **dibujarse** y **definirse** termodinámicamente, no constituye un modelo de ingeniería satisfactorio para centrales reales. Los obstáculos no son menores; son estructurales.

Para entender por qué, considérese un ciclo de Carnot de flujo estacionario que utilice agua/vapor como fluido de trabajo. La campana de saturación aparece de forma natural en los diagramas $T\!-\!s$ porque el cambio de fase se produce a lo largo de regiones extensas en los procesos reales del vapor.

Una posible implementación de Carnot (a menudo dibujada con el lazo intersectando la campana de saturación) es:

- **Proceso $1 \rightarrow 2$ (adición de calor isotérmica y reversible en un evaporador):**  
  El fluido de trabajo recibe calor a temperatura constante. En una región bifásica, esto puede lograrse manteniendo la presión constante, ya que la temperatura de saturación queda entonces fijada por la presión de saturación.

- **Proceso $2 \rightarrow 3$ (expansión isentrópica en una turbina):**  
  El fluido se expande de manera reversible y adiabática, produciendo trabajo.

- **Proceso $3 \rightarrow 4$ (rechazo de calor isotérmico y reversible en un condensador):**  
  Se rechaza calor a temperatura constante, de nuevo potencialmente realizable mediante condensación a presión constante en la región bifásica.

- **Proceso $4 \rightarrow 1$ (compresión isentrópica):**  
  El fluido de trabajo se comprime de manera reversible y adiabática de vuelta al estado inicial.

A primera vista, esto parece viable: existen evaporadores, turbinas, condensadores y compresores. Las dificultades aparecen en cuanto se intenta implementar los procesos requeridos con equipos reales y con el comportamiento real del fluido de trabajo.

---

(subsec_steam_carnot_difficulties)=
### Por qué el ciclo de Carnot de vapor no es un modelo de diseño práctico

* 1) **La transferencia de calor isotérmica limita severamente la temperatura máxima del ciclo**

        En la **región bifásica**, la transferencia de calor aproximadamente isotérmica no es difícil: si la presión se mantiene aproximadamente constante, la temperatura de saturación queda fijada, de modo que un evaporador o un condensador se aproxima de forma natural a un dispositivo isotermo.

        El problema es que restringir la adición de calor al cambio de fase vincula la temperatura máxima a la curva de saturación y, por tanto, limita cuánto puede elevarse $T_\mathrm{H}$ sin pasar a condiciones sobrecalentadas o supercríticas. Para el agua, la temperatura crítica es relativamente modesta (alrededor de $374^\circ\mathrm{C}$), de modo que la temperatura máxima accesible dentro de un proceso de adición de calor isotérmico en la región bifásica queda fundamentalmente acotada.

        Intentar elevar la temperatura máxima exige entonces añadir calor en una **región monofásica** (vapor sobrecalentado o líquido comprimido). Pero en una región monofásica, la presión constante *no* impone temperatura constante; lograr una transferencia de calor verdaderamente isotérmica se vuelve mucho más difícil y, en general, incompatible con intercambiadores de calor compactos y eficientes y con diferencias de temperatura realistas.

        :::{note}

        **LA CONTRAPARTIDA FUNDAMENTAL**

        La exigencia de Carnot (transferencia de calor estrictamente isotérmica) es fácil de aproximar durante la ebullición/condensación bifásica,
        pero la operación bifásica restringe $T_\mathrm{H}$ y, por tanto, restringe la eficiencia potencial.

        :::

* 2) **La expansión en la turbina lleva al vapor a condiciones húmedas (riesgo de erosión de álabes)**

        Una turbina bien diseñada puede aproximar razonablemente una expansión isentrópica. Pero para agua/vapor, la expansión isentrópica desde una condición de entrada saturada o ligeramente sobrecalentada suele penetrar en la **región bifásica**, reduciendo la **calidad del vapor** (aumentando el contenido de humedad).

        El vapor húmedo constituye un problema importante desde el punto de vista mecánico y de fiabilidad:

        - las gotas impactan sobre los álabes de la turbina,
        - lo que conduce a erosión y degradación del rendimiento,
        - e impone límites prácticos a la calidad admisible a la salida.

        En la práctica, los diseñadores suelen tratar de mantener la calidad del vapor a la salida de la turbina por encima de un cierto umbral (orden de magnitud habitualmente citado: por encima de aproximadamente 0.9) para reducir el daño asociado a la humedad.

        Esto no es una simple molestia; modifica la región factible de operación del ciclo. La humedad puede mitigarse mediante sobrecalentamiento, recalentamiento o eligiendo un fluido de trabajo diferente con características de saturación más favorables (una motivación que se vuelve importante en contextos ORC).

        :::{warning}

        **LA HUMEDAD NO ES UN DETALLE MENOR**

        Un diagrama termodinámico puede tolerar vapor de baja calidad. Los álabes de una turbina, no.
        Las restricciones de calidad del vapor constituyen una frontera de ingeniería dura que condiciona el diseño real de los ciclos de vapor.

        :::

* 3) **La compresión isentrópica de una mezcla bifásica no es una tarea realista para un componente**

        En muchos esquemas del Carnot de vapor, el proceso de compresión $4 \rightarrow 1$ implica comprimir una **mezcla bifásica** hasta alcanzar líquido saturado (u otro estado objetivo). Surgen dos problemas principales:

        - **Problema de control del estado:**  
          El condensador debe finalizar exactamente con la calidad requerida en el estado 4. En condensadores reales, alcanzar y controlar con precisión un estado bifásico de salida, especialmente bajo carga variable, no es algo sencillo.

        - **Problema de viabilidad del equipo:**  
          Los compresores no están diseñados para manejar mezclas bifásicas significativas. Comprimir una mezcla de líquido y vapor es mecánicamente problemático e ineficiente, y puede causar una severa inestabilidad operativa.

        Esta dificultad es una de las razones más decisivas por las que el ciclo de Carnot de vapor no se utiliza como plantilla práctica.

---

(subsec_steam_carnot_alternative)=
### Las disposiciones alternativas de Carnot no resuelven los problemas de fondo

Es posible reorganizar el lazo de Carnot (por ejemplo, intentando evitar ciertas operaciones bifásicas en un componente). Tales disposiciones alternativas pueden eliminar una dificultad, pero introducen otras, tales como:

- compresión hasta presiones extremadamente elevadas,
- requisitos de transferencia de calor isotérmica bajo presiones variables,
- u otras combinaciones de tareas de los componentes poco compatibles con máquinas reales.

La conclusión es que el ciclo de Carnot de vapor no constituye un modelo sólido ni realista para diseñar centrales con la tecnología hidro-termo-mecánica actual.

:::{important}

**QUÉ APRENDEMOS DE ESTE IMPRACTICABILIDAD CONCEPTUAL**

Carnot proporciona una referencia teórica y una orientación sobre “qué favorece la eficiencia” (aumentar $T_\mathrm{H}$, disminuir $T_\mathrm{C}$),
pero las plantas reales de vapor deben construirse en torno a procesos compatibles con componentes reales.
Precisamente por eso el ciclo Rankine —y no Carnot— se convierte en el ciclo de potencia de vapor canónico.

:::

---

### Hacia el ciclo Rankine ideal

Las deficiencias fundamentales del ciclo de Carnot de vapor sugieren una estrategia de diseño clara:  
en lugar de forzar al ciclo a obedecer procesos *termodinámicamente perfectos* pero *mecánicamente hostiles*, conviene construirlo en torno a **procesos que los componentes reales puedan ejecutar de manera eficiente y fiable**.

Esta es precisamente la lógica que hay detrás del **ciclo Rankine**.

Al **condensar completamente el fluido de trabajo hasta líquido saturado antes de la compresión** y al **permitir la adición de calor a presión constante a lo largo de un amplio intervalo de temperaturas**, el ciclo Rankine elimina las características más problemáticas del ciclo de Carnot de vapor, conservando al mismo tiempo su propósito esencial: la conversión de energía térmica en trabajo mecánico.

El **ciclo Rankine ideal** se define, por tanto, como un ciclo de potencia de vapor internamente reversible compuesto por cuatro procesos compatibles con componentes reales:

- **Proceso $1 \rightarrow 2$ — Compresión isentrópica (bomba):**  
  El agua líquida saturada se presuriza hasta la presión de caldera mediante una bomba.

- **Proceso $2 \rightarrow 3$ — Adición de calor a presión constante (generador de vapor):**  
  Se añade calor a presión constante, elevando primero la temperatura del líquido, luego vaporizándolo y, con frecuencia, sobrecalentando además el vapor.

- **Proceso $3 \rightarrow 4$ — Expansión isentrópica (turbina):**  
  El vapor sobrecalentado (o seco) se expande a través de una turbina, produciendo trabajo mecánico útil.

- **Proceso $4 \rightarrow 1$ — Rechazo de calor a presión constante (condensador):**  
  Se rechaza calor a presión constante, condensando completamente el vapor de nuevo hasta líquido saturado.

El equipo asociado —la **bomba**, el **generador de vapor**, la **turbina** y el **condensador**— se corresponde de manera directa e inequívoca con estos procesos termodinámicos. Esta correspondencia uno a uno entre proceso y componente es una de las principales fortalezas del ciclo Rankine como modelo de ingeniería.

El fluido de trabajo entra en la bomba en el estado 1 como **líquido saturado**. Como los líquidos son solo débilmente compresibles, el volumen específico cambia muy poco durante la compresión. Como resultado, el **trabajo de la bomba es pequeño** en comparación con el trabajo de la turbina, una ventaja crucial frente a los ciclos de gas. Aunque el agua suele modelarse como incompresible, en realidad se produce una ligera disminución del volumen específico, acompañada de un pequeño aumento de temperatura. Por tanto, el efecto principal de la bomba es un aumento de la **presión**, desplazando el fluido a una isóbara superior que fija las condiciones de saturación y sobrecalentamiento en la caldera.

En el estado 2, el fluido entra en el generador de vapor como **líquido subenfriado**. El calor se transfiere a presión constante hasta que el fluido se vaporiza y normalmente se **sobrecalienta** hasta el estado 3. Esta adición de calor se produce a lo largo de un amplio intervalo de temperaturas, lo cual se adapta bien a fuentes reales de calor, como gases de combustión o combustible nuclear. El evaporador y el sobrecalentador constituyen conjuntamente el **generador de vapor**, un elemento clave de las centrales de vapor.

Desde el estado 3, el vapor se expande isentrópicamente a través de la turbina, produciendo trabajo mecánico que normalmente se convierte en potencia eléctrica mediante un generador. Durante esta expansión, la presión y la temperatura disminuyen. El escape de la turbina en el estado 4 suele situarse en la **región bifásica**, pero con una calidad de vapor suficientemente alta para evitar una erosión excesiva de los álabes. El vapor de escape entra entonces en el condensador.

En el condensador, se rechaza calor a presión constante hacia un foco frío externo, condensando completamente el vapor hasta líquido saturado en el estado 1 y cerrando así el ciclo. La condensación a temperatura casi constante permite un rechazo de calor eficiente y una operación estable. Dependiendo de las restricciones del emplazamiento, los condensadores pueden estar refrigerados por agua o por aire.

En el diagrama $T$–$s$, el **área bajo el proceso $2 \rightarrow 3$** representa el calor suministrado al ciclo, mientras que el **área bajo el proceso $4 \rightarrow 1$** representa el calor rechazado. El área encerrada por el ciclo corresponde al **trabajo neto de salida**, en concordancia con la primera ley de la termodinámica.

---

### Propiedades de las sustancias puras en los ciclos de vapor

A diferencia de los ciclos de potencia de gas, los ciclos de potencia de vapor operan con **sustancias puras**, no con gases ideales. En la mayoría de los ciclos de vapor de interés ingenieril, el fluido de trabajo es agua.

Dentro de la campana de saturación, donde coexisten líquido y vapor, el estado termodinámico se describe mediante la **calidad** (o **título de vapor**) $x$, definida como la razón entre la masa de vapor y la masa total. Una calidad $x = 0$ corresponde a líquido saturado, mientras que $x = 1$ corresponde a vapor saturado. Para valores intermedios, las propiedades termodinámicas se obtienen mediante la **regla de la palanca**, siempre que se conozca la presión o la temperatura de saturación.

Fuera de la región bifásica, se aplican las relaciones usuales de propiedades monofásicas. Para estados de líquido comprimido (subenfriado), es habitual —y normalmente preciso— aproximar la mayoría de las propiedades intensivas por las del líquido saturado a la misma temperatura. La entalpía es la principal excepción, ya que los efectos de la presión deben tenerse en cuenta explícitamente.

Comprender estas relaciones de propiedades es esencial para analizar correctamente los ciclos Rankine, ya que el fluido de trabajo atraviesa de forma rutinaria regiones líquidas, bifásicas y de vapor durante su operación.

---

### Ciclos abiertos de vapor y perspectiva histórica

El ciclo Rankine no fue el primer ciclo de potencia basado en vapor. Las primeras máquinas de vapor prácticas, desarrolladas por **James Watt**, son anteriores al desarrollo formal de la termodinámica y operan como **ciclos de vapor abiertos o semicerrados**.

En una máquina clásica de Watt, el vapor producido en una caldera entra en un cilindro y se expande, empujando un pistón. El movimiento lineal del pistón se transmite, a través de una biela, a una rueda giratoria. Tras la expansión, el vapor se descarga y se condensa, a menudo mediante un condensador separado, antes de devolverse como agua líquida a la caldera. Los mecanismos de válvulas controlan la admisión y el escape del vapor, permitiendo ciclos repetidos de funcionamiento.

Existen numerosas variantes de las primeras máquinas de vapor, como la **máquina de cilindro oscilante**, en la que el vapor se admite a través de puertos sincronizados con el movimiento del pistón. Aunque mecánicamente simples e ineficientes según los estándares modernos, estas máquinas encarnan el mismo principio fundamental que las turbinas de vapor modernas: **la conversión de la energía térmica transportada por el vapor en trabajo mecánico**.

El ciclo Rankine puede verse, por tanto, como la idealización termodinámica y el refinamiento de estos conceptos tempranos, adaptados a operación en flujo estacionario y a generación de potencia a gran escala.

---

(subsec_steam_conceptual_closure)=
### Cierre conceptual

- Los ciclos de potencia de vapor se diferencian fundamentalmente de los ciclos de potencia de gas en que permiten el **cambio de fase** del fluido de trabajo.
- El ciclo de Carnot proporciona una referencia teórica de eficiencia, pero fracasa como modelo práctico de ciclo de vapor debido a la inviabilidad de sus componentes.
- El ciclo Rankine sustituye la transferencia de calor isotérmica y la compresión bifásica por **procesos compatibles con componentes reales**.
- La compresión del líquido requiere poco trabajo, lo que hace a los ciclos de vapor especialmente atractivos para la generación de potencia a gran escala.
- El comportamiento con cambio de fase y la calidad del vapor desempeñan un papel central en el análisis de ciclos de vapor.
- El ciclo Rankine constituye la base conceptual y práctica de las centrales modernas de potencia de vapor, desde plantas de carbón y nucleares hasta sistemas avanzados de ciclo combinado.

