Clasificación de los algoritmos internos:
1. Algoritmos de Selección
2. Algoritmos Intercambio
3. Algoritmos Inserción
4. Algoritmos Distribución
5. Algoritmos Intercalación

### Ordenamiento por Selección Directa
Su comportamiento es buscar directamente un elemento y colocarlo en su lugar, este proceso se repetirá hasta terminar.
1. Seleccionar el menor o mayor elemento del arreglo
2. Intercambiar dicho elemento con el primero
3. Repetir los pasos anteriores con los N-1, N-2 elementos hasta terminar con todos los elementos. 

**Ejemplo:**
Arreglo: 12 , 4, 25, 30, 6, 9, 13, 18

1º Iteración: El número más pequeño es el $4$. Este se intercambiara para estar en la primera posición ya que es el más pequeño.

Arreglo: **4**, 12, 25, 30, 6, 9, 13, 18

2º Iteración: Se comienzan a comparar todos los datos entre sí para encontrar el valor más pequeño, en este caso es el número $6$. Este se intercambiara con el dato que esta en donde debería estar el $6$. 

Arreglo: **4**, **6**, 25, 30, 12, 9, 13, 18

3º Iteración: Se intercambia el valor más pequeño: $9$. Se intercambiaría con quien esta en el lugar que debería estar que es el 25. 

Arreglo: $4$, $6$, $9$, 30, 12, 25, 13, 18. 

4º Iteración: Valor más pequeño: $12$. Intercambia con $30$ ya que esta en su lugar.

Arreglo: $4$, $6$, $9$, $12$, 30, 25, 13, 18

5º Iteración: Valor más pequeño: $13$. Intercambia con: $30$. 

Arreglo: $4$, $6$, $9$, $12$, $13$, 25, 30, 18

6º Iteración: Valor más pequeño: $18$. Intercambia con $25$. 

Arreglo: $4$, $6$, $9$, $12$, $13$, $18$, 30, 25

7º Iteración: Valor más pequeño: $25$. Intercambia con $30$. 

Arreglo: $4$, $6$, $9$, $12$, $13$, $18$, $25$, $30$

Ya se acaba el método ya que el arreglo termino ordenado. 

**Algoritmo**
```pseudocode
DESDE I = 1 HASTA N-1 
	MENOR = A[I]
	K = I
	DESDE J = I+1 HASTA N 
		SI A[J] < MENOR 
			MENOR = A[J]
			K = J
		FINSI
	FINDESDE
	A[K] = A[I]
	A[I] = MENOR
FINDESDE
```
### Métodos de ordenamiento por intercambio

**Método de la burbuja (intercambio directo)**
Trabaja de dos maneras distintas: 
- Llevando los elementos más pequeños a la parte izquierda del arreglo.
- Llevando los elementos más grandes a la parte izquierda del arreglo y los más pequeños a la parte derecha. 

**Ejemplo: En manera Ascendente Burbujeando de derecha a izquierda.**

Arreglo: 12, 4, 25, 30, 6, 9, 13, 18

Se comparará desde derecha a izquierda los datos comenzando con 18 y comenzar el recorrido en donde como se burbujea de derecha a izquierda, se revisa si el valor es mayor a menor al de la derecha y dependiendo del resultado se mueve. 

Se compara 18 con 13 y como el 13 es menor, ya están ordenados de manera ascendente. 
Se compara el 13 con el 9 y como el 9 si es menor, ya están ordenados de manera ascendente. 
Se compara el 9 con el 6 y el orden queda igual porque ya estan ordenados de manera ascendente. 
Se compara 6 con 30, como 30 no es menor a 6, intercambian lugares y se tiene el nuevo arreglo. 

Arreglo: 12, 4, 25, 6, $30$, $9$, $13$, $18$. 

Se continua comparando a 6 con 25, como 25 no es menor a 6, se intervambian lugares. 

Arreglo: 12, 4, $6$, $25$, $30$, $9$, $13$, $18$. 

Se compara a 6 con el 4, como 4 si es menor a 6, el arreglo queda igual porque esos dos ya estan ordenados de manera asncendente. 

Se compara a 4 con 12, como 12 no es menor a 4, se incercambian lugares. 

Arreglo: $4$, $12$, $6$, $25$, $30$, $9$, $13$, $18$. 

2º Iteración: 
Arreglo: 4, 6, 12, 9, 25, 30, 13, 18

3º Iteración: 
Arreglo: 4, 6, 9, 12, 13, 25, 30, 18

4º Iteración: 
Arreglo: 4, 6, 9, 12, 13, 18, 25, 30

5º Iteración: 
Arreglo: $4$, $6$, $9$, $12$, $13$, $18$, $25$, $30$

Se termina el algoritmo y solo tomo N-1 iteraciones. 

**Algoritmo de ordenación por el metodo de la burbuja**
```pseudocode
DESDE I = 2 HASTA N 
	DESDE J = N HASTA I
		SI  A[I-J]
```

**Método de la sacudida o embudo (Shaker sort, Shake Sort)**
**Algoritmo**
```
IZQ = 2 
DER = N 
K = N 
MIENTRAS DER >= IZQ
	DESDE I = DER HASTA IZQ 
```


