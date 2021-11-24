# Guía instalación de TailwindCSS en Ruby on Rails
El proceso de instalación es diferente dependiendo el entorno de desarrollo y puede llegar a sacar dolores de cabeza, pero no te desanimes son dos tecnologías increíbles, son de mis favoritas, espero que esta guía te evite algunos y que realmente te sea de utilidad.

### Desde tu consola o cmd
```sh
rails webpacker:install:stimulus
```
#### Instala via npm
```sh
npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat @tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9
```
### En la ruta: app/javascrip/stylesheets/
#### Crea el archivo application.scss y agrega las siguientes lineas:
```sh

@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities"; 
```
### En la ruta app/javascript/packs/
#### Agrega al archivo application.js lo siguiente:
```sh

require("stylesheets/application.scss")
```
### En la ruta app/views/layouts/
#### Agrega al archivo application.html.erb la siguiente linea:
```sh


<%= stylesheet_link_tag 'application', media: 'all', 'data-turbolinks-track': 'reload' %>
```
### En el archivo  postcss.config.js agrega la siguiente linea: 
```sh

require('tailwindcss'),

```
### Desde tu consola o cmd
#### * Omitir "ruby" sino se trabaja con Windows
```sh


 ruby bin\webpack

```
#### Por último ejecuta
```sh

yarn install --check-files

```
## ¿Te puedo ayudar?
#### Si tienes alguna duda me puedes contactar por Twitter: Daniel JS  [@peRKurgtZSaN](https://twitter.com/peRKurgtZSaN)
