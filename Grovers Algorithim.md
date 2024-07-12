---
tags:
  - Concept
Sumary: Explicación Algoritmo de Grover
---

# MOC
* [[Concepts MOC]]
# Related notes

```dataview
TABLE WITHOUT ID link(file.name) AS "Nota", file.cday AS "Created date" , Sumary
WHERE contains(file.outlinks, this.file.link)
OR contains(file.inlinks, this.file.link)
and !contains(file.name , "MOC")
AND file.name != this.file.name
```

# Resources 

* [Python notebook](https://github.com/Qiskit/textbook/blob/main/notebooks/ch-algorithms/grover.ipynb)
* [Explicación Teórica](https://github.com/Qiskit/textbook/blob/aebdd2bc86ddb7a79dd8441d52c839d312ffafbb/notebooks/intro/grover-intro.ipynb)

# Introducción y ejemplos del concepto
This quantum algorithm that allows for faster **searching of an unsorted list**. 

Suppose you are given an unsorted list of N elements. Among these elements there is one element with a unique property that we wish to locate. To do this, using **classical computation, one would have to check on average N/2 of these elements**, and in the **worst case, all N of them**. Using a quantum computer, however, we can find the **desired element in roughly √N step**s with Grover’s algorithm.
ne way this algorithm could be used is to brute-force the key of symmetric-key primitives (e.g., AES). This would mean that, for example, an AES-128 key could be brute-forced in 2^64 steps, which effectively halves the security of the algorithm. This can, however, still be mitigated by using hash functions with larger outputs (i.e., digest sizes).

# Description 

También se conoce como unstructured search.
Queremos buscar un elemento en una lista que no está ordenada.
Tenemos 2 a la n posibilidades y queremos encontrar el valor de entrada que hace que el resultado de la función sea 1. 
Cuantas veces tendríamos que hacer esto clásica-mente -> Necesitaríamos 2^n queries
El el caso cuántico es -> la raiz cuadrada de 2 ^n 
![[Pasted image 20240421103806.png|400]]

H aplicada a n qubits nos da como resultado una distribución uniforma de todos los posibles estados.

![[Pasted image 20240421103951.png|370]]

Es por eso que cuando se dice que la computación cuántica puede realizar operaciones en todos los estado a a la vez , ya que con este estado de superposición que conseguimos podemos aplicar operaciones a todos estos estados a la vez. Pero lo que no se ve es que no significa que podamos extraer el resultado directamente, **la salida puede ser únicamente una de estas posibilidades , por lo que lo que tenemos que hacer es crear un patrón de interferencia que nos permita extraer la información que se corresponde con la respuetsa al problema**.

![[Pasted image 20240421104622.png]]

Z0 -> Actúa como identidad excepto para el caso en el que todos son 0, en ese caso se le cambia el signo.

Todos los estados A son aquellos para lo que el resultado de f es 1 -> Subespacio Bueno 
Todos los estados B son aquellos para los que el resultado de f es 0 -> Subespacio malo.

Definimos el estado A como superposición de todos los estados del set A y hacemos igual con B.
Y la combinación lineal de estos -> no da la probailidad de obtener un estado corresto y la probabilidad de obtener un estado incorrecto.

![[Pasted image 20240421111036.png]]
![[Pasted image 20240421162140.png]]![[Pasted image 20240421162531.png]]
![[Pasted image 20240421162910.png]]![[Pasted image 20240421163058.png]]

De esta forma podemos ver que realmente lo que hacemos al aplicar G , es una rotación 2* theta.
Cuantas vedes debemos aplicar esta operación de forma que al hacer la medición . la probabilidad de medir un resultado que esté contenido en el estado A (el bueno) con una probabilidad alta.


![[Pasted image 20240421163705.png|500]]
Teniendo en cuanta que el peor escenario posible es que a = 1 , solo haya una entrada para la cual f(x) sea 1.
![[Pasted image 20240421163902.png|500]]
Hay que entender que si nos pasmos en el número de veces que debemos aplicar esto la probabilidad que queremos empezará a decrecer.

**Básicamnete lo que estamos haciendo esto:**
![[Pasted image 20240421164338.png|500]]

![[Pasted image 20240421164551.png]]
**Video Explicativo conceptual:**

https://www.youtube.com/watch?v=vEe02cABxY4&ab_channel=Ket.G
![[Pasted image 20240507150318.png|500]]
![[Pasted image 20240507155821.png|400]]
![[Pasted image 20240507155955.png|400]]
