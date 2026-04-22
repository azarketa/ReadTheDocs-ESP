(sec_icre_losses)=
## Pérdidas

Los ciclos Otto, Diesel y duales ideales son valiosos porque aíslan los principales mecanismos termodinámicos y proporcionan tendencias compactas de eficiencia. Sin embargo, los motores reales se desvían de esas idealizaciones de manera sistemática. Comprender **dónde** y **por qué** se producen esas desviaciones es esencial por dos razones:

1. Proporciona una explicación físicamente significativa de la diferencia entre las predicciones del ciclo ideal y las prestaciones medidas.
2. Orienta las estrategias de ingeniería para mitigar las pérdidas mediante el diseño (geometría, materiales, intercambio de gases) y el control (avance de encendido, inyección, distribución).

En esta sección, las pérdidas se organizan en dos grandes familias:

- **Pérdidas del ciclo termodinámico**, asociadas a cómo los procesos dentro del cilindro difieren del ciclo ideal.
- **Pérdidas mecánicas y auxiliares**, asociadas a la fricción y a la potencia absorbida por los subsistemas de apoyo.

---

(subsec_icre_losses_overview)=
### Clasificación de las pérdidas

#### Pérdidas asociadas al ciclo termodinámico

- **Pérdidas por transferencia de calor** (hacia las paredes del cilindro, culata, pistón, refrigerante y aceite)
- **Pérdidas por tiempo finito (duración de la combustión)** (“pérdidas temporales”)
- **Pérdidas de bombeo** (trabajo de intercambio de gases durante la admisión y el escape)

#### Pérdidas asociadas a subsistemas mecánicos y auxiliares

- **Fricción mecánica** (segmentos del pistón, cojinetes, tren de válvulas, etc.)
- **Cargas auxiliares** (bombas de agua/aceite, alternador, aire acondicionado, etc.)
- **Dispositivos de sobrealimentación** (compresor mecánico o turbocompresor, cuando existen, y su contrapresión / potencia de accionamiento asociadas)

:::{important}

**POR QUÉ IMPORTA ESTA SEPARACIÓN**

Las pérdidas del ciclo termodinámico modifican el ciclo **indicado** (el lazo $p-v$ dentro del cilindro),
mientras que las pérdidas mecánicas y auxiliares reducen la salida **efectiva** en el eje.
Mantener separados estos conceptos evita mezclar efectos de “eficiencia del ciclo” con efectos del “hardware del motor / la cadena motriz”.

:::

En lo que sigue, se pone el énfasis en las tres principales pérdidas del ciclo termodinámico, porque son las que deforman directamente los ciclos ideales Otto/Diesel hasta convertirlos en los diagramas indicadores medidos del motor.

---

(subsec_icre_heat_losses)=
### Pérdidas por transferencia de calor

Las pérdidas por transferencia de calor son una característica definitoria de los motores alternativos reales. En los ciclos ideales, la compresión y la expansión se tratan como adiabáticas (o al menos internamente reversibles y sin intercambio de calor). En los motores reales, los gases de trabajo alcanzan temperaturas muy elevadas y están confinados por fronteras metálicas, de modo que una cantidad significativa de calor fluye desde el gas hacia:

- la **culata** (y la región de las válvulas),
- la **corona del pistón**,
- la **camisa del cilindro**,
- los circuitos de **refrigerante** y **aceite lubricante**.

Estas pérdidas reducen el trabajo neto porque el estado termodinámico durante la expansión se altera: una menor temperatura intracilindro implica una menor presión y, por tanto, un menor trabajo de expansión para un mismo cambio de volumen.

#### Dónde y cuándo se concentran las pérdidas de calor

Las pérdidas de calor no son uniformes a lo largo del ciclo:

- Durante la **compresión**, las temperaturas del gas son relativamente más bajas y la duración es corta; existe transferencia de calor, pero a menudo es menos dominante que durante la expansión.
- Durante la **combustión y la expansión inicial**, las temperaturas del gas alcanzan su máximo y la diferencia de temperatura entre el gas y las fronteras metálicas es la mayor, por lo que la transferencia de calor se vuelve muy intensa.
- Durante el **escape**, los productos salen a alta temperatura, lo que representa otro canal importante de salida de energía del sistema motor.

