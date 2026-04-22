(sec_icre_system_classification_components)=
## Clasificación a nivel sistémico y componentes principales de los MACI alternativos

La clasificación mecánica (alternativos frente a rotativos, de dos tiempos frente a cuatro tiempos) explica *cómo* se produce el movimiento, pero no describe por completo *cómo se implementa el motor como sistema*. En la práctica, motores que comparten la misma arquitectura mecánica pueden diferir notablemente en prestaciones, eficiencia, fiabilidad, ruido, necesidades de mantenimiento y rango operativo debido a decisiones de diseño a nivel de sistema.

Por esta razón, suele adoptarse un segundo bloque de clasificación: una **clasificación no estrictamente termomecánica**, basada no en el ciclo termodinámico idealizado, sino en la **configuración y las características globales** del motor. Estos criterios son esenciales porque determinan si el motor puede operar cerca de su **temperatura estacionaria de funcionamiento** prevista, si puede integrarse y equilibrarse adecuadamente, y si puede suministrar el caudal de aire y combustible requerido en condiciones reales.

---

(subsec_icre_non_thermomechanical_classification)=
### Clasificación no estrictamente termomecánica

#### Clasificación según el sistema de refrigeración

Un primer criterio a nivel de sistema es el **sistema de refrigeración**. Su finalidad es mantener el motor funcionando cerca de la llamada **temperatura normal de funcionamiento** (o *temperatura estacionaria de funcionamiento*), es decir, el intervalo de temperaturas en el que el motor tiende a alcanzar sus mejores condiciones de prestaciones y durabilidad.

Un sistema de refrigeración debe satisfacer dos requisitos prácticos:

- debe permitir que el motor alcance rápidamente la temperatura normal de funcionamiento tras el arranque,  
- y debe mantener esa temperatura independientemente de las condiciones ambientales y de la carga del motor.

Esto no es un detalle menor. La combustión puede implicar temperaturas de gas de hasta $2000\ ^\circ\text{C}$, y una fracción importante de la energía química liberada por la combustión del combustible (del orden del $70\%$ en muchas situaciones prácticas) aparece en forma de calor. Si este calor no se disipa adecuadamente, las temperaturas de los componentes aumentan, los materiales se expanden, crecen las tensiones térmicas, empeora la calidad de la lubricación y descienden las prestaciones del motor. En casos extremos, un sobrecalentamiento excesivo puede conducir al gripado mecánico.

:::{important}

**POR QUÉ LA REFRIGERACIÓN ES UNA EXIGENCIA DE PRESTACIONES**

Un motor no se diseña para estar “lo más frío posible”, sino para funcionar en un *régimen térmico controlado*.  
Demasiado caliente: expansión excesiva, degradación del aceite, pérdida de tolerancias, riesgo de gripado.  
Demasiado frío: malas condiciones de lubricación, mayor fricción, vaporización incompleta y peor combustión en motores de encendido provocado, y en general peor eficiencia.

:::

Existen dos enfoques principales de refrigeración.

- **Refrigeración líquida (por refrigerante):**  
  Un fluido refrigerante circula por conductos y galerías del bloque motor y de la culata. A medida que atraviesa las zonas calientes, absorbe calor. Posteriormente, el refrigerante caliente pasa por un radiador (intercambiador de calor), donde transfiere energía térmica al aire ambiente forzado a través del radiador. Tras enfriarse, el fluido regresa al motor y el ciclo se repite.

  Un **termostato** desempeña un papel clave: restringe o bloquea la circulación del refrigerante cuando el motor está frío, permitiendo un calentamiento más rápido, y después regula el caudal para mantener el motor cerca de su temperatura normal de funcionamiento. Este control mejora tanto las prestaciones del motor como las condiciones de lubricación.

  La refrigeración líquida suele ser:
  - más eficaz y estable desde el punto de vista térmico,
  - más silenciosa (el refrigerante proporciona un efecto amortiguador),
  - pero más pesada, más costosa y más compleja,
  - y exige más mantenimiento debido a bombas, manguitos, conductos, radiador y conexiones.

