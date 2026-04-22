(sec_brayton_modified_cycles)=
## Ciclos Brayton modificados: regeneración, *intercooling* y recalentamiento

El ciclo Brayton simple proporciona el marco de referencia para el análisis de turbinas de gas, pero los diseños prácticos suelen incorporar dispositivos adicionales con el fin de mejorar bien la **eficiencia térmica** o bien el **trabajo específico neto**. Las modificaciones más relevantes son la **regeneración**, el ***intercooling*** (durante la compresión) y el **recalentamiento** (durante la expansión). Estas modificaciones se introducen aquí primero en términos ideales y más adelante se contrastan con las principales desviaciones observadas en los ciclos reales.

---

(subsec_brayton_regeneration)=
### Ciclo Brayton con regeneración

La **regeneración** es una estrategia mediante la cual la energía térmica contenida en una corriente caliente se transfiere a una corriente más fría dentro del ciclo, de modo que el fluido de trabajo entra en la cámara de combustión a una temperatura más alta. En la práctica, el regenerador no es más que un **intercambiador de calor**. La regeneración también es fundamental en los ciclos Stirling y Ericsson.

En un ciclo Brayton, la motivación física es inmediata: la temperatura de escape de la turbina suele ser significativamente mayor que la temperatura de salida del compresor. Por tanto, parte de la energía de escape que, de otro modo, se rechazaría al ambiente puede emplearse para **precalentar el aire comprimido** antes de la adición de calor.

:::{important}

**CUÁNDO LA REGENERACIÓN ES BENEFICIOSA**

La regeneración mejora la eficiencia térmica solo si la salida de la turbina está más caliente que la salida del compresor: $T_4 > T_2$. Si esta condición no se cumple (algo típico a altas relaciones de presión), la transferencia de calor tendría lugar en la dirección opuesta y la eficiencia del ciclo disminuiría.

:::

La salida del compresor se calienta desde el estado $2$ hasta el estado $5$ en el regenerador, mientras que el escape de la turbina se enfría en consecuencia. La temperatura máxima que puede alcanzar el aire comprimido está limitada por la temperatura de entrada al regenerador del escape de la turbina, $T_4$. Incluso para un regenerador ideal, $T_5$ no puede superar $T_4$.

Despreciando los cambios de energía cinética y potencial y suponiendo que el regenerador está bien aislado, el calor transferido al aire comprimido es:

(eq_q_regen)=
$$
q_{\text{regen}} = h_5 - h_2 .
$$

Para un regenerador ideal, el precalentamiento máximo posible corresponde a:

(eq_q_regen_ideal)=
$$
q_{\text{regen,id}} = h_4 - h_2 .
$$

---

(subsec_regenerator_effectiveness)=
### Eficacia del regenerador

El grado en que un regenerador real se aproxima al límite ideal se mide mediante su **eficacia** $\varepsilon$:

(eq_regen_effectiveness)=
$$
\varepsilon = \frac{h_5 - h_2}{h_4 - h_2}.
$$

Bajo la hipótesis estándar de aire frío ($c_p = \text{const.}$), esto se convierte en:

(eq_regen_effectiveness_T)=
$$
\varepsilon
= \frac{T_5 - T_2}{T_4 - T_2}.
$$

Una mayor eficacia implica un precalentamiento más intenso y, por tanto, una menor necesidad de combustible para alcanzar la temperatura de entrada a turbina deseada.

:::{note}

**EFECTIVIDAD FRENTE A DISEÑO PRÁCTICO**

Una alta eficacia suele requerir una mayor superficie de intercambio de calor, lo que incrementa el tamaño, el coste y, por lo general, la pérdida de presión asociada. En la práctica, son poco frecuentes valores de eficacia del regenerador superiores a $\varepsilon \approx 0.85$.

:::

---

(subsec_eta_brayton_regen)=
### Eficiencia térmica con regeneración

La definición de eficiencia térmica no cambia, pero los términos de aporte y rechazo de calor se modifican porque ahora una parte del calentamiento la proporciona el regenerador en lugar de la combustión.

Para un ciclo Brayton ideal con un regenerador ideal, y bajo la hipótesis estándar de aire frío, la eficiencia puede expresarse como:

(eq_eta_brayton_regen)=
$$
\eta_{\text{th,Brayton,regen}} = 1 - \frac{q_{\text{out}}}{q_{\text{in}}}.
$$

En esta configuración, la eficiencia del ciclo pasa a depender principalmente de:

- la relación de presión $r_p$,
- la razón entre las temperaturas máxima y mínima del ciclo ($T_3/T_1$).

Cualitativamente, la regeneración es más efectiva para **bajas relaciones de presión** y razones de temperatura relativamente moderadas, precisamente porque entonces la condición $T_4 > T_2$ se satisface con mayor facilidad.

---

(subsec_intercooling_reheating)=
### Ciclo Brayton con *intercooling*, recalentamiento y regeneración

El trabajo específico neto de un ciclo Brayton es la diferencia entre el trabajo suministrado por la turbina y el trabajo consumido por el compresor. Por tanto, puede aumentarse mediante:

- la reducción del trabajo del compresor,
- el aumento del trabajo de la turbina,
- o ambas cosas simultáneamente.

#### *intercooling* (compresión en varias etapas)

