---
dg-publish: true
dg-home: true
tags:
  - Concept
Sumary: Q&A respuestas
---
>[!SUMMARY] Table of Contents
>- [[Preguntas , respuestas y conceptos clave#¿Por qué e^(iθ) = cos(θ) + i*sin(θ) ?|¿Por qué e^(iθ) = cos(θ) + i*sin(θ) ?]]
>- [[Preguntas , respuestas y conceptos clave#Hilbert Space|Hilbert Space]]
>- [[Preguntas , respuestas y conceptos clave#Observables|Observables]]
>- [[Preguntas , respuestas y conceptos clave#Transpillation |Transpillation ]]
>    - [[Preguntas , respuestas y conceptos clave#pass_manager|pass_manager]]
>- [[Preguntas , respuestas y conceptos clave#Matrices |Matrices ]]
>    - [[Preguntas , respuestas y conceptos clave#Matriz Hermítica ?|Matriz Hermítica ?]]
>    - [[Preguntas , respuestas y conceptos clave#Matrices unitarias|Matrices unitarias]]
>- [[Preguntas , respuestas y conceptos clave#Time evolution |Time evolution ]]
>            - [[Preguntas , respuestas y conceptos clave#Hamiltoniano|Hamiltoniano]]
>- [[Preguntas , respuestas y conceptos clave#Valor esperado |Valor esperado ]]
>    - [[Preguntas , respuestas y conceptos clave#Global phase ??|Global phase ??]]
>- [[Preguntas , respuestas y conceptos clave#Cálculos y operaciones |Cálculos y operaciones ]]
>- [[Preguntas , respuestas y conceptos clave#Superdense Coding|Superdense Coding]]
>- [[Preguntas , respuestas y conceptos clave#Quantum teleportation|Quantum teleportation]]
>- [[Preguntas , respuestas y conceptos clave#Entrelazamiento|Entrelazamiento]]
>    - [[Preguntas , respuestas y conceptos clave#Es posible crear entrelazamiento si los qubits no han compartido espacio físico ?|Es posible crear entrelazamiento si los qubits no han compartido espacio físico ?]]
>- [[Preguntas , respuestas y conceptos clave#Operators |Operators ]]
>    - [[Preguntas , respuestas y conceptos clave#Reflection operators|Reflection operators]]
>    - [[Preguntas , respuestas y conceptos clave#Rotation operators|Rotation operators]]
>- [[Preguntas , respuestas y conceptos clave#Cómo se usa la interferencia la computación cuántica para llegar a resultados ?|Cómo se usa la interferencia la computación cuántica para llegar a resultados ?]]
>- [[Preguntas , respuestas y conceptos clave#Phase kickback|Phase kickback]]
>- [[Preguntas , respuestas y conceptos clave#Grovers Algorithm |Grovers Algorithm ]]



```dataview
TABLE Date, Title, Entity
FROM "Courses" and !"Courses/Content"
SORT file.name DESC
```

# ¿Por qué e^(iθ) = cos(θ) + i*sin(θ) ?

La relación e^(iθ) = cos(θ) + i*sin(θ) es conocida como la fórmula de Euler, que relaciona las funciones exponenciales complejas con las funciones trigonométricas seno y coseno. Esta fórmula se deriva a partir de la expansión en serie de Taylor de las funciones exponencial, seno y coseno.

La serie de Taylor es una representación de una función como una suma infinita de términos que se calculan a partir de las derivadas de la función en un punto dado. Las expansiones en serie de Taylor para e^x, sen(x) y cos(x) son:

e^x = 1 + x + x^2/2! + x^3/3! + x^4/4! + ...

sen(x) = x - x^3/3! + x^5/5! - x^7/7! + ...

cos(x) = 1 - x^2/2! + x^4/4! - x^6/6! + ...

Cuando sustituimos x con ix (donde i es la unidad imaginaria) en la serie de Taylor para e^x, obtenemos:

e^(ix) = 1 + ix - x^2/2! - ix^3/3! + x^4/4! + ...

Ahora, separamos los términos reales e imaginarios:

e^(ix) = (1 - x^2/2! + x^4/4! - ...) + i(x - x^3/3! + x^5/5! - ...)

Comparando los términos entre paréntesis con las expansiones en serie de Taylor de cos(x) y sen(x), vemos que:

e^(ix) = cos(x) + i*sen(x)

Por lo tanto, al reemplazar x con θ, obtenemos la fórmula de Euler:

e^(iθ) = cos(θ) + i*sin(θ)

Esta fórmula es fundamental en matemáticas y física, ya que permite expresar relaciones y propiedades de funciones trigonométricas y exponenciales en términos de números complejos de manera más simple y elegante.

# Oracle 
In computer science, an oracle is an abstract concept that represents a black box that can solve a particular problem in a single operation. However, the internal workings of the oracle are unknown or inaccessible.

¡Claro! Aquí está la traducción:

¿Qué gran pregunta?

En computación clásica, un oráculo es una caja negra que proporciona una salida específica para una entrada dada, sin revelar cómo se calculó la salida. En otras palabras, un oráculo es una función que toma una entrada y devuelve una salida, pero su funcionamiento interno es desconocido.

En computación cuántica, un oráculo es el análogo cuántico de este concepto. Es una operación cuántica que toma un estado cuántico como entrada y devuelve un estado cuántico como salida, sin revelar el funcionamiento interno de la operación.

Más formalmente, un oráculo cuántico es un operador unitario U que actúa sobre un sistema cuántico, típicamente denotado como |x, y devuelve un nuevo estado cuántico U|x. La característica clave de un oráculo cuántico es que no proporciona ninguna información sobre cómo se calculó la salida, al igual que un oráculo clásico.

Los oráculos cuánticos se utilizan a menudo en algoritmos cuánticos para resolver problemas que son difíciles o imposibles de resolver de manera eficiente en una computadora clásica. Por ejemplo, en el algoritmo de Shor para factorizar números grandes, se utiliza un oráculo cuántico para realizar una exponentiación modular, que es un paso crítico en el algoritmo.

Un aspecto importante de los oráculos cuánticos es que pueden ser consultados en una superposición de estados, lo que significa que la entrada puede ser una combinación lineal de diferentes estados. Esto permite que el oráculo sea consultado multiple veces simultáneamente, lo que puede llevar a una aceleración exponencial sobre algoritmos clásicos en ciertos casos.

Hay diferentes tipos de oráculos cuánticos, incluyendo:

1. **Oráculo de fase**: Este oráculo aplica un desplazamiento de fase al estado de entrada, dependiendo del valor de la entrada.
2. **Oráculo de bit**: Este oráculo invierte un bit del estado de entrada, dependiendo del valor de la entrada.
3. **Arbitrario**: Este oráculo puede aplicar cualquier operación unitaria al estado de entrada.

Los oráculos cuánticos tienen muchas aplicaciones en computación cuántica, incluyendo:

1. **Criptografía**: Los oráculos cuánticos se pueden utilizar para romper ciertos sistemas criptográficos clásicos, como RSA.
2. **Optimización**: Los oráculos cuánticos se pueden utilizar para resolver problemas de optimización, como el problema del viajante.
3. **Aprendizaje automático**: Los oráculos cuánticos se pueden utilizar para acelerar ciertos algoritmos de aprendizaje automático, como el clustering k-medias.


# Hilbert Space

El espacio de Hilbert es el marco matemático que utilizamos para describir y analizar sistemas cuánticos, como qubits y sus interacciones. En computación cuántica, los estados cuánticos de **los qubits se representan como vectores en el espacio de Hilbert**. Este espacio es un tipo especial de espacio vectorial que tiene propiedades y estructuras específicas que facilitan la descripción de sistemas cuánticos.

**La dimensión del espacio de Hilbert depende del número de qubits en el sistema.** Para un solo qubit, el espacio de Hilbert es un espacio vectorial complejo de dos dimensiones. En este espacio bidimensional, cada estado cuántico se puede representar como una combinación lineal de dos estados base, que generalmente se denotan como |0⟩ y |1⟩. **Cuando trabajamos con múltiples qubits, la dimensión del espacio de Hilbert aumenta exponencialmente (2^n,** donde n es el número de qubits), lo que permite representar y analizar sistemas cuánticos más complejos.

Algunas propiedades y conceptos importantes relacionados con el espacio de Hilbert en la computación cuántica incluyen:

1. **Normalización**: Los estados cuánticos en el espacio de Hilbert están normalizados, es decir, tienen una **longitud (norma) igual a 1**. Esto asegura que la suma de las probabilidades de medir un qubit en todos sus posibles estados sea igual a 1.

2. Producto interno: El espacio de Hilbert está **equipado con un producto interno que permite calcular ángulos y distancias entre estados cuánticos**. Esto es útil para analizar la relación entre diferentes estados y entender cómo evolucionan en el tiempo o cómo se ven afectados por operaciones cuánticas.

3. Operadores lineales: En el espacio de Hilbert, las **transformaciones que actúan sobre los estados cuánticos, como las puertas cuánticas, se representan mediante operadores lineales**. Estos operadores lineales nos permiten describir cómo cambian los estados cuánticos cuando aplicamos operaciones cuánticas.

4. Evolución temporal: La evolución temporal de los estados cuánticos en el espacio de Hilbert se describe mediante ecuaciones matemáticas, como la ecuación de Schrödinger. Estas ecuaciones nos permiten predecir y entender cómo cambian los estados cuánticos a lo largo del tiempo y cómo interactúan con otros sistemas cuánticos.


![[Math Toolkit II#The Qubit as a Hilbert Space]]

# Observables
En mecánica cuántica, un observable es una magnitud física que se puede medir en un sistema cuántico. Ejemplos de observables comunes incluyen la energía, el momento angular, la posición, el momento lineal, etc.

En el contexto de la computación cuántica, un observable se representa como una matriz hermítica (también conocida como una matriz de operador lineal) que actúa en el espacio de estados cuánticos. Esta matriz se llama operador de observable.

# Transpillation 

>[!Note]
>Para saber mas sobre esto recomiendo ir al notebook del lab2 del IBM Quantum Challenge [[📚 IBM Quantum challenge 2024]] and https://docs.quantum.ibm.com/transpile

En el contexto de la computación cuántica, **transpilación** es el proceso de **transformar un circuito cuántico en una forma optimizada que pueda ser ejecutada en un backend de destino, como una computadora cuántica o un simulador.**

La transpilación implica aplicar una serie de **transformaciones al circuito original, con el objetivo de mejorar su rendimiento, reducir errores y adaptarlo a la arquitectura y restricciones específicas del backend de destino.**

El proceso de transpilación típicamente involucra varios pasos, incluyendo:

1. **Análisis**: Descomponer el circuito original en sus operaciones y puertas constituyentes.
2. **Optimización**: Aplicar diversas técnicas de optimización, como cancelación de puertas, fusión de puertas y reordenamiento de puertas, para reducir el número de puertas y mejorar el rendimiento del circuito.
3. **Simplificación**: Eliminar puertas innecesarias y simplificar la estructura del circuito para reducir su complejidad.
4. **Asignación**: Adaptar el circuito a la arquitectura y restricciones específicas del backend de destino, como el número de qubits, conjuntos de puertas y conectividad.
5. **Mitigación de errores**: Aplicar técnicas para reducir el impacto de errores en la ejecución del circuito, como códigos de corrección de errores o puertas resistentes al ruido.

El proceso de transpilación es crucial en la computación cuántica, ya que permite la ejecución de algoritmos cuánticos en una amplia variedad de backends, desde simuladores de pequeña escala hasta computadoras cuánticas de gran escala.

## pass_manager

En el contexto de la computación cuántica y Qiskit, un **gestor de pasos** (pass_manager) es un **objeto** que gestiona una secuencia de pasos, que son **transformaciones aplicadas a un circuito cuántico para optimizar su ejecución en un backend de destino**.

Un **paso** es una transformación individual que modifica un circuito cuántico de alguna manera, como:

* **Optimización de secuencias de puertas**: Reordenar puertas para reducir el número de puertas o mejorar el rendimiento del circuito.
* **Simplificación de circuitos**: Eliminar puertas innecesarias o reducir la complejidad del circuito.
* **Asignación a un backend específico**: Adaptar el circuito a la arquitectura y restricciones específicas del backend de destino.
* **Mitigación de errores**: Aplicar técnicas para reducir el impacto de errores en la ejecución del circuito.


```python 
from qiskit_ibm_runtime import QiskitRuntimeService
from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager

backend_name = "ibm_brisbane"
backend = QiskitRuntimeService().backend(backend_name)
pass_manager = generate_preset_pass_manager(optimization_level=1, backend=backend)

qc_transpiled = pass_manager.run(qc)# transpiling the circuit
#Trnaspilling the operaotrs
#Transpile the list of operators (`operators`) to match the layout of the transpiled circuit (`qc_transpiled`).
operators_transpiled_list = [op.apply_layout(qc_transpiled.layout) for op in operators]
#The `apply_layout` method takes a layout as an input and applies it to the operator. This means that the operator's internal structure is modified to match the layout of the transpiled circuit.
```

# Matrices 

## Matriz Hermítica ?

Una matriz hermítica, también conocida como matriz hermitiana, es una matriz cuadrada (es decir, tiene el mismo número de filas y columnas) cuyos elementos son números complejos. La propiedad clave de una matriz hermítica es **que su matriz adjunta (o matriz conjugada traspuesta) es igual a la matriz original.**

La matriz adjunta se obtiene al tomar la **matriz traspuesta** (intercambiando filas por columnas) y, al mismo tiempo , **tomando el conjugado complejo de cada elemento**. El conjugado complejo de un número complejo es el número que se obtiene al cambiar el signo de su parte imaginaria.

En términos matemáticos, una matriz A es hermítica si A = A*, donde A* denota la matriz adjunta de A.

Por ejemplo, considere la siguiente matriz A:

A = | 1 + 0i  2 + 3i |
    | 2 - 3i  4 + 0i |

La matriz adjunta A* es:

A* = | 1 - 0i  2 - 3i |
     | 2 + 3i  4 - 0i |

Como A = A*, entonces A es una matriz hermítica.

Las matrices hermíticas son importantes en diversas áreas de la matemática y la física, especialmente en la mecánica cuántica, donde representan observables y operadores lineales autoadjuntos. Las matrices hermíticas Una matriz hermítica, también conocida como matriz hermitiana, es una matriz cuadrada (es decir, tiene el mismo número de filas y columnas) cuyos elementos son números complejos. La propiedad clave de una matriz hermítica es que su matriz adjunta (o matriz conjugada traspuesta) es igual a la matriz original.

La matriz adjunta se obtiene al tomar la matriz traspuesta (intercambiando filas por columnas) y, al mismo tiempo, tomando el conjugado complejo de cada elemento. El conjugado complejo de un número complejo es el número que se obtiene al cambiar el signo de su parte imaginaria.

En términos matemáticos, una matriz A es hermítica si A = A*, donde A* denota la matriz adjunta de A.

Por ejemplo, considere la siguiente matriz A:

A = | 1 + 0i  2 + 3i |
    | 2 - 3i  4 + 0i |

La matriz adjunta A* es:

A* = | 1 - 0i  2 - 3i |
     | 2 + 3i  4 - 0i |

Como A = A*, entonces A es una matriz hermítica.

Las matrices hermíticas son importantes en diversas áreas de la matemática y la física, especialmente en la mecánica cuántica, donde representan observables y operadores lineales autoadjuntos. Las matrices hermíticas tienen la propiedad de que sus **autovalores siempre son números reales y sus autovectores correspondientes a autovalores diferentes son ortogonales entre sí.**

>[!Note] **Que implicaciones tiene que los autovaloes sean reales y los autovectores ortogonales?**
>1. se puede encontrar una base de autovectores ortogonales que permite transformar la matriz hermítica en una matriz diagonal. La matriz diagonal resultante tiene los autovalores en la diagonal principal. Esta diagonalización simplifica el análisis y la solución de problemas que involucran matrices hermíticas.
>2. 



## Matrices unitarias

Las matrices unitarias son un tipo especial de matrices **cuadradas** (es decir, con el mismo número de filas y columnas) **cuyos elementos pueden ser números complejos**. La característica principal de una matriz unitaria es que su **matriz inversa es igual a su matriz conjugada traspuesta** (también llamada matriz adjunta).
**Los autovalores de estas matricesson complejo de módulo 1.** -> e^(iθ) 

En términos matemáticos, una matriz U es unitaria si U * U^* = I, donde U^* denota la matriz conjugada traspuesta de U e I es la matriz identidad del mismo tamaño que U. La matriz identidad es una matriz cuadrada en la que todos los elementos de la diagonal principal son 1 y el resto de los elementos son 0.

Las matrices unitarias tienen varias propiedades importantes:

1. Conservación de la norma: **Cuando se multiplica un vector por una matriz unitaria, la norma (o longitud) del vector se conserva**. Esto significa que las matrices unitarias **representan transformaciones que preservan la geometría y las distancias en el espacio en el que actúan**.

2. Ortonormalidad de las columnas y filas: **Las columnas (y filas) de una matriz unitaria son vectores ortonormales**. Esto significa que cada par de columnas (o filas) distintas es ortogonal, y cada columna (o fila) tiene norma 1. Esta propiedad es **útil para describir bases ortonormales y transformaciones que mantienen la estructura geométrica del espacio.**

3. Decomposición espectral: Las matrices unitarias desempeñan un papel importante en la diagonalización de matrices hermíticas y en la descomposición espectral. La descomposición espectral permite expresar una matriz hermítica como el producto de una matriz unitaria, una matriz diagonal con autovalores en la diagonal principal y la matriz unitaria conjugada traspuesta.
	 Esta técnica consiste en reescribir la **matriz hermítica como el resultado de multiplicar tres matrices**: una matriz **unitaria** (que conserva las distancias y tiene propiedades útiles), una matriz **diagonal** (con los autovalores en la diagonal principal y ceros en todas las demás posiciones) y la matriz **unitaria conjugada traspuesta** (que es la matriz unitaria original, pero con sus elementos conjugados y traspuestos). Al reescribir la matriz original en términos de matrices más simples, podemos resolver problemas y **realizar cálculos de manera más eficiente y clara.**

Las matrices unitarias tienen aplicaciones en diversas áreas de la matemática y la física, como la mecánica cuántica, el álgebra lineal, el análisis funcional, el procesamiento de señales y la teoría de la información. En la mecánica cuántica, por ejemplo, las matrices unitarias se utilizan para describir transformaciones y evoluciones temporales que conservan la probabilidad total y las propiedades geométricas de los estados cuánticos.

# Time evolution 
Continuous time evolution of a state of a closed quantum system is described by the **Schrödinger equation**:
$$i\hbar\frac{d\ket{\psi}}{dt}=H\ket{\psi}$$
where $\hbar$ is a physical constant known as _Planck's constant_, and $H$ is a [Hermitian operator](https://en.wikipedia.org/wiki/Hermitian_adjoint) known as the **Hamiltonian** of the system.
**The Hamiltonian is an operator representing the system's total energy function**. Generally, It may be a function of time, but for convenience, let us consider constant Hamiltonians. In this case, the solution to the Schrödinger equation for fixed times $t_1$ and $t_2$ is
$$\ket{\psi(t_2)}=e^{-i \, H(t_2-t_1) \, / \, \hbar}\ket{\psi(t_1)}$$
Por lo tanto: 
U = e^(-i * H * t / ℏ)

**Explicación en Español**
#### Hamiltoniano
Hamiltoniano (H) es un operador hermitiano,para entender esto, primero debemos entender qué es un operador y qué significa hermitiano.

Un operador es una función matemática que actúa sobre un objeto, como un vector o una función, y produce otro objeto del mismo tipo. En mecánica cuántica, los operadores actúan sobre estados cuánticos (representados por vectores en un espacio de Hilbert) y tienen propiedades específicas que los hacen adecuados para describir fenómenos cuánticos.

Un operador hermitiano (o autoadjunto) es un tipo especial de operador que satisface una propiedad particular en relación con su adjunta, que es la transposición conjugada del operador. Un operador hermitiano se denota como A, y su adjunta se denota como A†. Un operador A es hermitiano si cumple la siguiente condición:

**A = A†**

Esto significa que el **operador es igual a su adjunta**. En términos prácticos, **esto implica que los elementos de la diagonal principal de la matriz del operador son reales, y los elementos fuera de la diagonal principal son complejos conjugados simétricos.**

Entonces, cuando decimos que el Hamiltoniano (H) es un operador hermitiano, esto significa que H es un operador que actúa sobre estados cuánticos y satisface la propiedad de ser igual a su adjunta (H = H†). Esta propiedad es importante en mecánica cuántica porque asegura que los **valores propios (o autovalores) del Hamiltoniano sean reales, lo que es necesario para que la energía del sistema cuántico sea una cantidad real**. Además, los operadores hermitianos **tienen conjuntos completos de funciones propias ortogonales, lo que es útil para describir y resolver problemas cuánticos.**
Estos Hamiltonianos nos ayudan a entender cómo evoluciona el sistema cuántico en el tiempo a medida que se aplican las compuertas.

**¿Y para que nos interesa todo esto?**

La relación entre las operaciones unitarias y los Hamiltonianos es útil para diseñar y analizar algoritmos cuánticos, y para comprender cómo las compuertas cuánticas afectan la evolución temporal de los qubits.

Una aplicación práctica en la que esta relación es importante es la simulación de sistemas cuánticos en computadoras cuánticas. Un ejemplo específico es la simulación de moléculas y sus propiedades químicas utilizando algoritmos cuánticos, como el algoritmo de Trotter-Suzuki.

En este tipo de simulación, queremos modelar cómo evoluciona un sistema cuántico, como una molécula, bajo la influencia de su Hamiltoniano molecular. La evolución temporal del sistema molecular se puede describir mediante la ecuación de Schrödinger, y las compuertas cuánticas aplicadas en el algoritmo cuántico corresponden a las operaciones unitarias que describen la evolución del sistema en pasos de tiempo discretos.

El algoritmo de Trotter-Suzuki es un método para aproximar la evolución del sistema dividiendo el Hamiltoniano molecular en componentes más simples, cada uno de los cuales se puede simular utilizando compuertas cuánticas. La relación entre las operaciones unitarias y los Hamiltonianos es esencial para implementar este algoritmo, ya que nos permite traducir la evolución temporal del sistema molecular en una secuencia de compuertas cuánticas que se aplican a los qubits en la computadora cuántica.

Estas simulaciones cuánticas de moléculas y sus propiedades pueden tener aplicaciones prácticas en áreas como el diseño de nuevos materiales, la optimización de reacciones químicas y el desarrollo de medicamentos.

Básicamnte, mediante el uso de compuertas cuánticas, simulamos la evolución temporal del sistema cuántico, que está determinada por el Hamiltoniano.

El Hamiltoniano es un operador que describe la energía total de un sistema cuántico y cómo interactúan sus componentes. En el contexto de la simulación de sistemas cuánticos, como moléculas, el Hamiltoniano se deriva de las propiedades físicas y químicas del sistema que se está simulando.

En general, el Hamiltoniano se obtiene a partir de la teoría física y química subyacente. Por ejemplo, en el caso de una molécula, el Hamiltoniano puede incluir términos que representen la energía cinética de los electrones, la energía potencial de las interacciones entre los electrones y los núcleos atómicos, y las interacciones entre los electrones en sí. Estos términos se basan en las leyes de la mecánica cuántica y la teoría de campos electromagnéticos.

Una vez que se tiene el Hamiltoniano (ya sea exacto o aproximado), se puede utilizar el algoritmo de Trotter-Suzuki para dividirlo en componentes más simples que se pueden simular utilizando compuertas cuánticas. Luego, al aplicar estas compuertas cuánticas en una computadora cuántica, se puede simular la evolución temporal del sistema cuántico y, en última instancia, obtener información sobre las propiedades físicas y químicas del sistema que se está simulando.


---
# Valor esperado 

El valor esperado, también conocido como expectación, es un concepto estadístico que representa el valor promedio o central de una distribución de probabilidad. **En el contexto de álgebra lineal y mecánica cuántica, el valor esperado de un observable** (una propiedad física que se puede medir) **se puede calcular como la multiplicación de un vector por una matriz** (que representa el **operador del observable**) y luego por otro **vector**.

Supongamos que tenemos un estado cuántico representado por un vector columna ψ y un **observable representado por una matriz A**. El valor esperado del observable A en el estado ψ se denota como ⟨ψ|A|ψ⟩ y se calcula de la siguiente manera:

1. Tomar el vector conjugado traspuesto (también llamado "bra") del vector ψ. Esto significa que cambiamos el vector columna a un vector fila y tomamos el conjugado complejo de cada elemento. Denotamos este vector como ⟨ψ|.

2. Multiplicar el vector ⟨ψ| por la matriz A. Esto nos da un vector fila.

3. Multiplicar el vector fila resultante por el vector columna original ψ. Esto nos da un escalar (un número), que es el valor esperado del observable A en el estado ψ.

Matemáticamente, esto se puede escribir como:

**⟨ψ|A|ψ⟩ = ⟨ψ| * A * |ψ⟩**

El valor esperado nos proporciona información sobre el **resultado promedio de una medición del observable A en el estado ψ**. En la mecánica cuántica, este concepto se utiliza para describir el comportamiento de partículas y sistemas cuánticos, y tiene aplicaciones en áreas como la espectroscopia, la teoría de la información cuántica y la computación cuántica.
Sin embargo, en la **mecánica cuántica, cuando se trabaja con observables representados por matrices hermíticas, el valor esperado siempre será un número real**. Esto se debe a las propiedades especiales de las matrices hermíticas y su relación con los estados cuánticos.

## Global phase ??
Imagina que tienes una moneda que puede estar en dos estados: cara y cruz. En la computación cuántica, esta moneda puede estar en una "superposición" de ambos estados al mismo tiempo. La "superposición" es una combinación de los dos estados básicos (cara y cruz) con ciertos pesos, llamados amplitudes. Cada estado básico en la superposición tiene una amplitud compleja asociada. La amplitud es un número complejo que tiene una magnitud y una fase. La magnitud nos da información sobre la probabilidad de encontrar la moneda en ese estado básico, mientras que la fase proporciona información adicional sobre cómo se comporta el sistema cuántico.
Lo interesante es que, aunque las amplitudes A y B cambian, las probabilidades de encontrar la moneda en cara o cruz (que son el cuadrado de las magnitudes de las amplitudes) no cambian. Es decir, la fase global no afecta los resultados de las mediciones que realizamos en el sistema cuántico. Por lo tanto, dos sistemas cuánticos que difieren solo en una fase global se consideran físicamente equivalentes. 
**Ejemplo:**
Claro, aquí tienes un ejemplo concreto utilizando un qubit, que es la unidad básica de información cuántica.

Supongamos que tenemos un qubit en una superposición de sus dos estados básicos, |0⟩ y |1⟩. El estado cuántico del qubit se puede representar como:

|ψ⟩ = α |0⟩ + β |1⟩

Donde α y β son amplitudes complejas y cumplen con la condición |α|^2 + |β|^2 = 1 (esto asegura que la probabilidad total sea 1).

Imagina que α = 1/√2 y β = 1/√2, lo que significa que nuestro qubit está en una superposición igual de los estados |0⟩ y |1⟩. Entonces, nuestro estado cuántico es:

|ψ⟩ = (1/√2) |0⟩ + (1/√2) |1⟩

Ahora, vamos a aplicar una fase global de θ = π (pi). El factor de fase correspondiente es e^(iπ) = -1. Multiplicamos todas las amplitudes por este factor:

|ψ'⟩ = (-1) * (1/√2) |0⟩ + (-1) * (1/√2) |1⟩
|ψ'⟩ = (-1/√2) |0⟩ + (-1/√2) |1⟩

Entonces, nuestro nuevo estado cuántico |ψ'⟩ tiene amplitudes que han sido afectadas por la fase global. Sin embargo, las probabilidades de medir |0⟩ y |1⟩ no han cambiado:

Probabilidad de medir |0⟩ en |ψ⟩ = |α|^2 = (1/√2)^2 = 1/2
Probabilidad de medir |1⟩ en |ψ⟩ = |β|^2 = (1/√2)^2 = 1/2

Probabilidad de medir |0⟩ en |ψ'⟩ = |(-1/√2)|^2 = (1/√2)^2 = 1/2
Probabilidad de medir |1⟩ en |ψ'⟩ = |(-1/√2)|^2 = (1/√2)^2 = 1/2

Como puedes ver, a pesar de aplicar una fase global, las probabilidades de medir los estados |0⟩ y |1⟩ no han cambiado, lo que demuestra que la fase global no tiene un impacto observable en las mediciones. Por lo tanto, los estados |ψ⟩ y |ψ'⟩ se consideran físicamente equivalentes.

# Cálculos y operaciones 
![[Pasted image 20240506170210.png]]


# Superdense Coding

![[Day 4#Superdense Coding]]


# Quantum teleportation

![[Day 4#Quantum Teleportation]]

# Entrelazamiento
IMPORTNATE : Para crear entrelazamiento necesitamos operaciones sobre dos qubits que no se puedan representar como productos tensoriales.
La operación CNOT es la que se encarga de crear este entrelazamiento.
![[Pasted image 20240506170951.png]]

## Es posible crear entrelazamiento si los qubits no han compartido espacio físico ?

Sí, es posible crear entrelazamiento entre partículas que no han compartido el mismo espacio físico utilizando protocolos cuánticos específicos, como el llamado "entrelazamiento cuántico mediado por la interacción de terceras partículas". Este proceso no es el mismo que la teleportación cuántica, pero está relacionado.

El proceso generalmente involucra una tercera partícula (o un conjunto de partículas) que interactúa con ambas partículas que queremos entrelazar. Estas interacciones permiten que se establezca el entrelazamiento entre las dos partículas objetivo, incluso si nunca han compartido el mismo espacio físico.

Un ejemplo de esto es el proceso llamado "entrelazamiento cuántico de interacción de fotones". En este proceso, se emiten fotones desde átomos separados y, luego, estos fotones interactúan en un dispositivo óptico, como un divisor de haz. A través de estas interacciones, los fotones se entrelazan. Cuando los fotones se entrelazan, los átomos que originalmente emitieron los fotones también se entrelazan, aunque nunca han compartido el mismo espacio físico.

Por lo tanto, el entrelazamiento cuántico entre partículas que no han compartido espacio físico es posible, aunque requiere protocolos específicos y no es lo mismo que la teleportación cuántica.

# Operators 

## Reflection operators
A reflection operator is a linear transformation that reflects, or flips, the state vectors across a specific axis or plane in the vector space. In quantum computing, reflection operators are used to manipulate qubit states and perform specific tasks.
**Reflection operators have the property that when applied twice, they return the original state.**
Mathematically, this can be represented as R^2 = I, where R is the reflection operator and I is the identity operator.

## Rotation operators

In quantum computing, rotation operators are a class of unitary gates that perform a continuous rotation of a qubit's state around a specific axis in the Bloch sphere. These operators allow for precise and controlled manipulation of qubit states. Rotation operators are parametrized by an angle, which determines the extent of rotation.

There are three main rotation operators, each corresponding to a rotation around one of the three primary axes (X, Y, and Z) of the Bloch sphere:

1. Rx(θ): Rotation around the X-axis by an angle θ. The matrix representation of the Rx gate is:

   Rx(θ) = [[cos(θ/2), -i*sin(θ/2)],
            [-i*sin(θ/2), cos(θ/2)]]

2. Ry(θ): Rotation around the Y-axis by an angle θ. The matrix representation of the Ry gate is:

   Ry(θ) = [[cos(θ/2), -sin(θ/2)],
            [sin(θ/2), cos(θ/2)]]

3. Rz(θ): Rotation around the Z-axis by an angle θ. The matrix representation of the Rz gate is:

   Rz(θ) = [[exp(-i*θ/2), 0],
            [0, exp(i*θ/2)]]

These operators provide a way to smoothly modify the state of qubits, enabling the implementation of various quantum algorithms and more precise control over quantum states. In practice, rotation operators can be combined and used in sequence to achieve complex state transformations and reach specific target states.

# Cómo se usa la interferencia la computación cuántica para llegar a resultados ?

La interferencia es un fenómeno que ocurre cuando dos o más ondas se combinan, ya sea en fase (constructiva) o fuera de fase (destructiva), produciendo un efecto resultante que es la suma de las amplitudes de las ondas individuales en cada punto. Este fenómeno es clave en la computación cuántica debido a la forma en que se manipulan los qubits.

Un ejemplo común para entender esto es el algoritmo de Grover, utilizado para buscar un elemento específico en una base de datos no ordenada. Imagina que tienes una lista de números desordenados y quieres encontrar un número específico lo más rápido posible. En una computadora clásica, tendrías que revisar cada elemento de la lista uno por uno hasta encontrar el número que buscas, lo que tomaría tiempo proporcional al tamaño de la lista.

Sin embargo, en una computadora cuántica, puedes usar la superposición y la interferencia para realizar esta búsqueda de manera más eficiente. En lugar de revisar cada elemento individualmente, puedes representar cada elemento de la lista como un estado cuántico y realizar operaciones que aprovechen la interferencia cuántica para aumentar la probabilidad de encontrar el elemento deseado.

Durante la ejecución del algoritmo de Grover, se aplican operaciones cuánticas que manipulan los qubits de tal manera que los estados correspondientes a los elementos que no son la solución se cancelan entre sí de manera destructiva, mientras que el estado correspondiente al elemento deseado experimenta interferencia constructiva, aumentando su amplitud. Esto significa que al medir los qubits al final del algoritmo, es mucho más probable que obtengamos el estado que representa la solución deseada.

# Phase kickback
El retroceso de fase es un fenómeno que ocurre en la computación cuántica, donde un cambio en la fase de un qubit se propaga a otro qubit entrelazado con él, incluso si la operación no se aplica directamente a ese segundo qubit. Este efecto es importante porque permite que la información se comparta o se transmita entre qubits a través de sus fases.

En resumen, el retroceso de fase es un efecto que permite que los qubits entrelazados compartan información a través de sus fases, lo que resulta en cambios en los estados de varios qubits aunque solo se aplique una operación a uno de ellos.

El retroceso de fase es útil en varios algoritmos y protocolos cuánticos, como el algoritmo de estimación de fase cuántica y el algoritmo de Grover. Por ejemplo, en el algoritmo de Grover, el retroceso de fase se utiliza para implementar el oráculo de manera que el signo del elemento marcado se invierta. Esto permite que el algoritmo de Grover amplifique la probabilidad de encontrar el elemento buscado en menos pasos que un algoritmo clásico equivalente.

**Ejemplo:**
Claro, aquí tienes un ejemplo específico utilizando la compuerta CNOT para ilustrar el fenómeno del retroceso de fase:

1. Supongamos que tenemos dos qubits, qubit A y qubit B. Inicialmente, ambos qubits están en el estado |0⟩.

2. Aplicamos una compuerta Hadamard (H) al qubit A. Esto crea una superposición igual de los estados |0⟩ y |1⟩:

   Qubit A: |+⟩ = 1/√2 (|0⟩ + |1⟩)
   
3. Ahora aplicamos una compuerta CNOT controlada por el qubit A y actuando sobre el qubit B. La compuerta CNOT hace lo siguiente: si el qubit A está en el estado |1⟩, cambia el estado del qubit B (de |0⟩ a |1⟩ o viceversa); si el qubit A está en el estado |0⟩, no hace nada al qubit B.

   Como el qubit A está en una superposición de |0⟩ y |1⟩, el resultado después de aplicar la compuerta CNOT es un estado entrelazado:

   |Φ⟩ = 1/√2 (|00⟩ + |11⟩)

4. A continuación, aplicamos una compuerta de fase Z al qubit B. La compuerta Z agrega una fase de π a la componente |1⟩ del qubit B, pero no afecta la componente |0⟩:

   |Ψ⟩ = 1/√2 (|00⟩ - |11⟩)

5. Finalmente, aplicamos otra compuerta CNOT controlada por el qubit A y actuando sobre el qubit B:

   |Ω⟩ = H(1/√2 (|0⟩ - |1⟩)) ⊗ |0⟩ = |-⟩ ⊗ |0⟩

Observa que después de aplicar las compuertas CNOT y Z, la fase de π agregada al qubit B se ha "transferido" al qubit A a través del retroceso de fase. Ahora, el qubit A está en el estado |-⟩ en lugar de |+⟩, mientras que el qubit B ha vuelto al estado |0⟩.

Este ejemplo muestra cómo el retroceso de fase permite que la información de fase se transfiera entre qubits entrelazados, incluso cuando la operación (en este caso, la compuerta Z) solo se aplica directamente a uno de los qubits.

**Video:**
https://www.youtube.com/watch?v=h9LSfUpzGmA&ab_channel=BlochSphere

# Grovers Algorithm 

![[Day 5 Quantum search - Grovers Algorithm#Grovers Algorithm]]

**¿Para que podría usuarse?**

Imagina que eres un experto en seguridad informática y tienes una base de datos que contiene un gran número de contraseñas posibles, pero no ordenadas. Tu objetivo es encontrar una contraseña específica que coincida con un hash dado (una función criptográfica que transforma la contraseña en un valor único y de tamaño fijo). En este caso, el algoritmo de Grover podría ayudarte a encontrar la contraseña correcta mucho más rápido que un enfoque clásico de fuerza bruta.

Aquí se explica cómo se podría utilizar el algoritmo de Grover en este caso:

1. Preparación: Codifica todas las contraseñas posibles en qubits y colócalos en una superposición cuántica de todos los estados posibles.

2. Marcar el elemento objetivo: Diseña una función de oráculo cuántico que marque la contraseña correcta. Esta función de oráculo debe verificar si el hash de una contraseña en un estado cuántico coincide con el hash proporcionado y cambiar el signo del estado si hay una coincidencia.

3. Amplificación de amplitudes: Aplica los operadores de difusión de Grover para aumentar la probabilidad de medir la contraseña correcta y disminuir la probabilidad de medir las contraseñas incorrectas.

4. Repetición: Repite los pasos 2 y 3 aproximadamente √N veces, donde N es el número total de contraseñas en la base de datos.

5. Medición: Mide el estado cuántico. La medición te dará la contraseña correcta con una alta probabilidad.

Usando el algoritmo de Grover, podrías encontrar la contraseña correcta en aproximadamente √N intentos en lugar de los N/2 intentos promedio que se necesitarían en una búsqueda clásica de fuerza bruta. Esto podría ser especialmente útil si la base de datos de contraseñas es muy grande, ya que el algoritmo de Grover ofrece una aceleración cuadrática en comparación con los métodos clásicos. Sin embargo, cabe recordar que el algoritmo de Grover requiere un ordenador cuántico para ejecutarse.

**Otro ejemplo**
La detección de anomalías es el proceso de identificar elementos que se desvían significativamente de la mayoría de los elementos en un conjunto de datos. Estos elementos anómalos pueden ser indicativos de situaciones inusuales, errores, fraudes o eventos de interés. En un conjunto de datos con una gran cantidad de elementos normales y unos pocos elementos anómalos, puede ser difícil y lento encontrar estos elementos anómalos utilizando métodos clásicos.

El algoritmo de Grover puede ser adaptado para abordar el problema de la detección de anomalías de manera eficiente. Aquí se describe cómo se puede utilizar el algoritmo de Grover en este caso:

1. Preparación: Codifica todos los elementos del conjunto de datos en qubits y colócalos en una superposición cuántica de todos los estados posibles.

2. Marcar el elemento objetivo: Diseña una función de oráculo cuántico que marque los elementos anómalos. Esta función de oráculo debe ser capaz de evaluar si un elemento en un estado cuántico es anómalo según ciertos criterios y cambiar el signo del estado si es anómalo.

3. Amplificación de amplitudes: Aplica los operadores de difusión de Grover para aumentar la probabilidad de medir los estados correspondientes a elementos anómalos y disminuir la probabilidad de medir los estados correspondientes a elementos normales.

4. Repetición: Repite los pasos 2 y 3 aproximadamente √N veces, donde N es el número total de elementos en el conjunto de datos.

5. Medición: Mide el estado cuántico. La medición te dará un elemento anómalo con alta probabilidad.

Al utilizar el algoritmo de Grover en la detección de anomalías, puedes identificar elementos anómalos en un conjunto de datos mucho más rápido que los métodos clásicos. Esto podría ser útil en aplicaciones como la detección de fraudes en transacciones financieras, el diagnóstico médico basado en resultados de pruebas anómalos o el monitoreo de sistemas en busca de comportamientos inusuales.