En una comparación típica entre un ciclo ideal y un ciclo indicador medido, las pérdidas por transferencia de calor aparecen principalmente como una reducción del nivel de presión a lo largo de la trayectoria de expansión, reduciendo el área encerrada en el diagrama $p-v$ (y, por tanto, el trabajo indicado).

:::{note}

**LA TRANSFERENCIA DE CALOR NO ES “DESPERDICIADA” EN SENTIDO ABSOLUTO**

Una fracción significativa del calor transferido al **refrigerante** se elimina deliberadamente para mantener el motor cerca de su temperatura de funcionamiento de diseño (“temperatura de régimen”). Esto no es opcional: sin ello, la dilatación térmica, las tensiones térmicas, la degradación del lubricante y el daño de los componentes degradarían rápidamente las prestaciones y podrían conducir al gripado.

:::

---

(subsec_icre_heat_loss_modeling)=
### Modelado del balance energético del combustible en presencia de pérdidas de calor

En funcionamiento real, la energía química liberada por el combustible debe suministrar:

1. la salida efectiva útil,
2. la energía rechazada al refrigerante y al aceite,
3. la energía arrastrada por el escape,
4. irreversibilidades adicionales (incluyendo combustión incompleta, radiación, etc.).

Por tanto, una descomposición práctica del **aporte térmico equivalente** asociado al combustible suministrado puede escribirse conceptualmente como:

- **Término útil:** la parte de la energía liberada que se convierte en potencia efectiva de salida.
- **Transferencia de calor al refrigerante:** calor eliminado por el circuito de refrigeración (necesario para la regulación térmica).
- **Entalpía del escape:** energía que sale con los gases de escape (no totalmente convertible en trabajo sobre el pistón).
- **Combustión incompleta:** combustible no quemado o productos parcialmente oxidados (cuando existen).
- **Transferencia de calor al aceite:** calor absorbido por el lubricante (distinto del calor evacuado por el refrigerante).
- **Radiación:** transferencia de calor por radiación, que crece rápidamente con la temperatura (aproximadamente con $T^4$).

:::{important}

**EL ESCAPE ES UNA “SALIDA” TERMODINÁMICA**

Incluso si un motor estuviera perfectamente aislado de sus paredes, el escape seguiría arrastrando una energía considerable. Esta es una limitación fundamental: el ciclo debe rechazar energía para volver al estado inicial, y los procesos reales de escape suelen rechazar energía a temperaturas más altas de lo que sugiere el modelo ideal de rechazo de calor a volumen constante.

:::

---

(subsec_icre_heat_loss_magnitudes)=
### Magnitudes representativas e implicaciones cualitativas

Las temperaturas representativas de los componentes ayudan a explicar por qué algunas partes dominan las trayectorias de pérdida de calor:

- La **válvula de escape** puede alcanzar temperaturas del orden de **$700^\circ\text{C}$**, y está expuesta a los gases más calientes durante el blowdown y el comienzo del escape.
- La **corona del pistón** puede alcanzar temperaturas elevadas (cientos de grados Celsius), con grandes gradientes a través del material.

Como los productos de la combustión calientes tienden a ocupar la región superior de la cámara de combustión (menor densidad, estratificación impulsada por la flotabilidad y patrones de flujo), la **culata** suele representar la mayor fracción de las pérdidas de calor. Los repartos cualitativos típicos empleados en discusiones sobre pérdidas térmicas en motores son:

- culata: **aproximadamente 50–60%** de las pérdidas de calor a pared,
- paredes del cilindro: **aproximadamente 8–22%**,
- energía del gas de escape que abandona el cilindro: **aproximadamente 16–26%** del calor liberado (como canal energético separado).

Las pérdidas también están fuertemente concentradas en el tiempo:

- una gran parte ocurre durante la **expansión** (a menudo se cita **30–50%** de las pérdidas de transferencia a pared, según el motor y el régimen),
- y durante el **escape**, donde los gases calientes salen sin permitir una conversión térmica a trabajo completa.

Estos valores no son constantes universales; varían con el tamaño del motor, la carga, la velocidad de giro, la estrategia de refrigeración y el calado de la combustión. Su objetivo es anclar la intuición física: **la culata y las regiones próximas al escape son térmicamente críticas**.

