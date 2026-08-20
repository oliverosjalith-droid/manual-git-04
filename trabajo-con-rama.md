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

# Trabajar con ramas protegidas

Las ramas protegidas ayudan a los mantenedores a aplicar reglas en ramas importantes. Una rama protegida puede bloquear las inserciones o eliminaciones forzadas, requerir comprobaciones de estado, requerir revisiones, requerir aprobación del propietario del código o requerir confirmaciones firmadas antes de que los cambios se puedan combinar.

Estas protecciones ayudan a los equipos a mantener las ramas importantes estables y hacer que las expectativas sean claras antes de combinar una solicitud de incorporación de cambios.

## Reglas de Protección más Comunes

-   **Requerir Pull Request antes de fusionar:** Nadie puede hacer un `git push` directo a la rama. Todo cambio debe enviarse mediante un _Pull Request_ (PR).
    
-   **Aprobaciones obligatorias:** Exige que uno o más miembros del equipo revisen y aprueben el PR antes de hacer el _merge_.
    
-   **Comprobaciones de estado exitosas (_Status Checks_):** Exige que las pruebas automáticas (CI/CD) pasen sin errores antes de permitir la integración.
    
-   **Restringir quién puede hacer _push_ o _merge_:** Permite definir qué usuarios, equipos o roles tienen permiso para autorizar cambios.
    
-   **Bloquear eliminaciones y _force push_:** Evita que se elimine la rama por error o que se sobrescriba el historial de commits.

## Flujo de Trabajo en una Rama Protegida 
-   **Intento de push denegado:** Si intentas subir cambios directo con `git push origin main`, GitHub rechazará el comando.
    
-   **Crear rama secundaria:** Trabajas tus cambios en una rama independiente (`git checkout -b feature/nueva-funcion`).
    
-   **Subir rama y abrir PR:** Subes tu rama local (`git push origin feature/nueva-funcion`) y abres un Pull Request hacia la rama protegida en la web de GitHub.
    
-   **Revisión y pruebas:** Tu equipo revisa el código y las pruebas automáticas se ejecutan.
    
-   **Fusión (_Merge_):** Una vez cumplidos todos los requisitos, se habilita el botón de _Merge_ para integrar los cambios.

## Cómo Configurar una Rama Protegida en GitHub

1.  Ve a la pestaña **Settings** dentro de tu repositorio.

2.  En el menú lateral izquierdo, selecciona **Branches**.

3. Haz clic en **Add branch protection rule** (o edita una existente).

4.   Escribe el nombre o patrón de la rama (por ejemplo, `main`).

5.  Marca las reglas que deseas aplicar (ej. _Require a pull request before merging_) y guarda los cambios.

## Tipos de Ramas según su Propósito **(Estrategia de Trabajo)**

|tipo de rama|proposito y funcion |vida util|
|---|---|---|
|Main / Master|Contiene el código oficial y estable que está (o irá) a producción.|Permanente|
|Develop|Sirve como rama de integración para acumular todas las nuevas funciones antes de lanzarlas.|permanente|
|Feature **(feature/***)|Se usa para construir una funcionalidad específica (ej: feature/login-google).|Temporal (se elimina al fusionarse)|
|Hotfix **(hotfix/***)|Permite corregir errores críticos directamente sobre producción sin esperar el flujo normal.|Temporal (se fusiona a main y develop)|
|Release **(release/***)|Se utiliza para preparar, probar y ajustar un lanzamiento formal a producción.|Temporal|