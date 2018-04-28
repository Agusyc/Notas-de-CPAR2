# Git

## Conceptos
* Repositorio: Es un índice de los directorios y archivos de un proyecto, junto con sus cambios a lo largo del tiempo.
* Rama: Es una separación del código principal, para así poder tener distintas versiones del mismo en el repositorio a la vez.
* Tag: Es la etiqueta de un commit. Por ejemplo "Versión 1.0.0". Los cambios se deben escribir en el mensaje del commit, no su Tag.

* [GitHub](https://github.com) y [GitLab](https://gitlab.com): Servicios web para guardar y compartir repositorios.

## Creando tu primer repositorio
Para crear tu primer repositorio, se debe abrir una terminal y utilizar los siguientes comandos.

```bash
mkdir nombreCarpetaProyecto # Crea una carpeta para el proyecto
cd nombreCarpetaProyecto # Mueve el directorio de trabajo a la carpeta
git init # Crea un repositorio
touch README.md # Crea un archivo vacío con el nombre README.md en la carpeta
git add README.md # Añadir el archivo al commit
git commit -m 'Una buena descripción' # Envío el commit con comentario
```

En cualquier parte del proceso se pueden utilizar los comandos "ls", para listar los archivos y directorios de la carpeta, y "git status", para revisar el estado del repositorio.

## Subiendo tu repositorio a GitHub
Para subir un repositorio a GitHub, primero debes crear una cuenta y un repositorio en su sitio web. Luego, debes escribir el siguiente comando

```bash
git remote add origin https://github.com/user/repo.git
```

Recuerden reemplazar la palabra "user" por su nombre de usuario de GitHub, y la palabra "repo" por el nombre del repositorio que crearon.

Luego de hacer esto, deben ejecutar el comando

```bash
git push
```

Se les preguntará su nombre de usuario y contraseña de GitHub. Ingrésenlos y comprueben si el estado del repositorio en la página web del mismo es correcto.

### Creando una branch
Una branch es una separación del código principal, por ejemplo para tener una versión alpha, otra beta y una principal o estable. Los cambios que se hagan en una branch nunca afectan a los archivos de otra, a menos que se les haga un merge, donde los cambios más nuevos son incorporados.

Para crear una nueva branch, utilizamos el comando

```bash
git checkout -b nombreNuevaBranch
```

Cambiá el nombre a lo que quieras, pero utilizando sólo letras.

Para probar la nueva branch, hacemos cambios en el contenido del repo, hacemos un commit y ejecutamos "git push". Se debería poder observar que hay una nueva branch en el sitio web del repositorio.
