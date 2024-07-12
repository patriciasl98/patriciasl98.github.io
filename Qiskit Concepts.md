---
tags:
  - Concept
Sumary: Cubrimos muchos de los conceptos mecesarios para entnder la programción en Qiskit
---

# MOC
* [[Concepts MOC]]
# Related notes

```dataview
TABLE WITHOUT ID link(file.name) AS "Nota", file.cday AS "Created date" , Sumary
FROM #Concept 
WHERE contains(file.outlinks, this.file.link)
OR contains(file.inlinks, this.file.link)
and contains(file.name , "MOC")
AND file.name != this.file.name
```




# Qiskit Concepts


# Ejecución de un circuito cuántico en Qiskit 
Cuando se llama al método `run()` del **estimador**, se envía el circuito cuántico `qc` y las observables `observables` al backend especificado. El backend ejecuta el circuito cuántico y devuelve los resultados, que se almacenan en el objeto `Job`.
```python
# Configure el estimador
estimator = Estimator(backend=AerSimulator())
# Envíe el circuito al Estimador
pub = (qc, observables)
job = estimator.run(pubs=[pub])
```

En el código, se crea una tupla `pub` que contiene el circuito cuántico `qc` y las observables `observables`. Esta tupla se pasa como argumento al método `run()` del estimador.
Después de ejecutar un circuito cuántico en Qiskit, se puede obtener los resultados de la ejecución mediante el objeto `Job` que se devuelve. El objeto `Job` contiene información sobre la ejecución del circuito, incluyendo los resultados de las medidas.

```python
# Recopile los datos
data = ['IZ', 'IX', 'ZI', 'XI', 'ZZ', 'XX']
values = job.result()[0].data.evs
# Configure nuestro gráfico
container = plt.plot(data, values, '-o')
# Etiquete cada eje
plt.xlabel('Observables')
plt.ylabel('Values')
# Dibuje el gráfico final
plt.show()
```

* `job.result()`: Devuelve un objeto `Result` que contiene los resultados de la ejecución del circuito cuántico.
* `job.result()[0]`: Seleccionl primer resultado de la lista de resultados, que es un objeto `ResultData`.
* `job.result()[0].data`: Devuelve un objeto `Data` que contiene los datos de la medida.
* `job.result()[0].data.evs`: Devuelve una lista de valores que corresponden a los **eigenvalores** (valores propios) de la medida.

En otras palabras, `values` es una lista de valores que representan los resultados de la medida del circuito cuántico.

Aquí hay algunas opciones para obtener los resultados de un circuito cuántico en Qiskit:

* `job.result().get_counts()`: Devuelve un diccionario que contiene los **conteos de cada estado cuántico medida.**
* `job.result().get_statevector()`: Devuelve un **estado cuántico vectorial que representa el estado cuántico final del circuito.**
* `job.result().get_unitary()`: Devuelve una matriz unitaria que representa la evolución del circuito cuántico.
* `job.result().get_measurement()`: Devuelve una lista de valores que corresponden a los resultados de la medida.


## Observables

En el código que mencioné anteriormente, `observables` es una lista de objetos. Observable se utilizan para definir las **medidas que se desean realizar en el circuito cuántico qc**. Cuando se ejecuta el circuito cuántico, el backend devuelve los resultados de las medidas definidas por los observables.
Por ejemplo, se puede crear un observable que corresponda a la medida de la polarización de un qubit utilizando la clase `PauliZ`

## Estimator

 `Estimator` es un **objeto que se encarga de ejecutar un circuito cuántico en un backend** (dispositivo cuántico real o simulado) y **devuelve una estimación de las medidas cuánticas**. En otras palabras, el estimador se encarga de ejecutar el circuito cuántico y obtener los resultados.

En el código, se crea un objeto `Estimator` con el backend `AerSimulator()`. `AerSimulator` es un backend de simulación cuántica que simula el comportamiento de un dispositivo cuántico real. Otros backends pueden ser dispositivos cuánticos reales.

