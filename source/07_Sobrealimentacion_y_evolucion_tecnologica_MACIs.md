(sec_icre_overfeeding)=
## Sobrealimentación y evolución tecnológica de los MACI

Los motores alternativos de aspiración natural están, en última instancia, limitados por la cantidad de **masa de aire** que pueden admitir por ciclo. Para una cilindrada fija, la cantidad máxima de combustible que puede quemarse eficientemente está restringida por el oxígeno disponible. La sobrealimentación (turboalimentación/compresor mecánico) aborda este cuello de botella incrementando la **densidad en la admisión** (y, por tanto, la masa de aire aspirada), lo que permite:

- quemar más combustible por ciclo (mayor potencia para la misma cilindrada),
- mejorar el par en rangos útiles de funcionamiento,
- y, en muchos diseños modernos, mejorar el consumo de combustible mediante *downsizing*.

La idea fundamental es simple: **elevar la presión en el colector de admisión por encima de la atmosférica**, ya sea extrayendo trabajo de la corriente de escape (turboalimentación) o accionando mecánicamente un compresor desde el cigüeñal (sobrealimentación mecánica).

:::{important}

**LA SOBREALIMENTACIÓN ES UNA ESTRATEGIA DE CAUDAL MÁSICO**

Un motor sobrealimentado no es “más energético” porque su combustible sea diferente, sino porque admite **más aire por ciclo**. Más aire permite quemar más combustible, lo que incrementa el calor liberado por ciclo y, por tanto, el trabajo indicado potencial, sujeto a las limitaciones térmicas, mecánicas y de combustión.

:::

---

(subsec_icre_boost_devices)=
### Compresores y turbocompresores

Dos arquitecturas dominan la sobrealimentación práctica en automoción:

- **Turbocompresores** (turbina accionada por los gases de escape + compresor)
- **Compresores mecánicos** (compresor accionado por el cigüeñal)

Ambos elevan la presión de admisión, pero difieren en la forma en que se suministra el trabajo de compresión y en cómo responde el sistema a distintos regímenes del motor.

---

(subsec_icre_turbocharger)=
### Turboalimentación: recuperación de energía de escape para accionar un compresor

Un turbocompresor consta de:

- una **turbina** situada en la corriente de escape,
- acoplada mecánicamente (mediante un eje) a
- un **compresor** situado en la línea de admisión aguas arriba del motor.

La turbina extrae parte de la energía de los gases de escape (entalpía y presión) y la convierte en potencia de eje que acciona el compresor de admisión. Conceptualmente, esta disposición se asemeja al conjunto compresor–turbina de una turbina de gas de ciclo Brayton, pero aquí el propósito no es generar potencia neta de eje, sino **incrementar la carga de aire en el cilindro**.

#### Resultados prácticos de la turboalimentación

Para una cilindrada dada, la turboalimentación suele proporcionar:

- **mayor densidad de potencia** (más potencia por litro),
- la posibilidad de escalonamientos **en paralelo** o **en serie** para ampliar el rango útil de rpm,
- mejora del par a alta carga y potencial para reducir la cilindrada del motor.

Sin embargo, la turboalimentación también introduce efectos secundarios dinámicos y termodinámicos:

- **Limitaciones en la respuesta de sobrealimentación** a bajas rpm (energía de escape insuficiente → aceleración más lenta de la turbina, *turbo lag*).
- **Contrapresión de escape** introducida por la turbina, que puede aumentar el trabajo de bombeo durante la carrera de escape.
- Incremento de la temperatura de admisión tras la compresión, lo que afecta a la tendencia al picado (MEP) y a las emisiones/cargas térmicas (MEC).

:::{note}

**EL INTERCOOLING SUELE SER EL GRAN COMPLEMENTO DE LA TURBOALIMENTACIÓN**

La compresión del aire eleva su temperatura. Enfriar la carga después de la compresión aumenta su densidad a una presión dada y puede reducir las temperaturas máximas dentro del cilindro. Esto mejora el margen frente al picado en los motores de encendido provocado y puede reducir el esfuerzo térmico y la formación de contaminantes en los motores de encendido por compresión.

:::

#### Intercoolers (refrigeradores del aire de sobrealimentación)

Los sistemas turboalimentados suelen incluir un **refrigerador del aire de sobrealimentación** (*charge-air cooler* o intercooler) entre la salida del compresor y el colector de admisión. Dos configuraciones habituales son:

- intercoolers **aire-aire**,
- intercoolers **aire-agua** (a menudo denominados **WCAC**, *Water Charge Air Cooler*).

