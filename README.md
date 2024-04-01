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

