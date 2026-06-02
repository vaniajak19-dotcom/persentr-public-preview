# Persentr Expert Hub Public Preview Package

Эта папка — безопасный статический пакет для публичной публикации через GitHub Pages.

В рабочем процессе проекта этот пакет обновляется автоматической синхронизацией из `public_preview_package`; ручное копирование HTML/JSON больше не требуется.

## Состав пакета

- `index.html` — стартовая страница публичного preview;
- `roadmap_dashboard.html` — статический dashboard дорожной карты;
- `roadmap_status.json` — публичные данные для dashboard;
- `.nojekyll` — отключение Jekyll-обработки GitHub Pages.

## Что намеренно не входит

Пакет не содержит внутренние материалы проекта, включая:

- `02_expertise_units/`;
- `12_mvp_control_desk/`;
- `ROADMAP.md`;
- внутренние отчёты;
- source registry;
- рабочие документы Persentr.

## Как обновляется публичный preview

1. Внутренний репозиторий обновляет безопасный `public_preview_package`.
2. Workflow синхронизации публикует пакет в этот публичный репозиторий.
3. GitHub Pages отдаёт dashboard из корня публичного репозитория.

Dashboard загружает `roadmap_status.json` из той же папки, поэтому пакет остаётся статическим и не требует дополнительных зависимостей.
