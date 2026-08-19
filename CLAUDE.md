# Notas del proyecto — Disfrútalo

> Este archivo lo lee Claude automáticamente cada vez que trabaja en esta carpeta.
> Sirve para darle contexto y reglas del proyecto, así no hay que repetírselas.

## Qué es este proyecto

Landing page de una licorería (HTML + CSS + JS en un solo archivo `index.html`).
No usa frameworks ni dependencias externas: todo es vanilla JavaScript.

## Reglas de estilo

- Todo el código y los textos visibles van en **español (es-CL)**.
- Mantener todo en un único `index.html` (sin separar CSS/JS en otros archivos).
- Los colores se manejan con variables CSS en `:root`, no con valores sueltos.
- La paleta es burdeo + dorado; no introducir colores nuevos sin avisar.

## Cosas importantes del negocio

- Es obligatorio mantener el aviso de **mayor de 18 años** (Ley 19.925 de Chile).
- El pedido se envía por **WhatsApp**; el número está en la función `checkout()`.
- Los productos viven en el arreglo `PRODUCTS` dentro del `<script>`.

## Cómo desplegar

Se publica con **GitHub Pages** desde la rama `main` del repo `die-vt/disfrutalo`.
