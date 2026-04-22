(sec_exergy_destruction)=
## Principio de disminución de la exergía; balances de entropía y exergía

La exergía, como magnitud derivada de la **primera** y la **segunda ley**, hereda su significado físico: la primera garantiza la **conservación de la energía**, mientras que la segunda impone la **degradación de su calidad** mediante la **generación de entropía**. En consecuencia, puede enunciarse un **principio de disminución de la exergía**, que refleja de forma complementaria el principio de aumento de la entropía.

Mientras la **entropía** mide la *dispersión irreversible de la energía*, la **exergía** cuantifica la *pérdida de su utilidad*, es decir, el valor energético destruido por irreversibilidad. Así como *la entropía siempre se genera y nunca se destruye*, *la exergía siempre se destruye y nunca se genera*.

---

(subsec_isolated_exergy_destruction)=
### Derivación para un sistema aislado

El principio puede demostrarse considerando un **sistema aislado**, es decir, uno que **no intercambia energía ni masa** con su entorno. En la práctica, esto puede interpretarse como el **conjunto sistema + ambiente**, habitualmente denominado el **universo termodinámico**, el sistema aislado por excelencia.

Para tal conjunto, **no existen interacciones de frontera externas**. Cualquier intercambio mecánico o térmico entre el sistema y el entorno pasa a ser **interno** dentro del compuesto aislado. En particular, el término de **trabajo de presión ambiental** $p_0(V_2 - V_1)$ —que aparece al analizar el sistema *solo*— desaparece del balance global, ya que el trabajo **realizado por el sistema** sobre el entorno es **exactamente compensado** por el trabajo opuesto **realizado por el entorno** sobre el sistema. Así, sus efectos **se cancelan**, quedando únicamente el cambio de energía interna del conjunto universo.

Consecuentemente, la **primera ley** para el compuesto aislado queda:

(eq_first_law_isolated)=
$$
E_{\text{in}} - E_{\text{out}} = \Delta E_{\text{sys.}} = 0
\quad \Rightarrow \quad
E_2 - E_1 = 0
$$

La **segunda ley**, aplicada al mismo sistema, da:

(eq_second_law_isolated)=
$$
S_{\text{in}} - S_{\text{out}} + S_{\text{gen.}} = \Delta S_{\text{sys.}}
\quad \Rightarrow \quad
S_{\text{gen.}} = S_2 - S_1
$$

Multiplicando la segunda ley por la temperatura del entorno $T_0$ y restándola de la primera ley se obtiene:

(eq_combined_laws_isolated)=
$$
T_0 S_{\text{gen.}} = (E_2 - E_1) - T_0 (S_2 - S_1)
$$

Recordando que el **cambio de exergía** viene dado por:

(eq_exergy_change_general)=
$$
\Delta X = X_2 - X_1 = (E_2 - E_1) - T_0 (S_2 - S_1),
$$

la comparación de ambas expresiones conduce a la relación fundamental:

(eq_exergy_destruction_principle)=
$$
\boxed{
\Delta X = - T_0 S_{\text{gen.}} \le 0
}
$$

Esto demuestra matemáticamente que la **exergía solo puede disminuir** (o mantenerse constante en procesos reversibles), estableciendo el **principio de disminución de la exergía**.

:::{important}

**DESTRUCCIÓN DE EXERGÍA**

La entropía mide la **degradación de la energía**; la exergía cuantifica el **coste energético** de esa degradación. Siempre que se genera entropía $(S_{\text{gen.}} > 0)$, se **destruye** una cantidad equivalente de exergía $(X_{\text{dest.}} = T_0 S_{\text{gen.}})$. Así, *irreversibilidad* y *destrucción de exergía* describen el mismo fenómeno físico: uno en términos entrópicos, el otro en términos energéticos.
:::

:::{note}

**RELACIÓN ENTRE ENTROPÍA Y EXERGÍA**

La segunda ley, escrita en términos de **generación de entropía**, determina si un proceso es *reversible*, *irreversible* o *imposible*.  
Combinada con la primera ley, la misma clasificación puede expresarse en términos **energéticos (exergía)**:

| **Criterio** | **Entropía generada** $S_{\text{gen.}}$ | **Exergía destruida** $X_{\text{dest.}}$ | **Tipo de proceso** |
| :- | :- | :-: | :- |
| $> 0$ | Positiva | Positiva | **Irreversible** |
| $= 0$ | Nula | Nula | **Reversible** |
| $< 0$ | Negativa | Negativa | **Imposible** |

Así, la **generación de entropía** y la **destrucción de exergía** son *dos caras del mismo fenómeno*: la entropía cuantifica el *aumento del desorden*, mientras que la exergía cuantifica la *pérdida de energía útil* asociada.
:::

---

(subsec_entropy_exergy_balance_forms)=
### Formas de los balances de entropía y exergía

Los **balances de entropía** y **exergía** expresan dos aspectos complementarios de la segunda ley:

* El **balance de entropía** describe cómo la *entropía se transfiere y se genera* dentro de un sistema — una medida **cualitativa** de irreversibilidad.
* El **balance de exergía** describe cómo la *energía útil (potencial de trabajo)* se transfiere y se destruye — una medida **cuantitativa** de la misma irreversibilidad.

| **Tipo de formulación** | **Balance de entropía** | **Balance de exergía** | **Interpretación** |
| :- | :- | :- | :- |
| **Forma general** | $\displaystyle S_{\text{in}} - S_{\text{out}} + S_{\text{gen.}} = \Delta S_{\text{sys.}}$ | $\displaystyle X_{\text{in}} - X_{\text{out}} - X_{\text{dest.}} = \Delta X_{\text{sys.}}$ | Considera transferencia, almacenamiento y generación/destrucción interna. |
| **Forma en tasas** | $\displaystyle \dot{S}_{\text{in}} - \dot{S}_{\text{out}} + \dot{S}_{\text{gen.}} = \frac{\mathrm{d}S_{\text{sys.}}}{\mathrm{d}t}$ | $\displaystyle \dot{X}_{\text{in}} - \dot{X}_{\text{out}} - \dot{X}_{\text{dest.}} = \frac{\mathrm{d}X_{\text{sys.}}}{\mathrm{d}t}$ | Mismo balance expresado por unidad de tiempo. |
| **Forma específica (intensiva)** | $\displaystyle s_{\text{in}} - s_{\text{out}} + s_{\text{gen.}} = \Delta s_{\text{sys.}}$ | $\displaystyle x_{\text{in}} - x_{\text{out}} - x_{\text{dest.}} = \Delta x_{\text{sys.}}$ | Cambios de entropía o exergía por unidad de masa. |

:::{note}

**CONEXIÓN Y SIGNIFICADO**

* La **generación de entropía** $S_{\text{gen.}}$ mide el *grado de irreversibilidad* en términos de entropía.  
* La **destrucción de exergía** $X_{\text{dest.}} = T_0 S_{\text{gen.}}$ convierte esa irreversibilidad en *pérdida de calidad energética*.  
* En **procesos reversibles**, $S_{\text{gen.}} = 0$ y $X_{\text{dest.}} = 0$.  
* En **procesos irreversibles**, ambas magnitudes son positivas.  
* Ambos balances se aplican a **sistemas cerrados** y **abiertos**, usando las expresiones adecuadas para las transferencias de entropía y exergía.
:::

---

(subsec_conceptual_closure_exergy)=
### Cierre conceptual

* El **principio de disminución de la exergía** complementa el **principio de aumento de la entropía**: mientras la entropía cuantifica la *degradación de la calidad energética*, la exergía cuantifica la *pérdida del potencial de trabajo útil* asociado.

* En **procesos reversibles**, la generación de entropía es nula y **no se destruye exergía** $(S_{\text{gen.}} = 0 \implies X_{\text{dest.}} = 0)$.  
  En **procesos irreversibles**, la generación de entropía es positiva y **la exergía disminuye** $(S_{\text{gen.}} > 0 \implies \Delta X < 0)$.

* El **balance de exergía** extiende la lógica del **balance de energía**, incorporando explícitamente la irreversibilidad mediante el término de destrucción $T_0 S_{\text{gen.}}$. Proporciona así una **medida cuantitativa del coste impuesto por la segunda ley**.

* Entropía y exergía constituyen **dos visiones complementarias** de la misma limitación física: la entropía describe **dirección y viabilidad**, mientras que la exergía describe **utilidad y rendimiento**.