El intercooling puede:

- aumentar la densidad de admisión (más masa de aire por ciclo a la misma presión de sobrealimentación),
- reducir la tendencia al picado en motores de encendido provocado al disminuir la temperatura del gas extremo,
- reducir las temperaturas máximas del ciclo y las cargas térmicas asociadas.

---

(subsec_icre_vgt_series)=
### Configuraciones del turbocompresor: geometría variable y escalonamiento

Para ampliar el rango efectivo de funcionamiento, los sistemas de turboalimentación pueden configurarse de distintas formas:

- **Turbocompresores de geometría variable (VGT):**  
  Al variar el área efectiva de paso en la turbina, el VGT mejora la eficiencia de la turbina y la respuesta de sobrealimentación en un intervalo más amplio de rpm. Esta solución se utiliza ampliamente en muchas aplicaciones Diesel, donde la estrategia de control y las características del escape son compatibles con la operación VGT.

- **Turboalimentación en serie (dos etapas):**  
  El uso de dos compresores/turbinas en serie permite alcanzar relaciones de compresión elevadas y mejorar la respuesta en un rango más amplio, especialmente cuando se combina con estrategias de control que gestionan qué etapa domina en cada régimen.

- **Turboalimentación en paralelo:**  
  Dividir el flujo de escape entre dos turbinas (y el flujo de admisión entre dos compresores) puede reducir la inercia de cada turbo y mejorar la respuesta, algo habitual en configuraciones multicilíndricas.

La elección supone un compromiso de diseño entre respuesta transitoria, empaquetado, coste y eficiencia.

---

(subsec_icre_supercharger)=
### Sobrealimentación mecánica: compresores accionados por el cigüeñal

En los motores con compresor mecánico, el compresor es accionado directamente por el cigüeñal mediante correa, cadena o tren de engranajes. Las velocidades de giro típicas del compresor pueden ser muy elevadas (son comunes órdenes de magnitud del tipo 10\,000–15\,000 rpm, según el diseño y las relaciones de transmisión).

#### Ventajas de la sobrealimentación mecánica

- **Excelente par a bajo régimen:**  
  Dado que el compresor está accionado directamente por el cigüeñal, la sobrealimentación puede estar disponible incluso cuando la energía de escape no es suficiente para hacer girar un turbo.
- **Respuesta predecible:**  
  La presión de sobrealimentación está estrechamente ligada al régimen del motor y a la relación de accionamiento.

#### Principal inconveniente

- **Carga parasitaria:**  
  El compresor consume potencia de eje. Esto reduce directamente la potencia efectiva en comparación con una configuración turboalimentada equivalente a la misma presión en el colector.

Son posibles configuraciones híbridas (compresor mecánico + turbocompresor) para combinar una buena respuesta a bajo régimen con una gran capacidad a alto régimen.

:::{important}

**PRESIÓN DE SOBREALIMENTACIÓN FRENTE A BENEFICIO NETO**

La sobrealimentación incrementa el trabajo indicado potencial del motor, pero el beneficio neto depende de:
- las eficiencias del compresor y de la turbina,
- las pérdidas adicionales de bombeo (especialmente por contrapresión de escape),
- la potencia parasitaria de accionamiento (compresor mecánico),
- los límites de picado (MEP) y los límites térmicos/de emisiones (MEC).

La sobrealimentación no es “potencia gratis”; es una redistribución de energía y pérdidas entre subsistemas.

:::

---

(subsec_icre_boosted_otto)=
### Efectos de la sobrealimentación sobre el ciclo Otto (encendido provocado)

En un motor MEP, la sobrealimentación eleva la presión de admisión y normalmente incrementa la temperatura y la presión al final de la compresión. Esto tiene varias consecuencias directas:

- **Mayor masa atrapada y mayores presiones máximas** tras la combustión (potencialmente mayor par/potencia).
- **Mayor propensión al picado** (riesgo de autoencendido) porque el gas extremo alcanza temperaturas y presiones más altas.

Por esta razón, los motores MEP sobrealimentados suelen depender en gran medida del **intercooling**. Sin enfriamiento de la carga, el diseñador puede verse obligado a:

- reducir la relación de compresión geométrica,
- retrasar el encendido,
- enriquecer la mezcla para refrigerar la carga (en ciertos regímenes),
- o adoptar otras estrategias de mitigación del picado.

Estas medidas protegen el motor, pero pueden reducir la eficiencia, de modo que el intercooler pasa a ser un elemento central para hacer compatible la sobrealimentación con una elevada eficiencia.