- **Refrigeración por aire:**  
  La refrigeración por aire se basa en el flujo de aire sobre las superficies del cilindro y de la culata, a menudo mejorado mediante aletas que incrementan el área de transferencia de calor. Un ventilador accionado por el cigüeñal genera una corriente de aire forzada que se dirige hacia los cilindros. A medida que aumenta la velocidad del motor, el caudal de aire generalmente también aumenta, mejorando así la evacuación de calor.

  Los sistemas refrigerados por aire también pueden incorporar dispositivos termostáticos que regulan el flujo de aire mediante compuertas o clapetas, evitando un enfriamiento excesivo cuando el motor está frío y favoreciendo un calentamiento más rápido.

  La refrigeración por aire suele ser:
  - más simple (sin radiador, sin bomba de refrigerante, con menos componentes),
  - más ligera y más barata,
  - y más fácil de mantener,
  - pero potencialmente menos estable, ya que depende fuertemente de la temperatura ambiente y de las condiciones de flujo de aire.
  Puede resultar insuficiente bajo ciertos climas y cargas de funcionamiento, generando riesgo de sobrecalentamiento.
  Además, los cilindros aleteados y la ausencia de amortiguamiento hidráulico tienden a hacer que los motores refrigerados por aire sean más ruidosos.

:::{note}

**COMPROMISO DE INGENIERÍA**

La refrigeración líquida suele maximizar el control de temperatura y el confort acústico, a costa de mayor masa y complejidad.  
La refrigeración por aire maximiza la simplicidad y la baja masa, a costa de menor estabilidad térmica y, con frecuencia, mayor ruido.

:::

---

#### Clasificación según el número y la disposición de cilindros

Un segundo criterio a nivel de sistema es el **número y la disposición de los cilindros**, que afecta a la compacidad, el equilibrado, las vibraciones, la disposición del sistema de refrigeración y el diseño estructural. Entre las configuraciones más comunes se encuentran:

- **Motores en línea**,  
- **motores en V**,  
- **motores bóxer (planos)**, entre otras configuraciones menos frecuentes.

La disposición no es solo una decisión de empaquetado: tiene consecuencias mecánicas y estructurales directas.

- Las configuraciones en línea suelen presentar menos problemas de vibración y permiten una construcción más simple, pero pueden requerir bloques más largos, reduciendo la compacidad.
- Las configuraciones en V reducen la longitud del motor y pueden mejorar su integración, pero pueden introducir modos de vibración más intensos (según el orden de encendido, el ángulo entre bancadas y el equilibrado).
- Los motores bóxer pueden interpretarse como una configuración en V con un ángulo entre bancadas de $180^\circ$. Proporcionan una menor altura del motor y un centro de gravedad más bajo, y pueden reducir las vibraciones, pero a menudo requieren culatas y componentes del tren de válvulas duplicados, lo que incrementa el coste y la complejidad.

El tamaño del motor y su aplicación influyen notablemente en el número típico de cilindros. Las motocicletas pequeñas suelen tener menos de 4 cilindros, los turismos suelen situarse en torno a 4–6 cilindros (a veces 8 en vehículos de altas prestaciones), los camiones diésel pesados pueden emplear configuraciones en V de mayor tamaño, y los grandes motores diésel marinos o ferroviarios pueden utilizar un número muy elevado de cilindros para satisfacer las necesidades de potencia.

:::{tip}

**POR QUÉ LA DISPOSICIÓN DE CILINDROS IMPORTA EN TERMODINÁMICA**

Más adelante, al discutir las pérdidas de los ciclos reales, conviene recordar que la disposición de los cilindros afecta a:
- las relaciones entre área de transferencia de calor y volumen,
- la eficacia de la refrigeración y los gradientes térmicos,
- la fricción y las pérdidas mecánicas,
- y los recorridos del intercambio de gases (colectores de admisión y escape).

:::

---

#### Clasificación según el nivel de presión de admisión

Un tercer criterio es la **presión de admisión**, que permite distinguir entre:

- **Motores atmosféricos (de aspiración natural)**, en los que el llenado del cilindro depende de condiciones de admisión próximas a la atmosférica y de las diferencias de presión generadas por el movimiento del pistón.
- **Motores sobrealimentados**, en los que un compresor eleva la presión de admisión.

La sobrealimentación puede lograrse mediante:

- un compresor accionado mecánicamente (**supercharger**), o  
- un compresor accionado por turbina (**turbocharger**).

Aunque el análisis termodinámico de la sobrealimentación se abordará más adelante, la distinción a nivel de sistema ya es importante: elevar la presión de admisión incrementa la masa de aire admitida por ciclo, permitiendo mayor par y potencia para una misma cilindrada, pero también aumenta las cargas térmicas y mecánicas y refuerza la importancia de la refrigeración y la lubricación.

