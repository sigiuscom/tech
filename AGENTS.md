# AGENTS.md

This file provides guidance to Codex when working with code in this repository.

## Что это

mdBook-сайт "Tech Docs" (технические заметки для обучения / собеседований, язык `ru`),
автор Sergey Golubev. Git remote `sigiuscom/tech`. Контент в `src/`, оглавление `SUMMARY.md`,
конфиг `book.toml`. Домен (CNAME) `sigius.com`.

## Команды

```bash
mdbook serve    # локальный preview с авто-перезагрузкой
mdbook build    # сборка статики -> book/
```

## Деплой

GitHub Actions `.github/workflows/main.yml` (`publish`):
- триггер: push в `master`
- runner: `aks-self-hosted`
- setup mdBook `0.4.25` -> `mdbook build` -> копирование `CNAME` и `README.md` в `book/`
- публикация `./book` в ветку `deployment` (GitHub Pages) через `peaceiris/actions-gh-pages`

## Связанное

- Operational hub: `../CLAUDE.md`
