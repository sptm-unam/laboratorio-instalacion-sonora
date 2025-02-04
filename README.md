# Laboratorio de Instalación Sonora

Esta es el sitio web del «Laboratorio de Instalación Sonora», instancias del **Seminario Permanente de Tecnología Musical** del semestre 2025-2 de la UNAM. Coordinado por Lucía Rodríguez, Homero Guerrero y José Orozco.

## Crear nuevas páginas

Para crear una nueva página, basta con crear un archivo con extensión `.md` en este repositorio. Las páginas correspondientes a las sesiones deben ubicarse en el directorio `sesiones` y tener por nombre el número de sesión.

El contenido de estos archivo puede ser formateado utilizando la [sintaxis de Markdown para Github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

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