---

(subsec_icre_components)=
### Componentes principales de los MACI alternativos

Una vez establecidas las clasificaciones principales, resulta útil identificar los componentes más habituales presentes en los MACI. Los motores reales incluyen muchas piezas que interactúan entre sí, y una descripción mecánica completa puede ser compleja. Por ello, aquí el enfoque se centra en los componentes más comunes de los **motores alternativos de cuatro tiempos**, que representan la configuración estándar en muchas aplicaciones prácticas.

:::{important}

**LOS COMPONENTES COMO “MAPA” DE LAS PÉRDIDAS**

El estudio posterior de los ciclos Otto/Diesel reales implica pérdidas (transferencia de calor, fricción, caídas de presión, estanqueidad imperfecta, combustión en tiempo finito).  
Cada uno de estos fenómenos puede vincularse directamente con componentes concretos (paredes, segmentos, válvulas, colectores, conductos de refrigeración, etc.).  
Aprender ahora los componentes hace que el modelado termodinámico posterior esté físicamente fundamentado.

:::

---

* **Cilindro:**

    El **cilindro** aloja el pistón y guía su movimiento. Dado que el pistón se desliza continuamente, el cilindro requiere:

    - un buen acabado superficial,
    - tolerancias de fabricación estrictas,
    - alta resistencia al desgaste.

    Las cargas térmicas y mecánicas son importantes, por lo que los cilindros emplean con frecuencia camisas (secas o húmedas). Una camisa seca actúa como superficie resistente al desgaste, mientras que una camisa húmeda puede incorporar contacto con el refrigerante y mejorar la evacuación de calor.

<br/>

* **Bloque motor:**

    El **bloque motor** aloja los cilindros y soporta el conjunto pistón–biela–cigüeñal. Debe ser estructuralmente rígido y con frecuencia integra conductos de refrigeración.

    Los materiales se seleccionan buscando un equilibrio entre resistencia, comportamiento térmico y peso. La fundición y las aleaciones de aluminio son habituales: las aleaciones de aluminio reducen la masa y mejoran la conductividad térmica, favoreciendo la refrigeración, aunque pueden requerir camisas o tratamientos para resistir el desgaste.

    El diseño del bloque motor depende fuertemente de la disposición de los cilindros:

    - los bloques en línea son más largos,
    - los bloques en V son más cortos pero están divididos en bancadas,
    - los bloques bóxer son anchos y bajos, lo que reduce la altura del centro de gravedad.

<br/>

* **Cárter (depósito de aceite):**

    El **cárter** suele servir como depósito y colector de aceite, situado por debajo del bloque motor. A menudo va atornillado al bloque. Como normalmente no es un elemento estructural principal, suele fabricarse con aleaciones ligeras o chapas finas de acero.

<br/>

* **Culata:**

    La **culata** va montada en la parte superior del bloque y contiene:

    - la geometría de la cámara de combustión,
    - los conductos de admisión y escape,
    - las válvulas (o sus asientos),
    - y las bujías o los inyectores.

    Opera bajo elevadas tensiones térmicas y mecánicas. Las pérdidas de calor suelen ser importantes en esta zona, especialmente cerca de la región de escape.

    Un componente clave de estanqueidad es la **junta de culata**, situada entre la culata y el bloque. Su finalidad es asegurar una estanqueidad adecuada frente a:

    - gases de combustión,
    - fugas de refrigerante,
    - fugas de aceite.

    La junta debe ser lo suficientemente deformable como para adaptarse a las superficies y, al mismo tiempo, lo bastante resistente como para soportar altas presiones y temperaturas. Su fallo conduce a problemas graves: pérdida de compresión, contaminación cruzada entre aceite y refrigerante, y eventual daño del motor.

<br/>

* **Pistón:**

    El **pistón** es el elemento móvil que recibe las fuerzas de presión del fluido de trabajo y las transmite a la biela. Debe:

    - asegurar la estanqueidad junto con los segmentos,
    - ser ligero (reduciendo la inercia),
    - soportar altas temperaturas y gradientes térmicos,
    - resistir la corrosión y el desgaste.

    Los pistones experimentan temperaturas especialmente elevadas cerca de la cabeza y deben diseñarse para permitir una expansión térmica controlada.

<br/>

