# 01. Introducción

**unified** es un ecosistema que permite a proyectos como [Gatsby]() convertir Markdown en HTML estático. Muchas de las herramientas que usas actualmente lo usan internamente, como [Nodejs](), [Vercel](), [Netlify](), [Github](), [Mozilla](), [WordPress](), [Adobe](), [Facebook](), [Google](), [Mintter](https://mintter.com) y muchas más.


## ¿Qué es unifiedjs?

Unified es un ecosistema para manipular y procesar ASTs. El ecosistema está formado por programas (llamados plugins) que operan sobre ASTs.

Aprendamos las partes que forman el proceso de transformación y manipulación de los ASTs {{ img:8d2440 }}

Los “Parsers” convierten texto en tokens que juntos conforman un AST. Los “Compilers” convierten AST a texto. Los “transformes” se encargan de manipular, modificar y transformar el AST. Todas estas partes crean lo que se conoce como un “procesador”

Los procesadores son como piezas de lego, uno puede depender de otro y otros pueden depender de él. Es importante que los procesadores sean configurados de una manera predecible, ya que cada uno depende del proceso anterior.

Algunos e los procesadores más famosos son “rehype” (procesador de hast para HTML) y “remark” (procesador de markdown o mdast)

https://github.com/syntax-tree/hast
https://github.com/syntax-tree/mdast

Lo valioso de unified es que todos los ASTs están basados en “unist” (Universal Syntax Tree) que hace mucho más sencillo trabajar con ellos y entre ellos. Puedes explorar aquí todos los paquetes y proyectos compatibles con unified disponibles para usarlos: https://unifiedjs.com/explore/

En otros hilos indagaremos más en detalle sobre cada una de las partes de los procesadores, para #Mintter estamos creando transformadores para pasar nuestro contenido a “mdast”, a “hast” y viceversa.
