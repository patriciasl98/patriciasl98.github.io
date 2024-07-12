---
dg-publish: true
tags:
  - Concept
  - criptografía
Sumary: Indrocucción del algoritmo RSA
---
# Notas relacionadas
```dataview
TABLE WITHOUT ID link(file.name) AS "Nota", file.cday AS "Created date" 
FROM ""
WHERE contains(file.outlinks, this.file.link)
OR contains(file.inlinks, this.file.link)
AND file.name != this.file.name
```

# Descripción
![[Pasted image 20240508162544.png|500]]
Se basa en el hecho de que las funciones son fáciles de computar en un sentido pero muy complicadas en sentido contrario. (Como la factorización en números primos)
Si tenemos lo factores primos es muy sencillo calcular el número. Pero si conocemos el número es mucho más difícil de descomponer en sus componentes primos.

**Proceso:**
1. Generación de claves:
   a) Seleccionar dos números **primos grandes, p y q.** (por ejemplo p=3 y 1 =11)
   b) Calcular **n = p * q.** El valor n se utiliza como módulo en las operaciones de cifrado y descifrado. (n=33)
   c) **Calcular la función de Euler φ(n) = (p-1)(q-1)**. (φ(n) = (p-1)(q-1) = (3-1)(11-1) = 2 * 10 = 20.)
   d) Seleccionar un número **e impar tal que 1 < e < φ(n)** y **e sea coprimo (si no tienen ningún factor primo en común) con φ(n)**. El número e se denomina **exponente de cifrado.** (Podemos elegir e = 3 (otros valores posibles de e podrían ser 7, 11 y 17).
   e) Calcular **d**, el inverso multiplicativo de e modulo φ(n), es decir, **e * d ≡ 1 (mod φ(n))**. El número d se denomina exponente de descifrado. (d = 7 cumple con este requisito, ya que 3 * 7 = 21 ≡ 1 (mod 20) )

>[!Examle]
>Ejemplo Inverso multiplicativo: Buscamos un número 'b' tal que (a * b) % m = 1. En este caso, 5 * 2 = 10, y 10 % 9 = 1. Por lo tanto, el inverso multiplicativo de 5 módulo 9 es b = 2.

   f) El par de claves pública y privada es **{(e, n), (d, n)}.** ({(3, 33), (7, 33)}.)

2. **Cifrado**: Para cifrar un **mensaje M**, el remitente debe conocer la c**lave pública del destinatario (e, n)**. El mensaje **M debe ser convertido en un número entero m tal que 0 ≤ m < n**. El cifrado se realiza utilizando la siguiente operación:
   **C ≡ m^e (mod n)**
   Donde **C es el texto cifrado.**
   (Si M=5, , C ≡ m^e (mod n) = 5^3 (mod 33) = 125 (mod 33) = 26)
>[!Ejemplo]
>125 (mod 33) -> Esto es el resto de la división de 125 entre 33 -> 125/33 = 3 (con residuo 26)
>Interesante mirar esta nota para entender bien estos conceptos [[Modular aricmetic]]

3. **Descifrado**: Para descifrar el mensaje, el destinatario utiliza su clave privada (d, n). El descifrado se realiza utilizando la siguiente operación:
   **M ≡ C^d (mod n)**
   M ≡ C^d (mod n) = 26^7 (mod 33) = 8031810176 (mod 33) = 5
   
   Donde M es el mensaje original en forma numérica, que luego se convierte de nuevo al texto original.


4. Firmas digitales: El RSA también se puede utilizar para firmar mensajes. Para firmar un mensaje, el remitente utiliza su clave privada (d, n) y la función hash del mensaje:
   S ≡ H(M)^d (mod n)
   Donde S es la firma digital y H(M) es el valor hash del mensaje M.

5. Verificación de firmas: Para verificar la firma digital, el receptor utiliza la clave pública del remitente (e, n) y realiza la siguiente operación:
   H(M) ≡ S^e (mod n)
   Si el resultado coincide con el valor hash del mensaje H(M), la firma es válida y se confirma que el mensaje proviene del remitente legítimo.

El RSA es seguro siempre que **se utilicen números primos lo suficientemente grandes** (actualmente se recomienda utilizar al menos 2048 bits para n) y se mantengan en secreto p, q y d. La seguridad del RSA **se basa en la dificultad del problema de factorización, es decir, descomponer n en sus factores primos p y q**. 

![[Pasted image 20240509175542.png|500]]

**Videos explicativo:**
https://www.youtube.com/watch?v=qph77bTKJTM&ab_channel=TomRocksMaths
https://www.youtube.com/watch?v=CMe0COxZxb0&ab_channel=UPM


# Related Pages

* [[3. Asymmetric key cryptography#RSA]]
