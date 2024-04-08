# P1

mfernandezmarti@uoc.edu
Miguel Fernández Martín

# Pasos a seguir

> git init (para iniciar el repositorio -> carpeta oculta .git)

Crear el archivo .gitignore y añadirle las siguientes líneas (para que no suba al repositorio remoto: los módulos de node.js instalados, los archivos fuente del sitio *web*, la carpeta de pruebas dist, las caches generadas, el archivo *package-lock.json*)
    node_modules
    src
    dist
    .parcel-cache
    package-lock.json

> npm init -y (para crear el archivo *package.json*)

> npm install --save-dev parcel (para instalar Parcel)

Añadir las siguientes líneas al archivo *package.json*: Building a web app with Parcel (https://parceljs.org/getting-started/webapp/)
    {
        "name": "p1",
        "source": "src/index.html",
        "browserslist": "> 0.5%, last 2 versions, not dead",
        "scripts": {
            "start": "parcel serve src/index.html",
            "build": "parcel build --dist-dir dist --public-url https://mifemar.github.io/P1 src/index.html"
        },
        "devDependencies": {
            "parcel": "latest"
        }
    }

Crear los archivos *.postcssrc* y *.posthtmlrc* (para añadir los *plugins* necesarios)

> md src (para crear la carpeta *src*)

Añadir la estructura HTML, CSS, JS y PHP del sitio *web*

> npm install cssnano postcss-custom-properties postcss-import postcss-url --save-dev (para instalar los *plugins* de PostCSS: CSSNano, PostCSS-custom-properties, PostCSS-import y PostCSS-url)

Añadir las siguientes líneas al archivo *.postcssrc*
    {
        "plugins": {
            "postcss-custom-properties": {},
            "postcss-import": true,
            "postcss-url": true,
            "cssnano": {
                "preset": "default"   
            }
        }
    }

Crear un repositorio en GitHub (para evitar errores, no inicializar el nuevo repositorio con archivos README, licencia o gitignore. Se pueden agregar estos archivos después de que el proyecto haya sido enviado a GitHub)

> git remote add origin REMOTE-URL (para agregar la URL del repositorio remoto donde se enviará el repositorio local. Se puede verificar con el comando > git remote -v)

> git push origin master (para enviar los cambios del repositorio local a GitHub) (¡¡¡Importante!!! Que la rama local esté creada: Si no fuese así, se puede crear con el comando > git checkout -b master. Se puede comprobar si está creada con el comando > git branch. Finalmente, si está creada, se puede cambiar de nombre con el comando > git branch -m NEW-NAME)

En el repositorio creado en GitHub > Pestaña *Settings* > Menú *Pages* > Activar la dirección *web*, en su caso, en la sección **Build an deployment - Branch**


