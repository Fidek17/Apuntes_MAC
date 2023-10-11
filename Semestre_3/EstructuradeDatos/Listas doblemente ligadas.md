Es una estructura de datos conformada por nodos, en la que cada uno de ellos tiene 3 campos en lugar de 2 como en las listas ligadas simples:
1. Información
2. Apuntador
3. Apuntador 
Esto para poder hacer referencia a los datos antecesores y sucesores.

| | P | P| P | | | | | | .......| |F | F|F | |
| :-:|:-:| -| -| -|- |- | -| -|- |- |- | -| -|- |
| -><-|\* | info | \*| -><-| \*| INFO| \*|-><- | ........|-><-| \* | INFO|\*|-><-|
- \* = APUNTADOR
- P = PRINCIPIO
- F = FINAL 

###### *Algoritmo que crea una lista doblemente ligada añadiendo a cada elemento por el final*

```
NODODBLE=REGISTRO
	LIGAIZQ=^ NODODOBLE
	INFO=TIPO DE DATOS
	LIGADER= ^ NODODOBLE
FIN REGISTRO
	
	P,F,Q=^ NODODOBLE
	RESP=CARACTER
	
INICIO
	CREA(P)
	LEER(P^.INFO)
	P^.LIGAIZQ= NULL
	P^.LIGADER= NULL
	F= P
	ESCRIBIR("Hay mas informacion?")
	LEER(RESP)
	
	MIENTRAS RESP="SI"
		CREA(F^.LIGADER)
		F^.DER^.IZQ = F
		F = F^.DER
		LEER (F^.INFO)
		F^.LIFGADER=NULL
		ESCRIBIR ("Hay mas informacion?")
		LEER (RESP)
	FINMIENTRAS
	
ALTERNARTIVA DE MIENTRAS

	MIENTRAS(RESP ="SI")
		CREA (Q)
		Q^.LIGAIZQ = F
		F^.DER = Q
		F = Q
		F^-DER = NULL
		ESCRIBIR ("Hay mas informacion?")
		LEER (RESP)
	FINMIENTRAS
	
FINALGORITMO
```

***Algoritmo que elimina un elemento antes de uno dado***

Casos especiales: 
1. Existe la lista
	1. Se encuentra el elemento
		1. Es el primer elemento
			Nada que hacer
		2. Es el segundo elemento
			Reasignar el principio
		3. 3 er elemento en adelante
	1. No se encuentra el elemento
2. No existe la lista

```
SI P=NULL
	ESCRIBIR("NO HAY ELEMENTOS")
SINO 
	LEER(DATO)
	Q=P
	MIENTRAS(Q^.INFO!=NULL) Y (Q!=F)
		Q=Q^.liga
	FINMIENTRAS

	SI Q^.info!=DATO
		ESCRIBIR("NO SE ENCONTRO EL ELEMENTO")
	SINO
		SI Q=P
			ESCRIBIR("NO HAY ELEMENTO ANTERIOR AL PRIMERO")
		SINO
			SI Q^.LIGAIZQ = P
				P = Q
				QUITAR(Q^.LIGAIZQ)
				P^.LIGAIZQ = NULL
			SINO
				IZQ = Q^.LIGAIZQ
				IZQ^.LIGAIZQ^.LIGADER = Q
				Q^.IZQ = IZQ^.LIGAIZQ 
				QUITA(IZQ)
			FINSI
		FINSI
	FINSI
FINSI
```

**Algoritmo que inserte un elemento después de uno dado**

Casos especiales:
1. Existe la lista
	1. Se encontro el elemento
		1. Es el ultimo elemento
			Actualizar el nodo final
		2. Si es el último
	1. No se encontro el elemento
2. No existe lista

```
SI P = NULL
	ESCRIBIR ("NO HAY LISTA")
SINO 
	LEER (DATO)
	Q=P

	MIENTRAS (Q^.INFO != INFO) Y (Q != F)
		Q = Q^.LIGA
	FINMIENTRAS

	SI Q^.INFO != DATO
		ESCRIBIR (" NO SE ENCONTRO EL ELEMENTO ")
	SINO 
		SI Q = F
			CREA (Q^.LIGADER)
			Q = Q^.LIGADER
			Q^.LIGAIZQ = F
			LEER (Q^.INFO)
			F = Q
			F^.LIGADER = NULL
		SINO
			CREA(S)
			S^.LIGADER = Q^.LIGADER
			Q^.LIGADER = S
			S^.LIGAIZQ = Q 
			S^.LIGADER^.IZQ = S
			LEER (S^.INFO)
		FINSI
	FINSI
FINSI		
```