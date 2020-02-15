<h1 align="center">Entendiendo ES6</h1>

<img width=100% src="https://i.imgur.com/2Azquj5.jpg">

# Promesa
Me resuelve cuando un proceso ya esta listo o ya termino. 

```
doLogin()
.then((rta) => {
    console.log(rta);
})
.then((rta) => {
    console.log(rta);
})
.catch((error) => {
    console.log(error);
})
```
 El catch captura el error de la primera y segunda promesa.

 # Scope
 + let: variable de scope local.
 + const: 
 - definir constantes en mayúsculas (ejemplo: PI).
 - llaves de acceso a REST. 
 - URLs.

 # Arrow Function

```
 let numbers = [1, 2, 3, 4];
 numbers.map(item => item * 2); // arrow function de una línea.
// devuelve [2, 4, 6, 8].
```

```
let result = persons.map(person => {
    person.age = 2;
    return person;
});
console.log(result);
```
Resultado:
```
Array[2]
0: Person
    age: 2
1: Person
    age: 2
```

 # Clases
 ```
 class Person {
     name;
     age;

     constructor(name, age){
         this.name = name;
         this.age = age;
     }

     getName(){
         return this.name;
     }
 }
 ```

 Antes:
 ```
 // Declaración
 function doSomething(onDone){
     onDone();
 }

 doSomething(function (rta)){
     console.log(rta);
 }
 ```

 Ahora:
 ```
 doLogin()
 .then((rta) => {
     console.log(rta);
 });
 ```

 # Modificadores de acceso

 + private: solo la clase donde se crea tiene acceso.
 + public: cualquier clase tiene acceso.
 + protected: pública solo para las clases heredadas de esta.
 Ejemplo:
 ```
 class hijo extends Person {
     ...
 }
 ```
 El protected será público para esta clase porque es herencia de Person.

 # Decoradores

Indican a TS como manejar clases.

 @Injectable: Providers o servicios para usar en nuestros componentes.
 @Pipe: 
 + tubería: entra algo y sale transformación.
 + transformación de datos.
 + pasar valor o mayúscula.
 + dar formato a fecha.

 Existen pipes por defecto en Angular.
 + date
 + etc.

 @Directive: 
 + modifica el comportamiento de elementos.

 # Typescript

 + Transpilador.

archivo `declaration.d.ts`: Se recomienda comentar `declare module '*'`
+ Buena práctica.
+ Ayuda a reconocer errores.

# Funciones con parámetros opcionales
```
doSomething(a: number, b: number = 0){ // b: parámetro con valor por defecto
    return a + b;
}

// Tipos de ejecución
this.doSomething(3);
this.doSomething(3, 2);
```

# Arrays


Ejemplo 1: 
```
let numbers: number[] = [];
```
Insertar en array.
+ En este caso solo se pueden insertar valores de tipo number.
```
numbers.push(3);
```
---
Ejemplo 2:

```
import { Person } from './person';
let persons: Person[] = [];
let nicolas: Person = new Person('Nicolás', 22);
```

Insertar en array.
+ En este caso solo se pueden insertar valores de tipo Person.

```
persons.push(nicolas);
```
