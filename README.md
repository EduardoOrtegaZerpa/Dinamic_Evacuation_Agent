# Simulación de Evacuación Multiagente (NetLogo)

Este proyecto implementa un **modelo multiagente de evacuación** en NetLogo, donde personas intentan abandonar un entorno urbano con **obstáculos** y **salidas de capacidad limitada**. El comportamiento de los agentes incorpora **pánico**, **conocimiento del entorno** y **dinámicas sociales**.


## Agentes del modelo

### Personas
Individuos que se desplazan hacia una salida para evacuar.

**Atributos principales:**
- Velocidad  
- Nivel de pánico  
- Conocimiento del entorno  
- Estado de evacuación  
- Salida objetivo  

### Salidas
Puntos de evacuación con capacidad limitada y tasa de servicio.

**Atributos:**
- Capacidad máxima  
- Personas evacuadas  
- Probabilidad de evacuación por tick  

### Entorno
Parches que pueden contener obstáculos (edificios) que restringen el movimiento.


## Dinámica de la simulación

En cada tick:
- Las personas se mueven hacia su salida objetivo.
- La velocidad depende del pánico y la densidad local.
- Se evita atravesar obstáculos.
- La evacuación ocurre si la salida tiene capacidad disponible.

La simulación finaliza cuando todas las personas han evacuado.


## Selección de salidas

Las personas eligen una salida siguiendo este orden:
1. **Conocimiento del entorno** (salida más cercana).
2. **Imitación social** (seguir a vecinos).
3. **Elección aleatoria**.


## Visualización

- Personas coloreadas según su nivel de pánico.
- Obstáculos en negro y salidas en verde.
- Gráfica de personas evacuadas a lo largo del tiempo.


## Parámetros configurables

- Número de personas  
- Número de salidas  
- Número de edificios  
- Capacidad de las salidas  
- Nivel de pánico global  
- Porcentaje de visitantes  
