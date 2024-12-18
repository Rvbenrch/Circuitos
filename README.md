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
  <summary> Circuito en RC (práctica 2 / parte 1) </summary>
  

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


<details>
  <summary> Circuito RLC (práctica 2 / parte 2) </summary>
  

<details>
  <summary> La R tiene un valor R = 1k. </summary>

  
<summary>Imagen del circuito RLC: </summary>

![image](https://github.com/user-attachments/assets/b640d003-1f43-401d-bd5c-0c83d5d39fee)



<summary> Configuración del circuito: </summary>

- **Resistencia (R1):** 1 kΩ.
- **Inductor (L1):** 680 μH.
- **Condensador (C1):** 22 pF.

<summary>Configuración de simulación</summary>

![image](https://github.com/user-attachments/assets/86bb4c15-a14e-418d-8873-e15de9f8606a)



<summary>Cálculos teóricos y resultados: </summary>

![image](https://github.com/user-attachments/assets/709c3e78-952d-46c3-aa02-6444abcf4e36)



<summary>Mostrar resultados del cálculo</summary>

- R = 1 kΩ < R_c = 11.12 kΩ**
-  **Frecuencia amortiguada ≈ 1.295 MHz**
  
![image](https://github.com/user-attachments/assets/0a2abaeb-87f2-48ae-9dee-258010973f66)

![image](https://github.com/user-attachments/assets/5c7b921f-b7b2-43f2-926c-a27139fc029e)

![image](https://github.com/user-attachments/assets/6b63879f-2e59-4c1c-9eac-13092e0e68cd)



---

## **Conclusiones**
1. El sistema es **subamortiguado** porque \( R < R_c \).
2. Las oscilaciones amortiguadas coinciden con la teoría.
3. Si aumentamos \( R \), el sistema pasa a ser críticamente amortiguado o sobreamortiguado.

<details>
  <summary>Mostrar gráfica final del resultado obtenido</summary>

  ![image](https://github.com/user-attachments/assets/b45dabe1-a9bc-4ba5-aac5-d5e8312c01d7)
</details>

![image](https://github.com/user-attachments/assets/8821ae98-a6e3-411f-9618-5dfef0aee27f)

</details>

<details>
  <summary>Valor de K = 15kΩ: </summary>

### Circuito: 

![image](https://github.com/user-attachments/assets/6d68025c-0719-4a2d-a083-f39c9ed68f47)

-  Comportamiento de sobreamortiguado:
  
![image](https://github.com/user-attachments/assets/3e3c8068-868d-4a52-87ff-e85dda63bd0f)

- Explicación teórica:

![image](https://github.com/user-attachments/assets/b29a0e03-a9cd-4b07-855a-1dce70e90684)


![image](https://github.com/user-attachments/assets/33c1f200-5075-47c4-ac72-9845f0cb7f48)


- Resultado de la gráfica:

![image](https://github.com/user-attachments/assets/7e6333df-9e07-4d89-bd7c-54fe5ca7ae39)

- Conclusiones:

![image](https://github.com/user-attachments/assets/17457d07-995a-49e9-90fc-d511bf907a12)



</details>

<details> 
<summary> k = 11.12k  </summary> 

![image](https://github.com/user-attachments/assets/d25f21f7-8485-47d3-a1df-e8113bdb4f17)

![image](https://github.com/user-attachments/assets/ae3870bd-16bb-4efd-85c0-2b8cc9e2d440)


</details>
</details>
---

## **Autor**  
- **Nombre:** Rubén M. Rodríguez Chamorro  
- **Fecha:** 18/12/2024  
- **Herramienta utilizada:** LTspice
