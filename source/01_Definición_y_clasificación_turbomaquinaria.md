(sec_gas_cycles_intro)=
## Ciclos de gas y turbomáquinas

La termodinámica encuentra uno de sus campos de aplicación más destacados en la **generación de potencia**. En tales aplicaciones, la conversión de energía se logra mediante sistemas que operan según un **ciclo termodinámico**, es decir, un proceso en el que los estados inicial y final del fluido de trabajo coinciden. Los ciclos cuyo propósito es proporcionar una potencia neta de salida se denominan **ciclos de potencia**.

Los dispositivos que operan siguiendo un ciclo de potencia y entregan potencia mecánica útil se conocen comúnmente como **motores térmicos** o, simplemente, **motores**. Su clasificación puede abordarse desde distintas perspectivas, dependiendo de la naturaleza del fluido de trabajo, de cómo se maneja dicho fluido y de la manera en que se suministra calor durante el ciclo.

---

(subsec_classification_power_cycles)=
### Clasificación de los ciclos de potencia

Un primer nivel de clasificación se refiere al **estado termodinámico del fluido de trabajo** durante el ciclo:

- **Ciclos de gas:**  
  El fluido de trabajo permanece en estado gaseoso durante todo el ciclo. Ejemplos típicos son los motores de automóviles y los motores aeronáuticos.

- **Ciclos de vapor:**  
  El fluido de trabajo experimenta cambio de fase durante parte del ciclo y puede existir como mezcla bifásica. Los ciclos de vapor empleados en centrales térmicas y nucleares pertenecen a esta categoría, al igual que los ciclos combinados.

Una segunda clasificación distingue los ciclos según si el fluido de trabajo es **recirculado** o **renovado**:

- **Ciclos cerrados:**  
  El fluido de trabajo se recircula y regresa a su estado termodinámico inicial al final de cada ciclo. Ciertos ciclos combinados utilizados en centrales eléctricas operan de esta manera.

- **Ciclos abiertos:**  
  El fluido de trabajo se descarga al entorno al final del proceso y se introduce fluido fresco en el sistema. Aunque el dispositivo opera de forma mecánicamente cíclica, el fluido de trabajo no completa un ciclo termodinámico cerrado. Los motores de automóviles y de aeronaves son ejemplos típicos de ciclos abiertos.

Por último, los ciclos de potencia pueden clasificarse según el **modo de adición de calor**:

- **Ciclos de combustión interna:**  
  El calor se suministra mediante la combustión del combustible dentro de los límites del sistema, como ocurre en los motores de automóviles y aeronaves.

- **Ciclos de combustión externa:**  
  El calor se suministra desde una fuente externa, como un horno, un reactor nuclear o una fuente geotérmica, sin contacto directo entre el combustible y el fluido de trabajo.

---

(subsec_gas_cycles_scope)=
### Alcance de los ciclos de gas

La siguiente parte del curso está dedicada a los **ciclos de gas**, es decir, ciclos de potencia en los que se emplea una mezcla de aire y combustible para generar una potencia neta de salida, sin que ocurra cambio de fase durante el proceso.

Existen varios ciclos de gas clásicos, tradicionalmente identificados por nombres específicos asociados a su realización práctica. Entre ellos, los más relevantes son:

- el **ciclo Otto**, representativo de los motores de encendido por chispa (gasolina),
- el **ciclo Diesel**, representativo de los motores de encendido por compresión.

Estos ciclos, característicos de los motores alternativos de combustión interna, se abordarán en la próxima lección.

El presente tema se centra, en cambio, en el **ciclo Brayton**, que constituye la base tanto de los motores aeronáuticos como de las turbinas de gas estacionarias. En estos sistemas, el fluido de trabajo circula de manera continua a través de dispositivos rotativos, experimentando compresión, combustión y expansión. Por esta razón, los motores de ciclo Brayton se clasifican como **turbomáquinas**, y constituyen **sistemas abiertos**.

---

(subsec_turbomachines_intro)=
### Turbomáquinas

Las turbomáquinas admiten varios niveles de clasificación. Una primera distinción se basa en la **naturaleza del fluido de trabajo**:

- **Turbomáquinas hidráulicas**, que operan con fluidos incompresibles (líquidos).  
  Estas no se considerarán en el presente módulo.

- **Turbomáquinas térmicas**, que operan con fluidos compresibles (gases).  
  Estas son el foco de la discusión actual.

Independientemente del fluido de trabajo, las turbomáquinas pueden clasificarse según su **papel energético**:

- **Generadoras:**  
  Dispositivos que aumentan la energía del fluido. En las turbomáquinas térmicas, este papel lo desempeñan los **compresores**, que elevan la presión del fluido, y las **hélices**, que incrementan la energía cinética del flujo.

- **Receptoras:**  
  Dispositivos que extraen energía del fluido y producen una potencia neta de salida. Las turbinas de gas y de vapor pertenecen a esta categoría.

En las turbomáquinas térmicas, la extracción de energía puede producirse mediante:

- una reducción de la **entalpía**, como en las turbinas de gas y de vapor,
- una reducción de la **energía cinética**, como en ciertas aeroturbinas.

---

(subsec_gas_turbine_applications)=
### Aplicaciones de los sistemas de turbinas de gas

Las turbomáquinas térmicas estudiadas en este módulo son aquellas que proporcionan una **potencia neta de salida**. Dependiendo de su finalidad, se emplean distintas configuraciones:

- **Turbinas de gas estacionarias**, cuyo único objetivo es la generación de potencia mecánica y eléctrica. Estos sistemas se utilizan ampliamente en centrales de ciclo combinado, en grandes sistemas de propulsión marina y en aplicaciones industriales pesadas.

- **Turbinas de gas de propulsión**, cuyo objetivo es incrementar la energía cinética de los gases de escape para generar empuje, como en los motores aeronáuticos. Aunque el ciclo de gas subyacente es el mismo, existen diferentes arquitecturas de propulsión, como el **turborreactor**, el **turbofán** y el **turbohélice**. Su análisis detallado se pospone hasta que el ciclo Brayton haya sido estudiado a fondo.

---

(subsec_gas_cycles_conceptual_closure)=
### Cierre conceptual

- Los ciclos de potencia son ciclos termodinámicos diseñados para producir potencia mecánica neta.
- Los ciclos de gas operan íntegramente con el fluido de trabajo en fase gaseosa.
- Los ciclos de potencia pueden clasificarse según el estado del fluido, la renovación del fluido y el mecanismo de adición de calor.
- El ciclo Brayton constituye la base de las turbinas de gas y de los motores aeronáuticos.
- Las turbomáquinas son dispositivos de flujo continuo que intercambian energía con un fluido.
- Las turbinas de gas pueden diseñarse para generación estacionaria de potencia o para propulsión.

