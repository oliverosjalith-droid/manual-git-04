# comandos basicos git 
Los comandos básicos de Git estructuran el flujo de trabajo diario, desde la configuración inicial del entorno hasta la sincronización distribuida entre colaboradores.

## Configuración e Inicialización

**git config:** Configura las variables globales o locales de Git. Es indispensable al instalarlo por primera vez para asociar tu identidad a cada versión que guardes.

**Uso común:** git config --global user.name *"Tu Nombre"* y git config --global user.email *"tu@email.com"*

**git init:** Convierte una carpeta común de tu sistema en un repositorio local, creando la carpeta oculta .git donde se almacenarán las métricas, ramas e historial.

**git clone <url>:** Descarga una copia exacta de un proyecto alojado en un servidor remoto **(como GitHub)**, incluyendo todo su historial de commits, ramas y archivos.