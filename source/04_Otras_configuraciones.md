(sec_other_configurations)=
## Otras configuraciones

Tras haber estudiado los ciclos Rankine ideal y real, junto con modificaciones como el recalentamiento y la regeneración, pasamos ahora a configuraciones alternativas utilizadas en la industria. Estos diseños responden a necesidades específicas, como el aprovechamiento de fuentes de calor a baja temperatura o la maximización de la eficiencia mediante la combinación de distintos ciclos termodinámicos.

---

(subsec_cogeneration)=
### Cogeneración

En los ciclos de potencia estándar estudiados hasta ahora, el único objetivo es convertir calor en **trabajo** (electricidad), que es la forma de energía de mayor valor. El calor restante se rechaza al entorno (lago, océano, atmósfera) porque se considera de calidad demasiado baja como para resultar útil.

Sin embargo, muchas industrias requieren grandes aportes de energía térmica, conocidos como **calor de proceso**.
* **Industrias:** química, papelera, refino de petróleo, siderurgia, procesado de alimentos y textil.
* **Requisitos:** vapor típicamente entre $5$ y $7\ \text{atm}$ y temperaturas de $150\text{--}200 \ ^\circ\text{C}$.

**El problema termodinámico:**
Tradicionalmente, estas industrias queman combustible (carbón, gas, petróleo) únicamente para generar este vapor de baja temperatura. Esto es muy ineficiente porque la combustión del combustible genera temperaturas muy elevadas (energía de alta calidad), que después se degradan inmediatamente para producir vapor a baja temperatura (energía de baja calidad). Utilizar un potencial de alta calidad para realizar una tarea de baja calidad supone un despilfarro de exergía.

**La solución:**
Dado que estas industrias necesitan tanto **electricidad** como **calor de proceso**, tiene sentido producir primero la electricidad y utilizar después el calor “residual” de ese proceso para abastecer la planta industrial.

**Definición:**
La **cogeneración** es la producción de más de una forma de energía útil (normalmente calor de proceso + electricidad) a partir de una única fuente de energía.

---

(subsec_combined_cycle)=
### Ciclo combinado (gas-vapor)

La búsqueda constante de una mayor eficiencia térmica llevó a los ingenieros a combinar distintos ciclos. La configuración más importante es el **ciclo combinado gas-vapor**, que sitúa un ciclo de potencia de gas sobre un ciclo de potencia de vapor.

**La sinergia:**
* **Ciclo de gas (Brayton):** opera a temperaturas muy elevadas. Las turbinas de gas modernas soportan temperaturas de entrada de hasta $1425 \ ^\circ\text{C}$ (gracias a recubrimientos cerámicos y refrigeración de los álabes). Sin embargo, descargan gases a temperaturas todavía elevadas ($>500 \ ^\circ\text{C}$), lo que representa un potencial desaprovechado.
* **Ciclo de vapor (Rankine):** está limitado por restricciones metalúrgicas a aproximadamente $620\ ^\circ\text{C}$.

**Cómo funciona:**
En lugar de desperdiciar los gases calientes de escape de la turbina de gas, estos se conducen hacia un intercambiador de calor que actúa como la **caldera** (evaporador) de un ciclo de vapor situado “debajo”.
1.  **Parte superior:** la turbina de gas produce trabajo y gases de escape calientes.
2.  **Parte inferior:** el ciclo de vapor utiliza ese escape para hervir agua y producir más trabajo.

**Resultado:**
El ciclo combinado aprovecha la capacidad de las turbinas de gas para trabajar a altas temperaturas y la capacidad de los ciclos de vapor para recuperar calor. Las eficiencias térmicas pueden superar el **$60\%$**, significativamente por encima de las de cualquiera de los dos ciclos operando por separado.

---

(subsec_working_fluid_characteristics)=
### Características deseables de un fluido de trabajo

El agua es el fluido más habitual porque es barata y abundante, pero termodinámicamente no es “ideal”. Un fluido de trabajo ideal poseería la siguiente lista de propiedades deseables:

