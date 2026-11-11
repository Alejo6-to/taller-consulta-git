1.
Git es un sistema de control de versiones: guarda el historial de los cambios en los archivos de un proyecto. Así puedes ver qué se modificó, volver a una versión anterior o trabajar en cambios nuevos sin afectar la versión principal.

-Resuelve problemas como perder trabajo, no saber quién cambió algo o cuándo, y tener dificultades para combinar cambios de varias personas. Con Git puedes consultar el historial, recuperar versiones anteriores y trabajar en cambios separados sin afectar el proyecto principal.

**Diferencias clave entre Git y GitHub.** 
-GitHub: Es una plataforma en línea que utiliza Git para almacenar repositorios en la nube. Su función principal es permitir que los desarrolladores compartan sus proyectos, trabajen en equipo, revisen modificaciones y colaboren desde diferentes computadores. También permite administrar tareas, reportar errores y proponer mejoras en los proyectos.
-Git es un software que permite controlar las versiones de un proyecto, mientras que GitHub es una plataforma que permite almacenar y compartir esos proyectos.
-Git permite registrar los cambios realizados en el código, mientras que GitHub permite visualizar esos cambios y compartirlos con otros desarrolladores.
-Git permite crear ramas para trabajar en diferentes funcionalidades, mientras que GitHub facilita la colaboración y revisión de esas modificaciones.

**¿Qué es una nube de repositorios?** 
-Una nube de repositorios es un servicio en internet que permite almacenar, organizar y administrar proyectos de programación de manera remota. En estos repositorios se guarda el código fuente de un proyecto y su historial de cambios, permitiendo que los desarrolladores puedan acceder a sus archivos desde diferentes computadores y trabajar de manera colaborativa.

Su principal objetivo es mantener una copia del proyecto en internet, facilitar el trabajo en equipo, compartir código y evitar que toda la información dependa de un solo computador.

Además de almacenar los proyectos, estas plataformas permiten controlar las modificaciones realizadas por diferentes desarrolladores, revisar errores y proponer mejoras.

Tres alternativas a GitHub que existen en el mercado:

-GitLab: Es una plataforma que permite almacenar repositorios, controlar versiones y trabajar en equipo. También ofrece herramientas para automatizar pruebas y procesos de desarrollo de software mediante integración y entrega continua (CI/CD).

-Bitbucket: Es una plataforma desarrollada por Atlassian que permite alojar repositorios Git, administrar proyectos y facilitar la colaboración entre desarrolladores. Se integra con otras herramientas como Jira.

-Azure Repos: Es un servicio de Microsoft que permite almacenar y administrar repositorios de código mediante Git o Team Foundation Version Control (TFVC). Facilita el trabajo colaborativo y la administración de proyectos de software.


 **Glosario básico:** 
 
- Commit (Guardar cambios)
Es una operación que permite registrar los cambios que hemos realizado en un proyecto dentro del historial de Git. También nos permite escribir un mensaje corto explicando qué modificaciones hicimos.

Ejemplo práctico: Si agregamos un menú de navegación a nuestra página web, podemos registrar ese cambio con el siguiente comando:
git add .
git commit -m "Agregamos el menú de navegación"


- Branch (Rama)
Es una herramienta que permite crear diferentes ramas dentro de un mismo proyecto para trabajar en nuevas funcionalidades sin modificar directamente la rama principal. También permite identificar en qué rama estamos trabajando.

Ejemplo práctico: Si estamos desarrollando una página web y queremos crear un inicio de sesión, podemos crear una rama llamada login para trabajar en esa funcionalidad sin afectar la rama principal.
git branch login


- Merge (Fusión)
Es una operación que permite unir los cambios realizados en una rama con otra. Se utiliza cuando terminamos de desarrollar una funcionalidad y queremos integrarla al proyecto principal.

Ejemplo práctico: Si terminamos de desarrollar el inicio de sesión en la rama login, podemos unir esos cambios con la rama principal.
git merge login


- Pull y Push
Son dos comandos que permiten sincronizar nuestro proyecto local con un repositorio remoto, como GitHub.

Pull: Permite traer los cambios que se encuentran en el repositorio remoto y actualizar nuestro proyecto local.

Ejemplo: Un compañero subió modificaciones a GitHub y nosotros necesitamos traerlas a nuestro computador.
git pull


Push: Permite enviar los cambios que hemos registrado en nuestro repositorio local hacia el repositorio remoto.

Ejemplo: Terminamos de modificar nuestro proyecto y queremos subir los cambios a GitHub para que nuestros compañeros puedan verlos.
git push


- Pull Request (PR)
Es una solicitud que se realiza para proponer que los cambios desarrollados en una rama sean revisados e incorporados a otra rama. Permite que otros integrantes del equipo revisen el código antes de aceptar las modificaciones.

Ejemplo práctico: Terminamos de desarrollar el inicio de sesión y queremos agregarlo al proyecto principal. Creamos un Pull Request para que nuestro profesor o compañeros revisen el código y decidan si se puede integrar.
- Clone (Clonar)
Es una operación que permite copiar un repositorio remoto, como uno de GitHub, directamente a nuestro computador. De esta manera podemos acceder a los archivos, modificarlos y trabajar en el proyecto desde nuestra terminal o editor de código.

Ejemplo práctico: Nuestro profesor comparte un enlace de un proyecto en GitHub y nosotros queremos descargarlo para trabajar en él desde Visual Studio Code.
git clone https://github.com/usuario/proyecto.git


- Upstream y Origin
Son nombres que se utilizan para identificar repositorios remotos con los que trabajamos en Git.

Origin: Es el nombre que normalmente se asigna al repositorio remoto original que clonamos o al repositorio remoto principal de nuestro proyecto. Allí podemos subir nuestros cambios.

Upstream: Es el nombre que normalmente se utiliza para identificar el repositorio original del que proviene un proyecto cuando trabajamos con una copia propia (fork).

Ejemplo práctico: Imagina que encuentras un proyecto en GitHub y quieres colaborar en él. Primero haces una copia en tu propia cuenta de GitHub (fork). En ese caso:
- origin: es tu copia del proyecto en tu cuenta de GitHub.
- upstream: es el repositorio original del creador del proyecto.