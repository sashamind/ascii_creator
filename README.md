# ascii_creator

**ASCII image generator that runs entirely in the browser.**
Drop an image → get editable ASCII art → tweak it character by character → export.

**[→ Live demo](https://sashamind.github.io/ascii_creator/)**

---

## Features

- **Input** — file picker, drag & drop, paste from clipboard (Ctrl+V), or a built-in procedural demo image
- **Copy to clipboard** — one click to grab the result as plain text
- **Generation controls** — brightness, contrast, gamma, invert
- **Contour mode** — a Sobel edge-detection pass with an adjustable threshold. Outlines are drawn either with directional line characters (ASCII / box-drawing / heavy / double) or with any density set — including your own — mapped to edge strength; invert turns it into a stencil that keeps the chosen set
- **Character sets** — classic ramp, detailed 70-char ramp, blocks `░▒▓█`, strokes, binary, or type your own (light → dark), plus a shuffle button that randomizes the current set for textured, glitchy looks
- **Direct editing** — the output is editable text; click and retype any character. Clicking a character also loads it into the replace tool. Manual edits pause auto-regeneration so your work isn't wiped
- **Undo / redo** — a full history of the graphic (generation, manual edits, replacements) with ↶ / ↷ buttons and Ctrl/⌘+Z (Shift for redo)
- **Persistent settings** — all controls are saved to `localStorage` between sessions, with a one-click reset to defaults
- **Fixed, auto-fit size** — the image is sized to the working area and can't be resized by hand: on mobile it fills the screen width, on desktop it fits the height of the working area (width follows the aspect ratio). Always centered, and reflows on window resize / rotation
- **Typography** — monospace font presets + upload your own `.ttf` / `.otf` / `.woff2`, adjustable size, weight (100–900), line height, tracking. Typography controls change the character density inside that fixed size, not the image size itself
- **Color** — foreground/background pickers, swap, presets. The generator is background-aware: dense characters map to dark image areas on light backgrounds (like ink on paper) and to bright areas on dark backgrounds
- **Export** — `.txt`, `.png` (3× render), `.svg` (text elements — convert to outlines in a vector editor if you used a custom font)

Zero dependencies, zero build step, zero network requests. One HTML file.

## Run locally

Open `index.html` in a browser. That's it.

## Deploy to GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → Save.

---

## По-русски

**ASCII-генератор из картинок, работает целиком в браузере.**

Загрузи картинку (кнопкой, перетаскиванием или Ctrl+V) — получи ASCII-графику, которую можно править прямо как текст, посимвольно.

- Настройки генерации: яркость, контраст, гамма, инверсия
- Контурный режим: детекция краёв по Собелю с настраиваемым порогом. Контур рисуется либо символами линий по направлению края (ASCII / линии / жирные / двойные), либо любым набором плотности (включая свой) — по силе края; инверсия делает стенсил, сохраняя выбранный набор
- Размер картинки подгоняется под рабочую область и вручную не меняется: на мобильном — по ширине экрана, на десктопе — по высоте рабочей области (ширина из пропорций). Картинка всегда по центру, пересчёт при ресайзе окна и повороте
- Наборы символов: готовые + свой (порядок от светлого к тёмному) + кнопка случайного перемешивания набора для фактурных экспериментов
- Шрифты: базовые моноширинные + загрузка своих (`.ttf`, `.otf`, `.woff2`), кегль, толщина, интерлиньяж, трекинг — типографика управляет только плотностью символов внутри фиксированного размера, а не размером картинки
- Цвета текста и фона с пресетами; генератор учитывает светлоту фона
- Ручные правки не затираются автоперегенерацией; клик по символу подставляет его в замену
- Undo / redo всей графики (генерация, правки, замены): кнопки ↶ / ↷ и Ctrl/⌘+Z (Shift — вперёд)
- Настройки сохраняются между сессиями (localStorage), есть кнопка сброса к значениям по умолчанию
- Копирование результата в буфер одной кнопкой
- Экспорт: `.txt`, `.png` (3×), `.svg`

Без зависимостей и сборки — один HTML-файл. Открой `index.html`, и всё работает.

## License

MIT — see [LICENSE](LICENSE).
