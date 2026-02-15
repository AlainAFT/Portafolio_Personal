Link donde saque la info https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_advanced.html
# [[GDSCript]]

# [[GODOT]]

#  Variables & assignment
## ¿==Diferencia entre lenguaje estático y dinámico==?

normalmente el dinámico permiten muchas mas cosas que el otro , es como que te da mas libertad para que solo te concentres en desarrollar la lógica  básicamente en cambio el estático es mas manual donde vos sos como el admin que tiene el control de cada funcionamiento y te encargaras del proceso de gestiones de memoria.

==EJEMPLO:== 

En los lenguajes dinámicos una variable puede ser todas a la vez  y se define cada vez que su valor cambio a otro tipo de dato.

```
Static:

int a; // Value uninitialized.
a = 5; // This is valid.
a = "Hi!"; // This is invalid.

Dynamic: GDSCRIPT

var a # 'null' by default.
a = 5 # Valid, 'a' becomes an integer.
a = "Hi!" # Valid, 'a' changed to a string.

```


## As function arguments
Lo mismo pasa con las funciones : pueden devolver cualquier valor y vos lo decides y en cambio en los estáticos esta restringido al tipo de dato que colocaste al declarar la función.

```
Static:

void print_value(int value) {

	printf("value is %i\n", value);
}

[..]

print_value(55); // Valid.
print_value("Hello"); // Invalid.

Dynamic:

func print_value(value):
	print(value)

[..]

print_value(55) # Valid.
print_value("Hello") # Valid.
```




## Punteros

aquí en el lenguaje GDSCRIPT y la mayoría de lenguajes dinámicos suelen hacer que los punteros se eliminan de la memoria cuando se deja de usar el puntero , el lenguaje mismo te ayuda a liberarlo de la memoria asi que no debes preocuparte por desbordamiento de memoria .

```
func use_class(instance): # Does not care about class type
	instance.use() # Will work with any class that has a ".use()" method.

func do_something():
	var instance = SomeClass.new() # Created as reference.
	use_class(instance) # Passed as reference.
	    # Will be unreferenced and deleted.
```


## ARRAYS

los arrays en los lenguajes dinamicos suelen poder conter diferente tipo de datos dentro de ellos y puede ser como un vector que se le puede cambiar el tamaño del array en cualquier momento del codigo.

==ejemplo==:

```

var array = [10, "hello", 40, 60] # You can mix types.
array.resize(3) # Can be resized.
use_array(array) # Passed as reference.
# Freed when no longer in use.

```
otro ejemplo

```
var a = 20
if a in [10, 20, 30]:
	print("We have a winner!")
```



## Diccionarios

Estos son una herramienta poderosa para poder guardar llaves y valores util para diferentes casos si lo sabes usar y reconocer cuando usar.  Esta herramiente puede mapear cualquier valor con otro valor sin importar el tipo de dato que se use  , lo puedes usar como llave o valor a guardar .

son eficientes con la implementacion de las 

[[Tablas hashes]]

Ejemplos : del uso de Diccionarios 

```
var d = {"name": "John", "age": 22}
print("Name: ", d["name"], " Age: ", d["age"])

-------------------------------------------------
son dinamicos asi que puedes realizar cualquier cambio en cualquier momento con poco costo.

d["mother"] = "Rebecca" # Addition.
d["age"] = 11 # Modification.
d.erase("name") # Removal.

```

tiene diferentes formas de usarlo , tambien puedes usar con corchetes "[ ]" o con un punto y luego mencionando el nombre 

```
# Same example, lua-style support.
# This syntax is a lot more readable and usable.
# Like any GDScript identifier, keys written in this form cannot start
# with a digit.

var d = {
	name = "John",
	age = 22
}

print("Name: ", d.name, " Age: ", d.age) # Used "." based indexing.

# Indexing

d["mother"] = "Rebecca"
d.mother = "Caroline" # This would work too to create a new key.
```



# BUCLES

## For and WHILE

estos dos tipos de bucles se usan de manera similar asi que no habra demasiado cambio entre uno y otro.

algunos ejemplos de bucles

se puede iterar sin indices .

```
for s in strings:
	print(s)
	
	
------------------------
for key in dict:
	print(key, " -> ", dict[key])
	
```

iteracion con indices


```
for i in range(strings.size()):
	print(strings[i])
```

el range o rango puede agarrar 3 argumentos .

```
range(n) 

# Will count from 0 to n in steps of 1. The parameter n is exclusive.

range(b, n) 

# Will count from b to n in steps of 1. The parameters b is inclusive. The parameter n is exclusive.

range(b, n, s) 

# Will count from b to n, in steps of s. The parameters b is inclusive. The parameter n is exclusive.

```

ejemplo para recorrer de reversa

```
for i in range(10, 0, -1):
	pass
```
## WHILE

```
var i = 0

while i < strings.size():
	print(strings[i])
	i += 1
```

## Iteradores personalizados

Lo usas cuando los iteradores normales no pueden satisfacer las necesidades que buscas 



Ejemplo:

```
class ForwardIterator:
	var start
	var current
	var end
	var increment

	func _init(start, stop, increment):
		self.start = start
		self.current = start
		self.end = stop
		self.increment = increment

	func should_continue():
		return (current < end)

	func _iter_init(arg):
		current = start
		return should_continue()

	func _iter_next(arg):
		current += increment
		return should_continue()

	func _iter_get(arg):
		return current
```

y su implementacion de este iterador personalizado

```
var itr = ForwardIterator.new(0, 6, 2)
for i in itr:
	print(i) # Will print 0, 2, and 4.
	
```

Make sure to reset the state of the iterator in `_iter_init`, otherwise nested for-loops that use custom iterators will not work as expected.



## DUCK TYPING

Que es  [[DUCK TYPING]]

Este concepto suele estar muy conectado con lenguajes dinamicos y esto ayuda que el codigo sea muy directo al escribir y mucho mas simple de implentar , pero no queda muy obvio como funciona.



