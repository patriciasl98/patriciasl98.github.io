---
tags:
  - Concept
Sumary: Intro al concepto de comunicaciones cuanticas
---


Las comunicaciones cuánticas se basan en fenómenos de la física cuántica, como el entrelazamiento y la superposición, para transmitir y procesar información de manera más segura y eficiente que las comunicaciones clásicas.
Algunos de los conceptos clave de esta tecnología son:

1. **Criptografía cuántica:** La distribución cuántica de claves (**QKD**) es el método más conocido en criptografía cuántica. La QKD utiliza las propiedades cuánticas de las partículas, como los fotones, para transmitir claves de cifrado de forma segura entre dos partes. **Si un tercero intenta interceptar la clave, las leyes de la física cuántica aseguran que la clave se altere**, alertando a las partes involucradas sobre la intrusión. El protocolo de QKD más famoso es el protocolo [[BB84]] , **que utiliza fotones polarizados para compartir la clave secreta.**

El protocolo BB84 es un método de criptografía cuántica propuesto por Charles Bennett y Gilles Brassard en 1984 para el intercambio seguro de claves criptográficas entre dos partes. Aquí hay una explicación simplificada del protocolo:

1. La primera parte, llamada Alice, crea una secuencia de bits aleatorios (0s y 1s) que desea enviar a la segunda parte, llamada Bob.

2. Alice codifica cada bit en un fotón (partícula de luz) usando dos bases diferentes, llamadas base rectilínea (+) y base diagonal (x). Por ejemplo, Alice puede codificar un 0 en la base rectilínea como un fotón polarizado horizontalmente y un 1 en la base rectilínea como un fotón polarizado verticalmente. De manera similar, puede codificar un 0 en la base diagonal como un fotón polarizado a 45 grados y un 1 en la base diagonal como un fotón polarizado a 135 grados.

3. Alice envía los fotones codificados a Bob a través de un canal cuántico.

4. Bob mide cada fotón recibido utilizando una base elegida al azar (rectilínea o diagonal) y registra sus mediciones como una secuencia de bits.

5. Después de que todos los fotones han sido enviados y medidos, Alice y Bob se comunican a través de un canal clásico (público) para comparar las bases que utilizaron. Bob le dice a Alice qué base utilizó para medir cada fotón, pero no comparte sus mediciones.

6. Alice informa a Bob cuándo sus bases coinciden. Para los fotones en los que las bases coinciden, las mediciones de Bob deben coincidir con los bits originales de Alice. Estos bits comunes se convierten en la clave secreta compartida.

7. Alice y Bob pueden verificar si un espía (Eva) ha interceptado y medido los fotones durante la transmisión. Si Eva intenta copiar la información, la naturaleza cuántica de los fotones garantiza que perturbará su estado, lo que provocará errores en las mediciones de Bob. Si Alice y Bob encuentran un porcentaje aceptablemente bajo de errores, pueden confiar en que su clave secreta compartida no ha sido interceptada.

El protocolo BB84 utiliza los principios de la mecánica cuántica, como la superposición y el colapso de la función de onda, para garantizar la seguridad de la comunicación. La imposibilidad de copiar estados cuánticos sin perturbarlos (teorema de no clonación) dificulta que un atacante intercepte la clave sin ser detectado.

3. **Teleportación** cuántica: La teleportación cuántica es un proceso que permite transferir el estado cuántico de una partícula a otra partícula distante sin que las partículas se desplacen físicamente. Se basa en el entrelazamiento cuántico, un fenómeno en el cual dos partículas están correlacionadas de tal manera que el estado de una partícula está inmediatamente relacionado con el estado de la otra, independientemente de la distancia entre ellas. La teleportación cuántica podría permitir la transmisión de información a larga distancia sin pérdida de calidad y con una seguridad mejorada en comparación con las comunicaciones clásicas.

