# Curso de Python (Template)

![example workflow](https://github.com/fralfaro/DS-Python-Course/actions/workflows/documentation.yml/badge.svg)
<a href="https://fralfaro.github.io/DS-Python-Course/"><img alt="Link a la Documentación" src="https://img.shields.io/badge/docs-link-brightgreen"></a>


## Descripción del Repositorio

```
|
├───.github
│   └───workflows
│           documentation.yml
│
├────docs
│   ├───.images
│   │       logo.bmp
│   │       logo_python.svg
│   │
│   │   basic.ipynb
│   │   index.md
│   │   intro.ipynb
│   │   pandas.ipynb
│   │   seaborn.ipynb
│   │   __init__.py
│   
│   .gitignore
│   LICENSE
│   mkdocs.yml
│   poetry.lock
│   pyproject.toml
│   README.md
```

donde:

* `documentation.yml`: archivo para generar el CI del proyecto.
* `docs`: carpeta donde se almacenan los jupyter notebooks.
  * `images`: carpeta con las imagenes del *logo* y el *favicon*. 
  * `index.md`: archivo markdown inicial.
  * `*.ipynb`: archivos jupyter notebook.
* `.gitignore`: lugar donde se define los archivos a ignorar.
* `LICENSE`: licencia asociada al proyecto.
* `mkdocs.yml`: archivo que orquestará la documentación del proyecto.
* `poetry.lock`: archivo que orquestará el proyecto y sus dependencias.
* `pyproject.toml`: archivo que orquestará el proyecto y sus dependencias.
* `README.md`: archivo que describe el repositorio.

## Archivos a modificar

### [Readme.md](README.md)

```
![example workflow](https://github.com/fralfaro/DS-Python-Course/actions/workflows/documentation.yml/badge.svg)
<a href="https://fralfaro.github.io/DS-Python-Course/"><img alt="Link a la Documentación" src="https://img.shields.io/badge/docs-link-brightgreen"></a>
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-Python-Course**: nombre del curso.

### [`mkdocs.yml`](mkdocs.yml)

**Sección**: Project information - Repository

```
# Project information
site_name: Home
site_url: https://github.com/fralfaro/DS-Python-Course
site_author: Francisco Alfaro
site_description:

# Repository
repo_name: fralfaro/DS-Python-Course
repo_url: https://github.com/fralfaro/DS-Python-Course
edit_uri: ''
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-Python-Course**: nombre del curso.
* **site_author**: Nombre del autor

**Sección**: Theme

```
# Theme
theme:
  name: material
  language: es
  logo: images/logo.bmp
  favicon: images/logo_python.svg
```
Debe cambiar:

* **favicon**: imagen a utilizar como *favicon*.

**Sección**: Customization

```
# Customization
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/fralfaro
    - icon: fontawesome/brands/linkedin
      link: https://www.linkedin.com/in/faam/
    - icon: fontawesome/solid/globe
      link: https://fralfaro.github.io/portfolio/
```
En esta sección se agregan las redes sociales 
que ustedes maneja (más detalles, 
ver el siguiente [link](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/#with-animations)).

**Sección**: TOC

```
# TOC
nav:
    - Home: index.md
    - Conceptos Básicos:
        - intro.ipynb
        - basic.ipynb
    - Manipulación Datos:
        - pandas.ipynb
        - seaborn.ipynb
```

En esta sección se agregan los archivos `.ipynb` que necesita agregar a su documentación.

### Otros

#### [`pyproject.toml`](pyproject.toml)

```
[tool.poetry]
name = "docs"
version = "0.1.0"
description = "mkdocs - courses"
authors = ["Francisco Alfaro <francisco.alfaro.496@gmail.com>"]
license = "MIT"
readme = "README.md"
```

Cambiar `authors` por su nombre y correo personal.

#### [`index.md`](docs/index.md)

```
# Home

Introducción básica a Python

## Material

El material está disponible en el siguiente [repositorio](https://github.com/fralfaro/DS-Python-Course), para obtener el código de fuente basta con que ejecutes el siguiente comando:


> `https://github.com/fralfaro/DS-Python-Course`


## Contenidos temáticos

* Introducción a Python
* Nomenclatura
* Introducción Pandas
* Introducción Seaborn
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-Python-Course**: nombre del curso.


> **Nota**: Si necesita customizar su repositorio, se recomienda leer el siguiente [link](https://squidfunk.github.io/mkdocs-material/).