---

(subsec_icre_time_losses)=
### Pérdidas por tiempo finito (duración de la combustión)

En el ciclo Otto ideal, la adición de calor se modela como un aporte de calor **instantáneo a volumen constante**. La combustión real nunca es instantánea. Se necesita un intervalo finito de ángulo de cigüeñal para que se propague la llama (MEP) o para que tenga lugar la combustión controlada por mezcla (MEC). Durante ese intervalo, el pistón se mueve, de modo que el proceso de aporte de calor no es ni puramente isócoro (Otto) ni puramente isóbaro (Diesel); es una transformación mixta y de duración finita.

En una superposición idealizada en el plano $p-v$, las pérdidas por tiempo finito aparecen como un redondeo y un ensanchamiento de la línea ideal abrupta de aporte de calor alrededor del PMS. El resultado suele ser una reducción del incremento efectivo de presión en los ángulos de cigüeñal más favorables para la extracción de trabajo.

#### Por qué las pérdidas aumentan con la velocidad del motor

A medida que aumenta la velocidad de giro:

- disminuye el **tiempo** pasado cerca del PMS,
- la misma duración de combustión (en milisegundos) corresponde a un **intervalo angular de cigüeñal mayor**,
- por tanto, una fracción mayor de la liberación de calor ocurre cuando el pistón ya se está alejando del PMS.

Esto reduce la fracción de calor liberado que contribuye a una alta presión media efectiva durante la expansión inicial, disminuyendo la eficiencia y el trabajo indicado.

:::{important}

**EL CALADO DE LA COMBUSTIÓN ES UN PROBLEMA DE EXTRACCIÓN DE TRABAJO**

El objetivo no es simplemente una “combustión rápida” de forma aislada. El objetivo es liberar la mayor parte del calor cuando el volumen sigue siendo pequeño (cerca del PMS) para que el aumento de presión se traduzca en un alto trabajo de expansión, sin inducir combustión anómala (detonación en MEP, aumento excesivo de la presión y ruido en MEC).

:::

---

(subsec_icre_spark_advance)=
### Mitigación de las pérdidas temporales: avance de encendido / inyección y calado de la combustión

Una forma clásica de compensar la combustión de duración finita es iniciar la combustión **antes** del PMS, de modo que la presión máxima y la mayor parte de la liberación de calor ocurran cerca del ángulo de cigüeñal deseado.

En los motores de encendido provocado esto se consigue mediante el **avance de encendido**; en los motores de encendido por compresión, un control análogo se consigue mediante el instante de inyección y la conformación de la tasa de inyección.

Sin embargo, un avance excesivo puede generar problemas severos:

- desarrollo de llama no óptimo,
- presiones máximas excesivas,
- aumento de la transferencia de calor a las paredes (más calientes antes),
- mayor tendencia a la detonación o a la combustión anómala.

Por tanto, el calado debe ajustarse en función de las condiciones de operación, especialmente de la **velocidad del motor**.

---

(subsec_icre_wiebe_model)=
### Modelado de la duración de la combustión: la función de Wiebe

Un modelo empírico ampliamente utilizado para la fracción acumulada quemada (o equivalentemente, la fracción de calor liberado) es la **función de Wiebe**:

$$
x_b(\theta)
= 1 - \exp \left[-a \left(\frac{\theta - \theta_s}{\theta_d}\right)^{n}\right],
$$

donde:

- $x_b$ es la **fracción de masa de combustible quemada** (o fracción del calor total liberado),
- $\theta$ es el **ángulo de cigüeñal**,
- $\theta_s$ es el ángulo de cigüeñal al **inicio de la combustión**,
- $\theta_d$ es la **duración de la combustión** expresada como intervalo de ángulo de cigüeñal,
- $a$ y $n$ son **parámetros de forma/eficiencia** ajustados a datos experimentales para cada motor y régimen de funcionamiento.

El modelo refleja una observación experimental clave: la combustión suele comenzar lentamente, acelerarse hasta una tasa máxima y, después, decrecer a medida que disminuye la mezcla no quemada restante.

:::{note}

**INTERPRETACIÓN DE LOS PARÁMETROS DE WIEBE**

