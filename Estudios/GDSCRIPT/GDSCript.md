

GDSCRIPT ES UN LENGUAJE dinámico  y al ser este tipo permite que se muy fácil de aprender de captar como funciona el entorno de este lenguaje que es muy parecido a Python . Fue creado especialmente para Godot un motor grafico para poder crear principalmente juegos .

# GDSCRIPT `reference` 

# variables

se declaran con  `var`  y luego el nombre de la variable 

aunque la variable puede tener cualquier tipo de dato , se puede capar esta variable a uno usando el 
: o doble punto , luego mencionas el tipo de variable que quiere que sea capada

# variable estáticas

Son variables que te permiten que no tendrán demasiadas restricciones , normalmente se les puede acceder desde que cualquier lado.

Unos de los usos que le dan quizá puede ser en el numero de jugadores . No importa si la declaras en la clase base como atributo ,  la clases hijas podrán acceder a ella 

#  `@static_unload` anotación

Sirve para vaciar las variables estaticas claro , sabiendo de que esas variables que mencionas no contiene ningun valor importante 

# casting

Se podrá castear valores  siempre y cuando cumpla similitudes con la variable a la que se quiere castear 

**ejemplo**

No podría castear un VECTOR a INT , tiene que ser un tipo de dato similar .

# Constants

Son valores globales que no van a cambiar con el tiempo 

se les puede asignar o forzar a solo tener un tipo de dato 
# Enum

Es una forma de agregar valores consecutivos algunas constantes o variables 

```
enum {TILE_BRICK, TILE_FLOOR, TILE_SPIKE, TILE_TELEPORT}

# Is the same as:
const TILE_BRICK = 0
const TILE_FLOOR = 1
const TILE_SPIKE = 2
const TILE_TELEPORT = 3

```


# Funciones

Por defecto la funcion no te pedira ningun retorno de valor pero si la forzas a ser un tipo de dato si lo hara ,  en lo parametros de la funcion igual puedes forzar tipo de dato , puedes declarar por defecto algunas variables en el parametro .
y si la funcion es un `void ` no puede retornar algun valor



# lamda funciones


# Funciones estaticas




# Enlaces

DONDE SE SCA LA INFO
[documento de godot](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html)