(sec_maci_mechanical_classification)=
## Clasificación mecánica de los MACIs

Antes de introducir el modelado termodinámico (ciclos Otto/Diesel, ideal frente a real), resulta conveniente clasificar los MACIs mediante criterios que dependan únicamente del **movimiento mecánico** y de la forma en que el motor completa una secuencia de trabajo. Esta clasificación es independiente de cómo se idealice la adición de calor y, por tanto, proporciona una capa descriptiva neutral.

La clasificación mecánica se organiza en torno a dos preguntas principales:

- *¿Cómo se produce y se transmite el trabajo útil?*  
- *¿Cuántas carreras mecánicas se requieren para completar un ciclo?*

---

### Clasificación según el movimiento del elemento de trabajo

Un primer criterio se refiere al movimiento del elemento que interactúa con el fluido de trabajo y que, en última instancia, entrega trabajo mecánico.

- **Motores alternativos:**  
  El elemento de trabajo es un pistón que se desplaza linealmente en el interior de un cilindro. El pistón está conectado a una biela y a un cigüeñal, convirtiendo el movimiento alternativo en rotación. Esta es la configuración dominante en la mayoría de los vehículos de carretera y en una amplia gama de máquinas de uso práctico.

- **Motores rotativos:**  
  El pistón se sustituye por un rotor que gira de forma continua. El representante clásico es el **motor Wankel**, que emplea un rotor triangular que se mueve dentro de una cámara de geometría aproximadamente epitrocoidal.

:::{important}

**ALTERNATIVOS FRENTE A ROTATIVOS: UNA DISTINCIÓN MECÁNICA FUNDAMENTAL**

Los motores alternativos implican de forma inherente aceleraciones y desaceleraciones alternadas de masas, lo que produce vibraciones e impone restricciones mecánicas a altas velocidades.
Los motores rotativos evitan la inercia alterna, pero introducen otros desafíos, en particular el sellado y el control de la geometría de la cámara de combustión.

:::

---

### Clasificación según el número de carreras (motores alternativos)

Los motores alternativos se clasifican además según el número de carreras del pistón necesarias para completar un ciclo termo-mecánico:

- **Motores de cuatro tiempos**
- **Motores de dos tiempos**

El término *carrera* se refiere al desplazamiento del pistón desde una posición extrema hasta la otra:

- desde el **punto muerto superior** (PMS) hasta el **punto muerto inferior** (PMI),
- o desde el PMI hasta el PMS.

---

### Motores de combustión interna de cuatro tiempos

Los motores de cuatro tiempos reciben este nombre porque un ciclo requiere **cuatro carreras del pistón**, correspondientes a dos revoluciones del cigüeñal.

Para describir el ciclo, conviene recordar los principales componentes implicados:

- **pistón**, que se mueve dentro del cilindro,  
- **bulón**, que conecta el pistón y la biela,  
- **biela**, que transmite la fuerza al cigüeñal,  
- **cigüeñal**, que convierte el movimiento lineal en rotación,  
- **válvulas de admisión y escape**, que controlan el intercambio de gases,  
- y bien una **bujía** (encendido por chispa), bien un **inyector de combustible** (encendido por compresión).

Las cuatro carreras son:

- **Carrera de admisión:**  
  El pistón se mueve desde el PMS hasta el PMI mientras la válvula de admisión está abierta. La carga fresca entra en el cilindro:
  - una mezcla combustible-aire en motores de encendido por chispa,
  - aire solo en motores de encendido por compresión.

- **Carrera de compresión:**  
  El pistón se mueve desde el PMI hasta el PMS con ambas válvulas cerradas. La carga se comprime, aumentando la presión y la temperatura.

- **Combustión y expansión (carrera útil):**  
  Cerca del PMS, tiene lugar la combustión:
  - encendido por chispa en los motores SI,
  - inyección de combustible y autoencendido en los motores CI.  
  La rápida liberación de energía química incrementa la presión y empuja el pistón hacia el PMI, entregando trabajo mecánico.

- **Carrera de escape:**  
  El pistón vuelve desde el PMI hasta el PMS mientras la válvula de escape está abierta, expulsando los gases quemados.

:::{note}

**SEPARACIÓN MECÁNICA DE FUNCIONES**

En los motores de cuatro tiempos, la admisión, la compresión, la producción de potencia y el escape se separan mecánicamente en carreras distintas. Esto mejora el control del intercambio de gases y reduce el cortocircuito directo de carga fresca hacia el escape, lo que favorece la eficiencia y el control de emisiones.

