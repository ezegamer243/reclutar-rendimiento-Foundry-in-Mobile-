# Reclutar Rendimiento!

Módulo para **Foundry VTT v14** que permite jugar cómodo desde un **celular** o una **PC de pocos recursos**.
Funciona con cualquier sistema de juego. *(English below.)*

## Qué hace
- **Perfiles de rendimiento por usuario:** Celular, PC Bajo o PC Alto. El DM los asigna y cada jugador puede cambiar el
  suyo. Celular y PC Bajo bajan la calidad del lienzo, limitan a 30 FPS y apagan animaciones costosas. Sin perfil
  asignado, los celulares se detectan solos.
- **Interfaz táctil:** oculta la interfaz de Foundry y muestra una barra con seleccionar, objetivos (uno o varios),
  regla, deshacer, chat y configuración. Abajo al centro o en columna a la derecha (ajuste personal).
- **Cámara táctil:** un dedo mueve el mapa, dos dedos hacen zoom.
- **Personaje en la barra:** el avatar del personaje asignado; arrástralo al mapa para mover (o colocar) su token, o
  tócalo para abrir su hoja.
- **Ventanas ajustadas a la pantalla:** hojas, compendios y configuración se achican para entrar en el celular, también
  al girarlo.

## Instalación
En Foundry: *Add-on Modules → Install Module*, y pega en **Manifest URL**:

```
https://github.com/ezegamer243/reclutar-rendimiento-Foundry-in-Mobile-/releases/latest/download/module.json
```

## Uso
1. Activa el módulo en el mundo. La primera vez, el DM ve una guía rápida.
2. En *Configurar ajustes → Reclutar Rendimiento! → Elegir perfiles* (o clic derecho sobre un jugador en la lista de
   jugadores) asigna **Celular** a quienes juegan desde el teléfono.
3. Opcional: asigna a cada jugador su personaje (*Configuración de usuario → Personaje*) para verlo en la barra.

## Para desarrolladores
Para la interfaz táctil, el módulo reemplaza tres funciones de Foundry: `Token#_onClickLeft` (toque en modo
multi-selección/multi-objetivo), `ApplicationV2#render` (ajustar ventanas al abrirse) y `Notifications#notify` (oculta
el aviso de resolución mínima solo con la interfaz táctil). No usa libWrapper. El módulo no se conecta a ningún
servicio externo ni guarda datos fuera de Foundry.

## Créditos
Desarrollado por **Zeryu**, con la asistencia de **Claude** (Anthropic). Licencia [MIT](LICENSE).

---

# Reclutar Rendimiento! (English)

A **Foundry VTT v14** module for playing comfortably from a **phone** or a **low-end PC**. System agnostic.

- **Per-user performance profiles** (Mobile, Low-end PC, High-end PC), assigned by the GM or by each player. Phones are
  detected automatically.
- **Touch interface:** a bar with select, targets (one or many), ruler, undo, chat and settings, replacing Foundry's UI.
- **Touch camera:** one finger pans, two fingers zoom.
- **Character on the bar:** drag it onto the map to move (or place) its token, tap it to open its sheet.
- **Windows fitted to the screen**, including after rotating the phone.

**Install** with this Manifest URL:
`https://github.com/ezegamer243/reclutar-rendimiento-Foundry-in-Mobile-/releases/latest/download/module.json`

**Developers:** the touch interface replaces `Token#_onClickLeft`, `ApplicationV2#render` and `Notifications#notify`
(no libWrapper). No external services, no data stored outside Foundry.

**Credits:** made by **Zeryu**, with the assistance of **Claude** (Anthropic). [MIT](LICENSE) license.
