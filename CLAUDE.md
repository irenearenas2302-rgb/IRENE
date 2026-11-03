# Negocios de Irene: leer antes de hacer cualquier cosa

Irene tiene **dos negocios de dropshipping separados**. No se mezclan: cada uno tiene su carpeta, sus conectores, su idioma, su moneda y sus sesiones.

| | USA | Guatemala |
|---|---|---|
| Carpeta | `usa-ayrinshop/` | `guatemala-dropi/` |
| Tienda | AYRINshop (ayrinshopus.com) | Todavía no hay |
| Plataforma y proveedor | Shopify + Zendrop | Dropi (pago contra entrega) |
| Investigación de productos | TREND (Trendtrack) | Dropkiller |
| Idioma con los clientes | Inglés | Español |
| Moneda | Dólares (USD) | Quetzales (Q, GTQ) |
| Hora de referencia | Este de EE. UU. (ET) | Guatemala (UTC−6, sin horario de verano) |
| Etiqueta de sesión | `remote-agents-project:usa-ayrinshop` | `remote-agents-project:guatemala-dropi` |

## Reglas para no confundir los negocios

1. **Primero identificá el negocio.** Antes de actuar, decidí si la tarea es de USA o de Guatemala y leé el `CLAUDE.md` de esa carpeta. Si no está claro, preguntale a Irene.
2. **Cada conector es de un solo negocio.** Zendrop y TREND son de USA. Dropi y Dropkiller son de Guatemala. Si Irene pide usar uno en el otro negocio, que quede separado (por ejemplo, un tablero aparte en TREND con "Guatemala" en el nombre).
3. **Conectores compartidos: verificá la cuenta antes de actuar.**
   - **Shopify:** revisá con `get-shop-info` qué tienda está activa. Hoy el conector apunta a AYRINshop, que es USA. Si hace falta otra tienda, usá `switch-shop` y volvé a verificar.
   - **Windsor.ai y anuncios (Meta, TikTok):** confirmá que la cuenta publicitaria es la del negocio correcto antes de leer o cambiar algo.
4. **Cada archivo en su carpeta.** Lo de USA va en `usa-ayrinshop/` y lo de Guatemala en `guatemala-dropi/`.
5. **Reportes separados.** No sumes ventas, pedidos ni gastos de los dos negocios en un mismo número. Si Irene pide un resumen general, mostrá cada negocio por separado y cada uno en su moneda.
6. **Tareas programadas separadas.** Cada tarea programada es de un solo negocio y lo dice en el nombre, por ejemplo "USA · Revisión 6 PM" o "Guatemala · Revisión de pedidos".
7. **Sesiones con su negocio en el título.** Al empezar a trabajar en un negocio, poné "USA · " o "Guatemala · " al inicio del título de la sesión y agregale la etiqueta de la tabla.

## Siempre

- Hablale a Irene en español. Lo que ven los clientes de USA va en inglés.
- No cambies nada en tiendas, pedidos, incidencias o anuncios sin que Irene lo confirme.
- **Este repositorio es público.** Nunca guardes claves, tokens o contraseñas, ni datos de clientes (nombres, teléfonos, direcciones, correos). Mientras siga siendo público, tampoco guardes costos, márgenes, ventas ni los productos que se van a lanzar.
