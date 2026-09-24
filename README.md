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

La primera vez pide una clave de GitHub, que queda guardada en ese dispositivo:

1. Entrar a https://github.com/settings/personal-access-tokens/new
2. Si el repositorio está en una organización, en *Resource owner* elegir la organización.
3. *Repository access* → *Only select repositories* → este repositorio.
4. *Permissions* → *Repository permissions* → **Contents: Read and write**. Generar la clave y pegarla en el editor.

El link tarda alrededor de un minuto en activarse. Para corregir algo, se vuelve a publicar con el mismo nombre y el link se actualiza.
