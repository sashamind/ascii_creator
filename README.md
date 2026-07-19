# НАБОР / nabor

**ASCII image generator that runs entirely in the browser.**
Drop an image → get editable ASCII art → tweak it character by character → export.

*Набор* — Russian for both a typesetter's "composition" and a "character set". Which is exactly what this does.

**[→ Live demo](https://sashamind.github.io/nabor/)**

---

## Features

- **Input** — file picker, drag & drop, paste from clipboard (Ctrl+V), or a built-in procedural demo image
- **Copy to clipboard** — one click to grab the result as plain text
- **Generation controls** — width in characters (20–300), brightness, contrast, gamma, invert
- **Character sets** — classic ramp, detailed 70-char ramp, blocks `░▒▓█`, strokes, binary, or type your own (light → dark), plus a shuffle button that randomizes the current set for textured, glitchy looks
- **Direct editing** — the output is editable text; click and retype any character. Manual edits pause auto-regeneration so your work isn't wiped, and "regenerate" can be undone
- **Persistent settings** — all controls are saved to `localStorage` between sessions, with a one-click reset to defaults
- **Typography** — monospace font presets + upload your own `.ttf` / `.otf` / `.woff2`, adjustable size, weight (100–900), line height, tracking. The rendered image keeps a fixed size and aspect ratio: typography controls change the character density inside it, and the width slider anchors the size
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

- Настройки генерации: ширина в символах, яркость, контраст, гамма, инверсия
- Наборы символов: готовые + свой (порядок от светлого к тёмному) + кнопка случайного перемешивания набора для фактурных экспериментов
- Шрифты: базовые моноширинные + загрузка своих (`.ttf`, `.otf`, `.woff2`), кегль, толщина, интерлиньяж, трекинг — размер и пропорции картинки при этом не меняются: типографика управляет плотностью символов внутри, а размер якорится слайдером ширины
- Цвета текста и фона с пресетами; генератор учитывает светлоту фона
- Ручные правки не затираются автоперегенерацией; перегенерацию можно отменить
- Настройки сохраняются между сессиями (localStorage), есть кнопка сброса к значениям по умолчанию
- Копирование результата в буфер одной кнопкой
- Экспорт: `.txt`, `.png` (3×), `.svg`

Без зависимостей и сборки — один HTML-файл. Открой `index.html`, и всё работает.

## License

MIT — see [LICENSE](LICENSE).
