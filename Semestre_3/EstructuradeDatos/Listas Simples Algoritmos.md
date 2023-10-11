***Algoritmo para eliminar el nodo al final de la lista***
```pseudocode
	Si P=NULL
		Escribir("No hay elementos")
	SINO 
		SI P^.liga = NULL
			Quita(P)
			P=NULL
		SINO
			Q=P
			MIENTRAS Q^.Liga! = NULL
				T=Q
				Q=Q^.Liga
			FINMIENTRAS
			Quita(Q)
			T^.Liga=NULL
		FINSI
	FINSI
```
Escenarios posibles: 
1. Existencia de la lista
2. Existen elementos en la lista
	1. Hay más de un elemento
	2. Solo hay un elemento
Funcionará repasando todos los apuntadores de la lista y revisando a dónde apuntan, cuando se llega al apuntador que apunta a NULL significa que llegamos al final de la lista. 

***Algoritmo de búsqueda de un elemento en una lista***

Escenarios posibles: 
1. No hay elementos en la lista.
2. Si hay elementos en la lista. 
	1. No esta el elemento
	2. Si esta el elemento

```pseudocode
SI P=NULL 
	Escribir("No hay elementos en la lista")
SINO
	Escribir("Dame el dato a buscar")
	Leer(Dato)
	Q=P
	MIENTRAS (Q^.Liga!=NULL) y (Q^.INFO!=Dato)
		Q=Q^.Liga
	FINMIENTRAS
	SI Q^.INFO!=Dato
		Escribir("No se encontro el dato")
	SINO
		Escribir("Si esta presente el dato")
	FINSI
FINSI
	 
```
Primero revisará si existen elementos, cuando si existen va a pedir el dato a buscar, recorrerá la lista con el puntero Auxiliar $Q$  en un ciclo MIENTRAS, este ciclo mientras solo se ejecutará mientras no se haya llegado al final de la lista y mientras no se haya encontrado el dato. Esto quiere decir que cuando nos salgamos del ciclo mientras se cumplió que se llego al final de la lista o se cumplió que se encontró el dato y por lo tanto debemos hacer un SI  condicional para revisar que si se haya encontrado el dato y así imprimir si se encontró o no el dato.  

***Algoritmo que elimina un nodo que coincide con cierta información***

Escenarios Posibles: 
1. No hay lista existente
2. Si hay lista
	1. No se encontro el dato
	2. Si se encuentra el elemento
		1. Se encontró en el primer nodo: Actualizar a P
		2. Se encontró del segundo nodo en adelante
```psudocode
SI P=NULL
	Escribir("No hay elementos")
SINO
	Leer(Dato)
	SI P^.info=Dato
		Q=P
		P=P^liga
		Quita(Q)
	SINO
		Q=P
		MIENTRAS(Q^.liga!=NULL && Q^.info!=Dato)
			Aux=Q
			Q=Q^.liga
		FINMIENTRAS
		SI(Q^.Dato!=Dato)
			Escribir("No se encontro el dato")
		SINO
			Aux^.liga=Q^.liga
			Quita(Q)
		FINSI
	FINSI
FINSI
	
```
Primero se asegura que si exista la lista, si existe la lista se continua trabajando.
Leemos un dato 

***Insertar nodo antes del nodo que coincidió con un elemento dado***

Casos posibles:
1. No hay lista 
	1. Si hay lista
		1. Si hay elemento 
			1. Primer elemento
			2. Cualquier otro
		  2.  No esta el elemento

***Borrar antes del que coincide***

Casos Posibles:
1. No hay lista
2. Si hay lista
	1. No existe el elemento: No se borra
	2. Si existe el elemento 
		1. Primer elemento: No hay elemento anterior que borrar.
		2. Segundo elemento: Borrar el primero y actualizar al segundo como P
		3. Tercer elemento en adelante: 

***Borrar Nodo de enfrente al nodo que coincidió con con el dato dado***

Casos Posibles:
1. No hay lista
2. Si hay lista
	1. No existe el elemento: No se borra
	2. Si existe el elemento 
		1. Ultimo elemento: No se borra nada
		2. Penúltimo elemento: Asignar NULL a la liga del que coincidió.
		3. Cualquier otro elemento. 