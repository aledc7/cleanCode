<img src="https://raw.githubusercontent.com/aledc7/cleanCode/master/resources/cleancode.png" height="100" width="100">

[![aledc.com](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.com)
[![ingenea.com.ar](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/ingenea.svg)](http://ingenea.com.ar)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)

# Clean Code

## Este Repositorio es un resumen del libro CleanCode.   



## Costo a nivel de recursos sobre un producto de Software

El coste total de un producto software viene dado por la suma de los costes de desarrollo y de mantenimiento, siendo este último mucho más elevado que el coste del propio desarrollo inicial. A su vez, el coste de mantenimiento viene dado por la suma de los costes de entender el código, cambiarlo, testearlo y desplegarlo.

## Variables y nombres

El buen código tiene que ser simple y directo, debería leerse con la misma facilidad que un texto bien escrito.  
También debería poder leerse con la misma facilidad con la que leemos un texto bien escrito, es por ello que escoger buenos nombres es fundamental.  
Los nombres de variables, métodos y clases deben seleccionarse con cuidado para que den expresividad y significado a nuestro código.

## Nombres Pronunciables y Expresivos
Los nombres, imprescindiblemente en inglés, deben ser pronunciables. Esto quiere decir que no deben ser abreviaturas ni llevar guion bajo o medio, priorizando el estilo camelCase. Por otro lado, se debe intentar no ahorrar caracteres en los nombres, la idea es que sean lo más expresivos posible.


## Evitar que los nombres contengan información técnica
Si se está construyendo un software de tipo vertical (orientado a negocio), se debe intentar que los nombres no contengan información técnica en ellos, es decir, evitar incluir información relacionada con la tecnología, como el tipo de dato o la notación, el tipo de clase, etc. Esto sí se admite en desarrollo de software horizontal o librerías de propósito general.

## Léxico Coherente
Se debe usar el mismo vocabulario para hacer referencia al mismo concepto, no se debe usar en algunos lados User, en otro Client y en otro Customer, a no ser que representen claramente conceptos diferentes.

## Usa el nombre adecuado según el tipo de Dato

### Arrays
Los arrays son una lista iterable de elementos, generalmente del mismo tipo. Es por ello que pluralizar el nombre de la variable es una buena idea:

### Ejemplo de arrays
```js
Los arrays son una lista iterable de elementos, generalmente del mismo tipo. Es por ello que pluralizar el nombre de la variable puede
//bad
constfruit=['manzana','platano','fresa'];
//regular
constfruitList=['manzana','platano','fresa'];
//good
constfruits=['manzana','platano','fresa'];
//better
constfruitNames=['manzana','platano','fresa'];
````

### Booleanos
Los Booleanos solo pueden tener 2 valores, Verdadero o Falso. Dado esto, el uso de prefijos como “is”, “has” y “can” ayudará inferir el tipo de variable, mejorando así la legibilidad del código.

Ejemplo 6: Booleanos
```js
//bad
constopen=true;
constwrite=true;
constfruit=true;

//good
constisOpen=true;
constcanWrite=true;
consthasFruit=true;
````

### Números
Para los números es bueno elegir palabras que describan números, como “min”, “max”, “total”:
```js
Ejemplo 7: Números
//bad
constfruits=3;

//better
constmaxFruits=5;
constminFruits=1;
consttotalFruits=3;
````

## Funciones
Los nombres de las funciones deben representar __Acciones__, por ello que deben construirse usando el verbo que representa la acción seguido de un sustantivo. Estos deben de ser descriptivos y, a su vez, concisos.   Esto quiere decir que el nombre de la función debe expresar lo que hace, pero también debe de abstraerse de la implementación de la función.


