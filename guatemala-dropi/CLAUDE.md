# Guatemala: Dropi + Dropkiller

Negocio de dropshipping para clientes en Guatemala, con pago contra entrega. Lo de USA no va acá: está en `../usa-ayrinshop/`.

## Datos

- **Plataforma y proveedor:** Dropi Guatemala. El proveedor tiene el producto en Guatemala, la transportadora lo entrega y le cobra al cliente al recibir, y Dropi le acredita a Irene su ganancia en la billetera de Dropi.
- **Investigación de productos:** Dropkiller. Muestra cuánto venden y cuánto stock tienen los productos de los proveedores de Dropi, y espía anuncios de Facebook y TikTok.
- **Tienda:** todavía no hay. Si se hace en Shopify, tiene que ser una tienda **distinta** de AYRINshop y del mismo país que la cuenta de Dropi (así lo piden las guías de integración de Dropi).
- **Clientes:** pagan al recibir (contra entrega), en quetzales (Q).
- **Idioma con los clientes:** español (página, anuncios, WhatsApp).
- **Hora de referencia:** Guatemala (UTC−6, sin horario de verano).

## Conectores

| Conector | Para qué | Estado |
|---|---|---|
| Dropkiller | Buscar productos que se están vendiendo en Dropi Guatemala | Pendiente: Irene lo va a conectar |
| Dropi | Catálogo, proveedores, pedidos, envíos, devoluciones y billetera | Pendiente: Irene lo va a conectar |

- Si falta un conector, decíselo a Irene y no inventes datos.
- **Si es un conector de Claude** (un enlace de MCP): se agrega en https://claude.ai/customize/connectors y después se abre una sesión nueva, porque los conectores se cargan al iniciar la sesión.
- **Si es una clave de API:** va en la configuración del entorno (Network secrets o variables de entorno), nunca en el chat ni en este repositorio. Usá los nombres `DROPI_API_TOKEN` y `DROPKILLER_API_KEY`. También hay que permitir sus dominios en Network access: el 3 de noviembre de 2026 la red del entorno bloqueaba `dropi.co`, `app.dropi.co`, `dropi.gt`, `app.dropi.gt`, `dropkiller.com` y `app.dropkiller.com`.
- Cuando un conector quede funcionando, actualizá esta tabla.

## Cómo elegimos un producto (contra entrega)

En contra entrega no todos los pedidos se cobran: algunos clientes no reciben el paquete, y el envío de esos pedidos se pierde. Por eso la cuenta es distinta a la de USA, donde el cliente ya pagó.

- **Ganancia por pedido entregado** = precio de venta − costo del proveedor − flete − otros cobros de Dropi
- **Ganancia real por pedido** ≈ (% entregados × ganancia por pedido entregado) − (% devueltos × costo de la devolución) − costo de anuncios por pedido

Pasos:

1. En Dropkiller, con el país en Guatemala, buscar productos con ventas constantes en los últimos 7 y 30 días, no solo un pico de un día.
2. En Dropi, revisar al proveedor: stock suficiente, buena calificación y despacho rápido.
3. Calcular la ganancia real con las tarifas reales de Dropi Guatemala (flete y devolución). No las supongas.
4. Ver qué anuncios ya corren en Guatemala para ese producto (Dropkiller o la Biblioteca de anuncios de Meta).
5. Presentarle a Irene los candidatos con sus números. Ella decide.

Ya en operación, confirmar cada pedido por WhatsApp antes de despacharlo ayuda a bajar las devoluciones.

## Dónde guardar

- `investigacion/`: búsquedas en Dropkiller, con la fecha en el nombre del archivo.
- `productos/`: una ficha por producto elegido.

Recordá la regla del repositorio público del `CLAUDE.md` de la raíz.
