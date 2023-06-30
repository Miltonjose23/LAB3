Esta práctica conciste en una aplicacion web para leer un archivo json, que contine una lista de objetos representados en tarjetas que poseen dos propiedades: "Titulo" y "contenido" creados a partir de un archivo json, html, css y java script.

HTML
Dentro del apartado del index, se contempla la estructura básica del html de la prática integrando una serie de etiquetas como:

    !DOCTYPE html: Esta línea declara el tipo de documento como HTML5.

    html: Este elemento marca el inicio del documento HTML.

    head: Aquí comienza la sección del encabezado del documento, donde se definen 
    metaetiquetas, enlaces a archivos externos y otros elementos relacionados con la configuración 
    de la página.

    title: Esta etiqueta establece el título de la página, que se mostrará 
    en la pestaña del navegador.

    link rel="stylesheet" type="text/css" href="estilos.css">: Este enlace vincula un archivo CSS externo llamado "estilos.css" para aplicar estilos a la página. Se utiliza el atributo rel para especificar la relación del archivo y href para indicar la ruta del archivo CSS.

    head: Aquí termina la sección del encabezado.

    body: Aquí comienza la sección del cuerpo del documento, que contiene el contenido visible de la página.

    div: un contenedor que refleja los contenidos de las tarjetas por medio de un id

    script src="app.js: Se utiliza para especificar la ruta del archivo JS.

CSS
La hoja de estilos css cuenta con una estructura básica que definen los estilos de las tarjetas por medio de etiquetas como: .card, .card h2, .card p; que definen tanto los caracteres generales como del título y contenidos de las tarjetas.

JS
En el archivo js se definen una serie de parametros que nos permiten intregrar el archivo json y crear las tarjetas, agregando las clases para establecer los estilos css.

    fetch('data.json'): Utilizamos la función fetch para cargar el archivo JSON.

    .then(response => response.json()): Convertimos la respuesta del archivo JSON en un objeto JavaScript utilizando el método .json().

    .then(data => {...}): Cuando se completa la conversión del JSON, obtenemos los datos.

    const tarjetasContainer = document.getElementById('tarjetas-container'): en este elemento es donde agregaremos dinámicamente las tarjetas generadas.

    data.forEach(objeto => {...}): Iteramos sobre cada objeto del arreglo de datos.

    const tarjeta = document.createElement('div'): Creamos un elemento <div> le añadimos la clase "card" para aplicar los estilos CSS.

    const titulo = document.createElement('h2'): Creamos un elemento <h2> para el título de la tarjeta.

    const contenido = document.createElement('p'): Creamos un elemento <p> para el contenido de la tarjeta.

    tarjeta.appendChild(titulo): Añadimos el elemento del título como hijo del elemento de la tarjeta.

    tarjeta.appendChild(contenido): Añadimos el elemento del contenido como hijo del elemento de la tarjeta.

    tarjetasContainer.appendChild(tarjeta): Añadimos la tarjeta completa como hijo del contenedor de tarjetas.

    .catch(error => console.error(error)): Manejamos cualquier error que ocurra durante la carga del 
    archivo JSON y lo mostramos en la consola del navegador.
