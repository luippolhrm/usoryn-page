# Fichas de Personaje — Campaña D&D 2024

Portada con las fichas de personaje de la mesa, organizadas por jugador.
Sitio publicado con **GitHub Pages**.

---

## 📂 Estructura del repositorio

```
index.html          ← La portada. Lista a los jugadores y sus personajes.
lucho/              ← Carpeta de cada jugador (una por persona)
  usoryn.html
  darvin.html
  auriana.html
checho/
  <tu-personaje>.html
README.md           ← Este archivo
```

Cada jugador tiene **su propia carpeta** (en minúsculas, sin espacios ni tildes).
Dentro van las fichas, una por personaje, en formato `.html`.

---

## ➕ Cómo subir un personaje nuevo

1. Entra al repositorio en GitHub.
2. Abre **tu carpeta** (por ejemplo `checho/`). Si aún no existe, la creas en el paso 4 escribiendo `checho/` antes del nombre del archivo.
3. Clic en **"Add file" → "Upload files"**.
4. Arrastra tu archivo `.html`. Usa un nombre simple en minúsculas, sin espacios ni tildes:
   - ✅ `kaelen.html`, `mi-personaje.html`
   - ❌ `Mi Personaje.html`, `kaelén.html`
5. Abajo, clic en **"Commit changes"** para guardar.

> Si subes el archivo dentro de una carpeta que no existe todavía, GitHub la crea sola. Para eso, al subir, escribe el nombre de la carpeta y una barra antes del archivo en el campo de destino: `checho/kaelen.html`.

---

## 🔗 Cómo enlazar tu personaje en la portada

La portada usa un **acordeón por jugador**: cada jugador es un bloque plegable y dentro van sus personajes como filas de lista.

1. Abre `index.html` en GitHub y clic en el lápiz (✏️ "Edit").
2. Busca el bloque de tu jugador (empieza con `<!-- JUGADOR: Checho -->`).
3. Dentro de su `<div class="char-list">`, copia una fila existente y pégala cambiando los datos.

Para un personaje **con ficha lista** (es un enlace `<a>`):

```html
<a class="char" href="checho/kaelen.html">
  <span class="marker"></span>
  <span class="info">
    <span class="cn">Kaelen</span>
    <span class="meta">Elfo · Mago nivel 8 <span class="camp">Nombre de la campaña</span></span>
  </span>
  <span class="right">
    <span class="char-status ready">Lista</span>
    <span class="arrow">→</span>
  </span>
</a>
```

Para un personaje **sin ficha todavía** (es un `<span>` no clicable):

```html
<span class="char pending-row">
  <span class="marker"></span>
  <span class="info">
    <span class="cn">Kaelen</span>
    <span class="meta">Elfo · Mago nivel 8 <span class="camp">Nombre de la campaña</span></span>
  </span>
  <span class="right">
    <span class="char-status pending">Pendiente</span>
  </span>
</span>
```

- `href` → ruta a tu ficha (`carpeta/archivo.html`). Solo en la versión `<a>`.
- `cn` → nombre del personaje.
- `meta` → especie · clase y nivel.
- `camp` → nombre de la campaña (reemplaza "Campaña por definir" cuando lo tengas).
- Cuando una ficha quede lista, cambia el `<span class="char pending-row">` por `<a class="char" href="...">`, pon el estado en `ready` con texto "Lista" y añade la flecha `<span class="arrow">→</span>`.

4. Si añades un personaje, actualiza también el conteo del jugador (`<span class="count">3 personajes</span>`).
5. Clic en **"Commit changes"**.

> **Campaña:** mientras no tengas el nombre, deja `Campaña por definir`. Cuando lo definas, reemplaza ese texto en cada personaje.

---

## ✏️ Cómo actualizar una ficha existente

1. Entra a la carpeta del jugador y abre el archivo.
2. **"Upload files"** y sube la versión nueva con el **mismo nombre** (la reemplaza).
3. **"Commit changes"**. En 1-2 minutos la web refleja el cambio.

---

## 🌐 La URL del sitio

La portada vive en la raíz del sitio:
`https://<usuario>.github.io/<repositorio>/`

Cada ficha es accesible directamente por su ruta:
`https://<usuario>.github.io/<repositorio>/lucho/usoryn.html`

**En el móvil:** abre la URL y usa "Añadir a pantalla de inicio" para tenerla como ícono de app.

---

## 📝 Notas

- Las fichas son archivos HTML autónomos: no dependen de nada externo salvo las fuentes (que cargan solas con internet).
- Mantén los nombres de archivo y carpeta en minúsculas y sin tildes para evitar problemas de enlaces.
- Si una ficha aún no existe, deja su tarjeta con estado `pending` y sin `href` (o apuntando a `#`).
