# Pagar un producto / carrito

## Descripción 
Se valida el proceso de pago en linea para continuar con la compra

## Escenario
1. El usuario visualiza su carrito de compras
2. Da click en "Proceder al pago"
3. Se agregan los datos de dirección para la entrega
	3.1 Calle
	3.2 Numero exterior / interior
	3.3 Colonia
	3.4 Municipio
	3.5 Estado
	3.6 Código Postal
4. Se selecciona el método de pago 
5. Se agregan los datos de la tarjeta de debito/crédito en su caso
6. Se presenta la opción de guardar o no los datos del método de pago
7. El usuario confirma su método de pago
8. Se muestra una pantalla con los datos de envió y el método de pago como modo de confirmación
9. El usuario da click en "Realizar compra"
10.El sistema valida que el pago se haya completado de manera exitosa

## Validaciones

* Método de pago valido
* Dirección de envió valida


## Manejo de errores
* Pago rechazado
	* Se notifica que el pago no pudo ser procesado
	* Se da la opción de cambiar método de pago o cancelar la compra
* Dirección de envio no valida
	* Se valida que la dirección sea correcta y que el código postal exista



## Visuales
* Se muestra una pantalla de confirmación 
* Se redirige al carrito de compras actualizado
* Se crea una sección de seguimiento