* **Segmentos del pistón:**

    Los **segmentos del pistón** se alojan en ranuras alrededor del perímetro del pistón. Sus funciones principales son:

    - sellar la cámara de combustión (limitando el blow-by),
    - controlar la distribución del aceite sobre la pared del cilindro,
    - transferir calor del pistón a la pared del cilindro.

    Un conjunto típico puede incluir:

    - **segmentos de compresión** (también llamados segmentos de fuego): sellan los gases de combustión y limitan las fugas hacia el cárter, además de ayudar en la transferencia de calor,
    - un **segmento rascador de aceite**: distribuye uniformemente el lubricante y elimina el exceso de aceite,
    - un elemento **expansor**: actúa como un resorte que apoya los segmentos de aceite y mantiene la presión de contacto.

    La selección de segmentos y recubrimientos viene determinada por el desgaste, la temperatura, la reducción de fricción y los requisitos de estanqueidad. El diseño de los segmentos difiere entre motores de dos tiempos y de cuatro tiempos debido a la estrategia de lubricación y a las restricciones de funcionamiento.

<br/>

* **Biela:**

    La **biela** transmite fuerzas entre el pistón y el cigüeñal. Debe combinar baja masa con alta rigidez y resistencia, y debe satisfacer estrictos requisitos de tolerancia para garantizar una alineación adecuada y una correcta transmisión de carga. Se fabrica normalmente en acero forjado, aceros especiales, aleaciones ligeras o materiales de fundición más avanzados.

<br/>

* **Cigüeñal:**

    El **cigüeñal** transforma el movimiento de la biela en rotación. Está sometido a esfuerzos de torsión y flexión y suele incluir:

    - muñequillas y apoyos,
    - cojinetes,
    - contrapesos para reducir las vibraciones.

    Los cigüeñales suelen incorporar conductos internos de aceite para asegurar la lubricación de los cojinetes y de los contactos móviles. Entre los materiales habituales se encuentran el acero forjado y la fundición nodular (fundición de grafito esferoidal).

* **Válvulas:**

    Las **válvulas** regulan los flujos de admisión y escape. Las válvulas de escape, en particular, soportan temperaturas muy elevadas (a menudo de varios cientos de grados Celsius). Los diseños multiválvula pueden reducir las cargas térmicas y mejorar la capacidad de flujo. Los materiales se eligen por su resistencia a alta temperatura, empleándose habitualmente aceros aleados con cromo y níquel.

<br/>

* **Árbol de levas:**

    El **árbol de levas** acciona las válvulas de admisión y escape siguiendo una ley temporal prescrita. Suele estar situado en la culata y es accionado mecánicamente en sincronía con el cigüeñal.

<br/>

* **Correa de distribución / correa de transmisión:**

    Una correa (o cadena) conecta el cigüeñal con el árbol de levas, garantizando el sincronismo correcto de las válvulas. Además, las correas pueden accionar dispositivos auxiliares como:

    - ventiladores en motores refrigerados por aire,
    - compresores accionados mecánicamente en motores sobrealimentados.

<br/>

* **Motor de arranque:**

    Un motor de combustión interna no puede arrancar por sí mismo: requiere una fuente externa de energía para iniciar la rotación. El **motor de arranque** es una pequeña máquina eléctrica alimentada por la batería del vehículo. Convierte la potencia eléctrica en rotación mecánica engranando un piñón con el volante de inercia, forzando así el giro del cigüeñal hasta que la combustión pasa a ser autosostenida.

    En dispositivos pequeños (motosierras, motores fueraborda), esta función se realiza manualmente mediante cuerdas de arranque u otros mecanismos similares, que proporcionan la rotación inicial del cigüeñal.

---

(subsec_icre_system_closure)=
### Cierre conceptual

- La clasificación a nivel de sistema complementa la clasificación mecánica al describir la arquitectura del motor más allá del ciclo termomecánico ideal.
- La estrategia de refrigeración es esencial para garantizar el funcionamiento a una temperatura normal de operación controlada y para prevenir modos de fallo por sobrecalentamiento.
- La disposición de los cilindros determina la integración geométrica, el comportamiento vibratorio y la complejidad estructural.
- La clasificación según la presión de admisión distingue entre motores atmosféricos y sobrealimentados, con un fuerte impacto sobre la densidad de potencia alcanzable.
- Un mapa a nivel de componentes (cilindro, culata, junta, pistón, segmentos, tren de válvulas, tren alternativo-rotativo, motor de arranque) proporciona la base física necesaria para interpretar posteriormente las pérdidas de los ciclos reales.

