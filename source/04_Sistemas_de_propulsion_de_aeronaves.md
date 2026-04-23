(sec_aircraft_gas_turbines)=
## Sistemas de propulsión de aeronaves

La tecnología de turbinas de gas se emplea en dos aplicaciones amplias y conceptualmente distintas: **la generación estacionaria de potencia** y **la propulsión aeronáutica**. Aunque ambas se basan en ciclos de gas derivados del ciclo Brayton, sus objetivos, métricas de rendimiento y restricciones de diseño difieren de manera fundamental.

En las **turbinas de gas estacionarias**, el objetivo principal es la generación de una potencia mecánica o eléctrica neta de salida. Estos sistemas suelen instalarse en centrales eléctricas o en grandes buques, donde el tamaño y el peso son preocupaciones secundarias y es habitual la operación continua cerca de las condiciones de diseño. La búsqueda de mayores eficiencias térmicas en tales aplicaciones ha conducido a configuraciones avanzadas, entre ellas los ciclos combinados gas–vapor.

En cambio, las **turbinas de gas aeronáuticas** son sistemas de propulsión. Su propósito no es entregar potencia al eje de forma directa, sino generar **empuje** acelerando un fluido de trabajo. El peso, el área frontal, el ruido, el consumo de combustible y el rendimiento en amplios rangos de velocidad y altitud pasan a ser restricciones de diseño dominantes. Estas diferencias justifican un análisis separado de los motores aeronáuticos, aunque los principios termodinámicos subyacentes sigan estando estrechamente relacionados con los de las turbinas de gas estacionarias.

---

(subsec_aircraft_power_orders)=
### Órdenes de magnitud en la propulsión aeronáutica

Los niveles de potencia implicados en la propulsión aeronáutica son extremadamente grandes en comparación con los de los vehículos terrestres convencionales. Como ilustración, una aeronave comercial de fuselaje ancho, como el Boeing 777, equipada con dos motores General Electric GE90-115B, requiere del orden de $23\ \text{MW}$ por motor durante el crucero a plena carga.

Recordando que $1\ \text{hp} = 0.7457\ \text{kW}$, un solo motor operando a este nivel corresponde aproximadamente a $31\,000\ \text{hp}$. Como comparación, un coche de Fórmula 1 desarrolla aproximadamente $1\,000\ \text{hp}$, mientras que un automóvil de pasajeros típico entrega alrededor de $100\ \text{hp}$. Durante el despegue se alcanzan niveles de potencia aún mayores: por ejemplo, el Airbus A380, equipado con cuatro motores GP7200, puede requerir una potencia total superior a $300\ \text{MW}$.

Estas cifras ponen de manifiesto los extraordinarios flujos de energía involucrados en los sistemas de propulsión aeronáutica.

---

(subsec_aircraft_engine_types)=
### Principales sistemas propulsivos de aeronaves

Las turbinas de gas aeronáuticas se diseñan de acuerdo con el régimen operativo previsto, lo que da lugar a varias arquitecturas de motor claramente diferenciadas.

- **Motores turborreactores**

    El **turborreactor** representa la forma más simple de propulsión mediante turbina de gas y se basa directamente en el ciclo Brayton. Avanzando en la dirección del flujo, un turborreactor consta de:

    - un **difusor**, que desacelera el aire entrante,
    - un **compresor**, que eleva la presión del flujo,
    - una **cámara de combustión**, donde se añade calor,
    - una **turbina**, que acciona el compresor y los sistemas auxiliares,
    - una **tobera**, que convierte la entalpía en energía cinética.

    Los turborreactores son compactos y capaces de operar a velocidades de vuelo muy elevadas. Sin embargo, presentan un alto consumo de combustible, niveles de ruido elevados y una baja eficiencia a bajas velocidades.

<br/>

- **Motores turbohélice**

    En un **turbohélice**, la turbina acciona un eje conectado a una caja reductora y a una hélice. La mayor parte de la propulsión es proporcionada por la hélice y no por el chorro de escape.

    Esta configuración da lugar a:

    - menores velocidades de escape,
    - mayor eficiencia propulsiva a bajas velocidades,
    - un consumo de combustible significativamente menor en comparación con los turborreactores.

    Los turbohélices son muy adecuados para vuelos a baja velocidad y baja altitud, como en aviones de carga y helicópteros. Sus principales limitaciones se deben al peso del conjunto caja reductora–hélice y al inicio de condiciones sónicas en las puntas de las palas de la hélice, lo que restringe su velocidad máxima de operación.

<br/>

- **Motores turbofán**

    El **turbofán** combina características de los turborreactores y los turbohélices, y es el sistema de propulsión más ampliamente utilizado en la aviación comercial. Una parte del aire entrante evita el núcleo del motor y es acelerada por un gran ventilador.

    Esta configuración:

    - incrementa la eficiencia propulsiva,
    - reduce los niveles de ruido,
    - proporciona refrigeración adicional a los componentes del motor.

    Los turbofanes son más eficientes que los turborreactores en un amplio rango de velocidades subsónicas, aunque su mayor área frontal y su mayor peso reducen su efectividad a altitudes muy elevadas.

