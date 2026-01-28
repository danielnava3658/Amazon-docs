
# Agregar un producto al carrito

## Descripción 
El sistema agrega un articulo al carrito de compras validando la disponibilidad y stock del mismo


## Escenario 
1. El usuario encuentra un articulo en la pagina de inicio
2. El usuario da click en "Agregar al carrito"
3. El sistema valida el stock del producto
4. Aparece "Agregado al carrito" y muestra un catalogo de productos similares o recomendados

## Request
```json
{
"productId": "B08XYZ123",

"quantity": 1
}
```

## Validaciones
* Producto valido o disponible
* Stock mayor a 0

## Response
```json
{
"cartId": "c9a8b7j6s2",

"items": [

{

"productId": "B08XYZ123",

"name": "# Colgate Pasta Dental Blanqueadora Luminous White Brilliant White 2x75 ml. Remueve Manchas Superficiales, Protege el Esmalte y Ofrece Dientes Más Blancos, Ideal para la Salud Bucal Diaria",

"quantity": 1,

"price": 117.00

}

],

"totalItems": 1,

"subtotal": 117.00,

"currency": "MXN"

}
```
---
---