:::{note}

**VISIÓN DE CICLO IDEAL FRENTE A VISIÓN DE SISTEMA REAL**

En el modelo idealizado del ciclo Otto, el turbocompresor/intercooler no forma parte del bucle intracíclindro de cuatro procesos (compresión–aporte de calor–expansión–rechazo de calor). En motores reales, sin embargo, el hardware de sobrealimentación modifica:
- el estado de admisión (presión, temperatura),
- el trabajo de bombeo (a través de pérdidas de presión/contrapresión),
- las restricciones sobre el faseado de la combustión (encendido limitado por picado),

y, por tanto, modifica el ciclo *efectivo* y sus prestaciones.

:::

---

(subsec_icre_boosted_diesel)=
### Efectos de la sobrealimentación sobre el ciclo Diesel (encendido por compresión)

En los motores Diesel, el aumento de la temperatura de admisión tras la compresión no constituye un problema de picado: el autoencendido es parte fundamental de su funcionamiento. No obstante, la sobrealimentación afecta al funcionamiento Diesel de formas importantes:

- **Una mayor presión de admisión** incrementa la disponibilidad de oxígeno y permite mayores caudales de combustible inyectado → mayor potencia.
- El aumento de presión durante la combustión puede reducir ligeramente el comportamiento efectivo de corte (según la estrategia de inyección), mejorando a menudo las tendencias de eficiencia.
- **Mayores temperaturas** pueden incrementar la formación de ciertos contaminantes (en particular la tendencia a formar NOx), por lo que la gestión térmica y el postratamiento cobran aún más importancia.

#### Papel del intercooling en motores Diesel

El intercooling no es estrictamente necesario para la estabilidad del encendido, pero puede ser beneficioso:

- **Aumento de potencia:** aire más frío → mayor densidad → más masa aspirada a la misma presión de sobrealimentación.
- **Menores temperaturas máximas:** puede reducir el esfuerzo térmico y ayudar a disminuir la formación de contaminantes.
- **Efectos sobre la forma del ciclo:** el enfriamiento de la admisión puede alterar las condiciones dentro del cilindro y el desarrollo efectivo de la combustión; según cómo se gestionen el combustible y el avance, puede afectar ligeramente al comportamiento tipo corte y a la eficiencia térmica global.

El intercooling pasa así a ser una herramienta de optimización a nivel de sistema, más que una necesidad estricta.

---

(subsec_icre_gasoline_evolution)=
### Evolución tecnológica de los motores de gasolina (encendido provocado)

Históricamente, los motores de encendido provocado han dependido de un **control cuantitativo de carga** (mariposa) y de condiciones de mezcla próximas a la estequiometría para garantizar un encendido estable y la compatibilidad con el catalizador. Con el tiempo, sus estrategias de alimentación y combustión han evolucionado para reducir el consumo de combustible y las emisiones, y para mitigar las pérdidas de bombeo.

Una progresión tecnológica simplificada es la siguiente:

1. **Carburadores (basados en Venturi):**  
   Mecánicamente simples, pero limitados en precisión de control de mezcla y en eficiencia. Pueden funcionar sin un control electrónico sofisticado, pero están prácticamente obsoletos en la automoción moderna.

2. **Inyección en el colector o puerto de admisión (inyección indirecta):**  
   Inyectores de baja presión suministran combustible al colector de admisión o al puerto de admisión. Esto mejoró el control de la mezcla, la respuesta transitoria y las emisiones frente a la carburación.

3. **Inyección directa (DI) en la cámara de combustión:**  
   Inyectores de alta presión (del orden de cientos de bar en implementaciones modernas) permiten un mejor control de la formación de la mezcla y pueden sustentar estrategias que:
   - reduzcan las pérdidas de bombeo,
   - mejoren la estabilidad de la combustión en ciertos regímenes,
   - permitan funcionamiento con **carga estratificada** en determinadas condiciones.

4. **Hacia conceptos de gasolina similares al encendido por compresión:**  
   Una gran línea de investigación y desarrollo busca alcanzar mayores eficiencias haciendo funcionar motores de gasolina con mayor compresión efectiva y modos de combustión más próximos al encendido por compresión (diversas estrategias “sin chispa” o de modo mixto). El objetivo de fondo es combinar las propiedades del combustible gasolina con mecanismos de eficiencia propios del Diesel, controlando al mismo tiempo la estabilidad de la combustión y las emisiones.

:::{tip}

**QUÉ IMPULSA ESTA EVOLUCIÓN**

