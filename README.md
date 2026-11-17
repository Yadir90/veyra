# Veyra — Espejo de paquetes de actualización

Este repositorio público es el **espejo** de los paquetes de actualización
del juego **Veyra**. El **canal oficial** vive en Cloudflare Pages:

- Manifiesto oficial: https://veyra-4jx.pages.dev/manifiesto.json
- Índice del canal: https://veyra-4jx.pages.dev/

## Cómo funciona el canal

- La app de Veyra se instala **una vez** (la base). Todo lo demás — mapas,
  arte, razas, música y datos — llega en **paquetes** (`.pck`) que la app
  descarga y monta sola cuando hay conexión.
- Sin conexión, el mundo sigue corriendo con lo que ya tiene: la
  simulación nunca depende de internet.
- El archivo `manifiesto.json` es la lista oficial de paquetes: por cada
  uno, su **nombre**, **versión**, **tamaño** (bytes) y **sha256**. La app
  descarga solo lo nuevo y verifica el sha256 antes de montar cada paquete;
  si la descarga se corta, el paquete incompleto no se activa.

## Releases (el espejo)

Cada publicación del canal se refleja aquí como una **Release** con la
etiqueta `canal-N` (la primera: `canal-0`), que lleva como activos el
`manifiesto.json` de esa publicación y los paquetes `.pck` nuevos. Si el
canal oficial no responde, la app puede acudir a este espejo.

## Entrar con Google (diseño fallado)

Entrar con una cuenta de Google es **opcional**: suma la copia del mundo
en la nube ligada a la cuenta (si el teléfono muere, la historia única no
se pierde) y el nombre y la foto del jugador. Nunca cierra el juego: sin
cuenta y sin internet, el mundo abre igual.
