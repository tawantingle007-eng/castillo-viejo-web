# Castillo Viejo

Sitio web de una sola página para **Castillo Viejo**, café y pizzería en Hidalgo 19, San José de la Parrilla, Durango, México.

Es un sitio estático: un solo `index.html` con sus fotos en `assets/`. No necesita servidor, base de datos ni instalación.

## Qué hay en el sitio

- La bóveda de ladrillo con la lámpara de hierro (dibujada con código, no es una foto).
- **La casa**: descripción del salón y marcos para las fotos del local.
- **La carta**: carta de muestra sin precios.
- **Noches con música**: aviso de que algunas noches hay músicos.
- **Cómo llegar**: dirección, teléfono, Plus Code, coordenadas y horario.

## Publicar con GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `castillo-viejo`).
2. Sube el contenido de esta carpeta:
   ```bash
   git remote add origin https://github.com/USUARIO/castillo-viejo.git
   git push -u origin main
   ```
3. En GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`.
4. En uno o dos minutos el sitio queda en `https://USUARIO.github.io/castillo-viejo/`.

## Poner las fotos reales del local

Cada marco del sitio tiene un nombre. Para cambiar una foto de referencia, o llenar un marco vacío, por una foto del local:

1. Guarda la foto en `assets/local/` (JPG, de unos 1400 px de ancho).
2. En `index.html`, busca `FOTOS_DEL_LOCAL` y escribe el nombre del archivo:
   ```js
   const FOTOS_DEL_LOCAL = {
     salon: "salon.jpg",
     fachada: "fachada.jpg",
     ...
   };
   ```

| Marco | Qué foto va |
|---|---|
| `salon` | El salón con la bóveda y la lámpara de hierro |
| `fachada` | La fachada de arcos iluminada de noche |
| `boveda` | La bóveda de ladrillo vista desde abajo |
| `pizza` | Una pizza de la casa |
| `bebidas` | Los vasos con el castillo |
| `cafe` | El café |
| `musica` | Músicos tocando en el salón |

Cuando ya no se use una foto de referencia, bórrala de `assets/` y quita su crédito del pie de página y de `CREDITOS.md`.

## Datos que faltan confirmar con el dueño

- Carta real y precios (hoy dice "Pregunta").
- Horario de todos los días (solo está confirmado el viernes desde las 17:00).
- Fechas de música en vivo.
- Fotos del local.

Los datos están en `index.html`, en texto normal; se pueden editar con cualquier editor.

## Créditos

Las fotos de referencia son de Wikimedia Commons, con licencias Creative Commons. Ver [CREDITOS.md](CREDITOS.md).

---

## ภาษาไทย (สำหรับผู้ดูแล)

เว็บนี้เป็นไฟล์ HTML ไฟล์เดียว ขึ้น GitHub Pages ได้ทันที

1. สร้าง repository ใหม่บน GitHub แล้ว push โฟลเดอร์นี้ขึ้นไป
2. ไปที่ **Settings → Pages** เลือก branch `main` โฟลเดอร์ `/ (root)` แล้วกด Save
3. รอ 1–2 นาที เว็บจะขึ้นที่ `https://USUARIO.github.io/castillo-viejo/`

ถ้าได้รูปจริงจากร้าน ให้วางไฟล์ใน `assets/local/` แล้วพิมพ์ชื่อไฟล์ใน `FOTOS_DEL_LOCAL` ใน `index.html` (ดูตารางข้างบน)
