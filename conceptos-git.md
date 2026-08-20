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

