# Laboratorio de Instalación Sonora

Esta es el sitio web del «Laboratorio de Instalación Sonora», instancia del **Seminario Permanente de Tecnología Musical** del semestre 2025-2 de la UNAM. Coordinado por Lucía Rodríguez, Homero Guerrero y José Orozco.

A continuación encontrarás instrucciones para contribuir a este repositorio.

## Modificar o añadir contenido

Necesitarás una cuenta de Github. Créala seleccionando el botón correspondiente
en la parte superior de esta página.

La forma más fácil de contribuir al contenido de este sitio es modificándolo
directamente _in situ_. Para ello, selecciona el archivo que quieras modificar
y pica el botón con el lápiz (`Edit this file`).

El contenido puede ser formateado utilizando la sintaxis de
[Github Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
**Enfócate en el contenido textual**; posteriormente otrx usuarix o unx
administradorx puede corregir o añadir el formato.

Una vez que hayas terminado de editar, selecciona el botón `Commit changes...`
y añade un comentario corto y explicativo de las modificaciones que hiciste
en `Commit message`. _Realmente puede ser cualquier cosa_. Puedes dejar vacía la
sección `Extended description`.

Deja seleccionado `Commit directly to the main branch` y finalmente pica
`Commit changes` para que los cambios se reflejen en la página web. Puedes
seleccionar la opción `Create a new branch for this commit and start a pull request`
si quieres que tus modificaciones sean revisadas por lxs administradorxs antes de
integrarse a la página.

## Crear nuevas páginas

Para crear una nueva página en el sitio:

1. Crea un archivo con extensión `.md` en este repositorio, por ejemplo `pagina.md`.
  + Cerca de uno de los bordes inferiores del tope de la página pica el menú `Add file`
    y selecciona una de las opciones (`Create new file` o `Upload file`).
1. Las páginas correspondientes a las sesiones deben ubicarse en el directorio `sesiones`
y tener por nombre el número de sesión (por ejemplo `1.md`).
1. El contenido de estos archivo puede ser formateado utilizando la sintaxis de
[Github Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
1. Para poder navegar a la nueva página se debe incluir una liga en el archivo `index.md` utilizando la siguiente sintaxis:
`[Texto de la liga](./ruta/a/la/pagina.html)`.
Nota que es necesario cambiar la extensión de `md` a `html`.

## Despliegue local del sitio (opcional)

Para hacer modificaciones más complejas del sitio (por ejemplo, un cambio de tema
o modificar una plantilla), es conveniente hacer un despliegue local de la página
para probar los cambios antes de enviarlos al repositorio remoto.

> [!WARNING]
> Todo _commit_ a la rama _main_ del repositorio remoto (en Github)
> inicia un despliegue del sitio web.

Primero instala `bundler` (similar en funcionalidad a `npm` para JavaScript),
utilizando `rubygems` (administrador de paquetes de Ruby).[^ruby]

[^ruby]: Ruby se puede instalar utilizando el administrador de paquetes en Linux
  o [Homebrew](https://brew.sh/) en MacOS.
  Alternativamente se puede descargar directamente de su
  [sitio](https://rubygems.org/pages/download)
  y seguir las instrucciones.

``` shell
gem install bundler
```

Posteriormente instala todas las dependencias de la página.

``` shell
bundle install
```

Finalmente, se puede hacer un despliegue local con la opción `--livereload` para
que el sitio se actualice automáticamente con cada cambio guardado.

``` shell
bundle exec jekyll serve --livereload
```

Se puede acceder al sitio poniendo la siguiente dirección en el navegador:
`http://127.0.0.1:4000/`
