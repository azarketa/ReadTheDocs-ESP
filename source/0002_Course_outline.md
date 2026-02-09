(sec_course_outline)=
# Programa del curso

El curso se desarrolla de forma progresiva: desde los **fundamentos del razonamiento termodinámico** hasta el **análisis de ciclos térmicos canónicos** que sustentan los sistemas reales de conversión de energía. Cada bloque introduce un conjunto autónomo de principios, manteniéndose siempre basado en magnitudes medibles y en la interpretación ingenieril.

(subsec_fundamentals)=
## Fundamentos

Este primer bloque construye las herramientas conceptuales y matemáticas necesarias para analizar cualquier sistema termodinámico, independientemente de su naturaleza o escala.

* **Sistemas, entorno y fronteras**  
  Establece cómo definir un *sistema* (masa de control o volumen de control) y distinguirlo de su *entorno*. Introduce las *fronteras* (fijas o móviles) y el concepto de *interacción* entre sistema y entorno mediante calor y trabajo.

* **Propiedades y magnitudes**  
  Distingue propiedades *intensivas* (temperatura, presión) de *extensivas* (masa, energía). Define *estado*, *proceso* y *ciclo*; introduce el concepto de *funciones de estado* frente a *funciones de trayectoria* (p. ej., $U$ frente a $Q$, $W$). Presenta las condiciones de equilibrio y la noción de procesos *cuasiestáticos* como transformaciones idealizadas de referencia.

* **Modelos para las sustancias**  
  * *Modelo de gas perfecto*: la relación lineal más simple entre $p$, $v$ y $T$, válida a bajas presiones; ecuación de gas ideal como modelo de trabajo.  
  * *Gases reales*: desviaciones respecto a la idealidad mediante factores de compresibilidad; visión cualitativa de los efectos intermoleculares.  
  * *Sustancias puras*: comportamiento en cambio de fase, diagramas $p–v–T$, campana de saturación, punto crítico, líquido subenfriado y vapor recalentado.  
  * *Mezclas y aire atmosférico*: variables de composición, reglas de mezcla y la idea de *propiedades psicrométricas* (humedad, humedad específica, entalpía del aire húmedo).

* **Interacciones: trabajo y calor**  
  Define *trabajo* y *calor* como energía en tránsito, asociadas respectivamente al movimiento molecular *organizado* y *desorganizado*. Destaca las convenciones de signo y la dependencia de la trayectoria; incluye ejemplos de trabajo mecánico (de eje, de frontera, eléctrico) y de flujo.

* **$1^{\text{a}}$ ley de la termodinámica**  
  * *Sistemas cerrados*: cambio de energía interna como balance neto entre calor añadido y trabajo realizado, $\Delta U{}={}Q{}-{}W$. Introduce procesos especiales — isocórico, isobárico, isotermo, adiabático — y sus implicaciones energéticas.  
  * *Sistemas abiertos*: ecuación de energía en flujo estacionario (EEFE), mostrando la interacción entre entalpía, energía cinética y potencial. Dispositivos canónicos: **turbina**, **compresor/bomba**, **tobera/difusor**, **intercambiador de calor**, **cámara de mezcla**, **válvula de estrangulamiento**. Cada tipo de dispositivo se estudia bajo supuestos simplificadores que revelan su conversión característica de energía.

* **$2^{\text{a}}$ ley de la termodinámica**  
  Introduce los conceptos de *direccionalidad* y *limitación*. Expone las formulaciones de **Kelvin–Planck** y **Clausius**; define la *entropía* como propiedad cuyo cambio cuantifica la irreversibilidad. Establece el *balance de entropía*, procesos *reversibles* frente a *irreversibles* y eficiencias de dispositivos (isentropicas y globales).

* **Exergía e irreversibilidad**  
  Combina la primera y la segunda ley para expresar la *porción útil de energía* respecto a un entorno (el *estado muerto*). Define *exergía de flujo*, *exergía sin flujo* y *destrucción de exergía* $I{}={}T_0 S_{\text{gen}}$. Proporciona un marco unificado para cuantificar la *calidad* de la energía y las pérdidas en los sistemas.

:::{admonition} Nota: resumen del bloque de Fundamentos
:class: note

**Idea central:** Los fundamentos establecen un lenguaje — sistemas, estados, formas de energía, entropía y exergía — que permite expresar cualquier proceso o dispositivo real como un balance estructurado de *magnitudes* e *ineficiencias*. Esta base sustenta todo análisis posterior de ciclos.
:::

(subsec_gas_cycles)=
## Ciclos de gas

