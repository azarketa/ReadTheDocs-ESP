(sec_rankine_modifications)=
## Ciclos Rankine modificados

Ya hemos establecido previamente que aumentar la presión de la caldera mejora la eficiencia, pero introduce un efecto secundario peligroso: **humedad excesiva** en las etapas finales de la turbina.

¿Cómo podemos aprovechar presiones altas para ganar eficiencia sin destruir los álabes de la turbina con gotas de agua? El texto presenta dos vías principales para resolver este problema y optimizar aún más el ciclo: **recalentamiento** y **regeneración**.

---

(subsec_rankine_reheated)=
### El ciclo Rankine con recalentamiento

Para afrontar el problema de la humedad causado por la alta presión, en un primer momento podría sugerirse simplemente sobrecalentar el vapor a temperaturas *extremadamente* altas antes de la turbina. Aunque esto eleva la temperatura media de adición de calor, resulta prácticamente imposible debido a los **límites metalúrgicos** (los materiales se funden o fallan).

La solución práctica de ingeniería es el **ciclo con recalentamiento**.

**Cómo funciona:**
En lugar de expandir el vapor en una única caída continua desde la presión de caldera hasta la presión del condensador, la expansión se divide en dos (o más) etapas:
1.  **Expansión a alta presión:** el vapor se expande en una turbina de alta presión hasta alcanzar una presión intermedia.
2.  **Recalentamiento:** el vapor se envía de nuevo a la caldera (o a un intercambiador de calor dedicado), donde se recalienta a presión constante, normalmente hasta volver a la temperatura de entrada de la primera turbina.
3.  **Expansión a baja presión:** el vapor recalentado se expande en una segunda turbina hasta la presión del condensador.

**Impacto termodinámico:**
La inclusión de los estados 5 y 6 (en el diagrama $T-s$) desplaza el proceso de expansión hacia la derecha, reduciendo de forma significativa el contenido de humedad a la salida final.

Las ecuaciones de energía se ajustan para tener en cuenta las dos etapas:

* **Calor total aportado ($q_{\text{in}}$):** incluye el calor principal de la caldera más la energía de recalentamiento.
    $$q_{\text{in}} = q_{\text{primary}} + q_{\text{reheat}} = (h_{\text{primary,out}} - h_{\text{pump,out}}) + (h_{\text{reheat,out}} - h_{\text{reheat,in}})$$

* **Trabajo neto de turbina ($w_{\text{turb,out}}$):** suma del trabajo de ambas turbinas.
    $$w_{\text{turb,out}} = w_{\text{turb,I}} + w_{\text{turb,II}} = (h_{\text{inlet,I}} - h_{\text{outlet,I}}) + (h_{\text{inlet,II}} - h_{\text{outlet,II}})$$

:::{note}
**LA REGLA DE LOS RENDIMIENTOS DECRECIENTES**

Una única etapa de recalentamiento puede mejorar la eficiencia del ciclo entre un **4% y un 5%**, al elevar la temperatura media de adición de calor. Uno podría pensar: ¿por qué no añadir 10 etapas de recalentamiento?

A medida que aumenta el número de etapas, los procesos de expansión y recalentamiento se aproximan a un proceso **isotermo** (temperatura constante) a la temperatura máxima del ciclo, que es lo ideal. Sin embargo, la ganancia de eficiencia de una segunda etapa es solo la mitad de la de la primera, y una tercera etapa aporta la mitad de la segunda.

**Límite práctico:** debido a este rápido rendimiento decreciente y a la complejidad adicional de las tuberías y las pérdidas de presión, las centrales eléctricas rara vez superan **dos etapas** de recalentamiento, y el doble recalentamiento suele reservarse para plantas supercríticas.
:::

---

(subsec_rankine_regeneration_)=
### El ciclo Rankine regenerativo

Si examinamos el diagrama $T-s$ del Rankine ideal, observamos una deficiencia: el "agua de alimentación" (el líquido que sale de la bomba) entra en la caldera a una temperatura relativamente baja. Esto significa que una parte importante de la transferencia de calor ocurre simplemente para llevar este líquido frío hasta el punto de ebullición. Esto **reduce la temperatura media** de adición de calor y, con ello, la eficiencia.

**La solución: regeneración**
Para corregirlo, precalentamos el agua de alimentación (el agua que sale de la bomba) *antes* de que entre en la caldera principal.

Aunque podríamos usar un intercambiador de calor independiente, el método más práctico es **sangrar (extraer) vapor** desde varios puntos de la turbina. Ese vapor extraído, que podría haber producido más trabajo, se utiliza en su lugar para calentar el agua de alimentación en un dispositivo llamado **regenerador** o **calentador de agua de alimentación (Feedwater Heater, FWH)**.

**Beneficios de la regeneración:**
1.  **Aumenta la eficiencia térmica:** eleva la temperatura media del agua de alimentación que entra en la caldera.
2.  **Desaireación:** ayuda a eliminar aire del agua, evitando la corrosión en la caldera.
3.  **Control del caudal:** reduce el volumen de vapor que pasa por los grandes álabes finales de la turbina de baja presión (ya que parte de la masa fue extraída antes).

