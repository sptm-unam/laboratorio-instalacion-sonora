# Laboratorio de Instalación Sonora [^sptm]

Coordinado por Lucía Rodríguez, Homero Guerrero y José Orozco.

Este repositorio despliega el sitio web del laboratorio utilizando
[Github Pages](https://docs.github.com/es/pages).

[^sptm]: Instancia del Seminario Permanente de Tecnología Musical (SPTM) del
semestre 2025-2 de la UNAM.

El objetivo de este sitio es documentar el proceso, trabajo y reflexiones de este
seminario.

Invitamos a todxs lxs particpantes del laboratorio a participar en este ejercicio
de documentación, reflexión y memoria.
A continuación se detallan las instrucciones para contribuir.

## TODO

+ [ ] Subir los videos a servicio externo (¿Archive.org?) para vincularlos. 
Sesiones 6, 7 y 8 (laboratorios de materiales).

## Modificar o añadir contenido

Necesitarás una cuenta de Github. Créala seleccionando el botón correspondiente
en la parte superior de esta página. Además, solicita acceso de escritura
enviando tu nombre de usuarix a
[Xavier Góngora](mailto:xavier.gongora@comunidad.unam.mx).
Procederemos a añadirte a la organización del
[SPTM en Github](https://github.com/sptm-unam).

La forma más fácil de contribuir al contenido de este sitio es modificándolo
directamente _in situ_. Para ello, selecciona el archivo que quieras modificar
y pica el botón con el lápiz (`Edit this file`).
Se abrirá un editor de texto para que añadas o modifiques el archivo
seleccionado.[^git]

[^git]: Para saber más, consulta las referencias sobre el sistema de control
de versiónes `git` que tenemos en
[este](https://github.com/sptm-unam/sptm-docs/blob/main/git_tutorial.md)
repositorio.

El contenido puede ser formateado utilizando la sintaxis de
[Github Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
Sin embargo, **enfócate en el contenido textual**; posteriormente otrx usuarix
puede corregir o añadir el formato.

Una vez que hayas terminado de editar, selecciona el botón `Commit changes...`
y añade un comentario corto y explicativo de las modificaciones que hiciste
en `Commit message`. _Realmente puede ser cualquier cosa_. Puedes dejar vacía la
sección `Extended description`.

Deja seleccionado `Commit directly to the main branch` y finalmente pica
`Commit changes` para que los cambios se reflejen en la página web. Puedes
seleccionar la opción `Create a new branch for this commit and start a pull request`
si quieres que tus modificaciones sean revisadas por lxs administradorxs antes de
integrarse a la página.[^acceso]

[^acceso]: Si no tienes acceso de escritura en el repositorio, no apareceran estas
opciones y en lugar de `Commit changes` aparecerá el botón `Propose changes`.
Puedes utilizar está opción sin problema. Esta crea un _fork_ (una copia de
los archivos y su historia) en tu cuenta de Github automáticamente, desde la
que se proponen los cambios en un _pull-request_ o PR. Le mecánica exacta de
este proceso está más allá del alcance de estas instrucciones; basta saber que
los PR permiten que cualquiera pueda colaborar con un proyecto de código abierto.


## Crear nuevas páginas

Para crear una nueva página en el sitio:

1. Crea un archivo con extensión `.md` en este repositorio, por ejemplo `pagina.md`.
Cerca de uno de los bordes inferiores del tope de la página pica el menú `Add file`
y selecciona una de las opciones (`Create new file` o `Upload file`).
1. Las páginas correspondientes a las sesiones deben ubicarse en el directorio `sesiones`
  y tener por nombre el número de sesión (por ejemplo `1.md`).
1. El contenido de estos archivos puede ser formateado utilizando la sintaxis de
[Github Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
1. Para poder navegar a la nueva página se debe incluir una liga en el archivo `index.md` utilizando la siguiente sintaxis:
`[Texto de la liga](./ruta/a/la/pagina.html)`.
Nota que es necesario cambiar la extensión de `md` a `html`.

## Despliegue local del sitio (opcional)

Para hacer modificaciones más complejas del sitio (por ejemplo, un cambio de tema
o modificar una plantilla), es conveniente hacer un despliegue local de la página
para probar los cambios antes de enviarlos al repositorio remoto.

> [!WARNING]
> Cada _commit_ a la rama _main_ del repositorio (en Github)
> actualiza el sitio web automáticamente.

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
