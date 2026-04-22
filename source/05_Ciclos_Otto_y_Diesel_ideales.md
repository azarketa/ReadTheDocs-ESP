(sec_icre_ideal_cycles)=
## Ciclos termodinámicos ideales de los MACI: Otto y Diesel

Una vez definidos los principales parámetros geométricos, volumétricos y relacionados con la combustión, el siguiente paso es describir los **ciclos termodinámicos ideales** utilizados para modelar los motores de combustión interna alternativos (MACI). En este marco ideal, el objetivo es captar las transformaciones termomecánicas dominantes **sin** considerar todavía pérdidas reales, fricción, combustión a velocidad finita, transferencia de calor a las paredes, pérdidas de presión, combustión incompleta u otras irreversibilidades.

La idealización se basa en el **modelo aire-estándar** introducido previamente: el fluido de trabajo se trata como aire que experimenta una secuencia de procesos internamente reversibles, mientras que la combustión y el escape se representan mediante procesos equivalentes de **adición de calor** y **rechazo de calor**.

---

(subsec_icre_otto_diesel_processes)=
### Ciclo Otto y ciclo Diesel: procesos ideales

Tanto el ciclo **Otto** como el ciclo **Diesel** se construyen a partir de los mismos cuatro procesos fundamentales. Lo que los distingue es la representación idealizada del **proceso de combustión (adición de calor)**.

#### El ciclo Otto ideal

El ciclo Otto (típicamente asociado a los motores de encendido provocado) consta de cuatro procesos ideales:

- **Proceso $1 \rightarrow 2$ (compresión isentrópica):**  
  El pistón se desplaza hacia arriba tras la admisión, comprimiendo la carga.  
  En el ciclo ideal, la compresión es **adiabática y reversible**, por lo que es isentrópica.

- **Proceso $2 \rightarrow 3$ (adición de calor a volumen constante):**  
  La combustión se idealiza como una adición rápida de calor a **volumen constante**.  
  La hipótesis es que la liberación de calor es lo bastante rápida como para que, idealmente, el pistón no se desplace apreciablemente durante el evento de combustión.  
  Por tanto, $v_2 = v_3$.

- **Proceso $3 \rightarrow 4$ (expansión isentrópica):**  
  El gas a alta presión se expande mientras el pistón se desplaza hacia abajo, entregando trabajo.  
  La expansión se idealiza como **adiabática y reversible** y, por tanto, isentrópica.

- **Proceso $4 \rightarrow 1$ (rechazo de calor a volumen constante):**  
  El calor se rechaza a **volumen constante** cuando el gas se encuentra en el volumen máximo del cilindro,  
  devolviendo el fluido de trabajo a su estado termodinámico inicial.  
  Por tanto, $v_4 = v_1$.

:::{important}

**EL CICLO OTTO IDEAL ES UN MODELO TERMO-MECÁNICO CERRADO**

El ciclo Otto **no** modela explícitamente la admisión y el escape como procesos de intercambio gaseoso en sistema abierto.  
En su lugar, el ciclo se centra en la parte de sistema cerrado en la que el fluido de trabajo permanece dentro del cilindro y experimenta compresión, adición de calor, expansión y rechazo de calor.

:::

#### Admisión y escape en la representación ideal

En un motor real de cuatro tiempos, el pistón también realiza las carreras de **admisión** y **escape**. En la representación ideal más simple, estas pueden modelarse como dos trayectorias a presión constante a la presión de admisión/escape (a menudo próxima a la atmosférica en motores de aspiración natural, o igual a la presión del colector de admisión en motores sobrealimentados). Estos dos procesos abarcan todo el intervalo de volumen entre PMS y PMI y suelen dibujarse como dos líneas horizontales superpuestas en el diagrama $p-v$ a la presión $p_0$.

Los trabajos correspondientes son:

- admisión (trabajo realizado por los alrededores sobre el sistema pistón-gas):

  $$
  w_{\text{in},0\rightarrow 1} = p_0 (v_1 - v_0),
  $$

- escape (trabajo realizado por el sistema sobre los alrededores):

  $$
  w_{\text{out},1\rightarrow 0} = p_0 (v_1 - v_0).
  $$

Como estas áreas se superponen y tienen signos opuestos, se cancelan en la representación ideal, de modo que el trabajo neto del ciclo ideal viene gobernado por la parte cerrada ($1\rightarrow2\rightarrow3\rightarrow4\rightarrow1$).

