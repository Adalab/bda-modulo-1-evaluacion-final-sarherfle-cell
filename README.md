1º. Punto--> Estructura global: Se realiza una estrucura global para tener los datos bien estructurados y sea más comprensible a la hora de agregar productos. 
- inventario_tienda = []
- clientes = {}
- ventas_totales = 0.0

2º. Punto --> Funciones. 
2.1 Se declara la primera función que es la de agregar_productos. Ahora mismo, el inventario está vacío y se crea esta función para añadir productos teniendo en cuenta dos condiciones:
- Si el producto ya existe, actualiza la cantidad.
- Si no existe, agrega un nuevo producto al inventario.

Para añadir el primer producto, se aplica la condición if y finaliza con un return. Para seguir añadiendo productos, se crea un bucle for que recorra el inventario junto con dos condiciones:
- El producto ya existe. Se ha actulizado la cantidad
- El producto no lo teníamos. Se ha añadido
** Añadimos  return para que una vez que entre dentro de esa condición y se cumpla, no siga buscando. 

2.2 ver_inventario(): Muestra el inventario de productos con sus detalles.
2.3 0. buscar_producto(nombre): Busca un producto en el inventario por nombre y muestra sus
detalles si se encuentra.
2.4 Actualizar_stock(nombre, cantidad): Actualiza el stock de un producto en el inventario.
Debe recibir el nombre del producto y la cantidad a agregar o quitar como parámetros.
Utiliza un bucle for para recorrer el inventario.
2.5 3. eliminar_producto(nombre): Elimina un producto del inventario por nombre.

2.6. calcular_valor_inventario(): Calcula y muestra el valor total del inventario.
Para el calcular el valor total del inventario, empezamos con un contador a 0, es decir, el valor totaldel inventario previo del bucle, es cero, porque aun no se ha iniciado la operación que es igual a multiplicar precio * cantidad de cada producto. 
Una vez iniciaco el bucle, en cada recorrido va calculando cada "item" y cuando ya ha terminado, se imprime el total. 

2.7. Empezamos creando una lista de Carrito donde el cliente irá agregando los productos que a posterior irá comprando. También la acompaña la variable coste total que irá acumulando la suma del precio según cantidad de items que el cliente vaya añadiendo a la lista. 
Para ello, empezamos con el bucle principal con un while True, el cuál, se irá ejecutando mientras se cumpla una condición, es decir, mientras el cliente siga añadiendo items a la lista hasta romper dicho bucle con un break:

DENTRO DEL BUCLE WHILE TRUE
    1- Para la primera condición, lo primero que pide el ejercício es que se muestre el inventario al cliente. A través de un primer bucle for prodcuto in inventario_lista, en cada vuelta del bucle se irá imprimiento cada Item hasta que llegue al final. 
    2. Segundo paso, el cliente va a comprar. Para ello, al mismo nivel que el primer for, una vez que se ha imprimido el inventario se lanza la pregunta al cliente con un compra.imput Mientras el cliente siga añadiendo items al carrito, no parará el bucle. Lo hará cuando el cliente responda nada (con lower para poner las mayúsculas en minúsculas).
    3. Para añadir la información que el cliente ha solicitado, en un segundo bucle for si el item que ha elegido el cliente está dentro del inventario_lista, entonces sumará a carrito y a coste_totel. Imprimiendo el mensaje de , ejemplo "La camisa se ha añadido al carrito". 
    4. Si el cliente intenta añadir al carrito un item que no está dentro del inventario_lista, para ello, añadimos un else que podría definirse como un "de lo contrario", es decir, si el item no está en el inventario lista, entonces se imprime el mensaje "producto no encontrado en el inventario".
    
Uúltima parte del ejercício, Muestra el inventario de carrito y muestra el coste total. (simplemente se imprimen ambos)