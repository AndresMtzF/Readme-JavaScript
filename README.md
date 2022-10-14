# JavaScript

	* No permite lectura ni escritura del lado del servidor, porque es un lenguaje del lado del cliente
	* No puede ser utilizado para aplicaciones de red por si solo
	* No tiene capacidad multihilo o múltiples procesos simultáneos

## console.log
```js
console.log();
console.warn();
console.error();
console.info;
```

![Tipos de ConsoleLog](./images/Pasted image 20220906192417.png)


## Salida de cadenas y datos

```js
console.log(`Salida de datos (cadenas):  
            Dato Curiso  
            A toturial introduction to the programming language B  
            Por el autor Brian Kernigham  
            Fue donde se introdujo la oracion Hello Word, para ejemplificar la  
            salida de datos\n\n`)
```

Para la salida de datos tipo cade usamos " ", ' ' y plantillas ` `

## Tipo de datos

	* string: cadena de caracteres -> 'a' 'hola, mundo' '123'
	* boolean: true / false
	* null: variable vacia, no contiene datos
	* number: valores 
	* undefined: no definido
	* object: objeto

## Variables

Lenguaje débilmente tipado, no se asigna un tipo de dato, su tipo de dato es definido por el tipo de dato asignado.

	* Declarar variable: var (forma antigua de definir), let, const
		* Mutabilidad: cuando cambia de valor una variable o reasignar valor de una variable
		* Tienen escritura dinamica, las variables puede cambiar su tipo de dato
		* Variables anonimas se definen en el momento en que se utilizan
```js
let miPrimerVariable = 'Mi primer varaible';
	miPrimerVariable = 'Nuevo contenido';
let miBoolean = true;
let miOtroBoolean = false;
```

Para saber que tipo de dato es una variable, utilizamos `typeof`

```JavaScript
let miNumero = 1
typeof(miNumero)
```

Salida:

<code>'number'</code>

## Incrementos

`let x = 1`

Pre-incremento `let y = ++x` salida:  <code>2</code>

En el post incremente primero se realizar la igualación y luego se incrementa. 

Post-incremento `let y = x++` salida <code>2</code>

Funcionan los incrementos también con los decrementos.

## Operadores de igualdad 

```JavaScript
true === true //true
true === false //false
true !== false //false
false !== false //false
```

El uso de tres iguales comprobamos el valor, así como el tipo

```JavaScript
3 === 3 //true
3 == "3" //true
```

## Condicionales

Y otros temas como condicionales
	Sentencia if / if-else
	Sentencia switch

## Funciones

Sintaxis de una función:

```js
	function nombreFuncion(párametros){
		//bloque de codigo a ejecutar	
	}

	//invocar una función
	nombreFuncion(argumentos);
```

	*Las funciones incluso pueden ser mandadas a llamar o invocadas antes de su definición.
	*Todas las funciones regresan un valor. 
	*Una función puede recibir como parametros variables primitivas, objetos y funciones
	*Realizan una tarea en concreta de manera testeable.