La mayoría de las innovaciones en motores MEP responden a tres limitaciones prácticas:
- ineficiencia a carga parcial debida al estrangulamiento (pérdidas de bombeo),
- limitaciones por picado a alta carga/sobrealimentación,
- requisitos de emisiones y de postratamiento.

Por ello, los motores MEP modernos son cada vez más “motores-sistema”: combustión, sobrealimentación y control se diseñan de forma conjunta.

:::

---

(subsec_icre_diesel_evolution)=
### Evolución tecnológica de los motores Diesel (encendido por compresión)

Los motores Diesel regulan la potencia cualitativamente variando el combustible inyectado, mientras que normalmente admiten masas de aire similares (sin mariposa en los diseños clásicos). Históricamente, los sistemas de inyección Diesel evolucionaron para mejorar la atomización, la mezcla, el control de la combustión y las emisiones.

#### Sistemas de inyección indirecta (precámara)

Los primeros diseños Diesel utilizaron ampliamente arquitecturas de **precámara** (inyección indirecta):

- El combustible se inyecta en una pequeña precámara donde la turbulencia favorece la mezcla.
- La combustión inicial tiene lugar en la precámara, produciendo un aumento de presión que impulsa el flujo a través de un orificio hacia la cámara principal, donde la combustión continúa.

Entre las ventajas históricamente atribuidas a este enfoque se encuentran:

- mejora de la mezcla en determinadas condiciones,
- aumento de presión potencialmente más suave,
- inyectores situados lejos de la zona de combustión más severa, reduciendo ensuciamiento y carga térmica.

Sin embargo, la inyección indirecta también introduce inconvenientes:

- mayores pérdidas por transferencia de calor debido a relaciones superficie/volumen más altas y fuertes gradientes térmicos cerca de la culata,
- geometría de cámara de combustión más compleja,
- funcionamiento potencialmente menos estable que el de una inyección directa moderna optimizada.

#### Inyección directa y sistemas common rail

Los motores Diesel modernos emplean predominantemente **inyección directa common rail** con control electrónico:

- El combustible se suministra a un conducto de alta presión (un colector común).
- Cada inyector se alimenta desde ese conducto.
- Una unidad de control electrónico regula el instante de inyección, su duración, la presión y, en su caso, múltiples eventos de inyección (piloto/principal/post) para dar forma a la combustión.

Las altas presiones de inyección (del orden de miles de bar en los sistemas actuales) favorecen:

- una atomización fina,
- evaporación y mezcla más rápidas,
- mejor control del retardo al autoencendido y de la tasa de liberación de calor,
- compromisos más favorables entre eficiencia, ruido y emisiones.

Un esquema conceptual del sistema es:

- alimentación a baja presión desde el depósito,
- bomba de transferencia que alimenta una bomba de alta presión,
- bomba de alta presión que alimenta el conducto common rail,
- conducto que distribuye combustible a los inyectores bajo control electrónico.

:::{important}

**EL PROGRESO DIESEL ES CONTROL DE LA COMBUSTIÓN**

El common rail no es simplemente “más presión”. La ventaja clave es la capacidad de **moldear la historia de liberación de calor** mediante una programación de inyección precisa y flexible. Eso repercute directamente en la eficiencia, las tasas de aumento de presión, el ruido y la formación de contaminantes.

:::

---

(subsec_icre_overfeeding_closure)=
### Cierre conceptual

- La sobrealimentación incrementa la densidad de potencia del motor al aumentar la **masa de aire aspirada** por ciclo.
- Los turbocompresores extraen energía del escape para accionar la compresión, pero introducen contrapresión y retos de respuesta transitoria; el intercooling suele ser esencial.
- Los compresores mecánicos proporcionan una gran respuesta a bajo régimen, pero imponen un consumo parasitario de potencia; las estrategias híbridas de sobrealimentación pueden combinar ventajas.
- En motores MEP, la sobrealimentación está limitada por el **picado**; el intercooling y el control de la combustión son elementos centrales para lograr altas prestaciones con una eficiencia aceptable.
- En motores Diesel, la sobrealimentación es naturalmente compatible con el encendido por compresión, pero la gestión térmica y de emisiones cobra aún más importancia; el intercooling es una poderosa palanca de sistema.
- La evolución de las tecnologías MEP y Diesel está impulsada por los objetivos acoplados de eficiencia, cumplimiento de emisiones y conducibilidad, logrados mediante mejores sistemas de alimentación, arquitecturas de sobrealimentación y control electrónico.

