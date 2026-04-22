(sec_icre_parameters)=
## Parámetros fundamentales y características de los MACIs

Tras describir y clasificar los **motores alternativos de combustión interna (MACIs)** e introducir sus componentes principales, la exposición puede centrarse ahora en lo que más importa en un curso de termodinámica: el propio **ciclo termomecánico**. A partir de este punto, el objetivo es describir la evolución de la presión, la temperatura y el volumen dentro del cilindro de una forma que permita el modelado de ciclos ideales (Otto/Diesel) y, más adelante, la inclusión de las pérdidas de los ciclos reales.

Para ello, introducimos los principales parámetros **geométricos**, **volumétricos**, **de combustión** y **relacionados con la potencia** que caracterizan al motor.

---

(subsec_icre_geometric_parameters)=
### Parámetros geométricos

El sistema cinemático fundamental de un motor alternativo es el mecanismo **cámara de combustión–pistón–biela–cigüeñal**. Los parámetros geométricos estándar empleados para describirlo son:

- $\theta$: **ángulo del cigüeñal**, definido como $\theta=0^\circ$ cuando la biela y la manivela están alineadas en su máxima extensión.
- **PMS (punto muerto superior)**: posición del pistón correspondiente a $\theta=0^\circ$.
- **PMI (punto muerto inferior)**: posición del pistón correspondiente a $\theta=180^\circ$.
- $b$: **diámetro del cilindro** (*bore*), es decir, el diámetro del pistón.
- $l$: **longitud de la biela**, modelada típicamente como una barra recta rígida.
- $a$: **radio de manivela**.
- $s = 2a$: **carrera**, es decir, el desplazamiento del pistón entre PMS y PMI.

La **relación carrera-diámetro**, $s/b$, es un importante indicador geométrico. Sus valores típicos son:

- motores de automoción de **encendido por chispa (EC)**: $0.6 \le s/b \le 1.1$,
- motores de automoción de **encendido por compresión (ECmp)**: $0.9 \le s/b \le 1.2$,
- motores ECmp de cuatro tiempos, lentos y de mayor tamaño (por ejemplo, camiones y pequeños buques): $1.2 \le s/b \le 1.4$,
- grandes motores marinos ECmp de dos tiempos: $1.8 \le s/b \le 3$.

:::{note}

**POR QUÉ IMPORTA $s/b$**

La relación carrera-diámetro influye en:
- la velocidad media del pistón para un régimen de giro dado (y, por tanto, en la fricción y el desgaste),
- las relaciones entre área de transferencia de calor y volumen,
- el empaquetamiento mecánico y el régimen de giro alcanzable,
- y, de manera indirecta, en las características de la combustión a través de la geometría de la cámara.

:::

---

(subsec_icre_volumes_compression_displacement)=
### Volúmenes, relación de compresión y cilindrada

Más allá de los parámetros de escala longitudinal, la geometría del motor suele describirse mediante **volúmenes** y **relaciones de volúmenes**:

- $V_1$: volumen del cilindro en **PMI** (volumen máximo).
- $V_2$: volumen del cilindro en **PMS** (volumen mínimo, volumen de holgura o de cámara).
- $V_d$: **volumen desplazado** (volumen barrido), definido como:
  
  $$
  V_d = V_1 - V_2 = \frac{\pi}{4} b^2 s .
  $$

La **relación de compresión** se define como:

$$
r = \frac{V_1}{V_2}.
$$

:::{important}

**LA RELACIÓN DE COMPRESIÓN ES UNA RELACIÓN DE VOLÚMENES**

En los MACIs, $r$ es una relación de **volúmenes**, no de presiones.  
Esto contrasta con el ciclo Brayton, donde la relación característica es la **relación de presiones**.

:::

La **cilindrada del motor** (volumen barrido total) es:

$$
V_{d,\text{mot}} = Z\,V_d,
$$

siendo $Z$ el número de cilindros.

---

(subsec_icre_heat_input_combustion_parameters)=
### Aporte de calor y parámetros de combustión

Para conectar el funcionamiento del motor con el modelado de ciclos termodinámicos, resulta útil relacionar la energía liberada por el combustible con un **aporte de calor** equivalente.

#### Modelo estándar de aire frío (hipótesis air-standard)

Un punto de partida habitual es el **modelo estándar de aire frío**, que supone que:

- el aire es el fluido de trabajo, modelado como un **gas ideal**,
- todos los procesos son internamente reversibles,
- la combustión se sustituye por un proceso equivalente de **adición de calor**,
- el escape y la admisión se sustituyen por un proceso de **rechazo de calor** que devuelve el aire al estado inicial,
- el aire posee calores específicos constantes e iguales a sus valores a $25^\circ\text{C}$.

Bajo estas hipótesis, el calor aportado por unidad de masa de aire puede expresarse utilizando el poder calorífico inferior del combustible y la relación aire-combustible.

#### Aporte de calor con mezcla aire-combustible

Sea:

- $q_{\text{in}}$ el calor añadido (unidades habituales: $\text{kJ/kg aire}$ o $\text{kJ/kg mezcla}$),
- $\text{PCI}$ el **poder calorífico inferior** del combustible ($\text{kJ/kg combustible}$),
- $A_s$ la relación aire-combustible **estequiométrica** ($\text{kg aire}/\text{kg combustible}$),
- $A$ la relación aire-combustible real ($\text{kg aire}/\text{kg combustible}$),
- $\lambda$ la **relación relativa aire-combustible** (factor de exceso de aire), de modo que

  $$
  A = \lambda A_s .
  $$

