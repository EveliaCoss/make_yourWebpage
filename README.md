# Crea tu página web en R

Notas personales recabadas a partir de los tutoriales y ejemplos 😊. Espero que les funcione 💜

Video interactivo y explicativo conmigo en [OneDrive](https://drive.google.com/file/d/1TAgaQlp3EzN5pwZdLfwKPP3vz2EDwkva/view?usp=sharing). 

## Paquetes 📕

Paquetes necesarios para crear tu CV y página web en R.

- [rmarkdown](https://rmarkdown.rstudio.com/articles_intro.html)
- [pagedown](https://github.com/rstudio/pagedown)
- [devtools](https://www.r-project.org/nosvn/pandoc/devtools.html) - Instalacion de paquetes de Github
- [datadrivencv](https://nickstrayer.me/datadrivencv/)
- [postcards](https://github.com/seankross/postcards) - Tutorial del creador del paquete
- [fontawesome(https://rstudio.github.io/fontawesome/) - puedes encontrar la informacion de los iconos en su [pagina web](https://fontawesome.com/icons)

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

Las instrucciones se encuentran en el Github: [Make_yourCV](https://github.com/EveliaCoss/Make_yourCV). De igual manera, puedes seguir las indicaciones dadas en el [video](https://drive.google.com/file/d/1TAgaQlp3EzN5pwZdLfwKPP3vz2EDwkva/view?usp=sharing). 

### 2. Generar un dominio desde Github

Desde tu home de Github, vas a dar click en repositorios y vas a crear un nuevo repositorio con el nombre `Usuario.github.io`. Sin espacios y en vez de `Usuario` vas a escribir el nombre de tu usuario de Github. ejemplo: *`EveliaCoss.github.io`*. Vas a darle que sea     `public` y aceptar. 

Ya que tienes creado el repositorio tendrás en la parte superior un botón que dice *Settings* (un engranaje), vas a dar click y en caso de que te equivoques, aquí podrás editar el nombre en General. Vamos a ubicar el cursor en *Pages*, localizado en el menú de la izquierda. En donde dice *Branch* vas a cambiar la opción de *None a Main*. Automáticamente se activará un nuevo botón que dirá *root* con un símbolo de una carpeta. Da click en **Save**.

![branch](https://github.com/EveliaCoss/make_yourWebpage/blob/main/branch.png)

Actualiza la página y ten paciencia, a veces tarda Github en darte el dominio. Cuando todo esté listo tendrás un link como este https://eveliacoss.github.io/ pero con tu usuario.  

[dominio](https://github.com/EveliaCoss/make_yourWebpage/blob/main/dominio.png)

Posteriormente, tu repositorio tendrá el siguiente símbolo con palomita verde, validando que tienes una página web en Github.

[logo](https://github.com/EveliaCoss/make_yourWebpage/blob/main/logo_githubpages.png)


### 3. Subir a Github el CV


### 4. Crear la pagina web en R


https://github.com/EveliaCoss/EveliaCoss.github.io
https://github.com/EveliaCoss/CV


