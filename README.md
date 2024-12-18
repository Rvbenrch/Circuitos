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
- Durante el nivel alto del pulso (\( V = 2V \)), el condensador se **carga exponencialmente**.
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
\[
V_C(t) = V_{max} \cdot \left(1 - e^{-t / \tau}\right)
\]
- Donde \( \tau = R \cdot C \) es la constante de tiempo.

#### **Descarga del condensador**
La ecuación del voltaje durante la descarga es:
\[
V_C(t) = V_{max} \cdot e^{-t / \tau}
\]

### **2. Constante de Tiempo (τ)**
La constante de tiempo determina la rapidez con la que el condensador se carga o descarga:
- A \( t = \tau \), el voltaje en el condensador alcanza el **63% del valor final** durante la carga.
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

## **Próximos pasos**
En la siguiente parte de la práctica, analizaremos un **circuito RLC** para estudiar su comportamiento oscilatorio y su respuesta transitoria.

---

**Autor:** *(Rubén M. Rodríguez Chamorro)*  
**Fecha:** *(18/12/2024)*  
**Herramienta utilizada:** LTspice
