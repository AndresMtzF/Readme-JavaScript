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

![[Pasted image 20220906192417.png]]


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

### Objetos

```js
const miPrimerObjeto = {//propiedades 
}; //objeto vacio: colección de tipos de datos primirtivos o de objetos.

const segundoObjeto = {
	numero: 10, 
	texto: 'Nuevo Texto', //Buena Práctica agregar una coma al final
	objetioHijo: {
			
		}
};

//se puede acceder a datos concretos de un objeto:
console.log(miPrimerObjeto.numero);
```

Cuando un objeto es creado asigna un valor apuntando a un lugar en memoria, pero si se crea una nueva variable que se iguale a un objeto, está apuntará al mismo espacio en memoria.
Entonces un cambio en cualquiera de los dos objetos son afectados simultáneamente, o su lugar de memoria

```js
const a = {

    nombre: 'Sergio'

};

const b = a;

console.log(a);
console.log(b);

a.nombre = 'Perez'

console.log(a);
console.log(b);

b.nombre = 'Checo' 

console.log(a);
console.log(b);
```

Salida: ![[Pasted image 20220906204410.png]]
## Notación de Punto

```js
let persona = {
    nombre: 'Andres',
    apellido: 'Martinez',
    edad: 25,
    direccion: {
        pais: 'México',
        ciudad: 'CDMX',
        edificio: {
            nombre: 'Principal',
            telefono: '55 55112233'
        }
    }
};
```
Teniendo la creación del objeto anterior, cuando deseemos agregar una propiedad puede ser más practico agregarlo de esta manera, en lugar de modificar la estructura del objeto. Por ejemplo, si queremos agregar un propiedad de 'zipcode' al objeto anidado de dirección:

```js
	persona.direccion.zipcode = 45505;
```

y este se agregara y aparecerá si lo imprimimos en pantalla o hacemos uso de él.

Tal vez en algún punto las propiedades anidadas sean demasiadas que puede ser muy complicado escribir la notación de punto completa. Para acceder a una propiedad anidada en un nivel muy abajo podemos hacer esto:

```js
	let edificio = persona.direccion.edificio;
	edificio.nopiso = '8vo piso';
```

Salida: ![[Pasted image 20220906213037.png]]
## Notación de Corchetes

Es posible que se requiera un campo en especifico, como en un formulario, obtener el valor de un campo, es posible hacer esto más sencillo con la notación de corchetes, siguiendo con el ejemplo de persona:

```js

	console.log(persona['nombre'])
	// salida esperada: Andres

	console.log(persona['dirección']['pais']);
	// salida esperada: México

	let campo = 'edad';

	console.log = (persona[campo])
	// salida esperada: 25
```

Salida: ![[Pasted image 20220907003435.png]]
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

# Métodos de Arreglos

## Push

La formar facil dé anexar datos al final de un arreglo es con la función `push()`
`.push()` puede tomar uno o más parámetros y agregarlos al final de un array.

Ejemplo 

```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

`arr1` ahora tiene el valor dé `[1, 2, 3, 4]` y `arr2` tiene el valor dé `["Stimpson", "J", "cat", ["happy", "joy"]]`

## Pop

Otra forma de modificar los datos de un array es con la función `.pop()` 
`.pop()` es usada para eliminar el ultimo elemento de un arreglo, Podemos almacenar este elemento en un variable. `.pop()` remueve el ultimo elemento de un array y retorna ese elemento.

Cualquier tipo de dato puede ser eliminado de un array, números, cadenas e incluso arrays anidados.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```

El primer `console.log` desplegará `6` y el segundo desplegará `[1, 4]` .

## Shift 

`.shift()` funciona como `.pop()`, con la diferencia de que se elimina el primer elemento.

```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```

`removedFromOurArray` tendría que tener el valor del String `Stimpson` y `ourArray` deberá tener `["J", ["cat"]]`.

## Unshift

`.unshift()` trabaja exactamente como `.push()`, pero en lugar de agregar un elemento al final de un array, `.unshift()` agrega un elemento al inicio del array.

```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy")
```
