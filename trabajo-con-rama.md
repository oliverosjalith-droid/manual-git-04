# Trabajar-con-Ramas 

Use ramas en GitHub para aislar el trabajo de desarrollo, administrar ramas predeterminadas y colaborar eficazmente mediante solicitudes de incorporación de cambios y protecciones de rama.
Trabajar con ramas (_branches_) en GitHub es un flujo de trabajo que te permite duplicar el código principal de un proyecto para probar nuevas ideas, desarrollar funcionalidades o corregir errores sin alterar la versión estable y funcional (generalmente llamada `main` o `master`). 

##  Acerca de las ramas

Las ramas le permiten desarrollar características, corregir errores o experimentar de forma segura con nuevas ideas en un área independiente del repositorio.
Siempre puedes crear una rama a partir de otra rama existente. Habitualmente, puedes crear una rama nueva desde la rama predeterminada de tu repositorio. Podrás entonces trabajar en esta rama nueva aislado de los cambios que otras personas hacen al repositorio.

# Acerca de la rama predeterminada

Cuando creas un repositorio con contenido en GitHub, GitHub crea el repositorio con una sola rama. Esta primera rama en el repositorio es la rama predeterminada. La rama predeterminada es la rama que GitHub se muestra cuando alguien visita el repositorio. La rama predeterminada también es la rama inicial que Git verifica localmente cuando alguien clona el repositorio. A menos de que especifiques una rama diferente, la rama predeterminada en un repositorio será la rama base para las solicitudes de cambio nuevas y para las confirmaciones de código. 

## Características Principales

-   **Nombre estándar:** Históricamente se llamaba `master`, pero actualmente la norma de la industria y la opción predeterminada en GitHub es **`main`**.
    
-   **Código estable:** Representa la versión principal del proyecto donde converge todo el desarrollo terminado y probado.
    
-   **Base para Pull Requests:** Todas las ramas secundarias se derivan de ella y, al finalizar un trabajo, se busca fusionar los cambios de regreso a esta rama.

## Configuración y Manejo en GitHub

-   **Cambiar la rama predeterminada:** Si prefieres usar otro nombre (por ejemplo, `develop` o `release`), puedes ir a la pestaña **Settings > Branches** de tu repositorio en GitHub y seleccionar otra rama como predeterminada.
    
-   **Protección de rama (_Branch Protection Rules_):** Dado que contiene el código crítico, es una buena práctica activar reglas para evitar que se puedan subir cambios directamente (`git push`). Obliga a que todo cambio pase por un _Pull Request_ e incluya revisión de código. 
