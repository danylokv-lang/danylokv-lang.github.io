# World of Sea Battle — фан‑сайт гильдии

Готово к публикации на Netlify как статический SPA‑проект.

## Структура
- `index.html` — основной одностраничный сайт (SPA)
- `_redirects` — fallback‑редирект для SPA (все пути -> `index.html`)
- `netlify.toml` — минимальная конфигурация Netlify (`publish = "."`)
- Папка с изображениями (если используются локальные изображения) — положите рядом, например `./assets/`

## Публикация: быстрый способ (через UI)
1) Зайдите на https://app.netlify.com/ и создайте сайт.
2) Перетащите папку проекта в окно “Deploy a site by dragging & dropping”.
3) Убедитесь, что `_redirects` и `netlify.toml` попали на хостинг.

## Публикация через Git
1) Создайте Git‑репозиторий и запушьте проект на GitHub/GitLab/Bitbucket.
2) В Netlify → “Add new site” → “Import an existing project”.
3) Выберите репозиторий. Build‑команда: пусто. Publish directory: `.`
4) Дождитесь деплоя.

## Публикация через Netlify CLI (локально)
Требуется Node.js и Netlify CLI.

```powershell
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --dir . --prod
```

## Примечания
- Проект SPA: все маршруты отдаются через `index.html` (см. `_redirects`/`netlify.toml`).
- Изображения загружаются по номерам (`1.jpg`, `2.png`, `...`) с автоподстановкой расширений. Залейте соответствующие файлы рядом с `index.html` или скорректируйте пути в коде.