---

(subsec_high_speed_engines)=
### Propulsión a velocidades subsónicas altas y supersónicas

A mayores velocidades de vuelo se emplean conceptos alternativos de propulsión.

- **Estatorreactores** (*ramjets*) operan sin compresores ni turbinas. La compresión se logra mediante la desaceleración del flujo entrante de alta velocidad. Se inyecta combustible, tiene lugar la combustión y la expansión se produce a través de una tobera. Los estatorreactores son eficaces a velocidades subsónicas altas y supersónicas, pero no pueden operar desde reposo.

- **Estatorreactores de combustión supersónica** (*scramjets*) son una variación en la que la combustión ocurre en condiciones de flujo supersónico. Estos motores no contienen maquinaria rotativa y consisten esencialmente en un conducto con una geometría determinada. Los *scramjets* no operan según un ciclo Brayton y representan la arquitectura más simple desde el punto de vista mecánico.

- **Motores cohete** difieren de forma fundamental de los motores aerorreactores. Transportan tanto el combustible como el oxidante y no dependen del aire atmosférico. Sus principios de funcionamiento quedan fuera del alcance del análisis de turbinas de gas basado en el ciclo Brayton.

---

(subsec_propulsion_parameters)=
### Parámetros de rendimiento de los sistemas propulsivos

Para evaluar y comparar sistemas de propulsión, se definen varias magnitudes características.

El **empuje** producido por el motor viene dado por:

(eq_thrust)=
$$
F = \dot{m}{}(c_{\text{out}} - c_{\text{in}}),
$$

donde $\dot{m}$ es el caudal másico y $c$ denota la velocidad del flujo.

La **potencia térmica suministrada** por el combustible es:

(eq_thermal_power)=
$$
\dot{Q}_{\text{th}} = \dot{m}_{\text{fuel}}{\cdot}\text{LHV},
$$

donde $\text{LHV}$ es el poder calorífico inferior del combustible.

La **potencia añadida al flujo** está asociada al cambio de energía cinética:

(eq_power_flow)=
$$
\dot{W}_{\text{flow}} = \frac{1}{2}{}\dot{m}{}(c_{\text{out}}^2 - c_{\text{in}}^2).
$$

La **potencia propulsiva** se define como:

(eq_propulsive_power)=
$$
\dot{W}_{\text{prop}} = c_{\text{flight}}{\cdot}F,
$$

donde $c_{\text{flight}}$ es la velocidad de vuelo.

---

(subsec_efficiencies)=
### Eficiencias en la propulsión de aeronaves

A partir de las definiciones anteriores, se introducen tres eficiencias:

- **Eficiencia térmica:**

  $$
  \eta_{\text{th}} = \frac{\dot{W}_{\text{flow}}}{\dot{Q}_{\text{th}}}.
  $$

- **Eficiencia propulsiva:**

  $$
  \eta_{\text{prop}} = \frac{\dot{W}_{\text{prop}}}{\dot{W}_{\text{flow}}}.
  $$

- **Eficiencia global (motopropulsiva):**

  $$
  \eta_{\text{global}} = \frac{\dot{W}_{\text{prop}}}{\dot{Q}_{\text{th}}} = \eta_{\text{th}}{\cdot}\eta_{\text{prop}}.
  $$

Los distintos sistemas de propulsión presentan tendencias de eficiencia diferentes en función de la velocidad de vuelo. Los turbohélices son más eficientes a bajas velocidades, los turbofanes dominan un amplio régimen subsónico y los turborreactores se vuelven ventajosos a velocidades muy elevadas.

---

(subsec_specific_impulse)=
### Impulso específico y consumo de combustible

Un indicador adicional de rendimiento es el **impulso específico**, $I_{\text{sp}}$, definido como:

(eq_specific_impulse)=
$$
I_{\text{sp}} = \frac{F}{g_0{\cdot}\dot{m}},
$$

donde $g_0$ es la aceleración gravitatoria estándar y $\dot{m}$ es el caudal másico de combustible o propelente.

El impulso específico mide cuán eficientemente un sistema de propulsión utiliza su propelente. Un impulso específico alto implica un menor consumo de combustible para un determinado empuje y tiempo de operación.

El impulso específico está relacionado de forma inversa con el **consumo específico de combustible**, que cuantifica el combustible requerido para producir un determinado empuje durante un cierto intervalo de tiempo.

---

(subsec_aircraft_conceptual_closure)=
### Cierre conceptual

- Las turbinas de gas de las aeronaves son sistemas de propulsión, no generadores de potencia.
- Sus prioridades de diseño difieren de manera fundamental de las de las turbinas de gas estacionarias.
- Los turborreactores, turbohélices y turbofanes responden a distintos regímenes de vuelo.
- Los estatorreactores y los *scramjets* operan sin maquinaria rotativa y no siguen un ciclo Brayton.
- El empuje, las eficiencias y el impulso específico son métricas clave de rendimiento.
- Los turbofanes proporcionan la mayor eficiencia en la mayoría de las condiciones subsónicas del vuelo comercial.

