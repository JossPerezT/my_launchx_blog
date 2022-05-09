---
title: "Tercera semana aprendiendo Backend"
date: 2022-05-09
description: 'Recopilación de lo aprendido durante la tercera semana en la Mission Launch X'
---

# Hola 👋. 
El día de hoy haremos la recopilación del avance de lo que se aprendió en la semana 3 de esta mission. 

Temas principales: 

💫 Creación de proyectos de JS

💫 TDD para diseño de software

💫 Express JS como framework para crear servers


## 💫 Creación de proyectos de JS. 
Para la creación de un proyecto es necesario organizar sus archivos en carpetas, instalar dependencias y versionamiento. 

### ✨ Versionamiento 
Recordemos que un buen proyeto necesita versionarse, aquí usmos git y para crear un nuevo proyecto desde cero y versionarlo necesitamos usar los siguientes comandos: 

#### 🎇 Creación de una carpeta nueva en nuestro equipo. 
![Nueva Carpeta](https://user-images.githubusercontent.com/84040594/167332066-55e2e2f8-725c-4931-aee7-797cbd685996.png "Nueva Carpeta")

#### 🎇Creación de un repositorio local. 
1. Iniciamos un repositorio local con el comando 
```Console
git init
```
![repoLocal](https://user-images.githubusercontent.com/84040594/167332169-42c0917d-d459-4ad1-97b1-b7f8e7798d0d.png "repoLocal")

Como observamos, una vez que se crea el repo local se refleja el mensaje de "_master_" haciendo referencia a la rama en la que se esta trabajando.

![rama](https://user-images.githubusercontent.com/84040594/167332384-a80ff5dd-150e-42da-af31-d799d1dc3ff6.png "rama")

2. Creamos un archivo para comenzar a versionar. En este ejemplo usamos un 'readme.md'
![readme.md](https://user-images.githubusercontent.com/84040594/167333386-b78ed7b0-bb31-4dde-ae2c-5d28532a2374.png "readme.md")

3. Agregamos nuestro archivo al Stage Area en git con el comando 
```Console
git add
```
![git add](https://user-images.githubusercontent.com/84040594/167334295-5d020f7e-8cbc-475d-a66b-a67a9ea7ad94.png "git add")
4. Y mandamos nuestro archivo al repo con 
```Console
git commit -m "<mensaje>"
```
![git commit](https://user-images.githubusercontent.com/84040594/167334445-c282401b-c725-4c25-b254-1c00e6f0065e.png "git commit")
5. Listo. Tenemor un repositorio local.

#### 🎇 Creación de un repositorio remoto. 
Ya tenemos creado nuestro repositorio local, ahora lo vamos a enlazar con uno remoto con GitHub.

1. Creamos un repositorio remoto en GitHub. Le damos un nombre a nuestro repositorio remoto, una descripción y le damos a `Create repository`

![nombre repo remoto](https://user-images.githubusercontent.com/84040594/167336772-dc3f4435-b8b8-4e7b-b600-1dcf50dcb59f.png)
![Create repository](https://user-images.githubusercontent.com/84040594/167336888-878f1f5d-ac11-47a9-b4a0-8bd442cb3ebc.png)

2. Tenemos nuestro repositorio remoto creado. 

![image](https://user-images.githubusercontent.com/84040594/167337216-08bec293-178d-472a-983c-54d456de8fe6.png)

#### 🎇Conectar nuestro repositorio local con uno remoto. 
1. Para conectar nuestros repositorios usaremos el comando:
```Console 
git remote add origin <link>
``` 
![image](https://user-images.githubusercontent.com/84040594/167337687-31eb3885-2f88-4ced-b58b-7238cd135183.png)

2. Verificamos nuestra conexión con 
```Console
git remote -v
```
![image](https://user-images.githubusercontent.com/84040594/167337796-e89a2826-8ebc-4b06-9630-f5b6ad806604.png)

3. El link lo podemos encontrar en formato 'https' o 'ssh'
![image](https://user-images.githubusercontent.com/84040594/167337572-6b7922a0-0b6c-4865-88cc-aedeee79fc9e.png)
![image](https://user-images.githubusercontent.com/84040594/167337594-55731c0a-258e-4c4e-bf34-d4e6b9ae532b.png)

4. Para cargar los commits de la repo local a GitHub ejecutamos el comando 
```Console
git push origin master
```
![image](https://user-images.githubusercontent.com/84040594/167337958-f959c67c-defe-4f0d-9eb2-4344bef70070.png)

5. Listo!, Podemos ver nuestro repositorio remoto con los cambios creados (en este caso, el readme.md). 
![image](https://user-images.githubusercontent.com/84040594/167338131-c8bb2cf7-e45f-4e19-a056-188482a5f821.png)

### ✨ Dependencias
Las dependencias son bibliotecas de JavaScript que nos ayduan a ejecutar ciertas acciones. Para iniciarlas y crearlas ejecutamos: 
```Console
npm init
```
Dicho comando creará el archivo package.json el cual tendrá toda la configuración de nuestros proyectos. Si vemos un package.json en un proyecto sabremos que es de JavaScript. 
Para esta semana usaremos las dependencias de [Jest](https://jestjs.io/docs/getting-started) siendo una biblioteca que nos permite escribir y ejecutar tests. También es considera un marco de trabajo por su simplicidad y es usado en pltaformas como airbnb, twitter, spotify, etc. 
#### 🎇 Instalando Jest
```Console
npm install --save-dev jest
```
#### 🎇 .gitignore 
Una vez que instalamos alguna dependencia, se descarga una carpeta que contiene todos los paquetes de NodeJs que suaremos por medio de NPM llamada _node_modules_. Esta carpeta **NO NECESITA VERSIONARSE** para ello, creamos un archivo _.gitignore_ en la raíz de nuestro proyecto y agregamos la siguiente línea: 
```Console
**/node_modules
```
Este archivo si se versiona e ignorará cualquier carpeta con ese nombre. 

### ✨ Modularización.  
Es recomendable dejar los test en una carpeta aparte de nuestro código fuente.
La modularización busca que nuestro código sea dividido en pequeñas partes para que sea más sencillo de leer, entender y mantener (como ejemplo podemos crear una clase en un archivo, crear un json en otro, etc) y separarlos en carpetas según su función. 
Para que todo funcione en conjunto debemos importar y exportar los elementos necesarios.  
En JavaScript tenemos dos formas de hacerlo: 
#### 🎇 CommonJS
Para este método exportamos los modulos que requerimos al final de los archivos: 
```Console
// ejemplo.js
module.exports = ejemplo
```
E importamos al inicio de otro archivo con: 
```Console
// index.js
const ejemplo = require('./ejemplo')
```
Así podemos hacer uso de los elementos de 'ejemplo.js' en 'index.js' o cualquier otro archivo sin que deban estar en uno mismo. 

#### 🎇 EcmaScript Modules ESM
Para este método le indicamos a cada elemento que lo vamos a exportar al definirlo: 
```Console
// ejemplo.js
export class ejemplo {
}
export class ejemplo2 {
}
```
Y para importarla, al inicio del nuevo archivo: 
```Console
//index.js
import * as ejemplos from './ejemplo.js'
```
Decimos que queremos importar todo (por el asterisco * o cada elemento ) como una variable nueva desde la ruta de un archivo. 

## ✨ Recomendación 
Si tu VSCode no determina la ubicación conforme la escribes, te recomiendo la extensión _Node Require_ para importar elemntos más fácil. 

![image](https://user-images.githubusercontent.com/84040594/167343768-ee142ccd-537d-466d-84c8-1c55891ed377.png)

Escribí un post rápido sobre esto en [Node Require](https://jossperezt.github.io/my_launchx_blog/posts/post_6/)


## 💫 TDD para diseño de software

#### 🎇Configuración de Tests con Jest
Ya vimos lo que son los TDD que son las pruebas que nos permiten validar el funcionamiento de nuestro código. 
Un archivo de test debe ser nombrado con un '.test.js' para que sea reconocido como tal. 
Para configurar las pruebas de jest debemos instalar las dependencias de Jest y modificar algunas líneas del archivo 'package.json':

Linux: 
  ```Console
  "test": "node ./node_modules/.bin/jest"
  ```
Windows: 
  ```Console
  "test": "node --experimental-vm-modules ./node_modules/jest/bin/jest.js"
  ```
De esta manera podemos correr nuestros tests con el comando: 
```Console
npm test test/ejemplo.test.js (ruta)
```
#### 🎇 Formato de una prueba
![image](https://user-images.githubusercontent.com/84040594/167348982-6db44ac7-d465-48a2-a2e5-f8b5cf3b4ec8.png)

Una prueba esta conformada por: 

◾ _importando el módulo a testear_ : Se debe importar el módulo y su origen para poder usar sus elementos y testearlos.

◾ _describe("" , () => {_ : Se le da una descripción general a nuestro archivo de pruebas. 

◾ _test("", () => {_  : Se escribe una prueba única para cada caso. Pueden existir muchos en un solo archivo. 

◾ _cuerpo_ : Se desglosa el comportamiento que deberia de tener los elementos según ciertas condiciones. 

◾ _expect()_ : Lo que recibimos de esas condiciones. 

◾ _.toBe()_ : Lo que queremos recibir con esa prueba. Esto puede cambiar a _.toEqual, .toMatch, .toMatchObject, .toNotBe, etc_ puede ser consultado en la documentación de [Jest](https://jestjs.io/docs/getting-started)

Si _expect_ y _.toBe_ son iguales, las pruebas habrán pasado, de lo contrario nos informarán del error. 

> Nunca confies en una prueba que no veas fallar. 

#### 🎇 TDD Testing Driven Developer 
Es una técnica que consiste en modelar primero las pruebas y después crear el código con las funcionalidades necesarias para que pase la prueba. Entre sus ventajas esta en ayudar a delimitar los requerimiento y sus componentes pero éste llega a ser muy complejo porque debemos aprender a ser objetivos con los requerimientos, con lo  que se solicita y con lo que se necesita. 
Consta de 3 pasos: 
1. Escribir un test para la funcionalidad que queremos. Si corremos la prueba tendremos un fallo porque no tenemos nada que probar.
2. Escribir el código necesario para que la prueba pasé y se cumpla lo requerido.
3. Refactorizar el código. 

> "TODO CÓDIGO DEBE ESTAR RESPALDADO POR PRUEBAS." [@carlogilmar](https://twitter.com/@carlogilmar)

## 💫 Express JS como framework para crear servers
[Express](https://expressjs.com/es/) es un framework de NodeJs para desarrollo web y APIs (Aplication Programming Interface). Es sencillo y cuenta con muchos métodos http para la creación de servidores que se encargan de exponer lo que hay en nuestras apps. 

#### 🎇 Instalación. 
Además de las dependencias que hemos visto, es necesario instalar la dependencia de express: 
```Console
npm install express --save
```
Esto actualizará 'package.json' automáticamente donde indica la instalación y versión de express. 
#### 🎇 Uso
1. Debemos importar express a nuestro archivo
  ```Console
  const express = require ("express");
  ```
2. Debemos indicar que una variable usara express. 
  ```Console
  const app = express();
  ```
3. Creamos e indicamos en que puerto estará disponile nuestra app
  ```Console
  const port = 3000 // localhost/3000
  ```
4. Comenzamos a usar los métodos http.
  ```Console
  app.get('/', (request, response) => {
  response.send("Hola Mundo") });
  ```
5. Enviamos los paths para que se peudan visualizar. 
  ```Console
  app.listen(port, () => {
  console.log(`Puerto : ${port}`) 
  }
  ```
6. Ejecutamos: 
  ```Console
  node archivo.js
  ```
  Ingresamos al path que establecimos y debemos encontrar el mensaje enviado. 
  ```Console
  localhost:port | localhost:3000
  ```
#### 🎇 Estructura. 

◾ _app_: Es la variable que definimos que sería ocupada por express ('const app = express();)

◾ _.get_ : Es el método http que se esta usando, pueden cambiarse por PUT, DELETE, PUSH, etc. 

◾ _'/'_: Es la ruta del endpoint, se pueden diversas rutas como: '/v1/explorers/mission'.

◾ _request_: Es lo que recibimos del endpoint, puede ser una solicitud o Query Params (parámetros requeridos) 

◾ _response_: Es la respuesta que envíamos al servidor, lo que se muestra en la web al usar las rutas (path).

#### 🎇 Métodos HTTP

Existen varios métodos HTTP, entre los más usados son: 

◾ GET: Regresa información. 

◾ POST: Crea información. 

◾ PUT: Actualiza la información. 

◾ DELETE: Elimina la información. 

#### 🎇 Status de los Métodos 

Si los métodos son ejecutados correctamnete,regresa un código de status. 

◾ 200. Para GET, PUT y DELETE. 

◾ 201. Para POST


## TERMINAMOS. 
Se termino la semana 3 y esto fue un resumen de lo que se aprendio durante ese tiempo. 

Se van relacionando los primero temas y existe una secuencia en cada cosa que se ha aprendido, que no pueden saltarse. 

Sigo con mi autocrítica de organizar mejor mi tiempo, aunque si siento que he avanzado en ese sentido, como todo, es un proceso que lleva tiempo y disciplina. 

Vuelvo a agradecr a [@carlogilmar](https://twitter.com/@carlogilmar) por su forma de enseñar y esmero que pone a cada clase y práctica que nos brinda. Los ejemplos que muestro son derivados a los ejercicios que brinda. 
