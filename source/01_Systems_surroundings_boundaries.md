(sec_systems_surroundings_boundaries)=
## Sistemas, entorno y límites

La termodinámica comienza definiendo **qué** estamos estudiando y **cómo** lo separamos del resto del universo.
Esta sección establece el lenguaje fundamental para esa tarea: **sistemas**, sus **límites** y el **entorno** que interactúa con ellos.
Aprenderemos a clasificar los sistemas según los intercambios que ocurren a través de sus límites,
y cómo las propiedades del límite determinan el tipo de interacción termodinámica posible: masa, calor o trabajo.

---

(subsec_defining_the_system)=
### Definición del sistema

El análisis termodinámico siempre comienza decidiendo qué parte del mundo físico queremos estudiar. Esta porción se llama **sistema**, y es el objeto central del razonamiento termodinámico.

Para realizar un análisis termodinámico, el primer paso es decidir **qué es realmente el sistema**. Un **sistema** es cualquier región definida del espacio o cantidad de materia que aislamos —física o conceptualmente— para estudiar cómo se comporta bajo ciertas condiciones. Esta elección depende totalmente de la pregunta que queremos responder.

* Si queremos saber **cómo cambia la temperatura de un aula** durante una clase, el sistema es **el aire contenido en la sala**.
* Si queremos saber **cómo enfría un congelador**, el sistema es **el aire o el refrigerante dentro del compartimento del congelador**.
* Si queremos determinar **la potencia producida por un motor de combustión**, el sistema es **la mezcla de aire y combustible dentro del conjunto pistón–cilindro**.
* Si queremos estudiar **cómo se calienta un bloque de acero** dentro de un horno, el sistema es **la pieza de acero en sí**.

Estos ejemplos muestran que lo que importa no es **de qué está hecho el sistema**, sino **por qué lo estamos analizando**.
La definición de “sistema” es tanto **funcional** como **operativa**, no intrínseca: lo elegimos según el propósito del análisis.

---

(subsec_boundaries_and_environment)=
### Límites y entorno

Una vez definido el sistema, lo rodeamos conceptualmente con una **superficie imaginaria** que lo separa de todo lo demás. Todo lo externo al sistema se llama **entorno**, y la superficie que los separa se llama **límite**. Este límite determina qué puede o no atravesar entre el sistema y su entorno.

* Para el aire en una habitación → **paredes, ventanas y objetos** internos forman el límite.
* Para el congelador → la **caja aislada y la puerta** actúan como límite.
* Para el sistema pistón–cilindro → **paredes metálicas y la cara móvil del pistón** son el límite.
* Para la pieza de acero → la **superficie externa** del metal es el límite.

Todo lo que está fuera de esa superficie es el **entorno**.
La combinación del sistema y su entorno se conoce como el **universo termodinámico** — el dominio completo involucrado en un proceso.

:::{note}
**LOS LÍMITES PUEDEN SER REALES O IMAGINARIOS**

Un límite no tiene que ser una superficie tangible. Puede ser puramente conceptual — una división abstracta que nos ayuda a seguir lo que cruza entre el sistema y su entorno.
La termodinámica funciona precisamente porque tal separación siempre puede definirse.
:::

---

(subsec_the_role_of_interactions)=
### El papel de las interacciones

La termodinámica se centra en **los cambios que ocurren dentro de un sistema** — cambios en temperatura, presión, volumen o energía interna.
Pero esos cambios existen **solo** debido a interacciones con el entorno.
La energía y, en algunos casos, la materia atraviesan el límite y provocan transformaciones internas.
Podemos pensar en el sistema termodinámico como una **caja negra**:
no nos preocupamos por cada evento microscópico interno, solo por las **entradas** y **salidas** que cruzan el límite.

* No necesitamos conocer los mecanismos detallados del movimiento molecular.
* Solo necesitamos cuantificar lo que **entra y sale** como calor, trabajo o masa.
* Observando esos intercambios, podemos inferir la evolución interna del sistema.

:::{tip}
**TRATA EL SISTEMA COMO UNA “CAJA NEGRA”**

Al centrarse en las interacciones en el límite — no en los mecanismos internos — la termodinámica puede analizar sistemas extremadamente complejos (reactores, turbinas, células biológicas) usando las mismas leyes universales.
Si puedes identificar lo que cruza el límite, puedes aplicar la termodinámica.
:::