:::{note}

**FUNCIONAMIENTO ABIERTO FRENTE A CERRADO**

Aunque los ciclos Otto y Diesel ideales suelen presentarse como ciclos cerrados,  
un motor real alterna entre:
- funcionamiento en **sistema abierto** durante la admisión y el escape,
- funcionamiento en **sistema cerrado** durante la compresión, la combustión y la expansión.

Esta distinción se vuelve esencial al modelar las pérdidas de bombeo y el intercambio gaseoso real.

:::

---

(subsec_icre_diesel_processes)=
### El ciclo Diesel ideal

El ciclo Diesel (típicamente asociado a los motores de encendido por compresión) comparte tres de los procesos del ciclo Otto y difiere únicamente en la etapa de adición de calor.

- **Proceso $1 \rightarrow 2$ (compresión isentrópica):** igual que en el ciclo Otto.  
- **Proceso $2 \rightarrow 3$ (adición de calor a presión constante):**  
  En los motores de encendido por compresión, la inyección de combustible y la combustión se extienden a lo largo de un intervalo mayor de ángulo de cigüeñal y continúan en la parte inicial de la carrera de expansión.  
  Una idealización clásica consiste en modelar esta combustión prolongada como una **adición de calor a presión constante**, de modo que $p_2 = p_3$.  
- **Proceso $3 \rightarrow 4$ (expansión isentrópica):** mismo significado físico que en Otto.  
- **Proceso $4 \rightarrow 1$ (rechazo de calor a volumen constante):** mismo proceso de cierre que en Otto.

Así, el ciclo Diesel conserva la modelización de la compresión y la expansión, pero sustituye la combustión **isócora** por una combustión **isóbara**.

---

(subsec_icre_otto_efficiency)=
### Rendimiento térmico del ciclo Otto ideal

Para los ciclos Otto y Diesel, despreciando los cambios de energía cinética y potencial, la primera ley para un sistema cerrado a lo largo de un proceso puede escribirse en forma específica como:

$$
(q_{\text{in}} - q_{\text{out}}) + (w_{\text{in}} - w_{\text{out}}) = \Delta u .
$$

Para el ciclo Otto, el calor se añade y se rechaza a **volumen constante**, de modo que la transferencia de calor es igual a la variación de energía interna:

Adición de calor ($2 \rightarrow 3$):

$$
q_{\text{in}} = u_3 - u_2 = c_v (T_3 - T_2).
$$

Rechazo de calor ($4 \rightarrow 1$):

$$
q_{\text{out}} = u_4 - u_1 = c_v (T_4 - T_1).
$$

Por tanto, el rendimiento térmico es:

$$
\eta_{\text{th,Otto}} = \frac{w_{\text{net}}}{q_{\text{in}}} = 1 - \frac{q_{\text{out}}}{q_{\text{in}}} = 1 - \frac{T_4 - T_1}{T_3 - T_2}.
$$

Para expresar este rendimiento en función de la relación de compresión, se emplean las relaciones isentrópicas para los procesos $1 \rightarrow 2$ y $3 \rightarrow 4$, junto con $v_2=v_3$ y $v_4=v_1$:

$$
\frac{T_2}{T_1} = \left(\frac{v_1}{v_2}\right)^{\gamma-1} \quad \text{y} \quad \frac{T_3}{T_4} = \left(\frac{v_4}{v_3}\right)^{\gamma-1} = \left(\frac{v_1}{v_2}\right)^{\gamma-1}.
$$

Definiendo la relación de compresión como $r = v_1/v_2$, se obtiene que el rendimiento del ciclo Otto adopta la forma:

$$
\eta_{\text{th,Otto}} = 1 - \frac{1}{r^{\gamma-1}} .
$$

Este resultado compacto muestra que el rendimiento ideal de Otto aumenta al:
- aumentar la relación de compresión $r$,
- aumentar la relación de calores específicos $\gamma$.

:::{important}

**EL RENDIMIENTO DEL CICLO OTTO CRECE RÁPIDAMENTE PARA VALORES BAJOS DE $r$ Y SE FRENA PARA VALORES ALTOS DE $r$**

La función $1 - 1/r^{\gamma-1}$ aumenta bruscamente para valores pequeños o moderados de $r$,  
pero se aplana a medida que $r$ se hace grande.  
Por ello, aumentar $r$ indefinidamente produce rendimientos decrecientes en la eficiencia ideal.

