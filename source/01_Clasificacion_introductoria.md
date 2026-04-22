(sec_icre_introduction)=
## Clasificación introductoria de los MACI alternativos

Junto con las turbinas de gas que operan según ciclos de gas de tipo Brayton, los **motores de combustión interna alternativos (MACI)** constituyen la otra gran familia de ciclos de potencia de gas que domina la práctica de la ingeniería. Su relevancia se explica en gran medida por un hecho simple: proporcionan una forma compacta y robusta de convertir la energía química de un combustible en **trabajo mecánico**, con alta densidad de potencia y una amplia flexibilidad operativa. Por ello, son omnipresentes en el transporte (coches, motocicletas, barcos, aeronaves ligeras y unidades auxiliares de potencia), y también aparecen en muchas aplicaciones de generación de potencia a pequeña escala y de maquinaria móvil.

En la idealización termodinámica clásica, se utilizan dos ciclos como modelos de referencia para la mayoría de las implementaciones prácticas:

- el **ciclo Otto**, típicamente asociado a los motores de encendido por chispa (gasolina), y  
- el **ciclo Diesel**, típicamente asociado a los motores de encendido por compresión (diésel).

Estos dos ciclos ideales no describen toda la complejidad de los motores reales, pero proporcionan un lenguaje conceptual claro: explican, en una primera aproximación, cómo se añade y se rechaza calor, y cómo se obtiene trabajo mecánico a partir de una secuencia cíclica de estados.

:::{important}

**POR QUÉ LOS MACI SE ESTUDIAN POR SEPARADO DE LAS TURBINAS DE GAS**

Las turbinas de gas son, por lo general, turbomáquinas de flujo estacionario, en las que el fluido de trabajo evoluciona de manera continua a través de componentes rotativos.
Los MACI, en cambio, son *no estacionarios* por naturaleza: el fluido de trabajo queda confinado en un cilindro y experimenta compresión, combustión y expansión cíclicas, con grandes variaciones temporales de presión y temperatura. Esta diferencia es esencial tanto para la modelización como para el diseño.

:::

Debido a su uso generalizado, los MACI adoptan muchas formas tecnológicas. Motores que comparten la misma “semejanza de familia” termodinámica pueden, aun así, diferir fuertemente en:

- la disposición mecánica y la cinemática,
- la configuración a nivel de sistema (refrigeración, lubricación, admisión/escape),
- el número de cilindros y su disposición,
- el nivel de presión de admisión (aspiración natural frente a sobrealimentación),
- e incluso la secuencia de trabajo empleada para completar un ciclo (dos tiempos frente a cuatro tiempos).

Esta diversidad motiva un **enfoque por capas** del tema. Antes de entrar en el estudio termodinámico de los ciclos Otto y Diesel (ideales y reales), resulta útil establecer una base descriptiva coherente:

1. una descripción mecánica de cómo se produce y se transmite el movimiento,
2. una clasificación basada en el movimiento del pistón y en el número de tiempos,
3. una clasificación a nivel de sistema que no dependa del propio ciclo termodinámico,
4. y un repaso de los componentes principales, de modo que los conceptos termodinámicos posteriores puedan anclarse al hardware físico.

:::{note}

**UNA RAZÓN PRÁCTICA PARA ESTE ORDEN**

Muchos efectos no ideales que aparecen más adelante en el análisis termodinámico (pérdidas de calor, combustión incompleta, fricción, trabajo de bombeo, pérdidas de carga, combustión en tiempo finito) no son fenómenos abstractos: están directamente conectados con la geometría, los componentes y la arquitectura del sistema. Comprender primero la “máquina” hace que la termodinámica tenga más sentido.

:::

