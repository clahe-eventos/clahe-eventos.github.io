# Clahe Eventos · Invitaciones digitales

- `index.html`: la invitación. Lee sus datos del bloque `const CONFIG = {...}` que está al final del archivo.
- `admin.html`: el editor. Lleva `index.html` embebido en la constante `TEMPLATE` (una sola línea larga): si se toca `index.html`, hay que regenerar esa línea.
- `i/<nombre>/index.html`: invitaciones publicadas desde el editor, una carpeta por evento.

## Publicar con un link

El botón **Publicar (link)** del editor sube la invitación a este repositorio con la API de GitHub y GitHub Pages la sirve en
`<dirección del sitio>/i/<nombre>/`.

El editor deduce el usuario u organización y el nombre del repositorio de la dirección desde la que se abre, así que el
repositorio puede cambiar de dueño o de nombre sin tocar el código. Si el sitio pasa a usar un dominio propio, hay que
completar `PUB_FIJO` en `admin.html`.

La primera vez pide activarlo. Hay dos formas:

- **Desde otro celular ya activado**: botón *Pasar el acceso a otro celular*. Manda por WhatsApp un link
  (`admin.html#acceso=...`) que, al abrirse una vez, deja el editor activado en ese celular.
- **Desde la cuenta de GitHub**: generar un token fine-grained con permiso *Contents: Read and write* sobre el
  repositorio (el editor abre la página ya prellenada) y pegarlo en el editor.

El token vence al año: el editor avisa y se vuelve a activar con uno nuevo. El link de cada invitación tarda alrededor
de un minuto en activarse. Para corregir algo, se vuelve a publicar con el mismo nombre y el link se actualiza.
