# Crea tu página web en R

> Almacena este curso en tus favoritos, dando click en la estrella 🌟 de la parte superior derecha 😎.

Notas personales recabadas a partir de los tutoriales y ejemplos 😊. Espero que les funcione 💜

📹 Video interactivo y explicativo conmigo en [OneDrive](https://drive.google.com/file/d/1TAgaQlp3EzN5pwZdLfwKPP3vz2EDwkva/view?usp=sharing). 

## Paquetes 📚

Paquetes necesarios para crear tu CV y página web en R.

- [rmarkdown](https://rmarkdown.rstudio.com/articles_intro.html)
- [pagedown](https://github.com/rstudio/pagedown)
- [devtools](https://www.r-project.org/nosvn/pandoc/devtools.html) - Instalacion de paquetes de Github
- [datadrivencv](https://nickstrayer.me/datadrivencv/)
- [postcards](https://github.com/seankross/postcards) - Tutorial del creador del paquete
- [fontawesome](https://rstudio.github.io/fontawesome/) - puedes encontrar la informacion de los iconos en su [pagina web](https://fontawesome.com/icons)

### Instalación de paquetes

```
install.packages("rmarkdown")
remotes::install_github('rstudio/pagedown')
install.packages("devtools")
devtools::install_github("nstrayer/datadrivencv")
install.packages("postcards")
install.packages("fontawesome")
```

## Flujo de trabajo

1) Crear el CV en R. Github: [Make_yourCV](https://github.com/EveliaCoss/Make_yourCV)
2) Generar un dominio desde Github.
3) Subir a Github el CV.
4) Crear la pagina web en R.

### 1. Crear el CV en R

Las instrucciones se encuentran en el Github: [Make_yourCV](https://github.com/EveliaCoss/Make_yourCV). De igual manera, puedes seguir las indicaciones dadas en el [video](https://drive.google.com/file/d/1TAgaQlp3EzN5pwZdLfwKPP3vz2EDwkva/view?usp=sharing) 📹. 

### 2. Generar un dominio desde Github

Desde tu home de Github, vas a dar click en repositorios y vas a crear un nuevo repositorio con el nombre `Usuario.github.io`. Sin espacios y en vez de `Usuario` vas a escribir el nombre de tu usuario de Github. ejemplo: *`EveliaCoss.github.io`*. Vas a darle que sea  `public` 🔓 y aceptar. 

Ya que tienes creado el repositorio tendrás en la parte superior un botón que dice *Settings* (un engranaje), vas a dar click y en caso de que te equivoques, aquí podrás editar el nombre en General. Vamos a ubicar el cursor en *Pages*, localizado en el menú de la izquierda. En donde dice *Branch* vas a cambiar la opción de *None a Main*. Automáticamente se activará un nuevo botón que dirá *root* con un símbolo de una carpeta. Da click en **Save**.

![branch](https://github.com/EveliaCoss/make_yourWebpage/blob/main/branch.png)

Actualiza la página y ten paciencia, a veces tarda Github en darte el dominio. Cuando todo esté listo tendrás un link como este https://eveliacoss.github.io/ pero con tu usuario.  

![dominio](https://github.com/EveliaCoss/make_yourWebpage/blob/main/dominio.png)

Posteriormente, tu repositorio tendrá el siguiente símbolo con palomita verde, validando que tienes una página web en Github.

![logo](https://github.com/EveliaCoss/make_yourWebpage/blob/main/logo_githubpages.png)


### 3. Subir a Github el CV

Crea un nuevo repositorio publico que se llame `CV`, ademas vas a hacer que se repositorio se convierta en una pagina web. Lo mismo que hicimos en el paso anterior. 

> Ya que tienes creado el repositorio tendrás en la parte superior un botón que dice *Settings* (un engranaje), vas a dar click y en caso de que te equivoques, aquí podrás editar el nombre en General. Vamos a ubicar el cursor en *Pages*, localizado en el menú de la izquierda. En donde dice *Branch* vas a cambiar la opción de *None a Main*. Automáticamente se activará un nuevo botón que dirá *root* con un símbolo de una carpeta 📂. Da click en **Save**.

En este repositorio vas a subir los archivos generados para el CV. Debe contener como minimo los siguientes archivos:

- ✅ cached_positions.rds
- ✅ cv_usuario.html - Archivo renderizado (Paso 1)
- ✅ cv_usuario.rmd  - editado por el usuario (Paso 1)
- ✅ cv_printing_functions.R (Paso 1)
- 🔲 paquetes.R - Solo vienen indicaciones de los paquetes (No es importante)
- ✅ render_cv.R - editado por el usuario (Paso 1)

En mi [Github](https://github.com/EveliaCoss/CV) encuentras el ejemplo de mis archivos.

### 4. Crear la pagina web en R

Recuento, hasta este punto debemos tener 2 repositorios:

- ✅ Tu dominio, ejemplo: [EveliaCoss.github.io](https://github.com/EveliaCoss/EveliaCoss.github.io) - Debe estar Vacio
- ✅ CV, ejemplo: [CV](https://github.com/EveliaCoss/CV) - Con archivos

Vamos a Descargar la información que tengo en [mi dominio](https://github.com/EveliaCoss/EveliaCoss.github.io) y dentro de RStudio vamos a abrir el archivo `index.Rmd`. Recomiento que coloques tu foto en la misma carpeta en donde descargaste los archivos para que puedas editarla.

Ahora toca editar el YAML que se encuentra en la parte superior del archivo `index.Rmd`. El cual se ve asi:

![yaml](https://github.com/EveliaCoss/make_yourWebpage/blob/main/yaml.png)

Campos por cambiar:

- ☑️ `title` : Coloca tu nombre entre comillas.
- ☑️ `image` : Agrega el nombre de tu imagen con su extension. 
- ☑️ `url` :  Cambiar los url de cada parte.
- ☑️ `postcards::jolla` :  Cambiar estilo (jolla, jolla blue, trestles, onofre y solana). Elige el tuyo en la [pagina web](https://github.com/seankross/postcards)

La siguiente linea de codigo se encarga de generar un boton que contenga nuestro CV, el cual previamente subimos al repositorio de Github (Paso 3).

```
label: '`r fontawesome::fa(name = "user", fill = "steelblue")` CV'
url: "https://eveliacoss.github.io/CV/cv_ECoss.html"
```

Modifica tu información y da click en `Knit` para que genere un archivo HTML con tu pagina web. Ejemplo: https://eveliacoss.github.io/

---------------
💜 Nota: Puedes subir todos tus archivos en Github para siempre tenerlo disponible.

Y si llegaste al final 🌟💜 y ahora quieres hacer tu propio Github con tus notas y poner emogis, te dejo esta hermosa pagina que encontre con los emojis. Solo copialos y pegalos sin miedo 😏.

---------------
Cursos hechos con amor 💜
