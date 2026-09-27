# Guía del repositorio

## Estructura del proyecto

Este repositorio contiene la página de invitación al workshop del CEIDEF, en español.

- `index.html` contiene el marcado, los estilos en línea, los valores predeterminados de propiedades editables y el comportamiento en `script[data-dc-script]`.
- `assets/` contiene los logotipos e imágenes utilizados; `uploads/` conserva originales y referencias visuales.
- `support.js` proporciona el motor de renderizado generado; `image-slot.js` implementa el soporte para componentes de imagen.
- `_ds/organic-*/` contiene el sistema de diseño empaquetado, los estilos, el manifiesto y las pautas visuales.
- `README.md` describe el proyecto. No hay un directorio de código fuente separado ni una suite de pruebas.

## Comandos de desarrollo y verificación

Ejecutar desde la raíz del repositorio:

- `python -m http.server 8000 --bind 127.0.0.1`: servir el sitio localmente con Python instalado. Abrir `http://127.0.0.1:8000/` en el navegador.
- `git diff --check`: detectar errores de espacios en blanco antes del commit.
- `git diff --stat`: revisar el alcance de los archivos modificados.

No hay manifiesto de paquetes, compilación ni ejecutor de pruebas configurados. Los archivos se sirven directamente. La cabecera del motor menciona una compilación de `dc-runtime`, cuyo código fuente no está incluido.

## Estilo de código y nombres

Conservar el formato existente: HTML y CSS compactos, JavaScript con sangría. Usar dos espacios en bloques nuevos de JavaScript y evitar reformatear código ajeno al cambio. No hay formateador ni flujo ejecutable de lint configurado para el repositorio.

Mantener los textos en español y los acentos en UTF-8. Seguir los identificadores como `eventos`, las propiedades camelCase como `encuestaUrl` y el prefijo `ceidef-` para recursos de marca y animaciones. Conservar las vinculaciones de plantilla y los atributos `style-hover`. Preferir variables CSS existentes para valores compartidos. No editar manualmente el archivo generado `support.js`.

## Pautas de pruebas

Verificar la presentación en escritorio y móvil, las anclas de navegación, el foco por teclado, el movimiento reducido, las imágenes y la consola del navegador. Comprobar los enlaces de inscripción y encuesta sin enviar formularios. No hay umbral de cobertura ni convención de nombres para pruebas.

## Commits y solicitudes de cambios

El historial usa descripciones breves en español con `feat:` o `Feat:`. Preferir `feat:` para incorporaciones y `fix:` para correcciones.

Mantener cada commit enfocado. Las solicitudes deben describir el cambio, enlazar incidencias relacionadas, indicar verificaciones manuales e incluir capturas de escritorio y móvil para cambios visuales. Al modificar URLs de formularios, actualizar los valores predeterminados de propiedades y los valores alternativos de JavaScript en `index.html`.
