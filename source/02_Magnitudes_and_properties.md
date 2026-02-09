## Magnitudes y propiedades

La termodinámica trata con **sistemas físicos** y sus características medibles. Para describir cualquier fluido, necesitamos saber **qué magnitudes** definen su comportamiento y **cómo** se miden. Esta sección introduce las **magnitudes** y **propiedades** que permiten caracterizar los fluidos en términos macroscópicos, sentando las bases para leyes y relaciones de estado posteriores.

---

### Magnitudes físicas y unidades de medida
Una **magnitud** es cualquier cantidad física medible asociada a un sistema — como masa, volumen, temperatura o presión.
Cada magnitud debe ir acompañada de una **unidad de medida**, que sirve como referencia fija.
Una unidad válida debe cumplir tres condiciones esenciales:
1. Debe ser **constante** en el tiempo e independiente del lugar donde se use.
2. Debe ser **universal**, aplicable en todas las condiciones físicas.
3. Debe ser **reproducible**, para que cualquier laboratorio pueda realizarla.

:::{note}
**MAGNITUDES VS. UNIDADES**

Una magnitud expresa **qué** medimos (por ejemplo, energía o presión); una unidad expresa **cómo** lo medimos (joule, pascal).
La termodinámica requiere ambas para describir cuantitativamente el estado de un sistema.
:::

---

### El Sistema Internacional (SI)
El **Sistema Internacional de Unidades (SI)** define siete magnitudes fundamentales, de las cuales se derivan todas las demás.
En termodinámica, usamos habitualmente cinco:

| **Magnitud fundamental** | **Símbolo** | **Unidad (SI)** | **Símbolo (Unidad)** |
| :------------------------ | :---------: | :-------------: | :-------------------: |
| Longitud | $L$ | metro | $\text{m}$ |
| Tiempo | $t$ | segundo | $\text{s}$ |
| Masa | $m$ | kilogramo | $\text{kg}$ |
| Temperatura | $T$ | Kelvin | $\text{K}$ |
| Cantidad de sustancia | $n$ | mol | $\text{mol}$ |

A partir de estas, se construyen muchas **magnitudes derivadas**:

| **Magnitud derivada** | **Definición** | **Unidad SI** | **Expresión** |
| :--------------------- | :------------: | :-----------: | :-----------: |
| Densidad $(\rho)$ | $\rho = m/V$ | kg/m³ | $\text{kg}/\text{m}^3$ |
| Fuerza $(F)$ | $F = m \cdot a$ | Newton | $\text{N} = \text{kg}\cdot\text{m}/\text{s}^2$ |
| Presión $(p)$ | $p = F/A$ | Pascal | $\text{Pa} = \text{N}/\text{m}^2$ |
| Energía $(E)$ | — | Joule | $\text{J} = \text{N}\cdot\text{m}$ |
| Potencia $(\dot{W})$ | — | Watt | $\text{W} = \text{J}/\text{s}$ |

:::{tip}
**RAZONAMIENTO DIMENSIONAL**

Conocer cómo dependen las unidades derivadas de las fundamentales permite verificar errores y convertir magnitudes rápidamente.
La consistencia dimensional es una comprobación integrada de la corrección física.
:::

---

### Propiedades extensivas e intensivas
Las propiedades termodinámicas se agrupan según cómo dependen del tamaño del sistema:
* **Propiedades extensivas** escalan con el tamaño del sistema; son **aditivas**:

$$
X_{\text{total}} = \sum_i X_i
$$

Ejemplos: **masa** ($m$), **volumen** ($V$), **energía total** ($E$).
* **Propiedades intensivas** son **independientes** del tamaño del sistema; permanecen inalteradas al combinar subsistemas.
Ejemplos: **presión** ($p$), **temperatura** ($T$), **densidad** ($\rho$).

:::{warning}
**ADITIVIDAD VS. INDEPENDENCIA**

Las propiedades extensivas describen **cantidades de sustancia**; las intensivas describen **condiciones de la sustancia**.
La termodinámica las relaciona mediante razones como “por masa”, “por volumen” o “por mol”, que convierten extensivas en intensivas.
:::

---

### De extensivas a intensivas: conversiones de referencia
Las magnitudes extensivas pueden transformarse en intensivas dividiéndolas por una **magnitud extensiva de referencia**: volumen, masa o cantidad de sustancia.
Los resultados son densidades, magnitudes específicas o magnitudes molares:

| **Referencia** | **Magnitud extensiva** | **Propiedad intensiva** | **Expresión** | **Unidad SI** |
| :------------- | :---------------------- | :----------------------- | :-----------: | :-----------: |
| Volumen $V$ [m³] | Masa $m$ [kg] | Densidad $\rho$ | $\rho = m/V$ | kg/m³ |
| Volumen $V$ [m³] | Energía $E$ [J] | Densidad de energía $e$ | $e = E/V$ | J/m³ |
| Masa $m$ [kg] | Volumen $V$ [m³] | Volumen específico $v$ | $v = V/m = 1/\rho$ | m³/kg |
| Cantidad $n$ [mol] | Volumen $V$ [m³] | Volumen molar $v_m$ | $v_m = V/n$ | m³/mol |

