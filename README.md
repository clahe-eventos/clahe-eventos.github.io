# Clahe Eventos · Invitaciones digitales

- `index.html`: la invitación. Lee sus datos del bloque `const CONFIG = {...}` que está al final del archivo.
- `admin.html`: el editor. Lleva `index.html` embebido en la constante `TEMPLATE` (una sola línea larga): si se toca `index.html`, hay que regenerar esa línea.
- `i/<nombre>/index.html`: invitaciones publicadas desde el editor, una carpeta por evento.

## Crear link (modo normal)

El botón **Crear link** arma la dirección de la invitación en el momento, sin servidor ni cuenta: la invitación
entera viaja dentro de la URL (`index.html#d=<datos>`). Después la acorta con spoo.me para que quede una URL
normal; si el acortador no responde, el link largo funciona igual.

Limitación: la foto subida desde el celular no entra en un link, así que se omite. Para tener foto hay que pegar el
enlace de una imagen ya alojada (el editor convierte los enlaces "compartir" de Google Drive).

## Publicar en GitHub (modo avanzado, `admin.html?pro`)

Sube la invitación al repositorio con la API de GitHub y GitHub Pages la sirve en `<dirección del sitio>/i/<nombre>/`,
con la foto adentro y un link corto propio. Requiere activar el editor una vez con un token de GitHub
(*Contents: Read and write*); el editor abre la página de GitHub ya prellenada y verifica el token al pegarlo.
Desde un celular activado, *Pasar el acceso a otro celular* manda un link que activa otro dispositivo.
