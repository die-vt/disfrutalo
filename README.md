# 🍷 Disfrútalo · Licorería

Landing page de una licorería con **escala de dulzor**, **ranking de ventas** y un
carrito ("carrete") con descuentos por cantidad y checkout por WhatsApp.

> Proyecto de práctica: una sola página en HTML + CSS + JavaScript, sin dependencias
> externas. Todo vive en un único archivo: `index.html`.

---

## 📑 Tabla de contenidos

- [Características](#-características)
- [Cómo verlo](#-cómo-verlo)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Cómo editar los productos](#-cómo-editar-los-productos)
- [Configurar ofertas y WhatsApp](#-configurar-ofertas-y-whatsapp)
- [Paleta de colores](#-paleta-de-colores)
- [Desplegar en GitHub Pages](#-desplegar-en-github-pages)

---

## ✨ Características

- Verificación de edad (mayor de 18) antes de entrar.
- Filtros por **categoría**, **búsqueda** y **dulzor máximo**.
- Ordenamiento por más vendidos, dulzor o precio.
- Carrito lateral con descuentos automáticos y despacho gratis.
- Envío del pedido por WhatsApp con un solo clic.

## 🚀 Cómo verlo

No necesitas instalar nada. Basta con abrir el archivo en el navegador:

```bash
# Windows (PowerShell), desde la carpeta del proyecto
start index.html
```

O simplemente haz doble clic en `index.html`.

## 📂 Estructura del proyecto

```text
Primera Landing Page/
├── index.html   # Toda la página (HTML + CSS + JS)
└── README.md    # Este archivo
```

## 🛠 Cómo editar los productos

Los productos están en un arreglo llamado `PRODUCTS` dentro de `index.html`.
Cada producto es un objeto con estos campos:

| Campo     | Tipo     | Descripción                              |
| --------- | -------- | ---------------------------------------- |
| `id`      | número   | Identificador único                      |
| `nombre`  | texto    | Nombre del producto                      |
| `cat`     | texto    | Categoría (Vinos, Destilados, etc.)      |
| `emo`     | emoji    | Ícono que se muestra en la tarjeta       |
| `precio`  | número   | Precio en pesos (sin puntos)             |
| `dulzor`  | 0 a 5    | Nivel de dulzor                          |
| `ventas`  | 0 a 100  | % de recomendación / ranking             |
| `desc`    | texto    | Descripción corta                        |
| `grad`    | texto    | Graduación alcohólica (ej. `"13.5°"`)    |

Ejemplo para agregar un producto nuevo:

```javascript
{ id: 17, nombre: "Champagne Rosé", cat: "Espumantes", emo: "🥂",
  precio: 29990, dulzor: 2, ventas: 85,
  desc: "Burbuja fina y elegante.", grad: "12°" }
```

## ⚙️ Configurar ofertas y WhatsApp

Dentro del `<script>` en `index.html` puedes ajustar:

1. **Despacho gratis** — cambia el monto mínimo:
   ```javascript
   const FREE_SHIP = 30000;
   ```
2. **Descuentos por cantidad**:
   ```javascript
   const DISCOUNT_TIERS = [
     { units: 6, pct: 12 },
     { units: 3, pct: 7 },
   ];
   ```
3. **Número de WhatsApp** — reemplaza el número en la función `checkout()`:
   ```javascript
   window.open(`https://wa.me/56900000000?text=${msg}`, "_blank");
   ```

## 🎨 Paleta de colores

Los colores se definen como variables CSS en `:root`. Cambia una sola vez y
afecta a toda la página:

- `--bg` — fondo burdeo suave
- `--gold` — dorado de acentos
- `--wine` — vino para insignias

## 🌐 Desplegar en GitHub Pages

1. Sube el proyecto a GitHub (rama `main`).
2. Ve a **Settings → Pages**.
3. En *Source*, elige la rama `main` y la carpeta raíz (`/root`).
4. Guarda y espera ~1 minuto. Tu sitio quedará en:
   `https://<tu-usuario>.github.io/<repositorio>/`

---

## 📝 Nota sobre Markdown

Este archivo es un ejemplo de **Markdown** (`.md`), el formato que usa GitHub para
documentar proyectos. Algunos elementos que aparecen aquí:

| Sintaxis            | Resultado                        |
| ------------------- | -------------------------------- |
| `# Texto`           | Título (más `#`, más pequeño)    |
| `**texto**`         | **Negrita**                      |
| `*texto*`           | *Cursiva*                        |
| `- item`            | Lista con viñetas                |
| `1. item`           | Lista numerada                   |
| `` `código` ``      | `código en línea`                |
| ` ```lenguaje `     | Bloque de código con color       |
| `> texto`           | Cita                             |
| `[texto](url)`      | [Enlace](https://github.com)     |
| `\| a \| b \|`      | Tabla                            |

---

_Hecho con 🍷 como proyecto de aprendizaje._
