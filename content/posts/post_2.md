---
title: "Mi primera semana "
date: 2022-04-16T18:16:21-06:00
description: 'Descripción de mi primer semana en la Mission Backend NodeJs'
---
# Mi primera semana. 

Hola lectores 👋 

Como ya lo leyeron, esta fue mi primera semana en esta misión, la cual consistió y aprendí sobre:

- ◼ La importancia de las herramientas. 
  - ◻ Conocimiento de Git y GitHub. 
  - ◻ Conocimiento de nuestros Sistema Operativo. 
  - ◻ Conocimiento de nuestro editor de texto. 
- ◼ Aprender a interpretar código. 
- ◼ Ser autodidácta. 

----

## Importancia de las herramientas❗. 
La primera cosa que nuestro MissionCommander (MC) [@carlogilmar](https://twitter.com/carlogilmar) nos enseño fue la importancia de las herramientas, las principales son las de Git, GitHub, la terminal del símbolo de sistema (CMD, PowerShell, Bash, Fish, etc) y el editor de texto (Visual Studio Code, ATOM, entre otros), ya que nos aydudan a hacer un trabajo más eficiente y productivo. Para lograr es objetivo es necesario invertir tiempo y estudio a cada uno, algunas cosas se aprenden sobre la marcha, eso es seguro, pero el experimentar con ellas llegó a ser divertido y estresante para mi. 

### Conocimiento de Git y GitHub 🙇🏽‍♀️. 
Para empezar, alaremos la diferencia entre ambos conceptos y herramientas a lo que entendí:

  - ◼ Git es un software opensoruce que se encarga de controlar las versiones de los archivos. Es manejado por medio de comandos y puede ser utilizado desde varios programas, en mi caso, lo puedo manejar desde:
    - ◻ Git Bash
    
      ![Manejo de Git en Git Bash](https://user-images.githubusercontent.com/84040594/163694766-5c2dafab-442c-4d5d-b5fe-b12bd5e00941.png "Manejo de Git en Git Bash")
    - ◻ PowerShell o CMD
   
      ![Manejo de Git en CMD](https://user-images.githubusercontent.com/84040594/163694731-975a1132-9ba6-405d-acc0-7009a2e8e5c8.png "Manejo de Git en CMD")
    - ◻ WSL
    
      ![Manejo de Git en WSL](https://user-images.githubusercontent.com/84040594/163694802-af1dc509-4dfc-47e2-b7ad-6fc42dd78a56.png "Manejor de Git en WSL")

    
  - ◼ GitHub es la plataforma en la que se alojan los repositorios. Su manejo es por medio de su interfaz gráfica y tambien puede ser administrada por VSCode. 
    ![Manejo de GitHub](https://user-images.githubusercontent.com/84040594/163694914-75f1d6ea-b9de-4409-aded-6a4dd4997196.png "Manejo de GitHub")

Bueno, como parte de esta formación había ocupado GitHub desde el inicio, creando y subiendo mis repositorios y las actualizaciones por medio de VSCode o de forma directa. No me había animado en hacerlo de por medio de comandos, lo consideraba difícil de hacer y entender, pero mi MC me impulsó a usarlo dandonos múltiples beneficios de productividad y efectividad. Y gracias los recursos en línea que me recomendaron y encontré entre las búsquedas pude ejecutar comandos como: 
  - `git status`, `git diff`, `git add`, `git commit -m`, `git config --global user.name `, `git config --global user.email`, `git init`, `git clone`, `git show`, `git log`, `git push origin main`. 
 Los recursos que puedo recomendar y que me ayudan mucho son:
  - ◼ [Libro de Pro Git](https://git-scm.com/book/en/v2)
  - ◼ [Git Cheat Sheet](https://training.github.com/downloads/es_ES/github-git-cheat-sheet.pdf)
  - ◼ [Documentación de Git](https://git-scm.com/docs)
 
 
 ### Conocimiento de nuestro Sistema Operativo (SO) 👩🏽‍💻. 
 Durante este tema el punto era enfocarnos a las terminales que existen entre los diferentes SO. 
  - ◼ Los básicos de Linux son: bash, fish, zzh, ksh, sh, csh, tcsh. 
  - ◼ Los básicos de Windows son: CMD, PowerShell. 
  - ◼ La terminal de MacOs X es basada en UNIX, por lo que puede usar las mismas terminales de Linux. 
  
Ya tenía nociones básicas sobre el uso de comandos de las terminales de Windows y Linux, por lo que no se me resultó el familiarizarme con ellos. En esta ocasión se me hazo más sencillo, dinamico y productivo, usar el sistema de Linux que el Windows. sin embargo, en este punto de aprendizaje se complicó mi avance. 

Para usar el sistema de Linux en Windows es necesario instalar [WSL (Windows System for Linux)](https://docs.microsoft.com/en-us/windows/wsl/), que basicamente es una herramienta que nos permite ejecutar las herramientas de Linux por medio de sus terminales en Windows sin ningún problema, sin cambiar el SO y sin la carga de una máquina virtual. Es muy práctica y fácil de manejar. Y para trabajar con NodeJS es necesario instalarlo desde sus terminal y con los comandos correspondientes. Mi MC nos dió a conocer que estas terminales pueden hacerse más visuales y dar una buena presentación usando *fish* y personalizarla por **Oh My Fish**. Para mí, hacer esas configuraciones fueron las que se me dificultaron porque no se mostraban los íconos correspondientes en la terminal.

![WSL sin íconos](https://user-images.githubusercontent.com/84040594/163695989-2b0505c0-93dc-4a80-8429-33a931ff9133.png "WSL sin íconos")

No me iba a dar por vencida, queria una terminal atractiva visualmente además de que tiene un sistema de autocompletado que era muy práctico, leía la documentación de [oh-my-fish](https://github.com/oh-my-fish/oh-my-fish), instalaba nuevas fuentes, buscaba en google, y no encontraba una respuesta al por qué no se veían los íconos. Hasta que instale la [Terminal de Windows](https://www.microsoft.com/es-mx/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) pensando que me iba a ser útil para usar y cambiar a cualquier terminal de mi SO, tanto PowerShell,  CMD, WSL. Pues para mi sorpresa y beneficio, en este software si se presentaba los íconos, aún no sé exactamente porque aquí si funciona pero quedó. 
![Terminal de Windows WSL](https://user-images.githubusercontent.com/84040594/163696244-4c87a271-1e04-48e8-8f93-391b0e0ad77e.png "Terminal de Windows WS")

Durante mis búsquedas, encontré con una herramienta que personaliza las terminales de Windows, [Oh My Posh](https://ohmyposh.dev/docs/), es parecido a Oh My Fish pero peude ser aplicable a PowerShell, CMD y bash. Se me hizo una forma interactiva de hace mis terminales PowerShell y CMD más visuales. Aún estoy averguando como funciona y como establecerlo como predeterminado. Por lo que he experimentado entiende comandos de Windows y Linux por lo que sería una opción alterna. Si logro aplicarlo haré un tutorial, espero lo entiendan. 
![oh-my-posh](https://user-images.githubusercontent.com/84040594/163696738-70c1fdc2-356d-4872-88c2-2614bb1b510f.png "oh-my-posh")
![oh-my-posh-powershell](https://user-images.githubusercontent.com/84040594/163696788-7f0bfea8-2ff4-4b05-9a59-f2cb6a66ad96.png "oh-my-posh-powershell")



### Conocimiento de nuestro editor de texto. 
El editor de texto es un software que nos permite crear y editar textos sin formato. El que uso y estoy más familiarizada en [Visual Studio Code](https://code.visualstudio.com/docs). 
![Visual Studio Code](https://user-images.githubusercontent.com/84040594/163696435-592afd51-ebb5-4d3d-871e-bfb440b151bc.png "Visual Studio Code")
En algunas semanas intentaré usar ATOM y ver con cuál me acomodo más. 

----

## Aprender a inetrpretar código 📚. 
En este apartado Carlo nos brindó unos ejercicios para leerlos, ejecutarlos y prácticar. La ejecución de los ejemplos debe hacerce con [NodeJs](https://nodejs.org/es/), comenzando a adentrarnos en la herramienta de la misión. Cabe recordar que para el sistema de WSL es necesario instalarlo como se haría en Linux, les dejo el link de la documentación que explica la forma de hacerlo: [NodeJs en WSL](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl)

Los ejercicios fueron funcionales y copiarlos me permite practicar la esritura en la computadora y ver como funciona cada elemento. El reto en este apartado fue entender el código, pude comprender una parte de él pero aún se me dificulta aplicarlo. Aunque me sentí orgullosa de terminar los ejercicios propios. 

----

## Ser autodidacta 🔎. 
Puedo decir que para resolver los problemas de terminal, de ejecución, de la configuración de Fish y buscar como entender los ejercicios empleé la búsqueda propia. Para mí es un comienzo de aprender por cuenta propia así que pocoo a poco me desarrollaré en este ámbito. 

----

# Conclusión 🏆. 
Después de contarles toda mi historia y proceso en esta semana, concluyó que si avance y entendi la importancia de los temas, me hace falta profundizarlos pero cumplí con el objetivo. Una crítica constructiva que me hago es que debo organizarme en la distribución de mi tiempo pra aprender, avanzar y ser más eficaz porque me estoy atrasando. 
Carlo nos da demasidos recursos para avanzar, hay que aprovecharlos todos. Se nota demasiado el esfuerzo que pone en cada live, material, explicación y ayuda que da. [@carlogilmar](https://twitter.com/carlogilmar) si ves esto, te agradezco por cada detalle que nos has brindado, eres un super crack y una persona para admirar ✨✨. 