```

          +---------------+
          |  Estimator  |
          +---------------+
                  |
                  |  (qc, observables)
                  v
          +---------------+
          |  Job        |
          +---------------+
                  |
                  |  Ejecutar circuittico
                  v
          +---------------+
          |  Backend    |
          |  (AerSimulator) |
          +---------------+
                  |
                  |  Devuelve resultados
                  v
          +---------------+
          |  Job        |
          +---------------+
```


## Primitivas
* https://medium.com/qiskit/what-are-qiskit-primitives-9bf63c1eacc7
### Sampler 
En Qiskit, la primitiva `Sampler` es una clase que se utiliza para **muestrear los estados cuánticos de un circuito cuántico**. Esta primitiva se utiliza para obtener una muestra de los estados cuánticos posibles del circuito, lo que es útil para la simulación de sistemas cuánticos y la ejecución de algoritmos cuánticos.

```python
qc.measure_all()
### Write your code below here ###
sampler = StatevectorSampler()
pub = (qc)
job = sampler.run([pub], shots=256)
job_sampler = job
### Don't change any code past this line ###
result_sampler = job_sampler.result()
counts_sampler = result_sampler[0].data.meas.get_counts()
print(counts_sampler)
```

## ¿Estimator vs Sampler ?

En Qiskit, tanto el `Estimator` como el `Sampler` se utilizan para **obtener información sobre los estados cuánticos de un circuito cuántico**. Sin embargo, se enfocan en aspectos diferentes y se utilizan de manera diferente.

**Estimator**:

El `Estimator` se utiliza para calcular la **esperanza** (expectation value) de una observable en un estado cuántico. En otras palabras, el `Estimator` te permite calcular **el valor promedio de una propiedad cuántica (como la energía o el momento angular) en un estado cuántico.**

Cuando se utiliza un `Estimator`, se proporciona una observable (como una matriz de Pauli) y el estado cuántico del circuito. El `Estimator` entonces calcula la esperanza de la observable en ese estado cuántico.

**Sampler**:

El `Sampler`, por otro lado, se utiliza para obtener una **muestra de los estados cuánticos posibles de un circuito cuántico**. En otras palabras, el `Samplee permite obtener una lista de estados cuánticos posibles, junto con sus respectivas probabilidades.

Cuando se utiliza un `Sampler`, se proporciona un circuito cuántico y se especifica el número de muestras que se desean obtener. El `Sampler` entonces devuelve una lista de estados cuánticos posibles, junto con sus respectivas probabilidades.

**Key differences**:

* **Purpose**: El `Estimator` se utiliza para calcular la esperanza de una observable, mientras que el `Sampler` se utiliza para obtener una muestra de los estados cuánticos posibles.
* **Input**: El `Estimator` requiere una **observable** y un **estado cuántico**, mientras que el `Sampler` requiere un **circuito cuántico** y el **número de muestras que se desean obtener**.
* **Output**: El `Estimator` devuelve un **valor numérico que representa la esperanza de la observable**, mientras que el `Sampler` devuelve una l**ista de estados cuánticos posibles junto con sus respectivas probabilidades.**

# Qiskit Runtime 
Qiskit Runtime es una plataforma de ejecución de código cuántico que permite a los **desarrolladores ejecutar sus circuitos cuánticos en una variedad de dispositivos cuánticos, incluyendo dispositivos reales y simuladores.**

Qiskit Runtime se compone de varios componentes, incluyendo:

1. **Qiskit Runtime Service**: Es el servicio que se encarga de ejecutar los circuitos cuánticos en los dispositivos cuánticos.
2. **Qiskit Runtime Client**: Es la interfaz de programación de aplicaciones (API) que se utiliza para interactuar con el servicio Qiskit Runtime.
3. **Qiskit Runtime Provider**: Es el proveedor de dispositivos cuánticos que se encarga de proporcionar acceso a los dispositivos cuánticos.

# VQE Quiskit Qiskit Runtime and a Variational Quantum Eigensolver (VQE)