---

(subsec_simplifications_and_the_macroscopic_conception)=
### Simplificaciones y la concepción macroscópica

Como nuestro objetivo es comprender y modelar sistemas de ingeniería, introducimos varias **simplificaciones** que hacen el análisis manejable y significativo:

1. **Fluidos típicos:**
   Usaremos **aire y agua** como fluidos estándar que representan gases y líquidos, respectivamente.
   Son paradigmáticos en sistemas energéticos y cubren la mayoría de aplicaciones prácticas.

2. **Efectos excluidos:**
   Despreciamos fenómenos fuera del dominio mecánico o térmico — como efectos reológicos (viscosos dependientes del tiempo), eléctricos, magnéticos o reacciones químicas — salvo que se indique explícitamente.

3. **Punto de vista macroscópico:**
   Nuestro enfoque será la **termodinámica clásica o fenomenológica**:
   nos interesa el comportamiento **promedio** o **global** de los sistemas, no sus detalles atómicos.
   Esto contrasta con la **concepción microscópica**, usada en la **termodinámica estadística**, que explica las mismas leyes en términos del comportamiento molecular.

:::{important}
**ENFOQUES CLÁSICO VS. MICROSCÓPICO**

La termodinámica clásica describe el **comportamiento macroscópico** usando propiedades medibles (presión, temperatura, volumen, etc.) sin referirse a la estructura microscópica de la materia.
La termodinámica estadística explica **por qué** emergen esas leyes macroscópicas.
:::

---

(subsec_types_of_systems)=
### Tipos de sistemas

Según lo que el límite permite atravesar, clasificamos los sistemas como **aislados**, **cerrados** o **abiertos**.
Esta clasificación refleja qué tipos de interacciones — energía y/o masa — son posibles con el entorno.

1. **Sistema aislado**
   * No intercambia **ni masa ni energía** con el entorno.
   * El límite es **impermeable** (sin flujo de masa), **rígido** (sin trabajo) y **adiabático** (sin calor).
   * Es una **idealización** — en la práctica, ningún sistema está perfectamente aislado, aunque un termo Dewar es una aproximación cercana.

2. **Sistema cerrado** (masa de control)
   * Intercambia **energía** (calor y/o trabajo) pero **no masa** con el entorno.
   * Al menos una parte del límite permite interacción térmica o mecánica.
   * Ejemplo: un conjunto pistón–cilindro.

3. **Sistema abierto** (volumen de control)
   * Intercambia **energía y masa** con el entorno.
   * Los límites pueden ser **flexibles**, **diatérmicos** o **permeables**, según el proceso específico.
   * Ejemplo: una corriente de fluido en una tubería, un compresor o una turbina.

::::{important}
**CLASIFICACIÓN SEGÚN INTERACCIÓN EN EL LÍMITE**

La diferencia esencial radica en lo que puede cruzar el límite. Podemos llamar $E_{\text{sys.}}$ a la energía total del sistema y $m_{\text{sys.}}$ a la masa contenida en él. Sus variaciones se representan con el símbolo $\Delta$, es decir, $\Delta E_{\text{sys.}}$ y $\Delta m_{\text{sys.}}$. Los diferentes tipos de límites están condicionados por distintos modos de interacción:

* **Aislado:** sin energía, sin masa $\rightarrow \Delta E_{\text{sys.}} = 0$, $\Delta m_{\text{sys.}} = 0$
* **Cerrado:** solo energía $\rightarrow \Delta E_{\text{sys.}} \neq 0$, $\Delta m_{\text{sys.}} = 0$
* **Abierto:** energía y masa $\rightarrow \Delta E_{\text{sys.}} \neq 0$, $\Delta m_{\text{sys.}} \neq 0$

Resumen en forma tabular:

| **Tipo de sistema** | $\Delta E_{\text{sys.}}$ | $\Delta m_{\text{sys.}}$ |
| :------------------- | :-------------------------: | :-------------------------: |
| **Aislado** | $= 0$ | $= 0$ |
| **Cerrado** | $\neq 0$ | $= 0$ |
| **Abierto** | $\neq 0$ | $\neq 0$ |

La figura siguiente muestra los tipos de límites de manera ilustrativa, atendiendo a los tipos de interacción con el entorno.

