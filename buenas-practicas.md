# Buenas prácticas de Git

## 1.  ¿Qué es Git? ##

Git es un sistema de control de versiones que permite registrar y administrar los cambios realizados en un proyecto, especialmente en proyectos de programación. Fue creado para facilitar el trabajo de los desarrolladores y permitir que varias personas puedan trabajar sobre el mismo proyecto sin perder los cambios realizados.

Git permite guardar diferentes versiones de un proyecto, regresar a versiones anteriores y conocer qué cambios hizo cada integrante del equipo.

## 2. ¿Qué son las buenas prácticas de Git?

Las buenas prácticas de Git son un conjunto de recomendaciones que ayudan a mantener un proyecto organizado, seguro y fácil de mantener. También facilitan el trabajo en equipo y disminuyen la posibilidad de cometer errores o perder información.

## 3. Principales buenas prácticas

1. Utilizar mensajes de commit claros

Cada vez que se realiza un cambio importante se debe crear un commit. El mensaje debe explicar brevemente qué se modificó.
Ejemplo:

git commit -m "Agrega formulario de registro"

Es mejor evitar mensajes poco claros como:

git commit -m "cambios"

Actualmente, Editor Markdown es compatible con:

* GitHub
* Dropbox
* Bitbucket

Desde Editor Markdown también puedes redactar artículos en Medium.

Actualmente puedes exportar tus archivos a estos formatos:

* PDF
* HTML
* Markdown
2. Hacer commits pequeños y frecuentes

Es recomendable realizar commits cada vez que se completa una modificación específica. No es conveniente esperar hasta terminar todo el proyecto para hacer un único commit.

Esto permite identificar fácilmente cuándo y dónde ocurrió un problema.

3. Utilizar ramas (branches)

Las ramas permiten desarrollar nuevas funciones o realizar modificaciones sin afectar directamente la versión principal del proyecto.

Por ejemplo:

main: versión principal y estable.
develop: desarrollo del proyecto.
feature/login: creación del sistema de inicio de sesión.
fix/error-login: corrección de un error.

4. Mantener actualizada la rama local

Antes de comenzar a trabajar es recomendable obtener los cambios más recientes del repositorio remoto.

Por ejemplo:

git pull

Esto ayuda a evitar trabajar sobre una versión antigua del proyecto y reduce conflictos.

5. No subir contraseñas ni información privada

Nunca se deben subir al repositorio contraseñas, claves API, tokens, archivos de configuración con información privada o cualquier otro dato sensible.

Para evitarlo se puede utilizar un archivo .gitignore, que indica a Git qué archivos o carpetas no debe incluir en los commits.

6. Revisar los cambios antes de hacer commit

Antes de guardar los cambios es recomendable comprobar qué archivos fueron modificados.

Se puede utilizar:

git status

Y para revisar las diferencias:

git diff

Esto permite detectar errores antes de enviar los cambios al repositorio.

7. Utilizar nombres descriptivos para las ramas

Los nombres de las ramas deben indicar claramente el objetivo de la modificación.

Por ejemplo:

feature/registro-usuarios

es más descriptivo que:

rama1

8. Hacer Pull Request o Merge Request

Cuando se trabaja en equipo, es recomendable revisar los cambios antes de incorporarlos a la rama principal. Para esto se utilizan los Pull Requests o Merge Requests.

Esto permite que otros integrantes revisen el código, encuentren errores y hagan sugerencias antes de aprobar los cambios.

9. Evitar trabajar directamente sobre main

En proyectos colaborativos es recomendable utilizar ramas para desarrollar nuevas funciones y posteriormente integrarlas a main. De esta manera se protege la versión estable del proyecto.

10. Documentar adecuadamente el proyecto

Es recomendable mantener actualizado un archivo como README.md, donde se explique qué hace el proyecto, cómo instalarlo, cómo ejecutarlo y cuáles son sus principales características.

##  Comandos básicos de Git ##
| Comando      | Función                                           |
| ------------ | ------------------------------------------------- |
| `git init`   | Crea un nuevo repositorio Git                     |
| `git clone`  | Copia un repositorio existente                    |
| `git status` | Muestra el estado de los archivos                 |
| `git add`    | Prepara archivos para un commit                   |
| `git commit` | Guarda los cambios en el historial                |
| `git push`   | Envía cambios al repositorio remoto               |
| `git pull`   | Descarga e integra cambios del repositorio remoto |
| `git branch` | Permite administrar ramas                         |
| `git switch` | Permite cambiar de rama                           |
| `git merge`  | Une los cambios de una rama con otra              |
| `git log`    | Muestra el historial de commits                   |


##  Importancia de las buenas prácticas

Aplicar buenas prácticas de Git permite trabajar de manera más organizada y segura. En proyectos donde participan varias personas, estas prácticas ayudan a evitar conflictos, identificar errores, conocer el historial del proyecto y recuperar información cuando sea necesario.

Además, aprender a utilizar Git correctamente es importante para los desarrolladores de software, ya que es una herramienta ampliamente utilizada en proyectos profesionales.

# Conclusión #

Git es una herramienta fundamental para el desarrollo de software porque permite controlar y organizar las diferentes versiones de un proyecto. Sin embargo, utilizar Git no consiste únicamente en ejecutar comandos, sino también en seguir buenas prácticas como realizar commits claros, utilizar ramas, revisar los cambios, mantener actualizado el repositorio y proteger la información privada.

![buenas practicas](image.png)
