# Плейбук: разбор ошибок панелей

Для «Вебмастер красный» / «GSC Coverage» / «пропали страницы».

## Входы (без них плейбук почти бесполезен)

Попроси скрины или экспорты:

- Яндекс.Вебмастер → Индексирование / Диагностика / Безопасность / Регион
- GSC → Страницы (индексирование), Скорость, Безопасность, Настройки
- Список URL из sitemap и пример «исключённых»

Не логинься сам.

## Последовательность

1. Короткий P0: зеркало, HTTPS, не закрыт ли весь сайт в robots —
   `checklists/p0-gate.md` пункты 3–6.
2. `skills/yandex-webmaster/SKILL.md` + `checklists/yandex-webmaster.md`
3. `skills/google-gsc/SKILL.md` + `checklists/google-gsc.md` (если есть GSC)
4. `skills/panel-errors/SKILL.md` — нормализуй формулировки панелей
5. Для каждой **группы** ошибок (не каждого URL):
   - что говорит панель
   - что видно снаружи (headers, HTML, robots, canonical)
   - одно действие
6. Таблица `templates/panel-errors-table.md`
7. Если без панелей починили технику — одна гипотеза
   «после фикса переобход / переотправка sitemap».
8. Отчёт `templates/report-audit.md` с фокусом «панели».

## Правила группировки

Не раздувай 400 URL в 400 строк. Группы: `noindex`, `disallow`,
`canonical→другой хост`, `soft-404`, `redirect`, `server 5xx`,
`not found`, `duplicate without canonical`, `discovered not indexed`.

Нет evidence по группе — строка со статусом `нет данных`.
