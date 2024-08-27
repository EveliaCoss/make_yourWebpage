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

```mermaid
graph TD;
    Crear CV --> B;
    B-->D;
    C-->D;
```