4. **Computación cuántica**: La computación cuántica utiliza **qubits en lugar de bits clásicos.** Un qubit puede representar múltiples estados simultáneamente debido a la superposición cuántica, lo que permite a las computadoras cuánticas realizar cálculos de manera más eficiente que las computadoras clásicas. Algunos problemas, como la factorización de números grandes y la búsqueda en bases de datos no estructuradas, podrían resolverse mucho más rápidamente en una computadora cuántica. Sin embargo, las computadoras cuánticas aún se encuentran en etapas tempranas de desarrollo y enfrentan desafíos en términos de escalabilidad y corrección de errores.

5. **Comunicación cuántica a larga distancia**: Se están desarrollando tecnologías para permitir la comunicación cuántica a larga distancia, como **redes de satélites cuánticos y repetidores cuánticos**. Los satélites cuánticos pueden transmitir fotones entrelazados a largas distancias, lo que podría permitir comunicaciones cuánticas seguras y rápidas a escala global. Los repetidores cuánticos, por otro lado, pueden extender el alcance de las comunicaciones cuánticas al almacenar y retransmitir estados cuánticos, superando las limitaciones de distancia asociadas con la atenuación de la señal en las comunicaciones ópticas.Los repetidores cuánticos son dispositivos que permiten extender el alcance de las comunicaciones cuánticas, como las basadas en la distribución cuántica de claves (QKD), al almacenar y retransmitir estados cuánticos. En términos simples, actúan como "amplificadores" de la señal cuántica, pero con un enfoque diferente al de los amplificadores clásicos.

En las comunicaciones ópticas, como las comunicaciones por fibra óptica, la señal se debilita a medida que viaja a través del cable debido a la atenuación. Para superar esto en las comunicaciones clásicas, se utilizan amplificadores ópticos que aumentan la intensidad de la señal. Sin embargo, en las comunicaciones cuánticas, no se puede simplemente amplificar la señal cuántica debido al principio de incertidumbre cuántica y al teorema de no clonación, que prohíbe copiar estados cuánticos exactos.

Aquí es donde entran en juego los repetidores cuánticos. En lugar de amplificar directamente la señal cuántica, estos dispositivos capturan el estado cuántico de una partícula (por ejemplo, un fotón) y luego lo transfieren a otra partícula a través del proceso de teleportación cuántica, que se basa en el entrelazamiento cuántico. Al hacer esto, el repetidor cuántico puede retransmitir el estado cuántico sin violar las leyes de la física cuántica.

De esta manera, los repetidores cuánticos pueden extender efectivamente el alcance de las comunicaciones cuánticas, superando las limitaciones de distancia asociadas con la atenuación de la señal en las comunicaciones ópticas y permitiendo la transmisión de información cuántica segura a largas distancias.


>[!Info] El teorema de no clonación es un principio fundamental de la física cuántica que establece que no es posible crear una copia exacta e independiente de un estado cuántico arbitrario. En otras palabras, no podemos clonar perfectamente una partícula cuántica, como un fotón o un electrón, sin alterar el estado original. 
>Este teorema se deriva de las propiedades básicas de la mecánica cuántica y tiene importantes implicaciones en las comunicaciones cuánticas y la criptografía cuántica. Para entenderlo mejor, consideremos el siguiente ejemplo: 
>Supongamos que tenemos un fotón en un estado cuántico desconocido, y queremos crear una copia exacta de ese fotón. Según el teorema de no clonación, no podemos hacerlo sin afectar el estado original del fotón. La razón de esto es que medir el estado cuántico de una partícula implica alterar ese estado, debido al principio de incertidumbre cuántica. 
>Entonces, si intentamos medir el estado cuántico del fotón original para crear una copia, estaríamos cambiando el estado del fotón original en el proceso. Esto significa que no podríamos crear una copia perfecta e independiente del fotón original sin afectar su estado cuántico.
>El teorema de no clonación es crucial para la seguridad en criptografía cuántica, como en el caso de la distribución cuántica de claves (QKD). Si un atacante intenta interceptar y copiar una clave cuántica, el teorema de no clonación garantiza que el intento de clonación alterará el estado cuántico de la clave, alertando a las partes involucradas sobre la intrusión y protegiendo la información transmitida.



