# P1

mfernandezmarti@uoc.edu
Miguel Fernández Martín

# Pasos a seguir

> git init (para iniciar el repositorio -> carpeta oculta .git)

Crear el archivo .gitignore

> npm init -y (para crear el archivo package.json)

> npm install --save-dev parcel (para instalar Parcel)

Añadir las siguientes líneas al archivo package.json: Building a web app with Parcel (https://parceljs.org/getting-started/webapp/)
    {
        "source": "src/index.html",
        "browserslist": "> 0.5%, last 2 versions, not dead",
        "scripts": {
            "start": "parcel",
            "build": "parcel build"
        },
        "devDependencies": {
            "parcel": "latest"
        }
    }

Crear los archivos .postcssrc y .posthtmlrc (para añadir los plugins necesarios)

> md src (para crear la carpeta src)

Añadir la estructura HTML, CSS, JS y PHP del sitio web

> npm install cssnano postcss-custom-properties postcss-import postcss-url --save-dev (para instalar los plugins de PostCSS: CSSNano, PostCSS-custom-properties, PostCSS-import y PostCSS-url)

Añadir las siguientes líneas al archivo .postcssrc
    {
        "plugins": {
            "cssnano": {
                "preset": "default"   
            },
            "postcss-custom-properties": {},
            "postcss-import": true,
            "postcss-url": true
        }
    }

Crear un repositorio en GitHub (para evitar errores, no inicializar el nuevo repositorio con archivos README, licencia o gitignore. Se pueden agregar estos archivos después de que el proyecto haya sido enviado a GitHub)

> git remote add origin REMOTE-URL (para agregar la URL del repositorio remoto donde se enviará el repositorio local. Se puede verificar con el comando > git remote -v)

> git push origin main (para enviar los cambios del repositorio local a GitHub)
