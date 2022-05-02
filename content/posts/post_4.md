---
title: "Segunda semana aprendiendo Backend"
date: 2022-01-01
description: 'Recopilación de lo aprendido durante la segunda semana en la Mission Launch X'
---

# Hola  de nuevo 👋. 
El día de hoy haremos la recopilación del avance de lo que aprendí la semana 2 de esta mission. 

Los temas principales fueron: 
✨Contextos
✨Objetos en JS
✨Operadores
✨Clases y Objetos
✨Modularización de archivos
✨Pruebas Unitarias 

## 💫 Contextos. 
Los contextos, en programación y palabras simples, es aquel código que se encargan de encapsular comportamientos y que solo existen ahí. Es decir, si creamos una variable, un método, un objeto o lo que sea dentro del contexto, solo existirá ahi y en ningún otro lado. 
![Contextos](https://user-images.githubusercontent.com/84040594/166181724-e360d74e-7ba6-4505-ad79-85716bbd28c9.png)"Contextos")

¿Cómo se ve esto en un código? De la siguiente manera: 

- Esto es declarar las variables en un entorno global:
    ``` console
    let a = `JavaScript`
    let b = 10 
    ```

- Aqui las declaramos dentro de un contexto (función, en este caso). Las mismas variables solo estaran disponibles si mandamos a llamar a la función
  ``` console
  function my_function_to_show_scopes () {
      if (true) {
          let a = `Elixir`
          let b = 999 
          console.log (a, b) 
      }
  }
  ```

Al mandar a imprimir __console.log (a, b)__ nos imprime lo siguiente: 
  ``` console
  JavaScript 10
  ```

Pero si ejecutamos la función __my_function_to_show_scopes()__ imprime: 
  ``` console
  Elixir 999
  ```

Así funcionan los contextos, solo funcionan si mandamos a llamar la parte del código. 



## 💫 Objetos en JS
Los objetos son un conjunto de valores key-value y son usados para diseñar y modelar información para así transformarla. Pueden guardar funciones, métodos, listas y más objetos (objetos anidados).

Para definir un objeto se usan las llaves _{}_
```console
  const myObject2 = {
      name: "Joss" ,
      age: 23
}
```
Al impirmir se tiene que llamar al objeto y su propiedad: 

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
, 


  ```console
  { name: 'Joss', age: 23 }
  ```
Podemos tener infinidad de uso con los objetos, podemos tener objetos con métodos(tienen funciones dentro de un objeto), con listas, entre más.

> Recuerda: Para llamar un objeto en un método y usarlo debemos hacer uso de _this_ . _propiedad_

## 💫 Operadores
Los operadores nos ayudaran a manipular los datos que tenemos de una forma más sencilla. Algunos son:
  - For Each: 
  - Map
  - Filter
  - Reduce
  - Find
  - FindIndex
  - Some 
  - Sort

## 💫 Clases y Objetos

## 💫 Modularización de archivos

## 💫 Pruebas Unitarias

```console

```
