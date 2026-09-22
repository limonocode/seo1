# seo-skills-ru — публичные SEO/GEO skills для агентов (Яндекс + Google)

Markdown-пакет, чтобы любой агент (Cursor, Claude, DeepSeek, ChatGPT) мог
провести **гигиенический аудит** сайта в RU-поиске.

**Яндекс — primary. Google — secondary.**

Это публичный слой leadgen-гигиены: чеклисты, плейбуки и skills.
Не «операционка агентства» и не автопилот кабинета.

## Что внутри

- `skills/` — короткие инструкции «зачем / когда / шаги / стоп»
- `playbooks/` — последовательности аудита (полный, техника, панели, гео, прелоунч)
- `checklists/` — ворота и панели (Вебмастер, Метрика, GSC, PageSpeed, закон, домен)
- `templates/` — отчёт, карточка гипотезы, таблица ошибок панелей
- `prompts/` — system/user промпты, если нет Cursor rules
- `references/` — dead-list и публичные источники 2026
- `AGENTS.md` — контракт для любого агента
- `SKILL.md` — корневой skill пакета

## Это не

- автологин в Вебмастер / GSC / Метрику
- накрутка поведенческих факторов
- PBN, биржи ссылок, doorway, thin-контент-фабрика
- white-label «agency OS» с порогами SOP и клиентскими ТЗ
- обещание точных % факторов ранжирования

Частные пороги, SOP, нишевые брифы и коннекторы живут в **отдельном
приватном репозитории `seo1-private`** и сюда не входят.
См. [PUBLIC_VS_PRIVATE.md](PUBLIC_VS_PRIVATE.md).

## Установка

```bash
git clone https://github.com/limonocode/seo1.git
```

Дальше — любой из способов:

1. **Cursor / Claude Code** — положи репозиторий рядом с проектом сайта
   и укажи агенту читать `AGENTS.md` + `SKILL.md`.
2. **Cursor rule** — добавь `AGENTS.md` (или корневой `SKILL.md`) как rule.
3. **ChatGPT / DeepSeek / любой чат** — вставь `prompts/chatgpt-system.md`
   или `prompts/deepseek-system.md`, затем `prompts/universal-user-audit.md`.

Агент **не ходит в кабинеты сам**. Нужны скриншоты, экспорты, HTML,
`robots.txt`, sitemap и доступ к коду — то, что даст пользователь.

## Карта модулей

| Слой | Модули |
|------|--------|
| Ворота | `checklists/p0-gate.md` — критичный fail = стоп |
| Яндекс | requirements, webmaster, metrika, tech, geo-neuro |
| Google | requirements, gsc, analytics, pagespeed |
| GEO / локалка | geo-local, geo-catalogs |
| Гигиена | ru-ads-law, domain-trust, code-quality-perf, security-surface, panel-errors |
| Сценарии | full-audit, tech-only, panels-triage, local-geo, prelaunch |

Порядок для агента — в [AGENTS.md](AGENTS.md).

## Быстрый старт

1. Прочитай `SKILL.md` и выбери плейбук (`playbooks/full-audit.md` по умолчанию).
2. Прогони `checklists/p0-gate.md`. Критичный ❌ — не иди в контент.
3. Одна гипотеза за раз (`templates/hypothesis-card.md`).
4. Отчёт только по `templates/report-audit.md`. Не выдумывай метрики панелей.
5. Не предлагай пункты из `references/dead-list.md`.

## Исторический файл

В корне лежит `Без названия-3` — **не изменять, не переименовывать,
не удалять**. Это исторический blob репозитория (2017). Старые
заглушки `meta` / `robots.txt` / `sitemap` перенесены в
`archive/2017-stub/`.

## Лицензия

Тексты — [CC BY-NC-SA 4.0](LICENSE). Атрибуция: **limonocode / seo-skills-ru**.
Коммерческий white-label перепродаж пакета без разрешения запрещён.
Будущие скрипты в `scripts/` могут получить отдельную MIT-пометку.

## Сопровождение

Нужен полный аудит и ведение, а не только чеклист:

**https://prodvizhenie.agency**
