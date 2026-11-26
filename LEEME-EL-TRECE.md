# Tema El Trece (base Horizon de Shopify)

## Qué hay aquí
- Tema oficial Horizon + secciones propias `sections/et-*.liquid`, estilos compartidos en `assets/et-base.css`, verificación de edad en `snippets/et-age-gate.liquid` (incluida en `layout/theme.liquid`).
- Plantillas: `index.json` (portada completa), `page.empresas.json` (cotizador), `page.restaurantes.json`, `product.json` con ficha del vino.
- Revisado con `shopify theme check`: 0 errores.

## Secciones
| Archivo | Nombre en el editor |
|---|---|
| et-season-bar | El Trece: temporada (cuenta regresiva editable) |
| et-hero | El Trece: portada |
| et-featured-sets | El Trece: cajas (elegir productos; la primera se destaca) |
| et-corporate-quote | El Trece: empresas (precios, descuentos y colores editables; envía con el formulario de contacto, etiqueta `empresa`) |
| et-origin | El Trece: origen |
| et-trade-form | El Trece: restaurantes (etiqueta `restaurante`) |
| et-club | El Trece: Club (cliente suscrito con etiqueta `club`) |
| et-wine-sheet | El Trece: ficha del vino (lee metafields `vino.*`) |

## Para verlo en una tienda (en tu Windows)
1. Crear cuenta en Shopify Partners y una tienda de desarrollo, por ejemplo `eltrece-dev`.
2. Instalar Node 20+ y Shopify CLI: `npm install -g @shopify/cli`
3. En esta carpeta: `shopify theme dev --store eltrece-dev` (abre el navegador para iniciar sesión y da la liga de vista previa).
4. Para enseñárselo a Héctor: `shopify theme push --unpublished --store eltrece-dev` y compartir la liga de vista previa.

## Configuración en el admin de la tienda
- Metafields de producto (Configuración > Datos personalizados > Productos), namespace `vino`: `uva` (texto), `cosecha` (texto), `alcohol` (decimal), `barrica_meses` (entero), `temperatura` (texto), `maridaje` (texto multilínea).
- Productos: cada vino y las cajas de 3 y 6 como productos propios.
- Crear páginas "Empresas" y "Restaurantes" y asignarles las plantillas `page.empresas` y `page.restaurantes`.
- Aviso de privacidad en Configuración > Políticas.

## Pendiente de diseño
Colores y tipografías finales se ajustan desde el editor (Configuración del tema) cuando tengamos logotipo, paleta, fotos reales y el diseño original de Vercel. Precios del cotizador son de ejemplo.