- Aumentar $\theta_d$ reparte la combustión a lo largo de un mayor ángulo de cigüeñal, incrementando generalmente las pérdidas temporales.
- Desplazar $\theta_s$ (adelanto/retraso) mueve la ventana de combustión con respecto al PMS.
- Los parámetros $a$ y $n$ ajustan cuán “picuda” o “suave” es la tasa de combustión.

El modelo es lo bastante simple para simulaciones de ciclo y, al mismo tiempo, lo bastante flexible para reproducir perfiles de combustión medidos.

:::

---

(subsec_icre_wiebe_low_speed)=
### Intuición basada en Wiebe a baja velocidad del motor

A baja velocidad de giro, el pistón permanece cerca del PMS durante más tiempo, de modo que la combustión puede concentrarse razonablemente en el intervalo de volumen más favorable. Un valor ilustrativo típico es una duración de combustión del orden de:

- $\theta_d \approx 30^\circ$ (ejemplo de orden de magnitud para baja velocidad).

Si $\theta_s$ es **demasiado tardío** (poco o ningún avance), gran parte de la liberación de calor ocurre después del PMS, a volúmenes mayores, reduciendo la presión máxima y la extracción de trabajo.

Si $\theta_s$ es **demasiado temprano**, la combustión puede alcanzar su máximo antes del PMS, aumentando el trabajo negativo durante la última parte de la compresión y elevando la tendencia a la detonación.

Un avance intermedio tiende a maximizar tanto el trabajo indicado como la eficiencia al alinear la parte más pronunciada de la curva de combustión con la región angular en la que el aumento de presión es más beneficioso.

---

(subsec_icre_wiebe_high_speed)=
### Intuición basada en Wiebe a alta velocidad del motor

A alta velocidad de giro, el mismo tiempo físico de combustión corresponde a un intervalo angular de cigüeñal mayor; la combustión puede extenderse hasta:

- $\theta_d \approx 60^\circ$ (valor ilustrativo a alta velocidad).

En ese régimen, un avance que era óptimo a baja velocidad suele ser insuficiente: la combustión ocurriría efectivamente “demasiado tarde” en términos de ángulo de cigüeñal. Por tanto, se requiere un avance mayor (un $\theta_s$ más negativo con respecto al PMS) para mantener el calado deseado.

Esta dependencia es la razón por la que los mapas de encendido/inyección en las unidades de control del motor deben variar con las rpm y la carga.

:::{important}

**EL AVANCE DEPENDE DE LA VELOCIDAD**

El avance óptimo de encendido/inyección no es un número fijo.
Es función de:
- la velocidad (rpm),
- la carga,
- la composición de la mezcla,
- la fracción de gases residuales,
- la sobrealimentación y las condiciones de admisión,
- las limitaciones por detonación / gradiente de presión.

:::

---

(subsec_icre_pumping_losses)=
### Pérdidas de bombeo

Las pérdidas de bombeo surgen del hecho de que la admisión y el escape no son procesos cuasiestáticos y sin fricción. El intercambio de gases real exige vencer:

- restricciones de flujo en las **válvulas**,
- pérdidas de presión a través de **filtros** y del **conducto de admisión**,
- pérdidas en **colectores**, codos y mariposas,
- pérdidas a través de dispositivos de postratamiento (catalizador, filtro de partículas),
- silenciadores y contrapresión del sistema de escape.

En un diagrama real $p-v$, las carreras de admisión y escape ya no aparecen como líneas horizontales superpuestas a una única presión. En su lugar, forman un **bucle de bombeo cerrado** (a menudo con forma ovalada). El área de ese bucle representa el trabajo neto que debe suministrarse para mover los gases hacia dentro y hacia fuera del cilindro, reduciendo el trabajo indicado neto disponible del ciclo principal.

Las pérdidas de bombeo también reducen la carga fresca admitida, contribuyendo a un llenado incompleto del cilindro, algo que suele recogerse mediante una **eficiencia volumétrica**.

:::{tip}

**FRENO MOTOR**

El mismo mecanismo que crea pérdidas de trabajo de bombeo durante el funcionamiento a carga parcial puede aprovecharse para la deceleración: cerrar la mariposa (en motores MEP) incrementa el trabajo de bombeo y produce un par resistente conocido comúnmente como freno motor.

