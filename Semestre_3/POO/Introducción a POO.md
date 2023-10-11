La Programación Orientada a Objetos toma un paradigma totalmente distinto a lo visto antes en C. 
En la programación orientada a objetos es importante conocer lo que es la ***abstracción*** como concepto elemental, ya que es uno de los cuales esta fuertemente cimentado.

**Abstracción**: Proceso en el que se toman en cuenta los detalles más importantes de un ente de la realidad, así logrando crear una representación sintetizada del ente original.

Otro concepto de igual manera importante es el de clase, pero primero debemos preguntarnos. ¿Qué es **clasificar**?

**Clasificar**: Es el proceso mediante el cual a partir de un conjunto se agrupan elementos de este mismo en otros subconjuntos nuevos, según sus características o propiedades similares.

Esto se puede ya empezar a ver desde un punto de vista de *Programación Orientada a Objetos.*

Una clase de manera primitiva se observa de esta manera:
```
Clase ={Propiedades = {Propiedad_1, Propiedad _2, Propiedad_3 ... Propiedad_n}
Acciones = {Accion_1, Accion_2, ... Accion_m}}
```
Un ejemplo de una clase es:
```
Mamifero = {Propiedades = {Ojos, Naríz, Boca, ...}
			Métodos = {Comer(), Dormir(), Caminar()}}
```
La clase *Mamífero* tiene sus características o propiedades como un conjunto especifico de seres vivos y también métodos, estos son como funciones o acciones que lleva a cabo un mamífero.

La clase Mamífero es una clase porque sabemos que dentro del gran conjunto que son los seres vivos, los mamíferos son un subconjunto de los seres vivos que comparten características especificas que al cumplirlas es posible que entren a este subconjunto.

Una instancia es es un objeto de una clase, es decir, mamífero es mi clase, pero esto abarca a todos los seres vivos, si yo quiero referirme solo a un mamífero tengo a los *perros*, *gatos*, *humanos*, etc. Todos estos son objetos de la clase Mamífero, ya que cumplen con las características de uno. 
Por lo tanto las instancias de la clase ***Mamífero*** pueden ser las siguientes:
```
Mamíferos = {Perro, Gato, Persona, ...}
```
De manera que se puede decir que Mamíferos nació desde el conjunto enorme o clase enorme de los seres vivos en general, también es posible crear un nuevo subconjunto a partir del conjunto Mamíferos, esta se llamará **subclase** ya que se deriva de una clase especifica.

En este ejemplo sabemos que uno de los objetos o cosas que cumplen las características para ser considerado parte de la clase Mamífero es *Persona*, pero de esta se pueden derivar otras instancias según que también cumplen las características de *Mamífero* y de *Persona*, por lo que *Persona* se convierte en una subclase de *Mamífero* que cumplen otras características más especificas, un ejemplo de como se vería las instancias u objetos de esta subclase es la siguiente:
```
Persona{Doctor, Luis, Maestra, Mamá, Emperador, Cliente}
```
#### Polimorfismo

Antes de continuar es importante conocer lo que es el polimorfismo. 
Como ya vimos antes, es posible hacer clases heredadas, es decir,  que a partir de una clase poder crear una subclase más especifica, tal fue el caso desde la clase Mamífero a Persona, siendo esta una nueva subclase derivada de Mamífero. 

El **Polimorfismo** se refiere a la capacidad que tiene el lenguaje de, a partir de una clase con un método no implementado, generar nuevas subclases que implementen ese método solo definido y hacerlo de manera distinta para cada subclase si así se desea, a continuación mostrará un ejemplo códficado en Java ya que en este lenguaje deberá ser escrito el proyecto y además claro que es un lenguaje orientado a objetos

**Ejemplo:**
``` java
// Clase base Animal
class Animal {
    public void hacerSonido() {
        // Método base sin implementación específica
    }
}

// Clase derivada Perro
class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Woof!");
    }
}

// Clase derivada Gato
class Gato extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Miau!");
    }
}

public class Main {
    // Función que usa polimorfismo
    public static void hacerRuido(Animal animal) {
        animal.hacerSonido();
    }

    public static void main(String[] args) {
        // Crear instancias de las clases derivadas
        Perro perro = new Perro();
        Gato gato = new Gato();

        // Llamar a la función hacerRuido con diferentes objetos
        hacerRuido(perro);  // Output: "Woof!"
        hacerRuido(gato);   // Output: "Miau!"
    }
}

```

**Explicación:**
 1. Clase Animal: 
		Primero se crea una clase llamada *Animal*, esta solo contiene un método o acción, esta es **hacerSonido()**, como se puede observar, antes tiene escrito las palabras *public void*. 
			**Public:** Es un modificador que especifica quién tiene acceso a este método, el modificador **public** permite que el método *hacerSonido()* sea accesible desde cualquier parte del programa.
			**Void:** Ya lo conocemos bien desde el lenguaje C, este funciona para especificar el tipo de retorno de la función, el caso de Void es que nunca devolverá algo o ningún valor, solo se ejecutará pero no será necesario regresar ningún valor de esta.
		Como se puede ver el método **public void hacerSonido()** está declarado, pero no implementado, es decir, existe pero no se dice realmente qué hace esa acción, esta abierto a que se defina, es un método vacío, no implementado. 
		
