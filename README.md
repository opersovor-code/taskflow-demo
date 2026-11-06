# TaskFlow Demo

PWA-застосунок для управління завданнями (комп'ютерний практикум 2.3).

**Технології:** Vue 3, Framework7, Vite, vite-plugin-pwa, Cloudflare Workers.

## Запуск

```bash
npm install
npm run dev       # http://localhost:5173
npm run build     # збірка в dist/
npm run preview   # перегляд production-збірки
```

Згенерувати іконки з `public/icons/icon.svg`:

```bash
node scripts/generate-icons.mjs
```

## Деплой

Репозиторій підключений до Cloudflare Workers (Workers & Pages → Import a repository).
Після `git push` у гілку `main` автоматично виконується `npm run build` і `npx wrangler deploy`.
Налаштування — у файлі `wrangler.jsonc`.
