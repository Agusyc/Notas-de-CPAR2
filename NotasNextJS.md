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
  "license": "WTFPL" 
}
```

### Agregando las dependencias
Para que nuestra aplicación web funcione, debemos agregar al package.json nuestras dependencias. Para hacer esto, utilizamos el comando

```bash
npm add next react react-dom isomorphic-fetch
```

Esperen unos minutos a que npm termine de descargar e instalar las dependencias.

### Creando nuestra primer página
Las aplicaciones web que crearemos están basadas en páginas, las cuales irán en una carpeta llamada "pages". Para crear esta carpeta, ejecutamos

```bash
mkdir page
```

Con tu editor favorito, crea un archivo llamado "index.js". Este archivo será el que contendrá todo el código de la página principal de nuestra aplicación.

El contenido de estea rchivo debería ser

```javascript
export default class extends React.Component
 {
   render()
    {
     return (<h1>¡Hola, Campus Party!</h1>)
    }
 }
```

En este archivo, hemos creado una clase que extiende a React.Component. Tiene un método render(), que se encarga de renderizar la página web. Por así decirlo, se encarga de la parte gráfica de la misma. En este caso, vamos a mostrar un header 1 (<h1>) con el texto "¡Hola, Campus Party!". El texto puede ser cualquier cosa que quieran.

### Corriendo la aplicación
Para iniciar la aplicación, debemos ejecutar el comando

```bash
npm run dev
```

Luego, deben ir a su navegador favorito e ingresar "localhost:3000" en el campo de la URL, y luego ingresar a la misma.
