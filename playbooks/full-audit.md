# Плейбук: полный аудит

Для запроса «посмотрите сайт» / «SEO-аудит» / «что не так с органикой».
Яндекс — primary. Google — если пользователь отметил «оба» или Google.

## Последовательность

1. **Контракт** — корневой `SKILL.md` и `AGENTS.md`.
2. **P0-ворота** — `checklists/p0-gate.md`.
   Критичный ❌ → стоп, отчёт только с блокерами.
3. **Панели Яндекса**
   - `skills/yandex-webmaster/SKILL.md` + `checklists/yandex-webmaster.md`
   - `skills/yandex-metrika/SKILL.md` + `checklists/yandex-metrika.md`
4. **Панели Google** (если цель включает Google)
   - `skills/google-gsc/SKILL.md` + `checklists/google-gsc.md`
   - `skills/google-analytics/SKILL.md` — только если есть доступ/скрины
5. **Ошибки кабинетов** — `skills/panel-errors/SKILL.md`
   → таблица `templates/panel-errors-table.md`
6. **Техника**
   - `skills/yandex-tech/SKILL.md`
   - `skills/yandex-requirements/SKILL.md`
   - `skills/google-requirements/SKILL.md` (если Google в цели)
   - `skills/code-quality-perf/SKILL.md` + `skills/pagespeed/SKILL.md`
   - `skills/security-surface/SKILL.md`
   - чеклист `checklists/code-perf-security.md` и `checklists/pagespeed.md`
7. **Домен** — `skills/domain-trust/SKILL.md` + `checklists/domain-trust.md`
8. **Локалка** — если тип = local / есть офлайн-точка:
   `playbooks/local-geo.md` (не дублируй здесь шаги, вызови плейбук)
9. **Реклама** — `skills/ru-ads-law/SKILL.md` + `checklists/ru-ads-law.md`
   (если на сайте есть реклама, офферы партнёров или сам сайт — рекламный)
10. **Одна гипотеза** — `templates/hypothesis-card.md`
11. **Отчёт** — `templates/report-audit.md`

## Чего не делать в полном аудите

- Не собирать семантику на 500 ключей.
- Не писать контент-план, пока P0 не PASS.
- Не ставить «позиции» north star без бизнес-метрики.
- Не смешивать 10 гипотез в один отчёт.

## Выход

Один markdown-отчёт + опционально таблица ошибок панелей + одна карточка гипотезы.