Existen dos tipos principales de calentadores de agua de alimentación: **abiertos** y **cerrados**.

---

(subsec_rankine_open_fwh)=
### Calentadores abiertos de agua de alimentación (O-FWH o mezcla directa)

Un **O-FWH** es, esencialmente, una cámara de mezcla.
* **Proceso:** el vapor extraído se mezcla directamente con el agua de alimentación fría procedente de la bomba.
* **Resultado ideal:** la mezcla abandona el calentador como **líquido saturado** a la presión del calentador.

**Análisis del caudal másico:**
En los ciclos regenerativos, el caudal másico no es constante en todo el lazo. El análisis se realiza tomando como base **1 kg** de vapor que circula por la caldera.
* Sea $y$ la fracción de vapor extraída para el calentador.
* Entonces $(1 - y)$ es la fracción que continúa hasta el condensador.

**Análisis energético (por unidad de masa de vapor de caldera):**
* **Calor aportado:**

    $$
    q_{\text{in}} = h_{\text{turb,in}} - h_{\text{boiler,in}}
    $$
  
* **Calor rechazado:**
  
    $$
    q_{\text{out}} = (1 - y)(h_{\text{turb,exit}} - h_{\text{cond,exit}})
    $$
  
* **Trabajo de turbina:**
  
    $$
    w_{\text{turb}} = (h_{\text{in}} - h_{\text{extract}}) + (1-y)(h_{\text{extract}} - h_{\text{exit}})
    $$
  
* **Trabajo de bomba:** ahora tenemos dos bombas (una antes del mezclador y otra después).

:::{tip}
**OPTIMIZACIÓN DE CALENTADORES**

La eficiencia aumenta a medida que añadimos más calentadores. Las grandes centrales eléctricas pueden emplear hasta **8 calentadores de agua de alimentación**. El límite es económico: se deja de añadir calentadores cuando el ahorro de combustible ya no compensa el coste del equipo.
:::

---

(subsec_rankine_closed_fwh)=
### Calentadores cerrados de agua de alimentación (C-FWH)

En un **C-FWH**, las corrientes **no se mezclan**. Funciona como un intercambiador de calor convencional de carcasa y tubos.
* **Proceso:** el vapor extraído y caliente fluye por el exterior de los tubos que transportan el agua de alimentación fría.
* **Presión:** como no se mezclan, ambas corrientes pueden estar a presiones diferentes.

**Ideal frente a real:**
* *Ideal:* el agua de alimentación se calienta hasta la temperatura exacta de salida del vapor extraído.
* *Real:* el agua de alimentación sale ligeramente más fría que el vapor (debido a la capacidad finita de transferencia de calor).

**Gestión del condensado:**
Después de que el vapor extraído condense en la carcasa, debe dirigirse a algún lugar. Normalmente se conduce a través de una **trampa** —un dispositivo de estrangulamiento que reduce la presión (manteniendo constante la entalpía)— y descarga el fluido hacia una línea de menor presión o hacia el condensador.

---

(subsec_rankine_fwh_comparison)=
### Comparación y sistemas reales

| Característica | Calentador abierto de agua de alimentación | Calentador cerrado de agua de alimentación |
| :--- | :--- | :--- |
| **Complejidad** | Sencillo, barato. | Complejo (tuberías internas), costoso. |
| **Transferencia de calor** | Excelente (mezcla directa). | Menos eficiente (indirecta). |
| **Necesidad de bombas** | Requiere una bomba para cada calentador (la presión cambia en la mezcla). | No requiere bombas independientes (las presiones son independientes). |
| **Resultado** | Desairea el agua de forma eficaz. | Requiere desaireación por separado. |

**Aplicación en sistemas reales:**

Las centrales modernas de vapor rara vez eligen solo uno de ellos. Normalmente emplean una **combinación** de calentadores abiertos y cerrados para equilibrar coste, eficiencia y necesidades de desaireación.

---

(subsec_modified_rankine_closure)=
### Cierre conceptual

* **Los ciclos con recalentamiento** resuelven el problema del "vapor húmedo" causado por las altas presiones de caldera. Al recalentar el vapor entre etapas de turbina, mantenemos la línea de expansión dentro de la región seca y mejoramos la eficiencia al aproximar una adición de calor isotérmica.
* **Los ciclos regenerativos** resuelven el problema del "agua de alimentación fría". Al utilizar vapor extraído para precalentar el agua, elevamos la temperatura media de adición de calor.
* **Fracción másica ($y$):** en los ciclos regenerativos, la formulación matemática pasa a depender de fracciones másicas, ya que los caudales difieren en distintas partes del lazo.
* **Abiertos frente a cerrados:** los calentadores abiertos mezclan fluidos (eficientes, pero requieren bombas); los cerrados intercambian calor a través de paredes (tuberías más simples, transferencia de calor menos eficiente).
* **El estándar moderno:** una central eléctrica típica a gran escala combina **presiones supercríticas**, **múltiples etapas de recalentamiento** y **múltiples calentadores de agua de alimentación** (regeneradores) para maximizar la eficiencia térmica.