:::

---

(subsec_icre_pumping_SI)=
### Pérdidas de bombeo en motores de encendido provocado: control cuantitativo (basado en mariposa)

En el funcionamiento tradicional de los motores de encendido provocado, la combustión requiere una mezcla dentro de los límites de inflamabilidad, a menudo próxima a condiciones estequiométricas. Un intervalo típico para el factor de exceso de aire es:

- $\lambda \approx 1.0$ a $1.1$ en muchas condiciones de turismos (valor ilustrativo).

En el **control cuantitativo**, la potencia se controla modificando la **masa de mezcla** admitida mientras se mantiene aproximadamente similar la composición de la mezcla. Esto se consigue restringiendo el aire de admisión con una **mariposa**, lo que reduce la presión en el colector de admisión.

Esa restricción produce grandes pérdidas de bombeo, especialmente cuando:

- el consumo de combustible es significativo,
- la potencia demandada es baja (circulación urbana, carga ligera).

Como resultado, los motores MEP estrangulados por mariposa pueden presentar consumos de combustible desproporcionadamente altos a baja carga.

#### Estrategias de ingeniería para reducir las pérdidas de bombeo en MEP

Varios desarrollos tecnológicos buscan reducir estas pérdidas de bombeo inducidas por la mariposa:

- **Distribución variable / alzada variable de válvulas (distribución variable):**  
  Ajustar los instantes de apertura/cierre de las válvulas de admisión y escape modifica la respiración efectiva y puede reducir la necesidad de una fuerte estrangulación.  
  Los conceptos clásicos de distribución incluyen:
  - **AAA** (avance de apertura de admisión),
  - **RCA** (retraso de cierre de admisión),
  - **AAE** (avance de apertura de escape),
  - **RCE** (retraso de cierre de escape).
  
  Estos solapes crean un intervalo de **cruce de válvulas** (ambas válvulas abiertas), cuyo valor óptimo depende fuertemente de las rpm y de la carga. Un mayor solape puede favorecer el barrido y reducir el trabajo de bombeo en algunos regímenes, pero puede ser perjudicial en otros (reversión, gases residuales).

- **Inyección directa (MEP):**  
  Inyectar el combustible directamente en el cilindro permite una formación de mezcla más flexible y puede reducir las penalizaciones de bombeo al permitir distintas estrategias de control de carga y una mejor estabilidad de la combustión.

- **Funcionamiento con carga estratificada:**  
  Concentrar una mezcla más rica cerca de la bujía mientras se mantiene la mezcla global pobre puede sostener una ignición estable con menos estrangulación y menor trabajo de bombeo en determinadas ventanas de operación, afectando también a la duración de la combustión y a la eficiencia.

:::{note}

**POR QUÉ LA MARIPOSA PENALIZA**

Una mariposa reduce la presión de admisión, de modo que el pistón debe realizar trabajo extra durante la carrera de admisión para aspirar aire desde un colector de baja presión, y además debe empujar el escape contra una presión que puede ser mayor que la de admisión. Ese desajuste de presiones crea el área del bucle de bombeo.

:::

---

(subsec_icre_pumping_SI_regimes)=
### Tendencias de las pérdidas de bombeo en distintos regímenes de carga MEP (cualitativo)

Al comparar regímenes de operación típicos:

- **Ralentí:**  
  Mariposa casi cerrada → alta restricción en admisión → mal llenado.  
  El motor suministra justo el trabajo necesario para vencer el bombeo y la fricción.  
  Las pérdidas de bombeo pueden llegar a ser una fracción importante del trabajo indicado (a menudo se citan valores de hasta ~45% como ilustración de orden de magnitud en ralentí con mariposa).

- **Carga media:**  
  Mariposa parcialmente abierta → menor restricción → mejor llenado.  
  La fracción de pérdidas de bombeo disminuye significativamente (pueden ser típicos porcentajes de un solo dígito), pero rpm más altas pueden incrementar las pérdidas temporales.

