# Calistenia Militar Android V4

Proyecto Android para celular, tablet y Android TV/Google TV.

## Compilación automática con GitHub Actions

Este proyecto incluye el workflow:

`.github/workflows/build-apk.yml`

Cada vez que se haga `push` al repositorio, GitHub Actions compilará automáticamente una APK Debug y la guardará como artefacto descargable. También se puede ejecutar manualmente desde la pestaña **Actions** de GitHub.

El workflow usa Java 17 y Gradle 9.5. Android Gradle Plugin 9.3 requiere Gradle 9.5 o superior.

### Cómo usarlo

1. Crea un repositorio nuevo en GitHub, por ejemplo `calistenia-militar-android`.
2. Sube **el contenido de esta carpeta**, incluyendo `.github/workflows/build-apk.yml`.
3. Abre la pestaña **Actions**.
4. Entra en **Compilar APK Android**.
5. Pulsa **Run workflow** si quieres iniciar la compilación manualmente.
6. Cuando termine correctamente, abre la ejecución y descarga el artefacto **Calistenia-Militar-V4-debug**.
7. Descomprime el artefacto y encontrarás `app-debug.apk`.
8. Instala esa APK en el teléfono/tablet Android.

La APK Debug está firmada automáticamente con la clave de depuración y es adecuada para pruebas e instalación directa. Para Google Play necesitaremos posteriormente una compilación Release firmada con una clave privada propia.

## Nota

El reconocimiento por cámara utiliza la lógica incluida en `app/src/main/assets/index.html`. La aplicación solicita permiso de cámara de forma nativa cuando el reconocimiento necesita acceder a ella.
