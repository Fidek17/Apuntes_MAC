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