- **Plena carga:**  
  Mariposa totalmente abierta → restricción mínima en admisión → mejor llenado.  
  Las pérdidas de bombeo pueden caer a unos pocos puntos porcentuales, mientras que pasan a dominar otras limitaciones (detonación, límites térmicos).

Estas tendencias explican por qué los motores MEP tradicionales estrangulados son relativamente ineficientes en operación urbana de baja carga y por qué las tecnologías MEP modernas buscan reducir las pérdidas de bombeo.

---

(subsec_icre_pumping_CI)=
### Pérdidas de bombeo en motores de encendido por compresión: control cualitativo (basado en combustible)

Los motores Diesel no dependen de una chispa y, por tanto, no están obligados a mantener una mezcla casi estequiométrica para la ignición. Pueden operar en un rango más amplio de factores de exceso de aire. En la práctica, valores superiores a 1 son típicos y pueden llegar a ser muy altos a baja carga.

En el **control cualitativo**, el motor admite aproximadamente la misma cantidad de aire (sin mariposa en la configuración clásica), y la potencia se regula inyectando más o menos combustible:

- baja demanda de potencia → pequeña cantidad de combustible → mezcla muy pobre (alto $\lambda$),
- alta demanda de potencia → mayor cantidad de combustible → mezcla menos pobre (menor $\lambda$, aunque a menudo todavía >1).

Como el aire de admisión no se estrangula, las pérdidas de bombeo asociadas a la restricción en admisión suelen ser menores que en los motores MEP con mariposa.

Un beneficio adicional es que, a baja carga, un $\lambda$ alto tiende a reducir el comportamiento efectivo de corte de la combustión y puede mejorar las tendencias de eficiencia térmica, en consonancia con la discusión cualitativa sobre la eficiencia del ciclo Diesel.

:::{important}

**POR QUÉ LA CARGA PARCIAL DIESEL ES TERMODINÁMICAMENTE FAVORABLE**

A baja carga, un motor Diesel puede mantener alto el flujo de aire y reducir el combustible, produciendo una mezcla muy pobre.
Esto evita la mariposa y suele proporcionar mejor eficiencia a carga parcial que los motores MEP tradicionales.

:::

---

(subsec_icre_pumping_CI_disadvantages)=
### Limitaciones y fuentes de pérdidas de bombeo en motores Diesel

A pesar de la ventaja de evitar la restricción por mariposa, los motores Diesel no están libres de pérdidas de bombeo. Las caídas de presión pueden ser significativas debido a:

- pérdidas en filtros y conductos de admisión,
- cambios de dirección del flujo y fricción en colectores,
- restricciones en el lado del escape (áreas de paso en válvulas, colectores),
- dispositivos de postratamiento (catalizadores de oxidación, filtros de partículas),
- silenciadores y trazado del escape.

Algunos de estos elementos también existen en los motores MEP, pero el postratamiento Diesel y las elevadas exigencias de caudal pueden hacer que ciertas contribuciones sean mayores en configuraciones específicas. Además, las pérdidas de bombeo siguen creciendo con las rpm y con el caudal másico.

---

(subsec_icre_losses_closure)=
### Cierre conceptual

- Los ciclos reales de los MACI se desvían de los ciclos ideales Otto/Diesel/duales principalmente por la **transferencia de calor**, la **duración finita de la combustión** y el **trabajo de bombeo**.
- Las pérdidas por transferencia de calor reducen el nivel de presión durante la expansión y deben gestionarse mediante refrigeración y materiales; son más intensas cerca de las temperaturas máximas y a menudo dominan a través de la culata.
- La combustión de tiempo finito hace que el aporte de calor no sea ni isócoro ni isóbaro; el calado óptimo de la combustión depende fuertemente de las rpm y a menudo se modela con la **función de Wiebe**.
- Las pérdidas de bombeo se originan en las caídas de presión del intercambio de gases real y aparecen como un bucle de bombeo en el diagrama $p-v$.
- El control cuantitativo tradicional de los motores MEP mediante mariposa incrementa las pérdidas de bombeo a baja carga; el control cualitativo Diesel basado en el combustible las reduce, pero no las elimina debido a las restricciones de admisión/escape.
- La fricción mecánica y las cargas auxiliares reducen adicionalmente la potencia en el eje y deben tratarse por separado de las deformaciones del ciclo indicado.

