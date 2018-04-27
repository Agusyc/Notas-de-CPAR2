# Git

## Conceptos
* Repositorio: Es un índice de los directorios y archivos de un proyecto, junto con sus cambios a lo largo del tiempo.
* Rama: Es una separación del código principal, para así poder tener distintas versiones del mismo en el repositorio a la vez.
* Tag: Es la etiqueta de un commit. Por ejemplo "Versión 1.0.0". Los cambios se deben escribir en el mensaje del commit, no su Tag.

* [GitHub](https://github.com) y [GitLab](https://gitlab.com): Servicios web para guardar y compartir repositorios.

## Creando tu primer repositorio
Para crear tu primer repositorio, se debe abrir una terminal y utilizar los siguientes comandos.

* mkdir nombreCarpetaProyecto # Crea una carpeta para el proyecto
* cd nombreCarpetaProyecto # Mueve el directorio de trabajo a la carpeta
* git init # Crea un repositorio
* touch README.md # Crea un archivo vacío con el nombre README.md en la carpeta
* git add README.md # Añadir el archivo al commit
* git commit -m 'Una buena descripción' # Envío el commit con comentario

En cualquier parte del proceso se pueden utilizar los comandos "ls", para listar los archivos y directorios de la carpeta, y "git status", para revisar el estado del repositorio.