Entonces, al trabajar por unidad de masa de aire:

$$
q_{\text{in}} = \frac{\text{PCI}}{A}
= \frac{\text{PCI}}{\lambda A_s}.
$$

Si el fluido de trabajo se considera como la **mezcla aire-combustible** en lugar de considerar únicamente el aire, entonces, por unidad de masa de mezcla:

$$
q_{\text{in}} = \frac{\text{PCI}}{1 + A}
= \frac{\text{PCI}}{1 + \lambda A_s}.
$$

:::{tip}

**ELECCIÓN DE LA BASE ($\text{kg aire}$ frente a $\text{kg mezcla}$)**

En la práctica se utilizan ambas definiciones.  
Para el análisis ideal de los ciclos Otto/Diesel, suele ser conveniente trabajar por unidad de masa de aire, porque el modelo estándar trata el fluido de trabajo como aire durante todo el ciclo.

:::

---

(subsec_icre_power)=
### Potencia y caudal másico de aire

Una magnitud clave de prestaciones es la **potencia**, definida como:

$$
\text{Pot} = \dot{m}_{\text{air}}\, w_{\text{net}},
$$

donde:

- $\text{Pot}$ es la potencia ($\text{kW}$),
- $w_{\text{net}}$ es el **trabajo neto específico** ($\text{kJ/kg}$),
- $\dot{m}_{\text{air}}$ es el caudal másico de aire ($\text{kg/s}$).

Una estimación práctica de $\dot{m}_{\text{air}}$ puede construirse a partir de la geometría y del régimen de giro. Aproximando el caudal másico de aire admitido como:

- densidad por volumen por ciclo por número de ciclos por segundo,

se obtiene:

$$
\dot{m}_{\text{air}} = \rho \left(\frac{\pi}{4} b^2\right) s \left(\frac{N}{60}\right)iZ,
$$

y, por tanto:

$$
\text{Pot}
= w_{\text{net}} \, \rho \left(\frac{\pi}{4} b^2\right) s \left(\frac{N}{60}\right)iZ .
$$

Aquí:

- $\rho$ es la densidad del aire de admisión ($\text{kg/m}^3$),
- $N$ es el régimen de giro del motor en rpm,
- $Z$ es el número de cilindros,
- $i$ es un factor que tiene en cuenta la frecuencia con la que un cilindro admite carga fresca:
  - $i = \frac{1}{2}$ para motores **de cuatro tiempos** (un proceso de admisión cada dos revoluciones),
  - $i = 1$ para motores **de dos tiempos** (un proceso de admisión cada revolución).

:::{note}

**QUÉ CAPTURA ESTE MODELO DE POTENCIA (Y QUÉ NO)**

Esta expresión recoge el escalado de la potencia con:
- el trabajo específico $w_{\text{net}}$,
- el volumen desplazado ($b^2 s$),
- el régimen de giro $N$,
- el número de cilindros $Z$,
- y la densidad de admisión $\rho$ (que se relaciona directamente con la altitud y la sobrealimentación).

No incluye la eficiencia volumétrica, las restricciones al flujo, los gases residuales ni un modelado detallado del intercambio de gases, que se introducen más adelante al ir más allá de los ciclos ideales.

:::

---

(subsec_icre_fuel_consumption)=
### Consumo de combustible

El consumo de combustible se vincula comúnmente con la **relación aire-combustible**:

$$
A = \frac{\dot{m}_{\text{air}}}{\dot{m}_{\text{fuel}}}.
$$

Por tanto:

$$
\dot{m}_{\text{fuel}} = \frac{\dot{m}_{\text{air}}}{A} = \frac{\dot{m}_{\text{air}}}{\lambda A_s}.
$$

Esta expresión pone de manifiesto las dependencias clave:

- para $\dot{m}_{\text{air}}$ fijo, un funcionamiento más rico (menor $\lambda$) incrementa el caudal de combustible,
- aumentar el caudal másico de aire admitido (mayor $\rho$, mayor cilindrada, mayor rpm, sobrealimentación) incrementa el caudal de combustible para una determinada riqueza de mezcla.

:::{important}

**VÍNCULO CON LA EFICIENCIA**

Una vez que $q_{\text{in}}$ y $\dot{m}_{\text{fuel}}$ se definen de forma consistente, el enlace con las métricas de eficiencia es directo:
- un mayor $w_{\text{net}}$ a $q_{\text{in}}$ fijo implica una mayor eficiencia térmica,
- un menor $\dot{m}_{\text{fuel}}$ para una misma potencia implica un menor consumo específico de combustible.

Estas conexiones se harán explícitas al introducir los ciclos Otto y Diesel ideales y sus correcciones de ciclo real.

:::

---

(subsec_icre_parameters_closure)=
### Cierre conceptual

- El ciclo termomecánico de los MACIs se describe mediante una geometría basada en el ángulo del cigüeñal y en la evolución del volumen.
- Las magnitudes volumétricas clave son $V_1$, $V_2$, $V_d$ y la relación de compresión $r = V_1/V_2$.
- El aporte de calor puede expresarse por unidad de masa de aire o por unidad de masa de mezcla, utilizando el $\text{PCI}$ y la relación aire-combustible.
- La potencia escala con el caudal másico de aire admitido y con el trabajo neto específico: $\text{Pot}=\dot{m}_{\text{air}} w_{\text{net}}$.
- El caudal másico de combustible se obtiene directamente de $\dot{m}_{\text{fuel}}=\dot{m}_{\text{air}}/(\lambda A_s)$.

