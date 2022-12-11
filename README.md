# PracticalEvaluation
Public repository that contains the resolutions of the exercises from ProContacto.

## Exercise 1

El presente ejercicio busca realizar la instalación del ambiente para el desarrollo del trabajo práctico. A continuación se listará una serie de aplicaciones a instalar.

 ### Resolution
  
  **Proceso de instalación del IDE Visual Studio Code.**
![Captura de Pantalla 2022-12-10 a la(s) 18 41 56](https://user-images.githubusercontent.com/104602118/206881104-146df002-2977-4b20-94cc-ed67935a21bc.png)
  Click en el botón "Descargar" para el SO deseado (MacOS en este caso).
  
  **Visualización de la interfaz de usuario.**
  
  ![Captura de Pantalla 2022-12-10 a la(s) 18 43 34](https://user-images.githubusercontent.com/104602118/206881191-594b55df-c4b0-4f14-b8f1-b62e7bbd8325.png)

  **Proceso de instalación de Git y Git Bash**
  
  En este caso, al ser usuario de MacOS, no es necesario descargar alguna version de GIT Bash, puesto que, la terminal del MacOs ya cuenta con las herramientas necesarias para trabajar con GitHub, GitLab, BitBucket, etc.
  ![Captura de Pantalla 2022-12-10 a la(s) 18 49 23](https://user-images.githubusercontent.com/104602118/206881262-574e818f-6423-4bb0-a987-65cb31d60d68.png)

## Exercise 2

Las siguientes preguntas están orientadas a la comprensión del protocolo HTTP. Son agnósticas al lenguaje de programación, la idea es comprender los conceptos del estándar:

**1. ¿Qué es un servidor HTTP?**

> Un servidor HTTP es una pieza de software capaz de comprender URLs (direcciones web) y HTTP (el protocolo que tu navegador usa para obtener las páginas web). Un servidor HTTP puede ser accedido a través de los nombres de dominio de los sitios web que aloja, y entrega el contenido de esos sitios web alojados al dispositivo del usuario final. - Mozilla Developer Network.

En pocas palabras, un *servidor HTTP* es la parte del software que nos permite navegar por las páginas web que estén disponibles, esto mediante su protocolo de comunicación y varias reglas y validaciones internas.

Al nivel más básico, cuando un navegador necesita un archivo que está almacenado en un servidor web, el navegador requerirá el archivo al servidor mediante el protocolo HTTP. Cuando la petición alcanza al servidor web correcto (hardware), el servidor HTTP (software) acepta la solicitud, encuentra el documento requerido y lo envía de regreso al navegador, tambien a través de HTTP. (Si el servidor no encuentra el documento requerido, devuelve una respuesta **404** en su lugar.)

**2. ¿Qué son los verbos HTTP? Mencionar los más conocidos.**

> HTTP define un conjunto de métodos de petición para indicar la acción que se desea realizar para un recurso determinado. Aunque estos también pueden ser sustantivos, estos métodos de solicitud a veces son llamados HTTP verbs. -Mozilla Developer Network.

Podemos pensar en una petición HTTP como si tu navegador se conectara al servidor y le pidiera un recurso específico o le enviara datos. Hay varios tipos de métodos de petición HTTP, que modifican completamente el tipo de respuesta que obtienes del servidor.

Dentro de las peticiones en HTTP se encuentran los verbos:
- Get
- Head
- Connect
- Post
- Put
- Patch
- Trace
- Options
- Delete

Destacando **GET**, **POST** y **DELETE** que probablemente son los más utilizados.

**3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?**

- Petición o request: es la primera parte del proceso, donde la parte cliente hace una petición o request que llegará al servidor web.
- Respuesta o response: es la solución que brinda el servidor web después de hacer lo que necesita para darle respuesta. Aquí puede ejecutar un programa que tenga instalado, consultar una base de datos o cualquier otro archivo, entre otras herramientas. Una vez haya recogido la información, la unirá en el formato solicitado y la devolverá como respuesta.

> Las cabeceras HTTP contienen información de metadatos como, por ejemplo, información de autenticación de seguridad, el agente que se utiliza y los metadatos de control de la memoria caché. En la aplicación HTTP se definen cabeceras HTTP; sin embargo, puede utilizar cabeceras HTTP personalizadas, si fuera necesario. - IBM

Las cabeceras y los códigos de estado HTTP resultan útiles como ayuda para programas intermediarios y clientes a la hora de comprender la información sobre solicitudes y respuestas de aplicaciones. Las cabeceras HTTP contienen información de metadatos. Los códigos de estado HTTP proporcionan información de estado sobre la respuesta.

**4.	¿Qué es un queryString? (En el contexto de una url)**

Las Query String o cadenas de consultas es un término que se utiliza para hacer referencia a una interacción con una base de datos. Además, es la parte de una URL que contiene los datos que deben pasar a las aplicaciones web.

En resumen, las Query String permiten acceder a páginas web dinámicas con distintas variables consiguiendo así que las páginas web no estén compuestas de decenas de directorios y permitiendo que su estructura esté basada en URLs amigables.

Para evitar crear miles de directorios con las diferentes variables y crear megadirectorios de URLs se crearon las Query string con el fin de realizar consultas a las bases de datos y pintar los datos en URLs amigables.

De este modo, mediante el método GET podrás ver en internet URLs del tipo:

+ midominio.com/camiseta-roja (Para ver una camiseta roja de algodón talla M)

Sin tener que que ver algo como:

+ midominio.com/camiseta-roja?talla=m&material=algodon

**5. Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?**

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. Las respuestas se agrupan en cinco clases:

+ Respuestas informativas (100–199),
+ Respuestas satisfactorias (200–299),
+ Redirecciones (300–399),
+ Errores de los clientes (400–499),
+ y errores de los servidores (500–599).

**6.	¿Cómo se envía la data en un Get y cómo en un POST?**

La diferencia entre los métodos get y post radica en la forma de enviar los datos a la página cuando se pulsa el botón “Enviar”. Mientras que el método GET envía los datos usando la URL, el método POST los envía de forma que no podemos verlos (en un segundo plano u "ocultos" al usuario).

+ Un resultado usando el método GET, a modo de ejemplo, podría ser el siguiente:

http://www.aprenderaprogramar.com/newuser.php?nombre=Pepe&apellido=Flores&email=h52turam%40uco.es&sexo=Hombre

+ Un ejemplo de uso del método post sería este:

`<form action="http://www.aprenderaprogramar.com/prog/newuser" method ="post">`

**7.	¿Qué verbo http utiliza el navegador cuando accedemos a una página?**

En primera instancia, cuando accedemos a una página web se utiliza el método GET, sin embargo, también estamos habilitados a usar el método POST en ciertas ocasiones dentro de las peticiones de HTTP.

**8.	Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.**

+ XML (Extensible Markup Language):

Este estándar está desarrollado por la w3c y fue creado a partir del lenguaje SGML , con el fin de adecuarlo al uso web.

XML es uno de los formatos más utilizados para el intercambio de información entre sistemas. El formato de este estándar está basado en texto para representar información estructurada: datos, documentos, configuración, etc...

Por ejemplo, tenemos este bloque de información en formato XML:
~~~
<pieza tipo="A">
    <nombre>Tornillo</nombre>
    <descripcion>Cilindro mecanico con una cabeza utilizado en la fijación temporal de unas piezas con otras 
    </descripcion>
    <caracateristica>
        <tipo>metal</tipo>
        <tamanyo>10</tamanyo>
    </caracateristica>
    <vacio></vacio>
</pieza>
~~~

Este formato de texto es muy parecido al HTML, pero XML es más riguroso. Todas las etiquetas se deben cerrar, cosa que no es obligatorio en HTML y si existe un error en el XML las herramientas que los procesan darán error.

+ JSON (JavaScript Object Notation):

Años más tarde salió este formato de intercambio de información más legible por el ser humano e igual de eficaz que XML para la comunicación entre maquinas. Este estándar esta mantenido por ECMAInternational y está basado en un subconjunto del lenguaje de programación JavaScript (ECMA-262). Como el anterior estándar es independiente del lenguaje de programación y del sistema operativo que lo ejecute.

Veamos el ejemplo anterior pero en JSON:

~~~
{
    “pieza”: {
        “tipo”: “A”
        “nombre”: “Tornillo”,
        “descripcion”: “Cilindro mecánico con una cabeza utilizado en la fijación temporal de unas piezas con otras”,
        “caracteristica”: {
            “tipo”: “metal”
            “tamanyo”: 10
        },
        “vacio”: “”
     }
}
~~~

**9.	Explicar brevemente el estándar SOAP.**

**SOAP** es un estándar basado en XML para la transmisión de mensajes en HTTP y otros protocolos de Internet. Es un protocolo ligero para el intercambio de información en un entorno descentralizado y distribuido. Se basa en XML y consta de tres partes:

- Un sobre que define una infraestructura para describir el contenido del mensaje y cómo procesarlo.
- Un conjunto de normas de codificación para expresar instancias de tipos de datos definidos por la aplicación.
- Una convención para representar llamadas y respuestas a procedimiento remoto.

**10. Explicar brevemente el estándar REST full.**

Una API **REST** es una forma de permitir que diferentes programas de ordenador se comuniquen entre sí a través de Internet. Ya que la comunicación debe darse a través de protocolos y estándares para enviar y recibir datos, estas APIs están diseñadas bajo los principios de REST (que significa Representational State Transfer) y son útiles para interacciones simples. En otras palabras, son el puente de comunicación entre frontend y backend.

Usualmente los RESTful web service tienen estas características:

- Están asociados a información
- Permiten listar, crear, leer, actualizar y borrar información
- Para las operaciones anteriores necesitan una URL y un método HTTP para accederlas
- Usualmente regresan la información en formato JSON.
- Retornan códigos de respuesta HTML, por ejemplo 200, 201, 404, etc

**11.	¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?**

Los HTTP headers son la parte central de los HTTP requests y responses, y transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, etc. La primera línea es la línea del request, que contiene su información básica (método HTTP, URL y versión).

A su vez, la cabecera content type indica el tipo de archivo o medio utilizado en la comunicación entre el cliente HTTP y el servidor para ayudarlos a comprender el formato en que la información está siendo enviada y, de este modo, mejorar la manera en que se procesa y se muestra el contenido.

Dicho de manera más sencilla, cuando el content type se emplea en una solicitud de búsqueda, se le comunica al servidor qué tipo de archivo o medio está buscando y, aunque el servidor no necesariamente se tiene que apegar a la petición, le ayuda a encontrar los recursos correctos para retornarlos en el formato deseado.
