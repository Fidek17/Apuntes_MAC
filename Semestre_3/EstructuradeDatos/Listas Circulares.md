Es una lista simple en donde el último de los elementos siempre está ligado con el primero. 

|P| \*|-> | ...| F| \*P|->| P|
|-| -|-|-|-|-|-|-|
El nodo final apunta hacia **P** generando una especio de circulo. 
Las operaciones son las mismas que las de cualquier lista. Solo se deberá cuidar que el elemento siguiente al último siempre es **P**, y el elemento anterior a **P** es el último de la estructura.
##### Algoritmo que crea una lista circular insertando elementos por el final

```
NODO = REGISTRO
	INFO: TIPODEDATO
	LIGA: ^NODO
FINDEREGISTRO 

	P,Q: ^NODO
	RESP: CARACTER

	INICIO
		CREA(P)
		LEER(P^.INFO)
		P^.LIGA = P
		ESCRIBIR("HAY MAS DATOS?")
		LEER(RESP)
		Q=P

		MIENTRAS (RESP == SI)
			CREA(Q^.LIGA)
			Q = Q^.LIGA
			LEER(Q^.INFO)
			Q^.LIGA = P
			ESCRIBIR("HAY MAS DATOS?")
			LEER(RESP)
		FINMIENTRAS
	FIN
```

##### Algoritmo que borre el primer elemento de una lista circular
*Casos especiales:*
- No hay elemento.
- Si hay elementos
	- Solo hay un elemento
	- Más de un elemento

```
SI P == NULL
	ESCRIBIR("No hay elementos")
SINO
	SI (P^.LIGA == P)
		QUITA(P)
		P = NULL
	SINO
		Q = P
		MIENTRAS (Q^.LIGA != P)
			Q = Q^.LIGA
		FINMIENTRAS
		
		P = P^.LIGA
		QUITA(Q^.LIGA)
		Q^.LIGA = P
	FINSI
FINSI 
```

##### ALGORITMO QUE BUSCA UN ELEMENTO CON INFORMACIÓN DADA POR EL USUARIO EN UNA LISTA CIRCULAR Y QUE IMPRIMA LA DIRECCIÓN DEL ELEMENTO ANTECEDENTE Y LA INFORMACIÓN DEL ELEMENTO CONSECUENTE

*Casos especiales*
- No hay elementos
- Si hay elementos
	- No coincide
	- Si coincide
		- Solo un elemento
		- Coincide en el principio
		- Coincide con el segundo en adelante