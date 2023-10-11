Las diferentes formas de almacenamiento de las E.D, ventajas y desventajas.
## 2.1 Almacenamiento estático y dinámico
Estructuras estáticas =>Arreglos
Estructuras dinámicas => Apuntadores (a pesar de existir arreglos dinámicos. Es más común encontrarlo asi)

Aunque ahora los arreglos se consideran dinámicos ya que se aparta cierta cantidad de espacio para el arreglo, y sólo se usa la especificada, sin embargo sus otras propiedades siguen siendo estáticas, . . .
Sus diferencias son la reservación de memoria

### Bondades y desbondades

| **Almacenamiento estático** | **Almacenamiento dinámico** |
|--------------|--------------|
|Asignación de memoria fija para el tamaño de la E.D.| Asignación de memoria variable    |
| Se establece en tiempo de compilación    | Se establece en tiempo de ejecución   
||| 
| Dependiendo de las circunstancias puede faltar o sobrar memoria | La memoria se amplia o se retrae de acuerdo a las necesidades|
| *Referencia directa* a un elemento del arreglo |  Hay que recorrer la estructura para *localizar elementos*|
| Para eliminar o insertar elementos se debe *recorrer los demás elementos* de la E.D | Para eliminar o insertar basta con *actualizar ligas* |
| | |


### LP
- **E.D Elementales**
	- Arreglos
	- Registros o estructuras
	- Enumeraciones o colecciones
- **E.D No Elementales**

## 2.2 Arrays
Es una E.D homogénea, finita (que siempre existe un último elemento) y ordenada (porque hay elementos consecutivos en un mismo bloque de memoria) de elementos. Almacenan datos de cualquier tipo siempre y cuando sea una mismo para todos.
#### Componentes de un arreglo
- Elementos del arreglo
- índices
	- *Los cuales pueden ser cualquier tipo de dato ordinal (enteros, caracteres, enumeraciones)*
#### Para referenciar a un arreglo
- Identificador o nombe
- Indice(s)
#### Operaciones
- Inserción
- Eliminación
- Modificación
- Ordenación
- Búsqueda
#### Tipos 
- Unidimensional
	- Lista que se guarda en un arreglo
- Bidimensional
	- Para hacer referencia a un elemento se requieren 2 índices
- Multidimensional
	- [[#Arreglos multidimensionales]]
#### NTC (Número Total de Componentes) = límiteSuperior - límiteInferior +1
***Para arreglos bidimensionales la formula de NTC cambia a 
NTC = (limsup1 - liminf1 + 1) * (limsup2 - liminf2 +1)***
## Ejemplo
Algoritmo que lee  un arreglo de 10 elementos enteros, les suma el índice correspondiente e imprime el resultado
```
A,B = Arreglos[1. 10] de emtero
i = entero

INICIO
	Desde i = 1 hasta 10
		Escribir('Dame el elementos', i, 'del arreglo')
		Leer 
. . .

```


## Algoritmo que determine si una matriz es Identidad
``` DEFINICION DE VAIRABLES
A = arreglo[1,20; 1,20] int
int n,i,j, aux  = 0

INICIO
	Escribir('Dame dimensión. La matriz debe de ser cuadrada')
	Leer(n)
	
	Desde i = 1; hasta n
		Desde j = 1; hasta n
			Leer(A[i,j])
		FinDesde
	FinDesde

	Desde i = 1; hasta n
		Desde j = 1; hasta n
			si ( i == j)
				si (A[i,j] != 1)
					Aux = 1
				FinSi
			SiNo
				Si (A[i,j] != 0
					Aux = 1
				FinSi
			FinSi
		FinDesde
	FinDesde

	Si (Aux == 0){
		Imprimir "No es la matriz identidad"
	}
	Sino{
		Imprimir "Matriz identidad"
	}

```

### Arreglos multidimensionales
Es una E.D homogénea, ordenada y finita de elementos, donde se requere más de 2 índices para hacer referencia a un valor esoecífico.
Para leer este tipo de arreglos se necesitarían tantos bucles anidados como índices ó dimensiones se tuvieran

#### Sintaxis
```
Identificador = Arreglo [limInf1, limSup2, limInfo2, limSup2, ...,  limInfN, limSupN]
```

#### NTC = (limSup1-limInf 1+1) * (limSup2 - limInf 2+1) * . . . * (limSupN - limInf n+1) 

