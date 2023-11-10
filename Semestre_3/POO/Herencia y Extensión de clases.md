#### Herencia
Es la capacidad que tenemos de heredar propiedades en una clase (*hija*) a partir de otra clase (*Super clase*).
Nos deja crear jerarquía entre las clases y sub clases donde las sub clases pueden aprovechar y además extender las características de las super clases. 

**Tipos de herencia según James Rumbaugh**
- Herencia de interfaz: No hereda su implementación, la cambia y la personaliza, solo hereda su firma.
- Herencia de implementación: Heredar tanto la interfaz y también su implementación de la clase base. 

##### Generalización
Es la creación de una nueva clase (super clase) que es una versión más general o abstracta de una o más clases existentes (*sub clases*).

##### Especialización
Es lo que sucede cuando las sub clases perfeccionan o especializan a la super clase. Es casi como el proceso inverso de la generalización. Sucede cuando las sub clases heredan a super clase pero también añaden cosas a este molde o abstracción. 

##### Tipos de relaciones

**¿Qué principio hace que se elija que tipo de relación es?**
- Principio de Sustitución: De las siglas SOLID, proporcionado en la L por la señora Liskov.
###### (IS -A)/ "Es un tipo de "
Es cuando la sub clase siempre será del mismo tipo que el de la clase base.

###### (HAS-A)/ "tiene un"
Cuando una clase A "has a" clase B, significa que la clase A contiene un objeto de la clase B como parte de su estructura. 

**Ejemplo:**
Si tengo una clase Persona y sub clases, alumno, profesor y otra llamada materia. 
Alumno no es un tipo de materia, (is -a), tiene una o más materias (has-a).
También se puede decir que *Profesor* y *Alumno* no tiene una *Persona* (has-a), sino más bien es un tipo de *Persona* (is-a)
##### Tipos de herencia
###### Herencia Simple
La nueva clase puede heredar atributos y métodos que no existián en la clase original. 
Los objetos de la nueva clase heredan los atributos y métodos.

**Herencia por Implementación**
Implementación real de los métodos y propiedades de una clase padre por parte de una clase hija.

**Herencia múltiple**
Una clase hija puede heredar de múltiples clases padres.
Una de las desventajas es la colisión de nombres que ocurren cuando varias clases padre tienen métodos o atributos con el mismo nombre. 
*Alternativa para Java será herencia por interfaz*.

**Herencia por Interfaz**
Es una opción de la herencia múltiple para los lenguajes que no aceptan la herencia de este tipo.
Colección de métodos abstractos.
Métodos que solo tienen la firma pero no tienen implementación concreta, además de ser de acceso público. 
En Java, se crean clases como *interface* para crear una interfaz que nos dará la capacidad de heredar sus métodos vacíos y esto se hará al declarar la clase y usar la palabra reservada *implements* para traer los métodos vacíos de varias interfaces antes creadas. 
##### Transitividad
Si C hereda de B, B hereda de A, entonces C hereda de A. 
**Ejemplo:**
Si *Bicicleta* hereda de *Vehículo* y *Vehículo* hereda de *ObjetoTransporte*, entonces *Bicicleta* hereda indirectamente de *ObjetoTransporte*

#### Caracterización semantica de la herencia
###### Solapada:
Una clase hija modifica o "solapa" un método heredada con su propia implementación

###### Disjunta: 
La clase hija solo hereda el método sin modificarlo como si se tratara de algo sagrado. 

###### Completa:
Una clase derivada proporciona una implementación completa y funcional de todos los métodos heredados.

###### Incompleta:
Una clase derivada que no proporciona una implementación completa de uno o varios de los métodos heredados.

###### Estatica
Permite la decisión de que método llamar en tiempo de compilación. 

###### Dinamica
La decisión de que método llamar se tomará en tiempo de ejecución. 

#### Encapsulamiento o SCOPE
3 niveles de acceso: 
- Atributos y métodos públicos (Public: )
- Atributos y métodos privados (Private: )
- Atributos y métodos protegidos (Protected: )
