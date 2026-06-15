# 🐺 Los Hombres Lobo de Castronegro — Asistente del Narrador

Aplicación web de una sola página para dirigir partidas de **Los Hombres Lobo de Castronegro** (*The Werewolves of Millers Hollow*). Ayuda al Narrador a configurar la partida, consultar los roles y **narrar la noche en voz alta** con la voz del navegador.

🔗 **Demo:** https://TU-USUARIO.github.io/TU-REPO/

> Sustituye `TU-USUARIO` y `TU-REPO` por los tuyos una vez publicado.

---

## ✨ Funcionalidades

- **Inicio** — introducción al juego: ambientación, objetivos de cada bando y cómo se juega.
- **Jugadores** — eliges de 8 a 18 jugadores; recomienda el número de Hombres Lobo (2 / 3 / 4) según la tabla del manual.
- **Roles** — activa los personajes especiales (Vidente, Bruja, Cazador, Niña, Cupido, Ladrón, Alguacil), con descripción y responsabilidad de cada uno. El recuento de Aldeanos se calcula en vivo.
- **Reparto** — baraja y reparte las cartas en secreto, pasando el dispositivo de mano en mano.
- **Narrador** — guion de la noche y el día generado según los roles en juego, leído en alto con **síntesis de voz** (prioriza voces en **español latinoamericano**).
- **Referencia** — equivalencia carta-del-manual ↔ nombre en español + imagen de cada carta, y el orden de la noche.

---

## 🛠️ Tecnología

- HTML + CSS + JavaScript **vanilla**, en un **único archivo** (`index.html`).
- **Sin dependencias** ni build: no necesita npm, ni framework, ni conexión a internet.
- Narración mediante la **Web Speech API** (`speechSynthesis`) del navegador.

---

## ▶️ Uso en local

Al ser un archivo estático autocontenido, basta con abrirlo:

- **Doble clic** en `index.html` → se abre en tu navegador (recomendado: Chrome o Edge).
- O sírvelo con un servidor local (útil si tu navegador tarda en cargar las voces bajo `file://`):

```bash
# Python
python -m http.server 8000
# luego abre http://localhost:8000
```

En VS Code también puedes usar la extensión **Live Server**: clic derecho sobre `index.html` → *Open with Live Server*.

---

## 🚀 Publicar en GitHub Pages

1. Sube `index.html` (y este `README.md`) a la raíz del repositorio.
2. **Settings → Pages**.
3. En **Build and deployment → Source**, elige **Deploy from a branch**.
4. En **Branch**, selecciona `main` y la carpeta `/ (root)`. Pulsa **Save**.
5. Espera unos minutos: el sitio quedará en `https://TU-USUARIO.github.io/TU-REPO/`.

> El repositorio debe ser **público** para usar Pages en el plan gratuito.
> Cada *push* a la rama publicada vuelve a desplegar el sitio en la misma URL.

---

## 🔊 Sobre las voces

La voz la genera tu navegador, así que **depende de las voces instaladas en tu sistema**:

- **Chrome / Edge** suelen incluir *«Google español de Estados Unidos»* (latina), que la app elige automáticamente.
- **Windows** — para añadir más voces latinas: *Configuración → Hora e idioma → Voz → Administrar voces → Agregar voces → Español (México)*. Habilita voces como **Sabina** o **Raúl**.

La app agrupa las voces en *Latinoamérica / España / otras* y prioriza por defecto una latinoamericana (Colombia → México → EE. UU. → cualquier otra).

---

## 📁 Estructura

```
.
├── index.html   # la aplicación completa
└── README.md
```

---

## 📜 Créditos y aviso

*Los Hombres Lobo de Castronegro* (*The Werewolves of Millers Hollow* / *Les Loups-Garous de Thiercelieux*) es un juego de **Philippe des Pallières y Hervé Marly**, publicado por **Lui-même**.

Este proyecto es una **herramienta de apoyo no oficial, hecha por aficionados**, sin relación con los autores ni la editorial. **No incluye el arte de las cartas ni el texto del reglamento**: solo asiste al Narrador y describe los roles con palabras propias. Si quieres jugar, compra el juego original.

El **código** de esta app puede usarse bajo licencia MIT (o la que prefieras). Los derechos del **juego** pertenecen a sus autores.