**Ordenación pares y nones**
Solo es aplicable con arreglos con un numero par de elementos. 

Arreglo: 12, 4, 25, 30, 6, 9, 13, 18
Pares: (12, 4 ), (25, 30), (6, 9), (13, 18)

Ordenado: (4, 12), (25, 30), (6, 9), (13, 18) 

1º Non 
4, (12, 25), (30, 6), (9, 13), 18
Ordenado: 4, 12, 25, 6, 30, 9, 13, 18

1ª Par 
(4, 12), (25, 6), (30, 9), (13, 18)
Ordenado: 4, 12, 6, 25, 9, 30, 13, 18

2ª Non 
4, (12, 6), (25, 9), (30, 13), 18
Ordenado: 4, 6, 12, 9, 25, 13, 30, 18

2ª Par:
(4,6 ), (12, 9), (25, 13), (30, 18)
Ordenado: 4, 6, 9, 12, 13, 25, 18, 30

3ª Non
4, (6, 9), (12, 13), (25, 18), 30
Ordenado: 4, 6, 9, 12, 13, 18, 25, 30

3ª Par 
(4, 6,), (9, 12), (13, 18), (25, 30)       

**Método Quick Sort**

Arreglo: 12, 4, 25, 30, 6, 9, 13, 18

QS(Limíte inferior: Posición 1, Limite superior: Posición 8)

x = 12
Se comienza a comparar los daots con el lado desde más a la derecha

12 < 18 Bien
12 < 13 Bien
12 < 9 NO es cierto
Cambian posiciones. 

9, 4, 25, 30, 6, 12, 13, 18

Como se hizo un cambio, se cambia el sentido de la comparación, como lo estabamos haceidno desde la derecha hasta la izquierda, ahora se hará izquierda a derecha, teniendo como paro al número que estamos comparando. 

4 < 12 Bien 
25 < 12 No es cierto

Se cambian posiciones

9, 4, 12, 30, 6, 25, 13, 18

Se compara ahora de derecha a izquierda. 

12 < 6 No es cierto
Se cambian posiciones 

9, 4, 6, 30, 12, 25, 13, 18

Se compara de izquierda a derecha.

30 < 12 NO es cierto
Se cambian posiciones 

9, 4, 6, 12, 30, 25, 13, 18 

Como ya revise todo el arreglo, estamos seguros de que 12 ya esta en su lugar, resta acomodar los montones que no estan ordenados es decir, Quick Sort desde la posicion 1 hasta 3 que comprende a (9, 4, 6) y Quick sort desde 5 hasta 8 (30, 25, 12, 18)

Qs(1, 3)
x = 9 

Arreglo: 9, 4, 6

9 < 6 NO, se intercambia

6, 4, 9
Cambia a sentido de izquierda a derecha. 

9 >  4 Si
9 > 9 Como se esta comparando consigo mismo ya esta en su lugar ese elemento, se revisa el otro monton sobrante que serain los de la poscion 1 a 2 que son 6 ,4 

Qs(1, 2) 
x = 6 
6 < 4 NO, se intercambia 

4, 6 
Cambia a sentido de izquierda a derecha

6 < 6, Se trata del mismo numero entonces ya esta en su lugar y como ya no queda otro montón todo ese montón ya esta en su lugar, es decir 

Arreglo listo: 4, 6, 9, 12. Arreglo o montón faltante: 30, 25, 13, 18

Comenzamos a encargarnos del montón faltante:  30, 25, 13, 18
QS(5, 8)
x = 30 

30 < 18 NO es cierto, se intercambia 

18, 25, 13, 30
Se cambia a sentido de izquierda a derecha. 

25 < 30 Bien 
13 < 30 Bien 
30 < 30, Como ya se esta comparando el mismo con el mismo por lo tanto 30 ya esta en la posición correcta y ahora falta llamar al Quick sort a (5, 7), ya que es el montón faltante a ordenar. 


QS(5, 7)
Arreglo: 18, 25, 13
x = 18

18 < 13 No es cierto, intercambio

13, 25, 18
Se cambia a sentido de izquierda a derecha. 

25 < 18 No es cierto, se intecambia

12, 18, 25. 
Se cambia a sentido de derecha a izquierda

18 < 18 Como ya se esta comparando la misma posición consigo misma se sabe que el 18 ya esta en su lugar, faltarían los otros montones que son 12 un montón y 25 otro montón, entonces se llama a QS en cada uno de los montones, pero al ser montones de un solo elemento significaria que ya estan en su lugar. Para entenderlo mandaremos a llamar a QS con el montón de 12. 

QS(7)
Arreglo: 12

x = 12 

12 < 12 Ya se compara con la misma posición por lo que ya esta en su lugar. 


Como se observa al llamar a QS con un solo elemento ya estaría en su lugar desde el primer momento, se puede llamar que es un caso baso y como el montón 12 y el montón 25 ya están en su lugar como analizamos ahora significa que todo el monton (5, 7) ya esta ordenado y por lo tanto también el (5,8) por lo tanto todo el arreglo ya esta ordenado. 

### Método de ordenación por inserción
**Método de inserción Directa (Método de la baraja)**