1.  **Alta temperatura crítica:** esto permite transferencia de calor isotérmica a altas temperaturas (más cercana a la eficiencia de Carnot).
2.  **Presión máxima segura:** las altas temperaturas no deberían requerir presiones peligrosamente elevadas que sometan a los materiales a esfuerzos excesivos.
3.  **Bajo punto triple:** debe estar por debajo de la temperatura del entorno para evitar que el fluido se congele durante paradas o en condensadores fríos.
4.  **Presión de condensación manejable:** la presión de saturación a temperatura ambiente no debería ser extremadamente baja (vacío). Presiones muy por debajo de la atmosférica permiten la entrada de aire en el sistema, lo cual es perjudicial.
5.  **Alta entalpía de vaporización:** permite grandes transferencias de calor con bajos caudales másicos (bombas y tuberías más pequeñas).
6.  **Campana de saturación en “U invertida”:** la forma de la campana debería favorecer una expansión seca, eliminando la necesidad de recalentamiento o de un sobrecalentamiento excesivo para evitar humedad en la turbina.
7.  **Propiedades físicas:** alta conductividad térmica, no tóxico, químicamente inerte y barato.

---

(subsec_organic_rankine)=
### Ciclo Rankine orgánico (ORC)

Como no existe un fluido perfecto, los ingenieros seleccionan el fluido en función de la aplicación. Para **fuentes de calor a baja temperatura** (calor residual industrial, geotermia, captadores solares), el agua suele ser una mala opción porque hervirla requiere temperaturas elevadas o presiones de vacío.

**La solución:**
Los **ciclos Rankine orgánicos** sustituyen el agua por fluidos orgánicos (refrigerantes, hidrocarburos).

**Ventajas:**
* Hierven a temperaturas más bajas, lo que los hace perfectos para recuperar calor de baja calidad.
* **La campana de saturación:** muchos fluidos orgánicos presentan una campana de saturación cuya forma hace que la expansión isoentrópica permanezca naturalmente en la región seca y sobrecalentada. Esto elimina el riesgo de erosión de los álabes de la turbina y suprime la necesidad de sobrecalentamiento.

---

(subsec_binary_cycle)=
### Ciclo binario

Un **ciclo binario** utiliza dos lazos Rankine con fluidos distintos: uno para altas temperaturas y otro para temperaturas más bajas.
* **Ciclo superior:** utiliza un fluido con temperatura crítica muy alta (p. ej., mercurio, sodio, potasio).
* **Ciclo inferior:** utiliza agua.
* **Interfaz:** el condensador del ciclo superior actúa como caldera del ciclo inferior.

**El ejemplo del mercurio:**
El mercurio tiene una temperatura crítica de $898 \ ^\circ\text{C}$ (excelente para absorción de calor a alta temperatura) y una baja presión crítica.
* *¿Por qué no utilizar solo mercurio?* A temperaturas ambiente ($32 \ ^\circ\text{C}$), la presión de saturación del mercurio es prácticamente nula ($0.07\ \text{Pa}$). Mantener un vacío así es imposible.
* *La solución:* utilizar mercurio solo en el lazo de alta temperatura. Condensarlo en torno a $237 \ ^\circ\text{C}$ (donde su presión es manejable) y emplear ese calor para hervir agua en el lazo inferior.

**Resultado:**
Los ciclos binarios aproximan el ciclo de Carnot más estrechamente que un ciclo simple de agua, alcanzando eficiencias $>50\%$. Sin embargo, debido a la toxicidad y al coste de fluidos como el mercurio, han sido en gran medida sustituidos por los **ciclos combinados** (gas-vapor), que son más seguros y todavía más eficientes.

---

(subsec_configurations_closure)=
### Cierre conceptual

* La **cogeneración** evita el despilfarro de calor de baja calidad al generar electricidad *antes* de suministrar vapor de proceso a las industrias, maximizando la utilidad total del combustible.
* Los **ciclos combinados** representan el actual patrón de referencia en eficiencia ($>60\%$) al superponer un ciclo de gas de alta temperatura sobre un ciclo de vapor de temperatura media.
* **Fluidos de trabajo:** el agua es el estándar, pero los **fluidos orgánicos** son superiores para la recuperación de calor de baja calidad (ORC), y los metales líquidos (mercurio/sodio) se emplearon históricamente en **ciclos binarios** para empujar los límites de temperatura antes de que las turbinas de gas se volvieran dominantes.
* **El objetivo:** toda configuración —ya sea modificando la disposición del ciclo o cambiando el fluido— busca adaptar mejor la fuente de calor al proceso termodinámico, minimizando la destrucción de exergía.