Este bloque aplica las leyes de la termodinámica a sistemas de *flujo continuo* que trabajan principalmente con gases como fluido de trabajo. Explora tanto ciclos *idealizados* (como referencia) como configuraciones *realistas* (con pérdidas y eficiencias).

* **Nociones generales**  
  Define qué es un *ciclo*: una secuencia cerrada de procesos que devuelve el fluido de trabajo a su estado inicial. Introduce la *eficiencia térmica*, la *relación de trabajo* y la *relación de presiones* como indicadores de rendimiento. Diferencia ciclos *ideales* (reversibles, sin pérdidas) de ciclos *reales* (irreversibilidades e ineficiencias de componentes).

* **Tipos habituales y aplicaciones**  
  Presenta la diversidad de ciclos de gas: simples, regenerativos, con intercooler, con recalentamiento y formas combinadas. Discute dónde aparece cada uno — p. ej., **generación de energía**, **propulsión aeroespacial**, **turbinas industriales**.

* **Ciclo Brayton (ideal)**  
  Describe la secuencia *compresión → adición de calor → expansión → rechazo de calor*. Desarrolla relaciones para la eficiencia en función de la relación de presiones y los límites de temperatura; explica el concepto de relación de trabajo interno (*relación de retroceso*).

* **Ciclos Brayton reales**  
  Introduce las *eficiencias isentrópicas* para compresor y turbina, *pérdidas de presión* en combustión e intercambio de calor, y la *efectividad del regenerador*. Examina la sensibilidad del rendimiento y la optimización práctica (relación de presiones, temperatura de entrada a la turbina).

* **Turbinas de gas estacionarias**  
  Analiza compromisos de diseño, comportamiento a carga parcial y efectos de regeneración/recalentamiento. Destaca la diferencia entre configuraciones *simples* y *complejas* (turbinas industriales frente a aeroderivadas).

* **Sistemas de propulsión aeronáutica**  
  Introduce motores turbojet, turbofan y turbohélice; explica *empuje* y *consumo específico de combustible* de forma cualitativa. Muestra cómo la relación de derivación (*bypass ratio*) y la velocidad de escape influyen en la eficiencia y el ruido.

* **Toberas y difusores**  
  Revisa la expansión/compresión isentrópica; define *flujo estrangulado*, *efectos del número de Mach* y conceptos de *empuje bruto*. Explica el desajuste de presión y las tendencias de eficiencia en contextos de propulsión.

:::{admonition} Nota: resumen del bloque de ciclos de gas
:class: note

**Idea central:** Los ciclos de gas traducen los principios termodinámicos en procesos de flujo continuo donde la energía se convierte principalmente mediante compresión y expansión. El *marco Brayton* proporciona el vínculo conceptual entre sistemas estacionarios y móviles (propulsivos).
:::

(subsec_ICREs)=
## Motores alternativos de combustión interna  (MACI)

Este bloque examina **sistemas alternativos** donde la combustión ocurre *dentro* de la cámara de trabajo. Se modelan como **ciclos aire-estándar**, proporcionando referencias idealizadas para el funcionamiento práctico de los motores.

* **Noción general**  
  Describe los MACI como *sistemas abiertos periódicos* analizados mediante ciclos cerrados ideales por simplicidad. Destaca su ubicuidad: desde generadores pequeños hasta motores automotrices y de servicio pesado.

* **Tipos habituales y aplicaciones**  
  Diferencia sistemas de **encendido por chispa** y **encendido por compresión**, señalando sus métodos de ignición, tipos de combustible y características de eficiencia. Discute modos de aspiración: atmosféricos frente a sobrealimentados (turbo y compresor).

* **Ciclo Otto (encendido por chispa)**  
  Describe sus cuatro procesos: compresión isentrópica, adición de calor a volumen constante, expansión isentrópica y rechazo de calor a volumen constante. Explica cómo la *relación de compresión* gobierna la eficiencia y los límites de rendimiento (detonación, restricciones de materiales).

* **Ciclo Diesel (encendido por compresión)**  
  Similar al Otto pero con adición de calor a *presión constante*. Explora la *relación de corte* y su influencia en la eficiencia. Compara los ciclos Diesel y Otto a relaciones de compresión equivalentes; aclara por qué los Diesel pueden operar con mayor eficiencia.

* **Modelos de pérdidas (cualitativos)**  
  Reconoce desviaciones respecto al ideal: transferencia de calor, duración finita de la combustión, fricción, pérdidas de bombeo y expansión incompleta. Introduce factores de corrección simples o coeficientes empíricos de rendimiento usados en evaluaciones prácticas.

