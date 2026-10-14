# Bitácora de JavaScript interactivo

Laboratorio 08: JavaScript Interactivo - DOM, Eventos y Objetos.

Navegador usado: ESCRIBE AQUÍ TU NAVEGADOR

## Ejercicio 2: Seleccionar y modificar el DOM

| Instrucción                  | Qué cambió en la pantalla                   | Se mantiene al recargar (Sí/No) |
| ---------------------------- | ------------------------------------------- | ------------------------------- |
| textContent desde la consola | El título cambió a “Hola desde la consola”. | No                              |
| textContent desde app.js     | El título cambió a “Hola TECSUP”.           | Sí                              |
| style.color                  | El título se mostró en azul.                | Sí                              |
| classList.add                | El párrafo adquirió un fondo amarillo.      | Sí                              |
| createElement + appendChild  | Se agregó “JavaScript” a la lista.          | Sí                              |

## Ejercicio 3: Evento click

| Tipo de evento | Qué acción lo dispara                      | Cuánto suma por acción |
| -------------- | ------------------------------------------ | ---------------------- |
| click          | Hacer un clic en el botón.                 | 1                      |
| dblclick       | Hacer doble clic en el botón.              | 1                      |
| mouseover      | Mover el puntero hasta entrar en el botón. | 1                      |

evento.type mostró el nombre del evento: click, dblclick o mouseover.
evento.target mostró el botón que recibió el evento.

## Ejercicio 4: Eventos input y submit

| Prueba                                  | Qué pasó en la pantalla                        | Se recargó la página (Sí/No) |
| --------------------------------------- | ---------------------------------------------- | ---------------------------- |
| Escribir en el campo nombre             | El saludo se actualizó mientras escribía.      | No                           |
| Enviar sin preventDefault               | La página se recargó y el mensaje desapareció. | Sí                           |
| Enviar con preventDefault, correo sin @ | Apareció un mensaje de error en rojo.          | No                           |
| Enviar con preventDefault, correo con @ | Apareció “Enviado:” junto al texto ingresado.  | No                           |

Observación: La validación solo comprueba la presencia de @.
Por eso acepta “eliana@”, aunque su formato esté incompleto.

## Ejercicio 5: Clases y objetos

| Objeto  | nombre  | precio  | descripcion()       | conDescuento(0.25) |
| ------- | ------- | ------- | ------------------- | ------------------ |
| laptop  | Laptop  | 2500.00 | Laptop - S/ 2500.00 | 1875.00            |
| mouse   | Mouse   | 45.00   | Mouse - S/ 45.00    | 33.75              |
| teclado | Teclado | 120.00  | Teclado - S/ 120.00 | 90.00              |
| monitor | Monitor | 680.00  | Monitor - S/ 680.00 | 510.00             |

La clase permite crear productos con la misma estructura y reutilizar sus métodos.
Pude agregar un nuevo producto a la página sin modificar el HTML.

## Ejercicio 6: DOM, eventos y objetos juntos

| Prueba          | Total que muestra la página                          | Correcto (Sí/No) |
| --------------- | ---------------------------------------------------- | ---------------- |
| Cuaderno 12.50  | S/ 12.50                                             | Sí               |
| + Lapicero 3.20 | S/ 15.70                                             | Sí               |
| + Mochila 89.90 | S/ 105.60                                            | Sí               |
| Sin Number()    | S/ 0.00; ocurrió un error y no apareció el producto. | No               |

| Pieza  | Línea de tu código donde aparece                                           | Para qué sirve                              |
| ------ | -------------------------------------------------------------------------- | ------------------------------------------- |
| DOM    | listaCarrito.appendChild(li);                                              | Agrega el producto a la lista visible.      |
| Evento | formProducto.addEventListener("submit", (evento) => {                      | Ejecuta la función al enviar el formulario. |
| Objeto | const producto = new Producto(prodNombre.value, Number(prodPrecio.value)); | Crea un producto con los datos ingresados.  |