2. Clase Perro: 
		Tiene escrito **class Perro extends Animal**, esta sintaxis funciona para lo siguiente:
		
	**class Perro** especifica que se esta creando una clase llamada Perro, la parte extends es la que hace que la clase Perro se vuelva una clase heredada de **Animal**.
	
	Por lo tanto se trata de la declaración de una nueva clase llamada **Perro** que es heredada de Animal por medio de la palabra **extends**, esto significa que heredará sus variables (atributos o propiedades) y métodos (acciones) pero como se trata de una nueva clase tendrá la capacidad de agregar sus propios miembros y o métodos adicionales.
	
	**@Override**: Es notación que en Java se utiliza para indicar que un método de la subclase va a reescribir o remplazar un método de la super clase de la que es hija. Es importante recalcar que esto solo es anotación pero no es obligatoria, esto solo hace que el compilador y el programador pueda entender que el método de la subclase esta diseñado para remplazar uno de la super clase.
	
	**Public void hacerSonido()**: Se esta declarando un método con el modificador publico, esto significa que este método podrá ser accesible desde cualquier parte de código, es decir:
	- Desde la clase misma: Se podrá acceder al método desde la misma clase que en este caso es Perro.
	- Desde un objeto de la clase: Se podrá acceder al método desde cualquier objeto de la clase Perro, incluso si el objeto es creado en otra clase.
	- Desde alguna clase heredada: Se podrá acceder al método si se es una clase heredada, ya que hereda todos los atributos de la clase padre, si es que son públicos.
	Ya explicamos que *Void* solo especifica que el método no retornara ningún valor.

  **System.out.println("Woof!");**: Esto es lo que se encuentra dentro de la función **Public void hacerSonido()**, lo que realiza esta linea es imprimir o mostrar en consola lo que se encuentra dentro de las comillas, en este caso se imprimirá *Woof!*. System.out.print imprimiría el contenido dentro de las comillas, pero como en este caso se le agrego *ln* a print hará que se salte una línea, solo es para un formato más legible en la salida de la consola. 

  Es importante recordar que **hacerSonido()** es un método heredado desde *Animal* que solo se encontraba declarado pero no implementado (No hacia nada), pero al reescribirlo en Perro ahora si esta implementado e imprimirá *Woof!* en la consola.

3. **Clase Gato**: 
	Esta realizará exactamente lo mismo que la clase **Perro**, será una clase heredada de Animal gracias al siguiente fragmento de código: 
```Java
	class Gato extends Animal
```
También reescribirá el método **hacerSonido()** y esto lo sabemos gracias a que esta escrito arriba el @Override además de que sabemos que es posible ya que Gato es una clase heredada de Animal.
Al momento de reescribir el método **hacerSonido()**, lo implementa de manera que muestre un mensaje en la consola **Miau!** y esto lo hará a través de:
```Java
Sistem.out.println("Miau!");
```

4. **Clase Main**:
	Esta es la clase principal que será la que haga uso de las clases y será la que las mandará a llamar.
	Es declarada de manera Public, esto se hace ya que al momento de ejecutar el método siempre busca un método: 
	```Java
	public static void main(String[] args)
	```
	Este método será el que haga que inicie la ejecución de programa. Siempre es esta y después se explicará, pero al ser este método el que es necesario para la ejecución del programa debe ser sencillo de encontrar para la maquina Virtual de Java, por esto se hace a la clase principal "main" publica, facilita a la maquina virtual encontrar el método main para comenzar con la ejecución. 

  **public static void hacerRuido(Animal animal):**
	  El método se declara público para sea accesible para cualquier parte del código, se declara static para que pertenezca a la misma clase, en este caso main, esto significa que se podrá ejecutar el método directamente sin la necesidad de que se ejecute desde un objeto de la clase, en este caso main. 
	  Sino fuera **static** primero sería necesario crear un objeto de la clase main y a partir de este llamar al método **hacerRuido(Animal animal)**. 
	  Los parámetros de **hacerRuido** son *(Animal animal)*, es decir espera un objeto de la clase Animal y este será llamado dentro de la función como **animal**.

 **animal.hacerSonido();**: 
	 Se llama al método *hacerSonido()* desde el objeto animal, esta llamada puede variar a partir de varias cosas, si lo que se pasa como animal es una instancia directa de Animal sabemos que no hará nada porque el método **hacerSonido()** en la clase Animal no esta instanciado. 
	 Si se llama al método *hacerSonido()* desde el objeto animal que es un objeto de la clase Perro en este caso, este método imprimirá **Woof!**, ya que esto fue lo que instanciamos en esta clase.
	 Si se llama al método 