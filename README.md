# Práctica 2 - Análisis de un circuito RC

## **Introducción**
En esta práctica, hemos analizado el comportamiento de un **circuito RC** (Resistor-Capacitor) utilizando la herramienta de simulación **LTspice**. Se estudia la **respuesta temporal** del circuito al ser excitado con una señal de tren de pulsos.

---

## **Objetivo**
- Estudiar la carga y descarga exponencial de un condensador en un circuito RC.
- Obtener y comparar la constante de tiempo (τ) teórica y simulada.
- Visualizar el comportamiento de voltaje y corriente en el circuito.

---
<details>
  <summary> Circuito en RC (práctica 2 / parte 1 </summary>
## **Circuito Analizado**
<details>
  <summary>Mostrar imagen del circuito RC</summary>

  ![image](https://github.com/user-attachments/assets/9a1ba785-75ef-40f7-bd74-4663a22e2346)
</details>

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

<details>
  <summary>Mostrar configuración de la simulación</summary>

  ![image](https://github.com/user-attachments/assets/981ea8d7-9f96-4b87-8297-44e03e2b17b7)
</details>

---

## **Resultados obtenidos**


### **Medición de la constante de tiempo (τ)**
La constante de tiempo teórica se calcula como:


  <summary>Cálculo de la constante de tiempo</summary>

  ![image](https://github.com/user-attachments/assets/830084e5-0aab-44c1-9169-9c3c2d987586)


**Resultados de la simulación:**
<details>
  <summary>Mostrar resultados</summary>

  ![image](https://github.com/user-attachments/assets/d5e2d401-7b42-4d86-8cd0-151fde461903)
</details>

---

## **Conceptos Teóricos**

### **1. Circuito RC**

![image](https://github.com/user-attachments/assets/dce83658-088c-4de3-9498-d980c46c14bb)


- **Conclusión Ciruito RC:** 
Se cumple que cuando el condensador este descargado, se carga exponencialmente siguiendo las indicaciones anteriorores 🙏
---
</details>
## **Circuito RLC**
<details>
  <summary>Mostrar imagen del circuito RLC</summary>

![image](https://github.com/user-attachments/assets/b640d003-1f43-401d-bd5c-0c83d5d39fee)

</details>

### **Configuración del circuito**
- **Resistencia (R1):** 1 kΩ.
- **Inductor (L1):** 680 μH.
- **Condensador (C1):** 22 pF.

<details>
  <summary>Mostrar configuración de simulación</summary>

  ![image](https://github.com/user-attachments/assets/86bb4c15-a14e-418d-8873-e15de9f8606a)
</details>

---

## **Cálculos teóricos y resultados**

### **Frecuencia natural de oscilación**
\[
f_0 = \frac{1}{2\pi \sqrt{L \cdot C}}
\]

### **Cálculo de resistencia crítica**
\[
R_c = 2 \sqrt{\frac{L}{C}}
\]

### **Frecuencia amortiguada**
\[
f_d = f_0 \cdot \sqrt{1 - \left( \frac{R}{R_c} \right)^2}
\]

<details>
  <summary>Mostrar resultados del cálculo</summary>

  - **R = 1 kΩ < R_c = 11.12 kΩ**
  - **Frecuencia amortiguada ≈ 1.295 MHz**

  ![image](https://github.com/user-attachments/assets/6b63879f-2e59-4c1c-9eac-13092e0e68cd)
</details>

---

## **Conclusiones**
1. El sistema es **subamortiguado** porque \( R < R_c \).
2. Las oscilaciones amortiguadas coinciden con la teoría.
3. Si aumentamos \( R \), el sistema pasa a ser críticamente amortiguado o sobreamortiguado.

<details>
  <summary>Mostrar gráfica final del resultado obtenido</summary>

  ![image](https://github.com/user-attachments/assets/b45dabe1-a9bc-4ba5-aac5-d5e8312c01d7)
</details>

---

## **Autor**  
- **Nombre:** Rubén M. Rodríguez Chamorro  
- **Fecha:** 18/12/2024  
- **Herramienta utilizada:** LTspice