:::{admonition} Nota: resumen del bloque de MACI
:class: note

**Idea central:** El análisis de MACI conecta el razonamiento cíclico ideal con el comportamiento real del motor. Mediante compresión, combustión y expansión, estos sistemas ilustran cómo la energía química se convierte cíclicamente en trabajo mecánico — bajo las mismas restricciones de la **$1^{\text{a}}$ ley** y la **$2^{\text{a}}$ ley**.
:::

(subsec_steam_cycles)=
## Ciclos de vapor

Este bloque se centra en **ciclos de vapor**, donde la sustancia de trabajo experimenta *cambio de fase* como parte del proceso de conversión de energía. Establece el vínculo entre adición de calor, expansión, condensación y regeneración en sistemas que impulsan gran parte de la generación eléctrica moderna.

* **Noción general**  
  Define los ciclos de vapor como sistemas con *aporte externo de calor* y *recirculación interna del fluido*. Destaca el agua/vapor como fluido de referencia por sus propiedades termodinámicas bien conocidas y comportamiento de fase favorable.

* **Tipos habituales y aplicaciones**  
  Incluye ciclos tipo **Rankine** para generación eléctrica, sistemas de **cogeneración industrial** y esquemas de **recuperación de calor**. Señala dónde dominan los ciclos de vapor (centrales eléctricas, vapor de proceso, ciclos combinados).

* **Ciclo Rankine (ideal)**  
  Describe sus cuatro etapas principales: *bombeo (presurización del líquido)*, *ebullición (adición de calor)*, *expansión (turbina)* y *condensación (rechazo de calor)*. Relaciona la eficiencia con la temperatura media de adición de calor y la presión del condensador. Introduce diagramas *T–s* y *h–s* como herramientas de diagnóstico.

* **Mejoras del ciclo**  
  * *Recalentamiento*: mejora la sequedad a la salida de la turbina y aumenta ligeramente la eficiencia.  
  * *Regeneración*: eleva la temperatura del agua de alimentación para reducir irreversibilidad.  
  * *Sobrecalentamiento*: incrementa la temperatura media de adición de calor.

* **Centrales termoeléctricas**  
  Analiza configuraciones típicas: caldera, tren de turbinas, condensador, sistema de refrigeración. Señala restricciones ambientales y métodos de enfriamiento (húmedo, seco, híbrido).

* **Cogeneración (CHP)**  
  Explica cómo las turbinas de extracción/condensación o de contrapresión suministran tanto potencia como calor útil. Introduce compromisos entre producción eléctrica y térmica.

* **Ciclo Rankine orgánico (ORC)**  
  Describe el uso de fluidos orgánicos para fuentes de calor de baja temperatura. Introduce la clasificación cualitativa de fluidos de trabajo (secos, isentrópicos, húmedos) y su adecuación a niveles de fuente térmica.

* **Ciclos duales y combinados**  
  Presenta conceptos *topping–bottoming*, donde ciclos de gas de alta temperatura impulsan subsistemas de vapor u ORC de baja temperatura. Destaca las ganancias globales de eficiencia mediante el aprovechamiento en cascada de la energía y la utilización del calor residual.

:::{admonition} Nota: resumen del bloque de ciclos de vapor
:class: note

**Idea central:** Los ciclos de vapor ilustran la termodinámica en su forma más práctica: convertir calor en potencia mecánica dentro de restricciones tecnológicas y ambientales reales. Mediante condensación, regeneración y combinación con ciclos de gas, demuestran cómo cada joule de energía se degrada progresivamente pero sigue *gobernado* por las mismas leyes universales.
:::

:::{admonition} Importante: resumen del curso
:class: warning

**Progresión global.**

1. El bloque de **Fundamentos** proporciona el lenguaje de sistemas, energía y entropía.
2. Los **ciclos de gas** extienden esto a dispositivos de flujo continuo y propulsión.
3. Los **MACI** muestran cómo el razonamiento cíclico se aplica a sistemas alternativos de combustión interna.
4. Los **ciclos de vapor** cierran el ciclo introduciendo el cambio de fase y la conversión de energía a gran escala.

En todos los bloques, se mantienen los mismos pilares analíticos:

* **Conservación de la energía ($1^{\text{a}}$ ley).**
* **Direccionalidad y limitación ($2^{\text{a}}$ ley).**
* **Calidad y degradación de la energía (Exergía).**

Juntos forman una visión coherente de la **Termodinámica Aplicada**: desde los principios fundamentales hasta los sistemas energéticos interconectados.
:::

