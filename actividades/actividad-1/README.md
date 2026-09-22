---
description: Aprender a usar Gitbook, investigando qué son las redes.
---

# Actividad 1

Los pasos a seguir para crear el GitBook:

El procedimiento que he utilizado:

1. Crear la cuenta: Accedemos a GitBook y nos registramos con Google.
2. Diseñar la estructura: Tras el paso 1, la aplicación nos pedirá que diseñemos una nueva entidad.
3. Crear el grupo: Después de realizar los pasos anteriores, el programa nos solicitará planear el grupo dentro del cual desarrollaremos nuestras páginas.
4. Desarrollar nuestras páginas: A continuación, hacemos clic en el botón «+» dentro del grupo creado en el paso anterior. Creamos la página, la cual debe aparecer en blanco.
5. Editar la página: Tras crear la página, hacemos clic en el botón _Edit_. En la pestaña que se abre escribimos nuestro texto. En la parte inferior hacemos clic en _Crear solicitud de cambio_ y, finalmente, arriba seleccionamos _Merge_ para guardar la información.
6. Previsualizar y publicar: Para terminar, revisamos que todo esté correcto y sin faltas de ortografía. Después hacemos clic en _Publish_ y el contenido quedará publicado en GitBook.

#### Pasos para conectar GitBook con GitHub

1. Ir a los ajustes del espacio en GitBook:
   * Entra en tu espacio de trabajo de GitBook.
   * En el menú lateral o de configuración, busca la opción Integrations (Integraciones) o GitHub.
2. Autorizar la integración con GitHub:
   * Haz clic en Install GitHub Integration (o _Conectar con GitHub_).
   * Te redirigirá a GitHub para autorizar la aplicación de GitBook (_OAuth Application_).
   * Selecciona si deseas darle acceso a todos los repositorios o únicamente al repositorio específico de tu proyecto.
3. Configurar el repositorio y la rama (_Branch_):
   * Selecciona tu organización o cuenta de usuario de GitHub.
   * Elige el repositorio que quieres vincular (por ejemplo, el de la memoria de tu proyecto).
   * Selecciona la rama principal que quieres sincronizar (habitualmente `main` o `master`).
4. Elegir la dirección de sincronización:
   * Bidireccional (Recomendado): Permite editar tanto desde la interfaz de GitBook como directamente subiendo archivos Markdown en GitHub. Los cambios se actualizarán solos en ambos sitios.
5. Confirmar la sincronización inicial:
   * Haz clic en Sync / Save. GitBook importará los archivos de tu repositorio de GitHub (o exportará el contenido actual de GitBook a GitHub si el repositorio estaba vacío).