:::

#### Limitación práctica en motores de encendido provocado: el picado

En los motores de encendido provocado, aumentar $r$ eleva la temperatura al final de la compresión. Si la mezcla alcanza condiciones que favorecen la **autoignición** antes de que el frente de llama se propague de forma suave desde la chispa, partes de la mezcla pueden inflamarse prematuramente, produciendo una rápida subida de presión y ondas de presión. Este fenómeno es el **picado** o **knock** (a menudo percibido como un golpeteo metálico). El picado incrementa las solicitaciones mecánicas y térmicas y es perjudicial para la durabilidad.

Como resultado, los motores de encendido provocado suelen operar con relaciones de compresión del orden de:

$$
8 \lesssim r \lesssim 11 .
$$

Históricamente, el aumento del índice de octano mediante aditivos antidetonantes permitió emplear valores más altos de $r$. Por ejemplo, el tetraetilo de plomo $(\text{CH}_3\text{CH}_2)_4\text{Pb}$ se utilizó ampliamente a comienzos y mediados del siglo XX para aumentar la resistencia al picado, pero posteriormente fue eliminado por su toxicidad y su impacto ambiental. Los combustibles modernos de alto octanaje y un mejor control de la combustión han permitido volver a aumentar $r$ en algunas aplicaciones.

:::{note}

**EL PAPEL DE $\gamma$**

Para una relación de compresión fija, el rendimiento del ciclo Otto aumenta cuando aumenta $\gamma$.  
Los gases monoatómicos (por ejemplo, argón o helio, con $\gamma \approx 1.667$) proporcionan rendimientos ideales mayores que el aire diatómico ($\gamma \approx 1.4$), mientras que los gases poliatómicos presentan valores menores.

En motores reales, el fluido de trabajo no es un gas ideal fijo: la composición y la temperatura varían, y $\gamma$ no permanece constante. Aun así, la tendencia ideal sigue siendo una idea de diseño muy valiosa.

:::

Los motores reales de encendido provocado suelen alcanzar rendimientos térmicos del orden del $25\%$ al $30\%$, aunque el valor real depende de muchos factores adicionales (pérdidas térmicas, riqueza de mezcla, eficiencia volumétrica, fricción y fase de combustión).

---

(subsec_icre_otto_diagrams)=
### Diagramas $p-v$ y $T-s$ del ciclo Otto ideal

El ciclo Otto ideal puede interpretarse visualmente mediante los diagramas termodinámicos estándar:

- En el **diagrama $p-v$**:
  - $1 \rightarrow 2$ y $3 \rightarrow 4$ son curvas isentrópicas,
  - $2 \rightarrow 3$ y $4 \rightarrow 1$ son líneas verticales (volumen constante).  
  El trabajo neto producido es el **área encerrada** por el ciclo.

- En el **diagrama $T-s$**:
  - los procesos isentrópicos aparecen como líneas verticales (entropía constante),
  - la adición y el rechazo de calor a volumen constante aparecen como trayectorias curvas.  
  El calor neto aportado es igual al trabajo neto producido en el ciclo (primera ley), y la diferencia entre el calor añadido y el rechazado puede interpretarse mediante las áreas bajo las trayectorias correspondientes.

Un punto clave es que, aunque Otto y Diesel difieren de forma apreciable en el diagrama $p-v$ durante la adición de calor, sus diagramas $T-s$ siguen siendo cualitativamente similares: dos líneas verticales isentrópicas conectadas por dos curvas de transferencia de calor, donde la curva de adición de calor tiene distinta pendiente según el proceso sea isócoro (Otto) o isóbaro (Diesel).

---

(subsec_icre_diesel_efficiency)=
### Rendimiento térmico del ciclo Diesel ideal

En el ciclo Diesel, el proceso de adición de calor ocurre a **presión constante**, y por ello durante la combustión existe trabajo de frontera. Aplicando la primera ley al proceso $2 \rightarrow 3$:

$$
q_{\text{in}} - w_{b,\text{out}} = u_3 - u_2 .
$$

Para un proceso a presión constante de un gas ideal, esto conduce a:

$$
q_{\text{in}} = (u_3 - u_2) + p_2(v_3 - v_2) = h_3 - h_2 = c_p (T_3 - T_2).
$$

El rechazo de calor ($4 \rightarrow 1$) sigue modelándose a volumen constante:

$$
q_{\text{out}} = u_4 - u_1 = c_v (T_4 - T_1).
$$

Por tanto, el rendimiento térmico del ciclo Diesel es:

$$
\eta_{\text{th,Diesel}} = 1 - \frac{q_{\text{out}}}{q_{\text{in}}} = 1 - \frac{c_v (T_4 - T_1)}{c_p (T_3 - T_2)} = 1 - \frac{T_4 - T_1}{\gamma (T_3 - T_2)} .
$$

Para expresar el resultado en función de la relación de compresión y de un nuevo parámetro específico del ciclo Diesel, se define la **relación de corte**:

$$
r_c = \frac{v_3}{v_2}.
$$

Empleando las relaciones isentrópicas y la estructura del ciclo Diesel, se obtiene la forma estándar:

$$
\eta_{\text{th,Diesel}} = 1 - \frac{1}{r^{\gamma-1}} \left[\frac{r_c^\gamma - 1}{\gamma (r_c - 1)}\right].
$$

El término entre corchetes es siempre mayor que 1 para $r_c>1$, de modo que, para una misma relación de compresión:

$$
\eta_{\text{th,Otto}} > \eta_{\text{th,Diesel}} .
$$

:::{important}

**EL COSTE DE LA COMBUSTIÓN A PRESIÓN CONSTANTE**

A relación de compresión fija, el ciclo Diesel presenta menor rendimiento ideal que el ciclo Otto porque el calor se añade mientras el gas se expande, lo que incrementa $q_{\text{in}}$ en relación con el trabajo ganado para la misma compresión inicial.

Sin embargo, en la práctica los motores Diesel suelen operar con relaciones de compresión mucho mayores, lo que puede compensar con creces esta desventaja del ciclo ideal.

:::

---

(subsec_icre_diesel_considerations)=
### Interpretación y tendencias prácticas en motores Diesel

A partir de la expresión del rendimiento Diesel, se deducen varios resultados cualitativos importantes:

- **Una relación de corte menor aumenta el rendimiento:**  
  Cuando $r_c \rightarrow 1$, el proceso de adición de calor se aproxima a volumen constante y el factor entre corchetes tiende a 1.  
  Esto puede demostrarse mediante la aproximación de primer orden:

  $$
  r_c^\gamma - 1 \approx \gamma (r_c - 1),
  $$

  por lo que los rendimientos de Otto y Diesel coinciden en el límite $r_c \to 1$.

- **Los motores Diesel toleran valores más altos de $r$ (y los necesitan):**  
  El encendido por compresión requiere una temperatura suficientemente alta al final de la compresión para desencadenar la autoignición del combustible inyectado. Por ello, los motores Diesel operan con relaciones de compresión mucho mayores, típicamente:

  $$
  12 \lesssim r \lesssim 23,
  $$

  lo que incrementa fuertemente el rendimiento mediante el factor $1 - 1/r^{\gamma-1}$.

- **En la práctica, los rendimientos Diesel típicos son más altos:**  
  Los motores Diesel también tienden a operar con relaciones aire-combustible mayores (funcionamiento pobre) y con frecuencia a menores rpm para una misma aplicación, lo que favorece una combustión más completa y mejora la eficiencia global. Son típicos rendimientos térmicos del orden del $35\%$ al $40\%$ en muchas aplicaciones.

Debido a estas características, los motores Diesel han sido históricamente muy atractivos para aplicaciones de alta potencia y servicio severo, como camiones, locomotoras, barcos y unidades auxiliares de potencia. El precio final de los combustibles en los mercados reales depende de muchos factores además del coste de producción (precio del producto refinado, demanda estacional, logística e impuestos), pero las ventajas termodinámicas y operativas de los motores Diesel siguen siendo fundamentales en usos pesados.

:::{note}

**LA ELECCIÓN DEL MOTOR NO ES SOLO TERMODINÁMICA**

Incluso cuando los motores Diesel ofrecen un mayor rendimiento, la selección práctica depende también de:
- normativas de emisiones y requisitos de postratamiento,
- restricciones de ruido y vibraciones,
- disponibilidad del combustible y dinámica de precios,
- mantenimiento, perfil de operación y coste total de propiedad.

Estas consideraciones motivan el paso desde los ciclos ideales hacia el análisis de pérdidas en ciclos reales.

:::

---