:::

---

### Motores de combustión interna de dos tiempos

Los motores de dos tiempos completan un ciclo con solo **dos carreras** (una revolución del cigüeñal). La misma secuencia física (admisión, compresión, combustión y escape) sigue existiendo, pero se consigue mediante una disposición mecánica diferente.

En lugar de válvulas de asiento que controlen la admisión y el escape, los motores de dos tiempos suelen basarse en lumbreras:

- una **lumbrera de admisión** y una **lumbrera de escape** se abren y cierran según la posición del pistón,
- la configuración del motor suele integrar barrido por cárter u otros métodos para suministrar la carga fresca.

Una descripción simplificada es la siguiente:

- **Carrera descendente (expansión + barrido):**  
  La combustión tiene lugar cerca del PMS y, a continuación, la expansión empuja el pistón hacia abajo. Cerca del final de la carrera, se abre la lumbrera de escape y luego se abren las lumbreras de admisión/barrido, permitiendo que entren gases frescos y desplacen hacia fuera los gases de escape.

- **Carrera ascendente (compresión + preparación de la ignición):**  
  El pistón se mueve hacia arriba, comprimiendo la carga fresca. Cerca del PMS, se produce la ignición (SI) o se inyecta el combustible y se autoenciende (CI), dando comienzo a la siguiente expansión.

Debido al solapamiento entre admisión y escape, parte de la carga fresca puede escapar por el escape. Esto tiende a aumentar el consumo de combustible y las emisiones.

La lubricación suele diferir de la de los motores de cuatro tiempos. No siempre es viable disponer de un cárter de aceite separado, y el aceite puede mezclarse con el combustible o suministrarse de forma simplificada, lo que puede provocar su combustión y aumentar las emisiones contaminantes.

:::{important}

**POR QUÉ LOS MOTORES DE DOS TIEMPOS IMPLICAN UN COMPROMISO**

Los motores de dos tiempos pueden proporcionar una elevada potencia específica porque se produce una carrera útil en cada revolución.
Sin embargo, las pérdidas de barrido y las limitaciones de lubricación suelen reducir la eficiencia y aumentar las emisiones en comparación con los diseños de cuatro tiempos.

:::

Los desarrollos modernos (inyección directa, barrido controlado electrónicamente, combustión estratificada) han reducido de forma significativa las pérdidas por cortocircuito y han reavivado el interés por los conceptos de dos tiempos en aplicaciones especializadas.

---

### Motores rotativos (motores Wankel)

El motor Wankel sustituye la disposición pistón-cilindro por:

- un **rotor triangular**,
- que gira dentro de una cámara aproximadamente ovalada.

A medida que el rotor gira, se forman tres volúmenes separados entre las caras del rotor y la carcasa. Cada volumen experimenta admisión, compresión, combustión y escape, pero los procesos tienen lugar en diferentes regiones espaciales de la carcasa, en lugar de en carreras distintas separadas en el tiempo.

Entre sus ventajas suelen incluirse:

- funcionamiento suave y baja vibración (ausencia de masas alternativas),
- compacidad y elevada relación potencia-peso,
- capacidad para operar a altas velocidades de rotación.

Entre sus desventajas se incluyen:

- dificultades de sellado en los vértices del rotor,
- mayor consumo de combustible en muchas configuraciones,
- y posibles dificultades para controlar la forma de la cámara de combustión y las pérdidas térmicas.

:::{note}

**CARRERAS ESPACIALES**

Un motor Wankel puede compararse termodinámicamente con un motor de cuatro tiempos, pero mecánicamente es fundamentalmente distinto: las “carreras” están distribuidas espacialmente en lugar de separadas temporalmente.

:::

---

### Cierre conceptual

- La clasificación mecánica describe cómo se produce y se transmite el movimiento, con independencia del modelado termodinámico.
- Los motores alternativos y los rotativos difieren principalmente en la cinemática, los efectos de inercia y las restricciones de sellado.
- Los motores de cuatro tiempos priorizan la separación de funciones y un mejor control del intercambio de gases.
- Los motores de dos tiempos priorizan la simplicidad y la alta densidad de potencia, pero afrontan desafíos de barrido y lubricación.
- Esta base mecánica prepara el análisis de clasificaciones más amplias del motor a nivel de sistema.

