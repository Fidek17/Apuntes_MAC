
Índice:
	[[#1. Constructores]]
		[[#1.1 This o self]]
	[[#2. Relación con herencia]]
	[[#Inmutables]]
	[[#Constructores con sobre carga]]
#### 1. Constructores

Los constructores son funciones que provocan que una clase genere un mismo objeto o instancia de la clase misma.
Recordemos que la clase contiene objetos, qué se pueden entender como la clase pero con datos o información especifica, digamos que la clase es una plantilla que puede crear objetos a partir de ella pero más específicos. 
El constructor es la función de una clase que provoca que se cree una instancia de la misma clase. 
###### 1.1 This o self
Esto se va a lograr de manera mas sencilla con las palabras reservadas **self** o **this** que hace que se refiera al mismo miembro o instancia creado a partir de una misma clase por medio de de un constructor.
Ejemplo:
```

//Constructor de alguna clase, se trata de una funcion que recibe nombre y edad y los asigna a la misma instancia creada

//Espera recibir parametros que son un string y un int
//----------------------------------------------------------------------

Public Persona(string nombre, int edad){
	this.nombre = nombre;
	this. edad = edad ;
}

//----------------------------------------------------------------------
```
#### 2. Relación con herencia
Cuando se hereda una clase de otra clase sucede la herencia, digamos qué Animal es una clase que tiene un constructor, será posible hacer una clase heredada de Animal que digamos que es Perro y a su vez tiene su constructor.
Será posible heredar el constructor de Animal y hacer que se encuentre en una clase heredada de Animal y llamaremos Perro. 
En síntesis será posible heredar constructores ya que son funciones al final del día, pero tenemos que estar conscientes de cómo se heredan las funciones en 4 casos distintos.

#### Inmutables
Los inmutables son datos que no cambiaran a lo largo de todo el código, la manera de poder declararlo es con la palabra reservada `final` de la siguiente manera: 
```
final int numero = 10; 
final int pi = 3.1416
```
Cuál es la diferencia de `const` y `final`?
La diferencia es que cuando se crea una variable inmutable `const` será obligatorio ponerle un valor desde el momento en que se declara, mientras que con `final` es posible primero declarar una variable inmutable de este tipo y dar el valor de esta variable en algún punto del código.
#### Constructores con sobre carga

Son clases que contienen varios constructores dentro de ella misma. 
Es posible que la clase contenga más de un constructor y al momento de crear una instancia o un objeto de una clase será posible crearlo a partir del constructor preferido o que sea mejor.

#### Tipos de constructores
###### 1. Constructor Default
Es el tipo de constructor que se crea de manera automatica debido a no tener un constructor específico para poder crear una instancia de la clase.
###### 2. Constructor parametrizado

###### 3. Constructor por copia

###### 4. Constructor de Conversión

###### 5. Constructor de movimiento

#### Concepto: rvalue
Se refiere a un valor temporal y que no tiene una ubicación de memoria persistente. Es utilizado normalmente en C++.
Es el valor que se encuentra a la derecha de un igual o una igualación.

Su relación con los constructores tiene que ver y es utilizado especificamente con los constructores de **movimiento** y de **copia**

#### Organización de memoria de constructores
Los constructores en programación como ya dijimos crea un objeto 

#### Fabricas (Factory)
Es un interfaz que nos dará la opción de elegir clases concretas dentro de la interfaz que crean objetos específicos distintos dependiendo de la clase concrete elegida y por último tiene al cliente que será quién elija lo que se hará o que clase se usará. 




