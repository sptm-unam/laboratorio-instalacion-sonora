# Laboratorio de Instalación Sonora

Esta es el sitio web del «Laboratorio de Instalación Sonora», instancia del **Seminario Permanente de Tecnología Musical** del semestre 2025-2 de la UNAM. Coordinado por Lucía Rodríguez, Homero Guerrero y José Orozco.

## Crear nuevas páginas

Para crear una nueva página: 

1. Crear un archivo con extensión `.md` en este repositorio, por ejemplo `pagina.md`. Las páginas correspondientes a las sesiones deben ubicarse en el directorio `sesiones` y tener por nombre el número de sesión (por ejemplo `1.md`). El contenido de estos archivo puede ser formateado utilizando la [sintaxis de Markdown para Github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
1. Para poder navegar a la pagina desde el inicio se debe incluir una liga en el archivo `index.md` utilizando la sintaxis de Markdown: `[Texto de la liga](./ruta/a/la/pagina.html)`. Es necesario cambiar la extensión de `md` a `html`.

## Despliegue local del sitio

En caso de querer hacer modificaciones más complejas del sitio, es conveniente hacer un despliegue local de la página para poder probar los cambios antes de hacerlos en el repositorio remoto.

Para ello es necesario tener instalado Bundler (similar en funcionalidad a `npm` para JavaScript), que se instala utilizando `rubygems` (administrador de paquetes de Ruby).

``` shell
$ gem install bundler
```

Posteriormente es necesario instalar todas las dependencias de la página.

``` shell
$ bundle install
```

Finalmente, se puede hacer un despliegue local (por defecto a la dirección local `http://127.0.0.1:4000/`).

``` shell
$ bundle exec jekyll serve --livereload
```