:::{tip}
**NORMALIZACIÓN POR MAGNITUD DE REFERENCIA**

Relacionar una magnitud extensiva con una referencia (masa, volumen o mol) permite comparar propiedades entre sistemas.
Por ejemplo, energía por unidad de masa (energía específica) o por mol (energía molar) son descriptores estándar.
:::

---

### Propiedades fundamentales medibles
* **Volumen**: Para fluidos, el volumen es la única propiedad geométrica relevante. Se mide en m³.
* **Masa**: Mide la cantidad de materia y se expresa en kg. Es conservativa en procesos no reactivos.
* **Cantidad de sustancia**: Medida en moles (mol), conecta la descripción macroscópica con la molecular.
Por definición:

$$
1\ \text{mol} = N_A = 6{,}022\times10^{23}\ \text{entidades}.
$$

Así, $1\ \text{mol}$ de $\text{H}_{2}\text{O}$ contiene $6{,}022\times10^{23}$ moléculas de agua.

:::{note}
**POR QUÉ IMPORTA EL MOL**

Muchos procesos físicos y químicos escalan con el **número de partículas**, no con su masa.
A la misma temperatura y presión, un mol de cualquier gas ocupa el mismo volumen, independientemente de su masa molecular.
:::

---

### Propiedades complejas medibles: presión
* **Definición**:

    $$
    p = \frac{F_\perp}{A}.
    $$

  
    La figura siguiente muestra una definición esquemática de la magnitud presión. Un gas confinado dentro del volumen cilíndrico de un sistema pistón–cilindro está sometido a una presión $(p)$ que resulta de dividir la fuerza $(F_{\perp})$ aplicada sobre el pistón entre el área de la sección transversal $(A = \pi D^{2}/4)$ del cilindro.
    :::{figure} 1_fundamentals_figs/pressure_definition.svg
    :name: pressure_definition
    :width: 50%
    :align: center
    Sistema pistón–cilindro mostrando la definición de presión basada en la fuerza.
    :::
    
    Aunque la fuerza es un vector, la presión es un escalar porque actúa normal al elemento de superficie.


* **Unidades y escalas**:

    La unidad SI es el pascal (Pa = N/m²). Es pequeña, por lo que se usan múltiplos: kPa, MPa, atm, bar, etc.
    
    Es una unidad pequeña: una persona de 70 $\text{kg}$ de pie sobre una baldosa de $0,3\times0,3\ \text{m}^{2}$ ejerce  
    
    $$
    p = \frac{m g}{A} = \frac{70 \ \text{kg}\times9{,}81 \ \text{m}/\text{s}^{2}}{0{,}09 \ \text{m}^{2}} \approx 8\times10^{3} \ \text{Pa} = 8 \ \text{kPa}.
    $$
    
    Por ello, en la práctica se utilizan múltiplos mayores:
    
    | **Unidad**                         | **Símbolo**                | **Equivalente en Pa**                | **Uso típico**                     |
    | :--------------------------------- | :-------------------------: | :-----------------------------------: | :--------------------------------- |
    | kilopascal                        | $\text{kPa}$               | $10^{3}$ $\text{Pa}$                 | Ingeniería y laboratorio           |
    | megapascal                        | $\text{MPa}$               | $10^{6}$ $\text{Pa}$                 | Aplicaciones de alta presión       |
    | atmósfera                         | $\text{atm}$               | $1{,}01325\times10^{5}$ $\text{Pa}$    | Presión estándar a nivel del mar   |
    | bar                               | $\text{bar}$               | $10^{5}$ $\text{Pa}$                 | Uso industrial y meteorológico     |
    | milibar                           | $\text{mbar}$              | $10^{2}$ $\text{Pa}$                 | Datos meteorológicos               |
    | milímetro de mercurio             | $\text{mmHg}$ o $\text{torr}$ | $133{,}3$ $\text{Pa}$                | Manometría y medicina              |
    | kilogramo por centímetro cuadrado | $\text{kg}/\text{cm}^{2}$ | $\approx 9{,}81\times10^{4}$ $\text{Pa}$ | Unidad heredada (no SI)          |

:::{tip}
**INTERPRETACIÓN DE 1 ATM**

A nivel del mar, la presión atmosférica ≈ $1{,}013\times10^5$ Pa, equivalente al peso de una columna de aire de unos $200\ \text{kg}$ sobre la superficie de una mano ($\approx0.02\ \text{m}^{2}$).
No sentimos esta carga porque la presión interna del cuerpo la contrarresta; solo las *diferencias de presión* son perceptibles.
:::

