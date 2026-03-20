

# para agarrar errores

 **definición**

>  Son herramientas que nos sirven para poder agarrar errores , esto nos permite que el programa siga ejecutando el codigo a pesar de que halla saltado un error 



---

Son muy parecidos a las herramientas que se usan en [[SQL Server]] que tienen los mismos nombres 
de `try , catch "y" throw`.
## try  and  catch

Sirve para cuando tu codigo pueda tener riesgo de que halla un error que haga que pare de ejecutarse el programa

```
try {
  throw "myException"; // generates an exception
} catch (err) {
  // statements to handle any exceptions
  logMyErrors(err); // pass exception object to error handler
}
```

## throw

Sirve para lanzar errores o mensajes de errores

```
throw "Error2"; // String type
throw 42; // Number type
throw true; // Boolean type
throw {
  toString() {
    return "I'm an object!";
  },
};
```

## finally 

Una sentencia que se ejecuta si o si ,  ya sea si hubo error o no hubo.
```
openMyFile();
try {
  writeMyFile(theData); // This may throw an error
} catch (e) {
  handleError(e); // If an error occurred, handle it
} finally {
  closeMyFile(); // Always close the resource
}
```

# Bucles y Iteraciones

## Declaracion `For`

 ==Es un ciclo que se repite mientras una condición se cumple , se maneja a través de iteraciones. El bucle es muy similar a [[C]] o [[Java]]==


**Estructura**
```
for ([expresiónInicial]; [expresiónCondicional]; [expresiónDeActualización])
  instrucción
```

## declaracion `Do..While`

==Un `Do .. While`  se repite hasta que la condición se falsa==

Muy similar al [[#Declaracion `For`]] pero con la diferencia de que al menos se ejecutara una vez en el `Do..While`

```
do
  expresión
while (condición);
```

## Declaracion `While`

==Las diferencias entre [[#declaracion `Do..While`]]  y [[#Declaracion `While`]] son que el `While` si ejecuta primero la condición y luego ejecuta las instrucciones.==

```
while (condición)
  expresión
```

*Ten cuidado con la condición, por lo menos debe cumplirse una vez que no es verdadero *

## Declaracion `Break`
==Nos sirve para poder terminar un bucle o una estructura de control de flujo ==. [[#Declaracion `For`]][[#declaracion `Do..While`]][[#Declaracion `While`]]
*Puedes usar dos formatos de `break` , el sin `label` o con `label` *
```
break;
break [label];
```

*Para crear un `label` se hace lo siguiente*

```
// mencionas primero el nombre de la etiqueta
//  y luego ':' , para seguir con el bucle
labelCancelLoops: while (true)
```

## Declaracion `Continue`

==Nos sirve para salatarnos una iteracion de un bucle== [[#Declaracion `For`]][[#declaracion `Do..While`]][[#Declaracion `While`]]

```
continue [label];
```

## Declaracion `For in`

==Nos permite recorrer sin indices hasta el final de todas la propiedades de un objeto==

funciona con arrays y objetos
nos devuelve los índices, posiciones que puedes ocupar para sacar los valores que contiene el objeto.

```
for (variable in objeto)
  instrucción
```

## declaracion `For of`

==Nos devuelve valores directamente sin necesidad de índices
solo funciona con `int , strings , vectores , arrays y maps,sets` ==

*solo puede moverse por cosas que son iterables*

```
// estructura
for (variable of objeto)
  expresión
  
  // diferencia entre for of y  for in
  
  const arr = [3, 5, 7];
arr.foo = "hola";

for (let i in arr) {
  console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
  console.log(i); // logs 3, 5, 7
}
```

# Funciones

==Una función son instrucciones donde tendra entradas y salidas , y estas tendran alguna relacion entre ellas==

## definir funciones


