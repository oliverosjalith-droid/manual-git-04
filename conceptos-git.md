# Conceptos Fundamentales de Git
## ¿Qué es Git?
Git es un sistema de control de versiones distribuido (DVCS) creado por Linus Torvalds en 2005. Permite rastrear cambios en el código fuente durante el desarrollo de software, facilitando el trabajo colaborativo, la reversión de errores y el historial de versiones sin depender de un servidor central obligatorio.
## Estados y Flujo de Trabajo en Git
**Git organiza los archivos en tres áreas principales antes de registrarlos en el historial:**
Working Directory **(Directorio de Trabajo):** Es el entorno local donde creas y modificas los archivos de tu proyecto.

Staging Area **(Área de Preparación / Index):** Es una zona intermedia donde seleccionas y organizas los cambios específicos que formarán parte de la próxima versión.

Repository **(Repositorio / .git):** Es la base de datos donde Git almacena permanentemente el historial de versiones en forma de commits.

## Conceptos Clave
### 1. Repositorio **(Repository)**
Es el espacio de almacenamiento (carpeta) supervisado por Git. Contiene todos los archivos del proyecto, así como la base de datos de historial **(.git).** Puede ser local (en tu computadora) o remoto (alojado en plataformas como GitHub, GitLab o Bitbucket).

### 2. Commit
Es una captura de pantalla **(snapshot)** del estado de tu proyecto en un momento determinado. Cada commit tiene un identificador único **(SHA-1/SHA-256),** un autor, una fecha y un mensaje descriptivo que explica los cambios realizados.

### 3. Rama **(Branch)**
Es una línea de desarrollo independiente. Las ramas permiten trabajar en nuevas funcionalidades, correcciones o experimentos sin alterar la línea de código principal **(generalmente llamada main o master).**

### 4. Fusión **(Merge)**
Es el proceso de integrar los cambios y el historial de una rama hacia otra. Permite unificar el trabajo de diferentes desarrolladores en una sola versión del proyecto.

### 5. Conflicto de Fusión **(Merge Conflict)**
Ocurre cuando Git no puede unificar automáticamente dos líneas de código **(por ejemplo, cuando dos personas editan la misma línea del mismo archivo de forma diferente).** Requiere intervención humana para decidir qué cambios conservar.

## Importancia en el Desarrollo Moderno
**Trazabilidad:** Permite saber quién, cuándo y por qué se realizó un cambio en el código.

**Trabajo en Paralelo:** Múltiples desarrolladores pueden trabajar simultáneamente en el mismo proyecto sin sobrescribir el trabajo de los demás.

**Seguridad y Respaldo:** Permite restaurar versiones anteriores del proyecto ante fallos o errores en producción.

# Conceptos básicos de GitHub

-   **GitHub:** GitHub es un servicio de alojamiento web para repositorios Git. Ofrece funciones adicionales como una interfaz web, seguimiento de incidencias, solicitudes de extracción y herramientas de colaboración.
- 
-   **Repositorio remoto:** Un repositorio remoto es un repositorio Git alojado en un servidor remoto, como GitHub.
- 
-   **Bifurcación:** Bifurcar un repositorio crea una copia personal del repositorio en GitHub. Esto te permite experimentar libremente con los cambios sin afectar al repositorio original.
- 
-   **Solicitud de extracción:** Una solicitud de extracción es un mecanismo para proponer cambios en un repositorio. Permite a los colaboradores notificar a otros sobre los cambios que han realizado y solicitarles que los revisen y los integren al repositorio principal.
- 
-   **Seguimiento de incidencias:** GitHub proporciona un sistema integrado de seguimiento de incidencias para gestionar tareas, errores y solicitudes de nuevas funcionalidades de un proyecto.

## Colaboración con Git y GitHub

-   Agregar colaboradores: Puedes otorgar a otros usuarios de GitHub acceso a tu repositorio como colaboradores, permitiéndoles enviar cambios.

-   Descarga de cambios: Esta función obtiene los cambios de un repositorio remoto y los fusiona con la rama actual.

-   Resolución de conflictos: Los conflictos se producen cuando Git no puede fusionar automáticamente los cambios. Es necesario resolverlos manualmente editando los archivos en conflicto.

-   Revisión de código: GitHub permite a los revisores dejar comentarios y sugerir cambios en las solicitudes de extracción, lo que facilita un proceso de revisión de código colaborativo.

## Flujo de trabajo de Git

-   Inicialización de un repositorio: `git init`inicializa un nuevo repositorio Git en el directorio actual.

-   Agregar y confirmar cambios: `git add`agrega archivos al área de preparación y `git commit`confirma los cambios realizados en el área de preparación en el repositorio.

-   Enviar cambios: `git push`envía las confirmaciones locales a un repositorio remoto.

-   Descarga de cambios: `git pull`obtiene los cambios de un repositorio remoto y los fusiona con la rama actual.

-   Ramificación: `git branch`crea una nueva rama y `git checkout`cambia entre ramas.

-   Fusión: `git merge`combina los cambios de diferentes ramas en una sola rama.

-   Rebase: `git rebase`integra los cambios de una rama en otra moviendo o combinando confirmaciones.

-   Resolución de conflictos: Los conflictos se pueden resolver editando manualmente los archivos en conflicto y confirmando los cambios.

# Comandos de Git

### Configuración:

-   `git config --global user.name "Your Name"`: Establece tu nombre para las confirmaciones de Git.

-   `git config --global user.email "yourname@example.com"`: Configura tu correo electrónico para las confirmaciones de Git.

### Inicialización y clonación del repositorio:

-   `git init`Inicializa un nuevo repositorio Git.

-   `git clone <repository_url>`: Clona un repositorio remoto en tu máquina local.

### Flujo de trabajo básico:

-   `git status`: Muestra el estado del repositorio.

-   `git add <file>`: Agrega un archivo al área de preparación.

-   `git commit -m "Commit message"`: Confirma los cambios en el área de preparación.

-   `git push <remote> <branch>`: Envía confirmaciones a un repositorio remoto.

-   `git pull <remote> <branch>`: Obtiene y fusiona los cambios de un repositorio remoto.

### Ramificación y fusión:

-   `git branch`: Muestra todas las ramas del repositorio.

-   `git branch <branch_name>`: Crea una nueva rama.

-   `git checkout <branch_name>`: Cambia a la rama especificada.

-   `git merge <branch_name>`: Fusiona los cambios de una rama con la rama actual.

-   `git rebase <branch_name>`: Integra los cambios de una rama en otra rama.


### Historial y deshacer:

-   `git log`: Muestra el historial de confirmaciones.

-   `git reset <commit_hash>`: Restablece el repositorio a una confirmación específica.

-   `git stash`: Guarda temporalmente los cambios que no están listos para ser confirmados.


