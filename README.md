# Práctica [Jekyll, GitHub Pages y Netlify](https://ull-esit-gradoii-pl.github.io/practicas/jekyll-netlify) 
## Procesadores de lenguajes 2020-21
### Daniel del Castillo de la Rosa
## Resumen de lo aprendido
En esta práctica se ha hecho uso de las siguientes herramientas:
* [Jekyll](https://jekyllrb.com/). Un generador de páginas estáticas escrito en Ruby
* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/). Un tema para Jekyll, que ha facilitado gran parte del trabajo
* [GitHub Pages](https://pages.github.com/). El servicio de hosting para páginas estáticas de GitHub
* [Netlify](https://www.netlify.com/). Otro servicio de hosting para páginas estáticas
* [Liquid](https://jekyllrb.com/docs/step-by-step/02-liquid/). El lenguaje de 'templating' usado por Jekyll
* [Html proofer](https://github.com/gjtorikian/html-proofer). Una herramienta que permite testear ficheros HTML
## Despliegue de la página
La página se ha desplegado en [GitHub Pages](https://ull-esit-pl-2021.github.io/jekyll-github-pages-y-netlify-Daniel-del-Castillo/) y en [Netlify](https://daniel-page.netlify.app/)
Para el despliegue en GitHub Pages hubo que configurar correctamente los campus url y baseurl de la configuración de Jekyll. [Esta explicación](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#site-base-url) ayudó mucho. A la hora de desplegar en Netlify esa configuración también tenía que alterarse, por lo que se creó otra rama que solo difiere en esta cuestión para su despliegue en netlify
## Testeo de la página
Para testear la página se ha usado html-proofer, también se ha añadido CI para que se ejecute cada vez que hay un push.
## Uso de categorías y collections
En la página se ha creado una categoría llamada `blogs` y una colección llamada `languages`, para aprender como funciona cada una
## Uso de layouts
Se ha creado un layout para `blogs` y un layout para `languages`. Estos poseen distintas carecterísticas, por ejemplo los posts de tipo `language` poseen una lista de los post que hacen referencia a ese lenguaje.
## 404
Se ha creado una página personalizada de 404 que te muestra una foto de un samoyedo y una cita aleatoria.
## Páginas resumen
También se han creado dos páginas que, respectivamente, agrupan todos los `blogs` y todos los `languages` haciendo uso de liquid.
## Uso de Liquid
Aquí se puede ver un ejemplo de uso de Liquid que permite a una página listar links para cada uno de los `blogs` que hay
```html
{% assign blogs = site.categories["blogs"] %}

<ul reversed>
{%- for blog in blogs %}
    <li>  
        <a href="{{site.baseurl}}{{ blog.url }}">{{ blog.title }}</a> 
    </li>
{%- endfor %}
</ul>
```
## Añadir comentarios
También se ha añadido un sistema de comentarios usando [utterances](https://github.com/utterance/utterances) como proveedor