---


subsec_local_relative_pressures)=
### Medición local y relativa de la presión

Al medir la presión, lo que registran los instrumentos suele ser la **diferencia** entre la presión local y la presión atmosférica circundante.
Así, distinguimos cuatro magnitudes relacionadas:

| **Tipo de presión**             | **Definición / Expresión**                                  | **Instrumento típico**       |
| :------------------------------ | :---------------------------------------------------------- | :--------------------------- |
| **Presión atmosférica**         | Presión ambiente local                                      | Barómetro                    |
| **Presión absoluta**            | $p_\text{abs}$ — presión total respecto al vacío absoluto   | Barómetro                    |
| **Presión manométrica (gauge)** | $p_\text{man} = p_\text{abs} - p_\text{atm}$               | Manómetro                    |
| **Presión de vacío**            | $p_\text{vac} = p_\text{atm} - p_\text{abs}$               | Vacuómetro                   |

:::{tip}
**CÓMO INTERPRETAR LO QUE MUESTRA EL MANÓMETRO**

Los manómetros y medidores de presión informan la **diferencia** respecto al valor atmosférico actual.
Cuando un neumático marca “2 bar”, significa 2 bar *por encima* de la presión ambiente, no 2 bar absolutos.
:::

---

(subsec_complex_measurable_properties_temperature)=
### Propiedades complejas medibles: temperatura

(subsubsec_microscopic_macroscopic_temperature)=
#### Perspectivas microscópica y macroscópica

Desde el punto de vista **microscópico**, la temperatura mide la **energía cinética promedio** de las partículas:
cuanto mayor es su velocidad media, mayor es la temperatura.
Esto es análogo a la noción de presión microscópica como el efecto colectivo de innumerables impactos de partículas sobre las paredes.

Desde el punto de vista **macroscópico**, la temperatura es una **variable de estado** que indica el grado de equilibrio térmico entre sistemas.

::::{warning}
**NATURALEZA INTENSIVA DE LA TEMPERATURA**

A diferencia de magnitudes extensivas como la masa o la energía, **la temperatura es una propiedad intensiva** — no se suma. Combinar dos cuerpos de agua a $100\ ^\circ\text{C}$ no produce $200\ ^\circ\text{C}$; la temperatura final se sitúa entre ambas, dependiendo de las capacidades caloríficas y las masas.

La figura siguiente ilustra la diferencia entre propiedades extensivas e intensivas al combinar dos sistemas ($A$ y $B$) que, antes de unirse, presentan sus propias masas, volúmenes, temperaturas y presiones. La extensividad de masa y volumen permite sumarlos para obtener la masa y el volumen del sistema combinado. Sin embargo, tal aditividad no es aplicable a la temperatura y la presión, debido a la naturaleza intensiva de estas magnitudes.

:::{figure} 1_fundamentals_figs/magnitudes_extensivity_intensivity.svg
:name: magnitudes_extensivity_intensivity
:width: 60%
:align: center

Ejemplo ilustrativo de la naturaleza extensiva e intensiva de algunas magnitudes termodinámicas principales.
:::
::::

---

(subsubsec_operational_definition_temperature)=
#### Definición operacional

Como la temperatura no puede medirse mediante suma simple ni comparación directa, se requieren dos condiciones:

1. Una **unidad de medida** — el kelvin $\text{K}$ — definida como magnitud fundamental del SI.
2. Un **procedimiento de referencia** para comparar temperaturas, basado en el equilibrio y puntos de referencia reproducibles (por ejemplo, el punto triple del agua).

El establecimiento de tales procedimientos conduce directamente a la noción de **equilibrio termodinámico**,
una condición en la que no ocurren cambios macroscópicos netos y la temperatura es uniforme en todo el sistema.

:::{note}
**POR QUÉ IMPORTA EL EQUILIBRIO**

Definir la temperatura requiere que el sistema esté en equilibrio; de lo contrario, las variaciones locales impiden una medición coherente.
Las escalas termodinámicas de temperatura se basan en estados de equilibrio, que proporcionan condiciones de referencia reproducibles.
:::

---

(subsec_conceptual_closure_magnitudes_properties)=
### Cierre conceptual

* Las magnitudes y propiedades proporcionan el marco medible para describir sistemas termodinámicos.
* Las cantidades fundamentales y derivadas, junto con sus unidades, forman la base de todo análisis termodinámico.
* La distinción entre propiedades extensivas e intensivas define cómo el tamaño del sistema afecta las magnitudes medibles.
* La presión y la temperatura son variables intensivas clave que se conectan directamente con el equilibrio y el intercambio de energía.
* Estos conceptos preparan el terreno para el estudio del equilibrio, las escalas de temperatura y los procesos, como se hace {ref}`en la siguiente sección <sec_equilibrium_temperature_processes>`, donde se introducen formalmente las condiciones de balance y transformación entre estados.


