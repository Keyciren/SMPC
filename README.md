# Santa María Pickle Club · App de torneos

App web para organizar torneos de pickleball:
- Niveles y grupos todos contra todos.
- Programa por cancha y hora.
- Copa de Oro y Copa de Plata, con semifinales, final y partido por el 3er lugar.
- Exportación de imágenes y Excel.
- Historial de torneos.

Se publica gratis con **GitHub Pages** y se instala en el celular como una app.

## Qué hay en esta carpeta

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa |
| `manifest.webmanifest` | Nombre, ícono y colores para instalarla en el celular |
| `sw.js` | Permite que la app abra sin señal en la cancha |
| `icons/` | Íconos con el logo del club |
| `datos/inicial.json` | Datos del 1er Torneo. Se cargan solos la primera vez que se abre la app en un dispositivo |
| `.nojekyll` | Le indica a GitHub Pages que publique los archivos tal cual |

## Publicarla con Claude Code

1. Abre Claude Code con tu cuenta de GitHub conectada.
2. Pon esta carpeta (descomprimida) como carpeta de trabajo.
3. Pega este mensaje:

> Crea un repositorio público en mi GitHub llamado `pickle-club` con todos los archivos de esta carpeta (incluido `.nojekyll`), haz el commit inicial en la rama `main` y súbelo. Después activa GitHub Pages desde la rama `main`, carpeta raíz (`/`), y dame la URL pública cuando esté lista.

4. En uno o dos minutos la app queda en `https://TU-USUARIO.github.io/pickle-club/`.

### Si prefieres hacerlo a mano
1. En github.com, crea un repositorio **público** llamado `pickle-club`.
2. Sube todos los archivos con **Add file › Upload files**. Si `.nojekyll` no aparece porque está oculto, créalo con **Add file › Create new file**, déjalo vacío y guárdalo.
3. Ve a **Settings › Pages**, elige **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`, y guarda.

## Instalarla en el celular

- **iPhone (Safari):** abre el link, toca **Compartir** y luego **Agregar a pantalla de inicio**.
- **Android (Chrome):** abre el link, toca el menú **⋮** y luego **Instalar app** o **Agregar a la pantalla principal**.

Queda con el logo del club y se abre a pantalla completa, como una app.

## Importante: dónde se guardan los datos

- En esta versión los resultados se guardan **en el teléfono donde se anotan**. Quien abra el link desde otro celular ve su propia copia, no la tuya en vivo.
- Anota los resultados siempre desde **el mismo teléfono**.
- Usa **Resumen y exportar › Copia de seguridad › Descargar copia** de vez en cuando. Con **Cargar copia** pasas los datos a otro dispositivo.
- Para compartir resultados durante el torneo, usa las imágenes de **Resumen y exportar** y mándalas por WhatsApp.
- Si más adelante quieres que todos vean los resultados en vivo desde su celular, se puede conectar la app a una base de datos gratuita, como Firebase o Supabase.

## Actualizar la app

Reemplaza `index.html` en el repositorio y sube el cambio. Si actualizas `sw.js`, cambia también el número de `VERSION` dentro del archivo para que los celulares descarguen la versión nueva.
