# Menú dinámico - Banco Futuro

Nombre: Jordany Sosa
Matrícula: 100599903
Sección: INF5170-1
Asignatura: Lab Lenguaje de Programación III

## De qué trata
Hice un menú para un banco que se llama Banco Futuro. Las opciones del menú no están escritas en el HTML, se leen del archivo `menu.json` con JavaScript.

## Archivos
- `index.html`: la página
- `estilos.css`: los colores y el diseño
- `app.js`: el código que lee el JSON y arma el menú
- `menu.json`: las opciones del menú y sus submenús

## Lo que hace el programa
- Carga las opciones desde `menu.json`.
- Tiene varias opciones principales y submenús (Cuentas y Préstamos).
- Al hacer clic en una opción se abre el submenú y se muestra su texto. Si el enlace es una página externa, la abre en otra pestaña.
- Con el formulario se pueden agregar opciones nuevas y con el botón Eliminar se quitan. El menú cambia sin recargar la página.
- Valida que el ID no esté repetido y que el enlace empiece con # o con http(s)://.
- Para evitar inyección de código el texto se pone con `textContent` y no se aceptan los símbolos < y >.
- En el celular el menú se pone en una columna.

Para verlo hay que abrirlo desde GitHub Pages o con Live Server, porque si se abre con doble clic el navegador no deja leer el JSON.

## Conceptos que investigué

**API:** es una forma en que un programa le pide datos o servicios a otro programa.

**REST:** un estilo de API que usa HTTP y direcciones (URL). Usa GET para leer, POST para crear, PUT para modificar y DELETE para borrar. Casi siempre responde en JSON.

**SOAP:** un protocolo más viejo que manda los mensajes en XML con una estructura fija. Es más pesado pero se usa en empresas y bancos.

**JSON:** formato de texto para guardar datos con pares clave y valor. Es fácil de leer y JavaScript lo entiende directo. Es el que usé en `menu.json`.

**XML:** formato de datos con etiquetas, parecido al HTML. Es más largo que JSON y lo usa SOAP.

**GraphQL:** lenguaje para pedir datos a una API donde el cliente escoge exactamente los campos que necesita en una sola petición.

**Cómo se relacionan:** una aplicación manda una petición a otra por medio de una API (REST, SOAP o GraphQL) y la respuesta llega en JSON o XML. En mi proyecto el navegador pide `menu.json` y con esos datos dibuja el menú.

## Uso de inteligencia artificial
Usé Claude como ayuda para entender los requisitos, armar el código y revisar los errores. Después probé el programa y lo ajusté a mi idea.

## Referencias
- https://www.w3schools.com/js/js_json_intro.asp
- https://www.w3schools.com/xml/
- https://graphql.org/learn/
- https://www.w3schools.com/xml/xml_http.asp
- https://www.w3schools.com/xml/xml_soap.asp
