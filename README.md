# Práctica 2 - Análisis de un circuito RC

## **Introducción**
En esta práctica, hemos analizado el comportamiento de un **circuito RC** (Resistor-Capacitor) utilizando la herramienta de simulación **LTspice**. Se estudia la **respuesta temporal** del circuito al ser excitado con una señal de tren de pulsos.

---

## **Objetivo**
- Estudiar la carga y descarga exponencial de un condensador en un circuito RC.
- Obtener y comparar la constante de tiempo (τ) teórica y simulada.
- Visualizar el comportamiento de voltaje y corriente en el circuito.

---

## **Circuito Analizado**
El circuito RC utilizado es el siguiente:

![image](https://github.com/user-attachments/assets/9a1ba785-75ef-40f7-bd74-4663a22e2346)


- **R1 (Resistencia):** 10 kΩ.
- **C1 (Condensador):** 22 pF.
- **Generador de señales:** Tren de pulsos configurado como:
  - **Nivel bajo (Vinitial):** 0 V.
  - **Nivel alto (Von):** 2 V.
  - **Tiempo de subida (Trise):** 1 ns.
  - **Tiempo de bajada (Tfall):** 1 ns.
  - **Duración del pulso (Ton):** 1 ms.
  - **Periodo total (Tperiod):** 10 ms.


---

## **Configuración de la simulación**
Para observar la respuesta del circuito, realizamos una simulación **transitoria**:
- **Stop time:** 20 ms.
- **Maximum Timestep:** 0.1 ms.
![image](https://github.com/user-attachments/assets/981ea8d7-9f96-4b87-8297-44e03e2b17b7)

---

## **Resultados obtenidos**
### **Gráficas**
1. **Señal de entrada (tren de pulsos):**
   - Señal rectangular alternando entre 0 V y 2 V.
2. **Voltaje en el nodo del condensador:**
   - Curva exponencial de carga y descarga.

### **Observaciones:**
- Durante el nivel alto del pulso (V = 2V), el condensador se **carga exponencialmente**.
- Cuando la señal vuelve a 0 V, el condensador se **descarga exponencialmente**.

### **Medición de la constante de tiempo (τ):**
La constante de tiempo teórica se calcula como:

![image](https://github.com/user-attachments/assets/830084e5-0aab-44c1-9169-9c3c2d987586)


**Resultados de la simulación:**
- La curva medida en LTspice confirma que el tiempo para alcanzar el **63%** del valor final (1.26 V) corresponde aproximadamente a **220 ns**.

  ![image](https://github.com/user-attachments/assets/d5e2d401-7b42-4d86-8cd0-151fde461903)


---

## **Conceptos Teóricos**

### **1. Circuito RC**
Un circuito RC está compuesto por una **resistencia (R)** y un **condensador (C)** conectados en serie.

#### **Carga del condensador**
La ecuación del voltaje en el condensador durante la carga es:


Vc(t) = V{max} * (1 - e^{-t / tau})

- Donde ( tau = R * C ) es la constante de tiempo.

#### **Descarga del condensador**
La ecuación del voltaje durante la descarga es:

Vc(t) = V{max} * e^{-t/tau}


### **2. Constante de Tiempo (τ)**
La constante de tiempo determina la rapidez con la que el condensador se carga o descarga:
- A (t = tau), el voltaje en el condensador alcanza el **63% del valor final** durante la carga.
- En la descarga, el voltaje cae al **37% del valor inicial**.

### **3. Respuesta transitoria**
La respuesta transitoria describe el comportamiento del circuito cuando se aplica una señal no constante (como un pulso).
- El condensador se carga y descarga exponencialmente, siguiendo las ecuaciones anteriores.

---

## **Conclusiones**
1. El circuito RC responde de acuerdo con la teoría:
   - La carga y descarga del condensador siguen una curva exponencial.
   - La constante de tiempo teórica coincide con la medida en la simulación.
2. La herramienta **LTspice** permite visualizar y analizar de manera precisa la respuesta transitoria del circuito.

---

## **Circuito RLC**
 **circuito RLC** para estudiar su comportamiento oscilatorio y su respuesta transitoria.
* Circuito RLC Serie
- Resistencia (R1): 1kΩ.
- Inductor (L1): 680μH.
- Condensador (C1): 𝐹22pF.
Generador de pulsos (V1): Tren de pulsos como en el caso anterior

// 
**Comportamiento esperado.**
En este circuito RLC, se combina resistencia, Inductor y Condensador, lo que produce un movimiento oscilatorio amortiguado. Dependiendo del valor de la resistencia, el circuito puede clasificarse como: 
- 1. Subamortiguado: Oscilaciones amortiguadas (R pequeña)
  2. Criticamente amortiguado: Respuesta más rápida sin oscilaciones (R óptima).
  3. Sobreamortiguado:: Respuesta lenta sin oscilaciones (R grande).

- **Frecuencia natural de oscilación.**
  
![image](https://github.com/user-attachments/assets/659f2ac2-1f5c-4a1b-98c6-a569c58e29da)

- Configuración de la simulación Ltspice.
  
![image](https://github.com/user-attachments/assets/86bb4c15-a14e-418d-8873-e15de9f8606a)

**¿Qué es esto de tipos de movimiento oscilatorios?**
Tipos de Movimiento Oscilatorio
La naturaleza de las oscilaciones depende del amortiguamiento, que está determinado por la resistencia 
R. Hay tres tipos de respuesta en un circuito RLC:

- **a) Subamortiguado**
  
![image](https://github.com/user-attachments/assets/fe3c9091-8ccf-4b00-b78b-bdd56053cc8c)

- **b) Amortiguamiento crítico**
  
![image](https://github.com/user-attachments/assets/ba4c9533-4db2-413a-bce2-58ecd99d5c37)

- **c) Sobreamortiguamiento**
  
![image](https://github.com/user-attachments/assets/7be48677-9d03-4207-963b-854b992cd2ff)

![image](https://github.com/user-attachments/assets/2bc22a4a-6ec7-4068-afbc-b5f88f3598be)

![image](https://github.com/user-attachments/assets/01679d15-83f8-4799-9046-84f14d05e358)

** Cómo lo calculamos en nuestro circuito:**
Datos: 
  - R = 1kΩ
  - L = 680μH
  - C = 22pF



​![image](https://github.com/user-attachments/assets/6eea7564-838b-4c4a-8e0d-0d1694e5221e)


![image](https://github.com/user-attachments/assets/15fdad9c-12fc-4346-851a-69a782286cc3)


Teniendo en cuenta los cálculos teorícos de los respectivos amortiguamientos concluimos con que es subamortiguado: 

El sistema actual es subamortiguado porque:
** 𝑅=1 𝑘Ω < 𝑅𝑐 = 11.12𝑘Ω.**

Las oscilaciones amortiguadas observadas en la gráfica coinciden con la teoría:
La frecuencia amortiguada es aproximadamente 
1.295 MHz Si aumentamos R, podremos observar los otros tipos de amortiguamiento:
* Amortiguamiento crítico: La oscilación desaparece.
* Sobreamortiguado: La respuesta es más lenta.

![image](https://github.com/user-attachments/assets/6b63879f-2e59-4c1c-9eac-13092e0e68cd)

Sabiendo esto de arriba 👆

¿A cuál corresponde con el resutlado que hemos obtenido? 👇

**EL RESULTADO OBTENIDO:**

![image](https://github.com/user-attachments/assets/b45dabe1-a9bc-4ba5-aac5-d5e8312c01d7)

---


**Autor:** *(Rubén M. Rodríguez Chamorro)*  
**Fecha:** *(18/12/2024)*  
**Herramienta utilizada:** LTspice
