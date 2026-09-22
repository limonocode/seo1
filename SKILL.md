---
name: seo-skills-ru
description: >
  Публичный пакет SEO/GEO-гигиены для аудита сайтов в RU-поиске.
  Яндекс — primary, Google — secondary. Для агентов Cursor, Claude,
  DeepSeek, ChatGPT. Чеклисты и плейбуки, не agency OS и не автологин.
license: CC-BY-NC-SA-4.0
---

# seo-skills-ru — корневой skill

## Зачем пакет

Дать агенту **одинаковый контракт** на аудит сайта:

1. Не сломать индекс и не советовать запрещённое.
2. Сначала техника и панели, потом контент.
3. Писать отчёт с evidence, а не с выдуманными %.

Пакет закрывает публичную гигиену. Не закрывает ведение клиента,
закупку ссылок, пороги SLA и нишевые ТЗ.

## Когда использовать

- Пользователь просит аудит / «посмотри SEO» / «готовы ли к запуску».
- Нужно разобрать ошибки Вебмастера или GSC.
- Локальный бизнес: карты, NAP, каталоги, Яндекс.Бизнес.
- Проверка закона о рекламе (маркировка) на уровне гигиены.
- Техдолг: HTTPS, зеркала, SSR, CWV, безопасность поверхности.

## Когда не использовать

- Нужны приватные пороги, SOP, коннекторы — это `seo1-private`.
- Пользователь просит накрутку ПФ, PBN, биржи, Turbo, thin-фабрику.
- Задача — написать 500 programmatic-страниц «под ключи».
- Нужен автологин или обход кабинетов.

## Порядок (всегда)

1. `AGENTS.md` — контракт.
2. Плейбук из `playbooks/` (по умолчанию `full-audit.md`).
3. `checklists/p0-gate.md` — критичный fail = стоп.
4. Релевантные `skills/*/SKILL.md` + парные чеклисты.
5. Одна гипотеза: `templates/hypothesis-card.md`.
6. Отчёт: `templates/report-audit.md`.

## Карта skills

| Skill | Панель / тема | Чеклист |
|-------|----------------|---------|
| `yandex-requirements` | Требования Яндекса | `p0-gate` |
| `yandex-webmaster` | Яндекс.Вебмастер | `yandex-webmaster` |
| `yandex-metrika` | Метрика | `yandex-metrika` |
| `yandex-tech` | Техника под робота Яндекса | `p0-gate`, `code-perf-security` |
| `yandex-geo-neuro` | Карты / Бизнес / Neuro | `geo-nap-catalogs` |
| `google-requirements` | Требования Google | `p0-gate` |
| `google-gsc` | Search Console | `google-gsc` |
| `google-analytics` | GA4 (вторично) | — |
| `pagespeed` | CWV / PageSpeed | `pagespeed` |
| `geo-local` | Локальная выдача | `geo-nap-catalogs` |
| `geo-catalogs` | Каталоги (не PBN) | `geo-nap-catalogs` |
| `ru-ads-law` | Маркировка рекламы | `ru-ads-law` |
| `code-quality-perf` | Код и скорость | `code-perf-security` |
| `security-surface` | Поверхность атаки / HTTPS | `code-perf-security` |
| `panel-errors` | Разбор ошибок кабинетов | `yandex-webmaster`, `google-gsc` |
| `domain-trust` | История и доверие домена | `domain-trust` |

## Входы

Минимум:

- URL канона и список зеркал
- регион / язык
- цель: Яндекс / Google / оба
- что пользователь уже видел в панелях (или «панелей нет»)

Без панелей можно сделать **внешний** техсрез (HTML, robots, sitemap,
редиректы, SSR). Нельзя ставить вердикт «индекс чистый».

## Выходы

- Отчёт по шаблону
- 0–1 гипотеза (не дорожная карта на 40 пунктов)
- Список недостающих evidence

## Стоп-условия

- Критичный P0 fail и пользователь не чинит технику — не уходи в «контент-стратегию».
- Запрос из dead-list — отказ + ссылка на `references/dead-list.md`.
- Просьба раскрыть private SOP — отказ, указать `seo1-private`.
- Попытка изменить файл `Без названия-3` — отказ.

## Источники

Официальные ссылки — `references/sources-2026.md`.
Сначала документация Яндекса и Google, потом блоги.
