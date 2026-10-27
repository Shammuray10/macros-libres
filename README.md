# Macros Libres (APK)

App de macros y calorías, gratis y sin anuncios. Es la misma app web envuelta en una app Android (WebView). Los datos se guardan en el propio móvil.

## Compilar el APK gratis (GitHub Actions)

1. Crea una cuenta gratuita en github.com y un repositorio nuevo (por ejemplo `macros-libres`).
2. Sube el contenido de esta carpeta al repositorio. Desde Termux:

       pkg install git unzip
       unzip macros-libres-apk.zip -d macros-libres && cd macros-libres
       git init && git add -A && git commit -m "Macros Libres"
       git branch -M main
       git remote add origin https://github.com/TU_USUARIO/macros-libres.git
       git push -u origin main

   (GitHub pide un token personal como contraseña: Ajustes > Developer settings > Personal access tokens, con permiso `repo` y `workflow`.)
3. En el repositorio entra en la pestaña **Actions**. Cuando termine "Compilar APK" (unos 3-5 minutos), abre la ejecución y descarga el archivo `macros-libres-apk`.
4. Descomprime y abre `app-debug.apk`. Android pedirá permitir instalar apps de esta fuente.

El APK sale firmado con la clave de depuración, suficiente para uso personal. No se ha compilado antes de entregarlo: si Actions da algún error, copia el texto del error y se corrige.