:::{figure} 1_fundamentals_figs/system_boundary_types.svg
:name: fig-system-boundaries
:width: 90%
:align: center
Clasificación genérica de sistemas según las restricciones de intercambio impuestas por los límites.
:::
::::

---

(subsec_terminology_of_boundary_behavior)=
### Terminología del comportamiento del límite

Para describir la naturaleza física de los límites con mayor precisión, la termodinámica utiliza una terminología simple y sistemática:

| Interacción | Límite que **la impide** | Límite que **la permite** |
| ----------- | ------------------------- | -------------------------- |
| **Masa**    | Impermeable              | Permeable |
| **Calor**   | Adiabático               | Diatérmico |
| **Trabajo** | Rígido                   | Flexible |

:::{note}
**SIGNIFICADO DE LOS DESCRIPTORES DEL LÍMITE**

Cada término describe **cómo se comporta el límite** respecto a un modo específico de interacción.
Por ejemplo, una pared **rígida, adiabática, impermeable** define un sistema **aislado** ideal.
Por el contrario, un límite **flexible, diatérmico, permeable** define el caso más general — y más realista — el de un **sistema abierto**.
Con las nociones desarrolladas hasta ahora, podemos concebir una tabla combinada que establezca las relaciones entre los tipos conceptuales de límites y las realizaciones físicas que permiten o restringen.

| **Tipo de sistema** | $\Delta E_{\text{sys.}}$ | $\Delta m_{\text{sys.}}$ | **Límite — Masa** | **Límite — Calor** | **Límite — Trabajo** |
| :------------------- | :-------------------------: | :-------------------------: | :----------------: | :-----------------: | :----------------: |
| **Aislado** | $= 0$ | $= 0$ | Impermeable | Adiabático | Rígido |
| **Cerrado** | $\neq 0$ | $= 0$ | Impermeable | Diatérmico o Adiabático | Flexible o Rígido |
| **Abierto** | $\neq 0$ | $\neq 0$ | Permeable | Diatérmico o Adiabático | Flexible o Rígido |
:::

---

(subsec_fluid_systems_and_the_coninuum_hypothesis)=
### Sistemas de fluidos y la hipótesis del continuo

Aunque la termodinámica se aplica a sólidos, líquidos y gases, la práctica ingenieril se concentra en **fluidos**, porque son los medios de trabajo en casi todos los sistemas energéticos — turbinas, compresores, motores, bombas, condensadores e intercambiadores de calor.
Para estos análisis, adoptamos la **hipótesis del continuo**:
suponemos que un fluido puede tratarse como un medio continuo en el que propiedades como densidad, presión y temperatura varían suavemente en el espacio y el tiempo.
Matemáticamente, consideramos que dentro de un volumen representativo pequeño, lo bastante grande para contener muchas moléculas pero pequeño comparado con el sistema completo,

$$
\rho(\mathbf{x}) ; T(\mathbf{x}) ; P(\mathbf{x})
$$

son funciones continuas bien definidas.

:::{tip}
**LA HIPÓTESIS DEL CONTINUO COMO PUENTE**

La aproximación del continuo es lo que vincula la termodinámica con la mecánica de fluidos.
Permite definir campos macroscópicos, aplicar relaciones diferenciales y tratar gases y líquidos reales como medios continuos que obedecen los mismos principios de conservación.
:::

---

(subsec_systems_surroundings_boundaries_conceptual_closure)=
### Cierre conceptual

Los elementos básicos del análisis termodinámico ya están establecidos:

* El **sistema**, la porción del universo bajo estudio.
* El **límite**, que puede ser físico o imaginario.
* El **entorno**, todo lo demás capaz de interactuar con el sistema.
* Los **tipos de sistema**, definidos por los intercambios (energía, masa) posibles.
* Las **simplificaciones** que centran nuestro estudio en fenómenos mecánicos y térmicos, principalmente en **sistemas de fluidos** tratados como **medios continuos**.

:::{important}
**ESENCIA DEL ENFOQUE MACROSCÓPICO**

La termodinámica clásica no intenta describir mecanismos atómicos.
Estudia cómo los sistemas intercambian energía y materia con su entorno y cómo esos intercambios determinan el estado macroscópico del sistema — temperatura, presión, volumen y contenido energético.
:::

