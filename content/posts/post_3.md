---
title: "Error 0x00000001 en WSL"
date: 2022-04-25
description: 'Cómo solucionarlo'
---
# Error 0x00000001
```console
  [proceso termiando con el código 1 (0x00000001)]
```

---
Hola. Un gusto saludar al lector del otro lado de la pantalla. 
Tuve un error en la terminal WSL y aquí te digo: 
  - Que hice para llegar a ese error. 
  - Mi solución. 
  - Mi error. 


Mi Sistema Operativo es Windows 10, y en esta nueva travesía empece a usar el Subsistema de Linux en Windows (WSL) con Ubuntu 20.04 e intenté personalizarlo con "oh-my-zsh". Pero hubo un error al querer establecerlo como predeterminado no me lo permitía: 

![error you not change](https://user-images.githubusercontent.com/84040594/165224927-a6674eae-90c0-42db-8d29-e3c99e5ef98f.png "error you not change")

"Tratando" de solucionarlo, encontré esto:

![posible solución](https://user-images.githubusercontent.com/84040594/165225375-c06a29b5-d77d-4b7b-93b1-64d4ac2ad67e.png "posible solución") ![posible solución ejecutada](https://user-images.githubusercontent.com/84040594/165227295-db88a063-07c4-4e5d-8c15-31d295070954.png "posible solución ejecutada")


Pero solo provocó el error: 

```console
  [proceso termiando con el código 1 (0x00000001)]
```
![error](https://user-images.githubusercontent.com/84040594/165224298-535875cb-d1b0-46e1-9ba8-22468c35158c.PNG "error")



# MI SOLUCIÓN

Busqué la manera de arreglarlo antes de desinstalar e instalar WSL de nuevo, y, según lo que encontré, es un error que le pasa a muchos en WSL, incluso hay un Issue en GitHub acerca de esto, donde te dan varios consejos que pueden o no servir, así que intenté con varios y mi solucion fue:

## 1. Abrir CMD como administrador.
## 2. Ejecutar el siguiente comando: 
  ```code
    wsl --user root -d [distro name]
  ```
   ![wsl](https://user-images.githubusercontent.com/84040594/165229826-a02f4a3d-66b7-444e-bd7b-518001b2d838.png "wsl")
   
  ### 2.1 Esto hará que CMD sea usado por el usuario root (quien tiene acceso administrativo al sistema Linux) 
  
   ![root](https://user-images.githubusercontent.com/84040594/165229904-d5210b90-3052-45dc-9fd8-34bbeeeaa30d.png "root")
   
## 3. Ejecutarás el siguiente código.

  ```code
  chsh --shell /bin/bash [username]
  ```

![chsh](https://user-images.githubusercontent.com/84040594/165230008-64f272eb-833d-4255-9327-a8ce2085b05f.png "chsh")
## 4. Vuelves a abrir tu terminal, y listo. 
![solucion](https://user-images.githubusercontent.com/84040594/165229636-0408d3c8-61f2-4a3c-baab-1c2cb1014b56.png "solucion")

## 5. Establecer shell
Solucionado el error  0x00000001, podemos volver a establecer la shell que se tenía, en mi caso, fish.
![fish](https://user-images.githubusercontent.com/84040594/165231521-d18d5ab8-c49b-444b-8079-3e33e9b16264.png "fish")



# Mi error y lo que aprendí/recordé
El error original, "no poder estabelcer una shell como predeterminada", fue a que no supe hacerlo bien y al volver a establecer fish para hacer este post, recordé lo básico de la instalación y que es aplicable para otras shells:

◾ Primero: se debe cambiar a la shell que se quiere: 
  ```code
  fish | zsh | bash
  ```
◾ Luego: se ejecuta el comando para que sea prederminada. 
  ```code
  chsh -s /usr/bin/<shell>
  ```
![zsh](https://user-images.githubusercontent.com/84040594/165233181-b431209d-85ea-47e5-962b-7b3b60be24e5.png)

Algo muy sencillo se convirtió en un problema. 


# ISSUE 
Aquí les dejo el link del [Issue](https://github.com/microsoft/WSL/issues/4899) de GitHub donde hay más soluciones del mismo problema que pueden probar por si este no les funcionó.
