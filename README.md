# Robotica_movil_Laboratorio_1

## Integrantes
  - Javier Danilo Tovar Rodriguez
  - David Felipe Ruiz Reyes
  - Diego Andres Fernandez Sosa
 
## Introducción

En el mundo de la robótica móvil, el uso de vehículos terrestres tiene gran relevancia. Por ello, es vital el reconocimiento de las siguientes características que llegan a tener por ejemplo el Lego EV3 utilizado en este laboratorio, como: el comportamiento del movimiento en llantas, el comportamiento de los sensores junto a sus formas de comunicación y el uso de una lógica de una programación asertiva, correspondiente a la mecánica/electrónica del robot.

## Objetivos

 - Realizar las actividades propuestas utilizando el robot LEGO EV3 y el software LEGO MINDSTORMS Education EV3 para el reconocimiento de los requerimientos de ingeniería en robots móviles desde una vista práctica.
 - Reconocer las características y la lógica que utilizan los sensores, actuadores y comunicaciones del Robot Lego EV3.

## Retos

## Actividad 1

 - ### Reto 1: 
    - **Objetivo:** Realizar un programa que permita al robot avanzar en linea recta, durante x tiempo, luego avanzar un tiempo diferente y verificar la linealidad de la velocidad.
    - **Solución planteada:**
    Para resolver el reto planteado, se implementa un codigo que realiza un avance por dos segundos, luego se detiene y regresa por dos segundos, despues de esto se repite el proceso con un avance de 4 segundos.
    - **Diagrama de flujo:**
    El flujo del programa se plantea de forma secuencial, en la siguiente imagen:
    ![Diagrama de flujo Punto 1](./img/flujo_1.png)
    - **Codigo de bloques:**
    ![Codigo de bloques Punto 1](./img/bloques_1.png)
    - **Resultados:**
  
      
 - ### Reto 2: 
    - **Objetivo:** Usar el encoder de los motores para contar las revoluciones de las ruedas y avanzar en linea recta hasta completar 8 revoluciones. Aparte, se debe generar una trayectoria en forma de S.
    - **Solución planteada:**
    Para resolver el reto planteado, se implementa un codigo que realiza un avance constante dentro de un bucle, el cual evalua el numero de revoluciones de las ruedas y se detiene cuando alcanza o supera las 8 revoluciones * Se añade una pausa al inicio para poder colocar el robot en la posicion deseada y que este pueda avanzar en linea recta *.
    - **Diagrama de flujo:** El diagrama de flujo, es simplemente un ciclo con una condicion de parada.
    ![Diagrama de flujo Punto 1](./img/flujo_2.png)
    - **Codigo de bloques:**
    ![Codigo de bloques Punto 1](./img/bloques_2.png)
   
    - **Resultados:** 2 * pi * 8rev * 28mm_radio = 1,4 metros de avance. 

 - ### Reto 3: 
    - **Objetivo:** Usar el sensor ultrasónico para detener un movimiento de línea recta cuando se detecte un obstáculo a 10cm de distancia.
    - **Solución planteada:** Dentro de un ciclo while se evalua la condicion del sensor de distancia ultrasónico y se ordena la parada cuando se cumpla.
    - **Diagrama de flujo:** El diagrama de flujo, es simplemente un ciclo con una condicion de parada.
    - **Codigo de bloques:**
    - **Resultados:** Diferencias entre medición del sensor y el flexómetro a dos distancias distintas:
      (REAL=9cm y sensor=9,5cm Potencia=10) (REAL=7cm y sensor=6,7cm Potencia=50)

  
## Actividad 2:
  - ### Reto 1:
    - **Objetivo:** Mover las ruedas a distintas velocidades en ambas direcciones. La diferencia se dará en que una rueda se moverá en las siguientes proporciones con respecto a la otra: 1/2 y 1/3. 
    - **Solución planteada:** Se condiciona la velocidad de las ruedas independientemente, se ejecuta el programa y se mide el radio de giro correspondiente.
    - **Diagrama de flujo:**
    - **Codigo de bloque:**
     ![Codigo de bloques Punto 2](./img/2.png)
  
  - **Resultados:**
    
  - ### Reto 2:
    - **Objetivo:** Crear una trayectoria en forma de S
    - **Solución planteada:** Se realiza un bucle y una interrupción, en donde para las "i primeras revoluciones" se tenga un motor con menos potencia generando el giro y despues al superar esas i revoluciones
    se inviertan las potencias de los motores, generando el giro inverso. El bucle acaba despues de n revoluciones.
    - **Diagrama de flujo:**
    - **Codigo de bloque:**
      ![Codigo de bloques Punto 2 - S](./img/s.png)
  
  - **Resultados:**



## Actividad 3:
  - ### Reto:
    - **Objetivo:** Usar el girosensor para generar un movimiento en línea recta que en cierto momento cambie su dirección en 45 y 135 grados. 
    - **Solución planteada:** Se programa el robot para que avance tres revoluciones inicialmente, luego dentro de un bucle se da giro y se evalua si este es mayor o igual al valor indicado (45 y 135), si se cumple la condicion permite de nuevo realizar un avance recto como al principio.
    - **Diagrama de flujo:**
    - **Codigo de bloque:**
   ![Codigo de bloques Punto 3](./img/rotat_135.png)
   
  - **Resultados:**


## Actividad 4:
 - ### Reto: 
    - **Objetivo:** Usar el sensor infrarrojo para realizar la siguiente lógica: Avance indeterminado en línea recta donde al detectar un obstáculo a Xcm de distancia se devuelva 10cm, gire 45° y siga su camino.
    - **Solución planteada:** Se programa un bucle para evaluar el estado del receptor infrarrojo mientras el robot avanza en linea recta, cuando se cumple la condicion de distancia se da reversa al robot y se le da giro. Al terminar se le da un avance final en linea recta.               
    - **Diagrama de flujo:**
      
   ![Diagrama de flujo Punto 4](./img/FlujoAct4.png)

    - **Codigo de bloque:**
    - 
   ![Codigo de bloques Punto 4](./img/infrarrojo_90.png)

    - **Resultados:**

## Actividad 5:
 - ### Reto: 
    - **Objetivo:** Usar el sensor de contacto para realizar la siguiente lógica: Avance indeterminado en línea recta donde al detectar un obstáculo a Xcm de distancia se devuelva 10cm (distancia dada por otro sensor), gire 45° y siga su camino.
    - **Solución planteada:** Se programa un bucle para que el robot avance mientras se evalua la condicion del sensor de contacto. Cuando se cumple dicha condicion, se da reversa al robot y se le da giro de 90°. Al terminar se regresa al inicio del programa y vuelve a comenzar.
    - **Diagrama de flujo:**

     ![Diagrama de flujo Punto 5](./img/FlujoAct5.png)

    - **Codigo de bloque:**
      
   ![Codigo de bloques Punto 5](./img/infrarrojo_90.png)
   
    - **Resultados:**


