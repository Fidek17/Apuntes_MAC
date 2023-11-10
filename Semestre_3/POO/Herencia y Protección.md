
### 1. Herencia 
Es un concepto que permite la creación de clases nuevas basadas a partir de clases existentes y failita la reutilizacion de codigo. 

### 2. Tipos de clases
- Clase Base:
	Proporciona la estructura y comportamiento base que heredan las clases de este.
- Clase Derivada
- Clase Abstracta: Una clase que no puede ser instanciada por si misma, funciona como una plantilla para otras clases y generalmente contiene uno o más métodos abstractos que deben ser implementados por las subclases. 
- Clase Final: Una clase que no puede tener clases derivadas de si 
- Clase Mixim 
- Clase concreta: Es una clase que se
- Clase intermedia: Se utilizan clases intermedias para organizar y dividir la funcionalidad entre las clases base y las clases hijas

### 3. Principio de Menor Privilegio 
El objetivo principal del principio de menor privilegio es minimizar los riesgos de seguridad y reducir la superficie de ataque de un sistema funcione cuando se le otorgan a los usuarios y procesos únicamente los privilegios necesarios para llevar a cabo sus funciones. 

**Aplicado en POO**
En este contexto lo aplicamos controlando el alcance de los miembros (métodos y propiedades) de una clase determinando su visibilidad. 
- Evitar hacer herencia innecesaria

### Herencia en términos de visibilidad
- Herencia Pública
- Herencia Protegida
- Herencia Privada

### Tipos de Herencia por Niveles
1. Simple: Tiene lugar cuando una clase hija hereda los atributos y métodos de solo una clase padre. 
2. Multinivel: Se produce cuando una clase hija hereda a una padre pero a su vez esta se convierte en una clase padre. 
3. Múltiple: hace referencia a que una clase puede heredar caracteristicas de más de una clase. 
	1. Java no permite herencia múltiple: 
		1. Evitar ambigüedad de código.
		2. Problema del diamante
			1. Como resolverlo: Interfaces 
4. Herencia Jerárquica: Una super clase y varias clases heredan de esta super clase. 
5. Herencia Hibrida: Es una mezcal de dos o más tipos de herencia anteriores y es necesario usar interfaces para que pueda funcionar. 


