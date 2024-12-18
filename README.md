# Práctica 2 - Análisis de un circuito RC

## **Introducción**
En esta práctica, hemos analizado el comportamiento de un **circuito RC** (Resistor-Capacitor) utilizando la herramienta de simulación **LTspice**. Se estudia la **respuesta temporal** del circuito al ser excitado con una señal de tren de pulsos.

---

## **Objetivo**
- Estudiar la carga y descarga exponencial de un condensador en un circuito RC.
- Obtener y comparar la constante de tiempo (τ) teórica y simulada.
- Visualizar el comportamiento de voltaje y corriente en el circuito.

---
## **Práctica 2** 

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

![image](https://github.com/user-attachments/assets/2c8b8409-2dbe-4f43-923e-be1e8a8bd048)


</details>

### Cómo verificamos que hemos realizado bien los procedimientos, vamos a ver y comprobarlo de manera teórica, tenemos que:


![image](https://github.com/user-attachments/assets/b1dda854-7733-4cdd-a784-350b49da275e)

Para confirmar que estamos en el régimen adecuado y comprobar los resultados Usamos la fórmula anterior 👆
- 1. Si el régimen es crítico: Las raices son iguales y negativas (s1 y s2)
- 2. Su es sobreamorticuado ( R > Rc): Entonces las raices (s1 y s2) son reales, distintas y negativas.
- 3. Para R = 15kΩ (sobreamortiguado):

![image](https://github.com/user-attachments/assets/2b77a580-f106-4324-829c-388b964fa21c)


</details>
---


### Preguntas Práctica 2 (2024):

<details> 
<summary>PREGUNTAS:</summary>
  
<details>
  <summary>Pregunta 1: </summary>
  
![image](https://github.com/user-attachments/assets/4778d3b2-d4a2-4acc-81ff-3ea99e8e4262)

- Solución 1: 
  
![image](https://github.com/user-attachments/assets/52de9b1c-867c-4388-8c9f-d816107a214d)

El polo de un sistema RC está relacionado con la inversa de la constante de tiempo (τ).

</details>

<details>
<summary>Pregunta 2: </summary>
  
![image](https://github.com/user-attachments/assets/399b8477-74d2-4586-9727-02c9ab165903)


<summary>Solución 2: </summary>
Aquí nos están pidiendo la (T) que nos indicaban antes su inversa:


  ![image](https://github.com/user-attachments/assets/795e09ee-438b-4656-8370-7693eb0de7ce)

</details>


<details>
  <summary>Regunta 3: </summary>

  ![image](https://github.com/user-attachments/assets/73283ba3-0d41-4b80-aba5-aa670c4b78ad)

  - Solución:
Al simular el circuito en LTspice, se midió la constante de tiempo directamente desde la curva exponencial de carga/descarga del condensador.
El valor obtenido en simulación confirma que:
La constante de tiempo teórica (220𝑛𝑠) coincide con el valor medido, lo cual valida tanto el modelo teórico como la simulación.
  
</details>

<details>
  <summary>Regunta 4: </summary>

![image](https://github.com/user-attachments/assets/bb28b829-fcc2-4e6e-b413-d98ea10757d6)

- Solución:

Si miramos antes hemos configurado:


![image](https://github.com/user-attachments/assets/738b1e29-2b35-4a94-b411-1320b263d196)

(creo que este apartado lo habia configurado mal antes pero ya sabemos que tiene que ser en t period 2ms :(

</details>

<details>
  <summary>Pregunta 5 , 6 y 7: </summary>

  ![image](https://github.com/user-attachments/assets/48682df3-433b-4ed2-abb9-e44f914e03f2)



- Solución 5:
  
![image](https://github.com/user-attachments/assets/1a7300c6-7781-4b07-8a4f-680e5a4c2fd8)

- Solución 6:

![image](https://github.com/user-attachments/assets/a722ca57-1962-46b3-81aa-3d9562e452dd)

- Solución 7:

![image](https://github.com/user-attachments/assets/cba890a6-fd8a-4438-be16-c5746cd977c3)

</details>
</details>

<details>
  <summary> Resumen de las preguntas práctica 2: </summary>

  ![image](https://github.com/user-attachments/assets/567dafb4-e0de-4587-af59-21bc8a4e03b9)

</details>


# Práctica 3

![image](https://github.com/user-attachments/assets/741223a3-fbe5-467d-9622-b1a89ef00e18)

![image](https://github.com/user-attachments/assets/d0e9a325-1932-45f0-be92-d38bae9fe58e)


![image](https://github.com/user-attachments/assets/b3c147f2-5dc5-48ca-bdbf-56a25f7ae29b)


![image](https://github.com/user-attachments/assets/0464d79a-7cec-4225-851b-1531821adbb5)

![image](https://github.com/user-attachments/assets/427ff4ec-c038-4492-9457-fbcd19803708)


![image](https://github.com/user-attachments/assets/00900143-b0a4-4e1a-bd81-6b2fcb3e7fcc)

![image](https://github.com/user-attachments/assets/426714a2-bc7d-4c92-8747-d1d22f63e57e)

### **2.1. Estudio teórico previo:**

![image](https://github.com/user-attachments/assets/1e35733a-86dd-4222-8544-960f00ce5e9b)


![image](https://github.com/user-attachments/assets/a00e6006-f956-4494-94bc-ff177de983a9)



![image](https://github.com/user-attachments/assets/7bcb33ad-2c16-41bd-ba7a-217d5b8f5452)

¿ Qué signfica todo esto?

DEFINICIÓN:
- Un amplificador no inversor es un circuito operacional (Op-Amp)
- La señal de entrada Vi, se aplica al terminal no inversor (+)
- La ganancia es positiva, lo que significa que la saida está en fase con la entrada.

Ganancia teórica: 

![image](https://github.com/user-attachments/assets/2612b6ab-45b9-4f07-9c2f-31e4a2021884)

La ganancia en (db) se calcula como 20 log10(H) porque es una fórmula.

![image](https://github.com/user-attachments/assets/9b9a772b-7c06-486c-ab1d-189a52a9d520)


## **Autor**  
- **Nombre:** Rubén M. Rodríguez Chamorro  
- **Fecha:** 18/12/2024  
- **Herramienta utilizada:** LTspice
