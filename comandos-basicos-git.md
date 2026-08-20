# comandos basicos git 
Los comandos básicos de Git estructuran el flujo de trabajo diario, desde la configuración inicial del entorno hasta la sincronización distribuida entre colaboradores.

## Configuración e Inicialización

**git config:** Configura las variables globales o locales de Git. Es indispensable al instalarlo por primera vez para asociar tu identidad a cada versión que guardes.

**Uso común:** git config --global user.name *"Tu Nombre"* y git config --global user.email *"tu@email.com"*

**git init:** Convierte una carpeta común de tu sistema en un repositorio local, creando la carpeta oculta .git donde se almacenarán las métricas, ramas e historial.

**git clone <url>:** Descarga una copia exacta de un proyecto alojado en un servidor remoto **(como GitHub)**, incluyendo todo su historial de commits, ramas y archivos.

## inspección e Historial

**git status:** Informa el estado actual del proyecto. Muestra qué archivos han sido modificados, cuáles están listos para ser guardados ***(staged)*** y cuáles no están siendo rastreados ***(untracked).***

**git log:** Muestra la lista cronológica de commits realizados en la rama actual, incluyendo el identificador hash, autor, fecha y mensaje.

**Variación útil:** git log *--oneline --*graph muestra una vista compacta y gráfica de las ramas.

**git diff:** Compara las diferencias de código línea por línea entre el directorio de trabajo y el área de preparación ***(staging)***, o entre dos commits específicos.

## Gestión de Cambios **(Staging y Commit)**

**git add <archivo>:** Traslada los cambios del directorio de trabajo al Staging Area ***(preparación)***. Puedes añadir un archivo específico o usar git add . para incluir todas las modificaciones pendientes.

**git commit -m "mensaje":** Guarda permanentemente en el historial los cambios almacenados en el área de preparación. El mensaje debe ser breve pero descriptivo respecto a qué se implementó o corrigió.

**git restore <archivo>:** Descarta las modificaciones locales no guardadas en el directorio de trabajo, regresando el archivo a su estado en el último commit.