(subsec_icre_otto_diesel_comparisons)=
### Comparación entre los ciclos Otto y Diesel

En el análisis de ciclos son útiles varios niveles de comparación:

- **Misma relación de compresión ($r$):**  
  Otto proporciona mayor rendimiento ideal que Diesel porque el modelo de adición de calor del ciclo Diesel incluye el efecto de corte.

- **Relación de compresión variable:**  
  A medida que aumenta $r$, aumentan tanto el trabajo neto como el rendimiento, pero:
  - los motores SI están limitados por el picado,
  - los motores CI están limitados por condicionantes mecánicos y térmicos de diseño (presiones máximas, tensiones en los componentes).

- **Efecto de la riqueza de mezcla (factor de exceso de aire):**  
  Las mezclas más ricas (menor $\lambda$) pueden aumentar la energía química liberada, pero también pueden conducir a combustión incompleta y mayores emisiones.  
  Las mezclas pobres (mayor $\lambda$) tienden a aumentar el rendimiento del ciclo en parte debido a las propiedades termofísicas efectivas de la mezcla y a la reducción de la disociación y de las pérdidas térmicas en ciertos regímenes.

En análisis más avanzados, la dependencia de la $\gamma$ efectiva con la composición de la mezcla puede introducirse mediante calores específicos promediados de la mezcla, haciendo que $\gamma$ sea una función creciente de la relación aire-combustible en muchos rangos prácticos.

---

(subsec_icre_dual_cycle)=
### El ciclo dual (mixto)

Los motores modernos de encendido por compresión con inyección rápida y subida rápida de presión suelen presentar un comportamiento de combustión que no queda bien representado por un modelo puramente a presión constante.

En muchos motores:

- una fracción de la liberación de calor ocurre muy rápidamente cerca del final de la compresión (aproximadamente a volumen constante),
- seguida de una liberación continua de calor al inicio de la expansión (aproximadamente a presión constante).

Esto motiva el **ciclo dual (mixto)**, que modela la adición de calor como una combinación de:

- **adición de calor a volumen constante** ($2 \rightarrow x$), seguida de
- **adición de calor a presión constante** ($x \rightarrow 3$).

Se definen dos parámetros:

- una **relación de presión** a través de la parte a volumen constante:

  $$
  r_p = \frac{p_x}{p_2},
  $$

- una **relación de corte** a través de la parte a presión constante:

  $$
  r_c = \frac{v_3}{v_x}.
  $$

El rendimiento del ciclo dual depende de $r$, $r_p$, $r_c$ y $\gamma$, y su expresión es más compleja que en los casos Otto y Diesel. No obstante, el ciclo dual suele ser una idealización más realista de los motores CI modernos que el ciclo Diesel puro, manteniendo al mismo tiempo la posibilidad de un tratamiento analítico.

:::{tip}

**CASOS LÍMITE**

El ciclo dual contiene a Otto y Diesel como casos particulares:

- Si la parte a presión constante desaparece ($r_c \rightarrow 1$), el ciclo dual se aproxima a un modelo de adición de calor tipo Otto.
- Si la parte a volumen constante desaparece ($r_p \rightarrow 1$), el ciclo dual se aproxima al ciclo Diesel.

Esto convierte al ciclo dual en un puente conveniente entre las dos idealizaciones clásicas.

:::

---

(subsec_icre_ideal_cycles_closure)=
### Cierre conceptual

- El ciclo Otto ideal modela la combustión como una adición de calor a volumen constante; el ciclo Diesel la modela como una adición de calor a presión constante.
- Ambos ciclos emplean compresión y expansión isentrópicas y se cierran con un rechazo de calor a volumen constante.
- El rendimiento ideal de Otto depende solo de $r$ y $\gamma$: $\eta_{\text{th,Otto}} = 1 - 1/r^{\gamma-1}$.
- El rendimiento ideal de Diesel introduce la relación de corte $r_c$: $\eta_{\text{th,Diesel}} = 1 - \frac{1}{r^{\gamma-1}}\left[\frac{r_c^\gamma-1}{\gamma(r_c-1)}\right]$.
- Para igual $r$, Otto es más eficiente que Diesel, pero los motores Diesel operan con valores más altos de $r$ en la práctica y suelen alcanzar mayores rendimientos reales.
- El ciclo dual capta una adición de calor mixta a volumen constante/presión constante y proporciona un modelo ideal más flexible para los motores CI modernos.

