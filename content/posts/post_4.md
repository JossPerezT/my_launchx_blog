---
title: "Segunda semana aprendiendo Backend"
date: 2022-05-01
description: 'Recopilación de lo aprendido durante la segunda semana en la Mission Launch X'
---

# Hola  de nuevo 👋. 
El día de hoy haremos la recopilación del avance de lo que aprendí la semana 2 de esta mission. 

Los temas principales fueron: 
- ✨Contextos
- ✨Objetos en JS
- ✨Operadores
- ✨Clases y Objetos
- ✨Modularización de archivos
- ✨Pruebas Unitarias 

## 💫 Contextos. 
Los contextos, en programación y palabras simples, es aquel código que se encargan de encapsular comportamientos y que solo existen ahí. Es decir, si creamos una variable, un método, un objeto o lo que sea dentro del contexto, solo existirá ahi y en ningún otro lado. 

![Contextos](https://user-images.githubusercontent.com/84040594/166181724-e360d74e-7ba6-4505-ad79-85716bbd28c9.png)"Contextos")

¿Cómo se ve esto en un código? De la siguiente manera: 

- 💥 Así se declaran las variables en un entorno global:
    ``` console
    let a = `JavaScript`
    let b = 10 
    ```

- 💥 Aqui las declaramos dentro de un contexto (función, en este caso). Las mismas variables solo estaran disponibles si mandamos a llamar a la función
  ``` console
  function my_function_to_show_scopes () {
      if (true) {
          let a = `Elixir`
          let b = 999 
          console.log (a, b) 
      }
  }
  ```

- 💥Al mandar a imprimir __console.log (a, b)__ nos imprime lo siguiente: 
      ``` console
      JavaScript 10
      ```

- 💥Pero si ejecutamos la función __my_function_to_show_scopes()__ imprime: 
      ``` console
      Elixir 999
      ```

> Así funcionan los contextos, solo funcionan si mandamos a llamar la parte del código. 



## 💫 Objetos en JS
Los objetos son un conjunto de valores key-value y son usados para diseñar y modelar información para así transformarla. Pueden guardar funciones, métodos, listas y más objetos (objetos anidados).

- 💥 Para definir un objeto se usan las llaves _{}_
    ```console
      const myObject2 = {
          name: "Joss" ,
          age: 23
    }
    ```
- 💥 Al impirmir se tiene que llamar al objeto y su propiedad: 

      ```console
      // (objeto)
      console.log (myObject2)
        { name: 'Joss', age: 23 }
      ```

      ```console
      // (objeto.propiedad)
      console.log (myObject2.name)
        Joss
      ```

      ```console
      // (objeto["propiedad"])
      console.log (myObject2["age"])
        23
      ```

Podemos tener infinidad de uso con los objetos, podemos tener objetos con métodos(tienen funciones dentro de un objeto), con listas, entre más.

> Recuerda: Para llamar un objeto en un método y usarlo debemos hacer uso de _this_ . _propiedad_

## 💫 Operadores
Los operadores nos ayudaran a manipular los datos que tenemos de una forma más sencilla. Algunos son:
  - 💥For Each: recorre una lista de elementos y ejecuta la función por cada uno. 
  - 💥Map: Crea una nueva lista a partir de un recorrido de una función. 
  - 💥Filter: Similar a map, crea una nueva lista de los elementos que cumplan con la función. 
  - 💥Reduce: Funciona como un acumulador (acc). Es una función reductoea sobre una lista y regresa un valor único. 
  - 💥Find: Busca y regresa el primer elemento que cumpla con la función. 
  - 💥FindIndex: Busca y regresa el índice del primer elemento que cumpla con la función. Si no lo cumple devuelve -1
  - 💥Some: Busca y determina si __al menos un elemento__ cumple con la función. 
  - 💥Every: Busca y determina si __TODOS__ los elementos cumplen con la función.
  - 💥Sort: Ordena los elementos. 
  - 💥Includes: Determina si alguna letra, frase, palabra, etc. se encuentra en un elemento.

> Recuerda: Una lista es un array en programación. 

## 💫 Clases y Objetos
Las clases son "funciones especiales". Son una especie de plantilla para encapsular objetos y poder trabajar con esa información. 

- 💥Para definirlas se requiere el siguente código:
    ```console
    class nameClass {

    }
    ```
- 💥Los objetos se pueden instanciar de una clase por medio de un constructor, 
    ```console
        class Student { // Creación de la clase
            constructor (name, age, subjects){ // Se definen los atributos que los objetos tendran por medio de un contructor.
                this.name = name // Se define a que atributo nos referimos.
                this.age = age 
                this.subjects = subjects 
            }
        }
    ```
    - 💢Instanciar un nuevo objeto: 
        ```console
        const jossStudent = new Student ("Joss", 23, ["NodeJS, Python"]) // Se crea una variable, se usa _new nombreClase_ para refrerirnos a la clase y se le agregan los atributos correspondientes.
        ```
        
- 💥Getters: Es un método que obtiene el valor de una propiedad 
- 💥Setters: Método que asigna y actualiza la información de una propiedad. 
- 💥Métodos estáticos: nos permiten escribir métodos en una clase sin tener que instanciar un objeto.
- 💥Herencia: Nos permite usar las clases entre ellas y usar sus componentes. Una clase hija puede usar los mismos componentes de la clase padre y agregar más. 

> Mi definición de __instanciar__: Es la manera de crear un nuevo objeto derivado de una clase. 

## 💫 Modularización de archivos
La modularización de archivo se refiere a la forma de organizar nuestros proyectos y códigos. La modularización nos sirve para fraccionar nuestro código en módulos para que sea más entendible y fácil de leer, importando y exportando los módulos. 
> El software por naturaleza tiende a ser complejo. 

## 💫 Pruebas Unitarias
- 💥Las pruebas unitarias son muy importantes para nuestros proyectos. Nos ayudan a determinar si nuestro código cumple con los requerimientos necesarios, además de que nos avisan si existe algún error o falla durante su comportamiento. 
- 💥Hacer pruebas es difícil, pero son necesarias para el buen funcionamiento y optimización del proyecto. 

> Nunca confies en una prueba que no veas fallar. 


## Más recursos
💥 [Developer Mozzilla](https://developer.mozilla.org/es/docs/Web/JavaScript/)


# LISTO!!
Terminamos la recopilación de la semana 2. 

Espero que este post les sea de ayuda para entender un poco más de los temas desde mi punto de vista, experiencia y entendimiento. 

Si en algún concepto tengo la idea errónea házmelo saber para corregirla. 

Gracias por leer 📖
