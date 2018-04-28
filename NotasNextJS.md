# NEXT.JS

## Concepto
NEXT.JS es un framework basado en REACT que se utiliza para hacer aplicaciones web.

Ventajas:
* Tiene una API simple.
* Tiene mucha optimización.
* Se usa en sitios grandes, de 20 o 30 millones de usuarios. Sin demasiada configuración, puede aguantar de 10 mil a 10 millones de usuarios.

## Nuestra primer aplicación
Primero, se debe tener instalado NodeJS versión 9.0.0 o mayor y npm versión 5.6.0 o mayor.

### Conceptos básicos de terminal
Para poder crear nuestra aplicación, necesitaremos saber cómo utilizar mínimamente nuestra terminal.

Algunos comandos básicos:
* "mkdir *nombreDeCarpeta*" Crea una carpeta con el nombre *nombreDeCarpeta*
* "cd *nombreDeCarpeta*" Cambia el directorio de trabajo actual a *nombreDeCarpeta*
* "ls" Muestra los archivos del directorio de trabajo actual.

### Creando la carpeta y estructura de proyecto
Para empezar, se debe crear una carpeta que contendrá todos los archivos del proyecto. Puede tener cualquier nombre excepto "nextjs".

```bash
mkdir PrimerAppWeb
```

Luego de hacer esto, cambiamos el directorio de trabajo actual a esa carpeta.

```bash
cd PrimerAppWeb
```

Ahora, para crear el archivo "package.json", que contendrá información muy importante sobre nuestro proyecto, como dependencias, nombre, versión, autor entre otros, ejecutaremos este comando:

```bash
npm init -y
```

Si ahora listan los archivos del directorio, deberían poder observar que el archivo "package.json" se ha creado.

### Configurando los scripts
Una vez que tienen el archivo package.json, deben abrirlo con su editor favorito y escribir toda la información de su proyecto. Pueden dejarlo como está, o pueden cambiar los campos:
* Name
* Version
* Description
* Author
* License

Si no tienen experiencia con JSON, les recomiendo dejar el archivo como está.

El siguiente paso será configurar los scripts del proyecto. Para esto, deben borrar el objeto "scripts" y reemplazarlo por este:

```json
"scripts": {
  "dev": "next",
  "build": "next build",
  "start": "next start"
}
```

El archivo terminado debe verse como este, pero con sus datos propios o los predeterminados:

```json
{
  "name": "NextJSRepo",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "next",
    "build": "next build",
    "start": "next start"
  },
  "keywords": [],
  "author": "Agustín Roth",
  "license": "WTFPL",
  "dependencies": {
    "isomorphic-fetch": "^2.2.1",
    "next": "^5.1.0",
    "react": "^16.3.2",
    "react-dom": "^16.3.2"
  }
}
```