Una forma directa de reducir el trabajo del compresor es dividir la compresión en múltiples etapas y enfriar el fluido de trabajo entre ellas (***intercooling***). A medida que aumenta el número de etapas, la compresión se aproxima a un proceso cuasi isotermo llevado a cabo cerca de la temperatura de entrada al compresor. Dado que el trabajo de compresión depende fuertemente del volumen específico, reducir la temperatura reduce el volumen específico y, por tanto, disminuye el trabajo requerido.

#### Recalentamiento (expansión en varias etapas)

Una forma directa de aumentar el trabajo de la turbina es dividir la expansión en múltiples etapas y calentar el fluido de trabajo entre ellas (**recalentamiento**). A medida que aumenta el número de etapas, la expansión se aproxima a un proceso cuasi isotermo llevado a cabo cerca de la temperatura máxima admisible, lo que incrementa el volumen específico y, por tanto, aumenta el trabajo útil obtenible.

Estas dos ideas pueden resumirse mediante un único principio físico:

:::{important}

**PRINCIPIO DE DISEÑO (EFECTO DEL VOLUMEN ESPECÍFICO)**

Para compresión y expansión en flujo estacionario, la magnitud del trabajo está fuertemente ligada al volumen específico del fluido.

- Para reducir el trabajo del compresor, la compresión debe producirse al menor volumen específico posible
  (baja temperatura) $\Rightarrow$ *intercooling*.
- Para aumentar el trabajo de la turbina, la expansión debe producirse al mayor volumen específico posible
  (alta temperatura) $\Rightarrow$ recalentamiento.
  
:::

El *intercooling* disminuye la temperatura de salida del compresor, y el recalentamiento aumenta la temperatura de escape de la turbina. Ambas tendencias hacen que la regeneración sea más factible y potencialmente más beneficiosa, lo que conduce a diseños combinados con ***intercooling*, recalentamiento y regeneración**.

---

(subsec_two_stage_brayton_layout)=
### Configuración ideal de dos etapas con *intercooling*, recalentamiento y regeneración

Una configuración ideal representativa incluye:

- dos etapas de compresión con *intercooling*,
- un regenerador antes de la cámara de combustión,
- dos etapas de turbina con recalentamiento,
- y recuperación de calor mediante el regenerador a partir del escape de la turbina.

Una secuencia típica de estados puede describirse como sigue:

1. $1 \rightarrow 2$: compresión isentrópica en la primera etapa,
2. $2 \rightarrow 3$: *intercooling* a presión constante (a menudo idealizado como un retorno a $T_1$),
3. $3 \rightarrow 4$: compresión isentrópica en la segunda etapa,
4. $4 \rightarrow 5$: regeneración (precalentamiento a presión constante),
5. $5 \rightarrow 6$: adición principal de calor (combustión) a presión constante,
6. $6 \rightarrow 7$: expansión isentrópica en la primera etapa,
7. $7 \rightarrow 8$: recalentamiento a presión constante (a menudo idealizado como un retorno a $T_6$),
8. $8 \rightarrow 9$: expansión isentrópica en la segunda etapa,
9. $9 \rightarrow 10$: enfriamiento del escape a través del regenerador a presión constante.

El ciclo se cierra entonces bien mediante un enfriamiento adicional hasta el estado $1$ (idealización de ciclo cerrado), o bien mediante la descarga y renovación del fluido de trabajo (operación típica de ciclo abierto).

---

(subsec_real_brayton_deviations)=
### Ciclos Brayton ideales frente a reales

Los ciclos Brayton reales se desvían de las predicciones ideales principalmente debido a:

1. **Irreversibilidades en la compresión y en la expansión**  
   La compresión y la expansión no son isentrópicas. Esto motiva la definición de las **eficiencias isentrópicas** del compresor y de la turbina. En un diagrama $T\!-\!s$, los procesos reales se desvían hacia valores de entropía más altos, reduciendo el área encerrada y, por tanto, disminuyendo el trabajo neto producido.

   - La irreversibilidad del compresor incrementa el trabajo requerido para una relación de presión dada y tiende a reducir la eficiencia global.
   - La irreversibilidad de la turbina reduce el trabajo producido para un estado de entrada dado y también disminuye la eficiencia.

2. **Pérdidas de presión en los dispositivos de adición y rechazo de calor**  
   En la práctica, se producen pérdidas de presión en las cámaras de combustión, los intercambiadores de calor, los regeneradores y los sistemas de escape.

   - Las pérdidas de presión aguas arriba de la turbina reducen el trabajo producido por la turbina.
   - Las pérdidas de presión en el lado de escape reducen la capacidad efectiva de expansión y también reducen la potencia neta.

Ambos efectos reducen el trabajo específico neto y, por lo general, requieren un mayor aporte de combustible para obtener la misma potencia útil de salida.

---

(subsec_brayton_modified_conceptual_closure)=
### Cierre conceptual

- La regeneración recupera parte de la energía del escape de la turbina para precalentar el aire comprimido.
- La regeneración es beneficiosa solo si $T_4 > T_2$; en caso contrario, degrada las prestaciones.
- La efectividad del regenerador cuantifica cuán cerca se encuentra el dispositivo del límite ideal.
- El *intercooling* reduce el trabajo del compresor; el recalentamiento aumenta el trabajo de la turbina.
- El *intercooling* y el recalentamiento suelen hacer que la regeneración sea más factible.
- Los ciclos Brayton reales se desvían de los ideales debido a irreversibilidades y pérdidas de presión, que reducen el trabajo neto y la eficiencia.

