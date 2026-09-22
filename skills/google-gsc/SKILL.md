---
name: google-gsc
description: >
  Разбор Google Search Console по скринам: покрытие, sitemap,
  URL inspection, CWV, ручные меры. Без автологина.
---

# Skill: Google Search Console

## Зачем

Увидеть, как Google **заявляет** статус URL. Не путать с Вебмастером
и не смешивать числа двух кабинетов.

## Когда

- Цель включает Google.
- Coverage / «Discovered – currently not indexed» / ручные меры.

## Когда не

- Нет свойства в GSC — статус `не проверено`.
- Только Яндекс в цели и пользователь не просил Google.

## Шаги

1. Тип ресурса: domain vs url-prefix. Канон должен входить в ресурс.
2. Sitemap отправлен и совпадает с каноном.
3. Отчёт «Страницы»: сгруппируй причины (`panel-errors`).
   Типичные: `alternate with proper canonical`, `crawled currently not indexed`,
   `excluded by noindex`, `blocked by robots`.
4. URL Inspection 2–3 money-страниц, если скрин есть:
   запрошенный vs выбранный канон Google.
5. `Disallow` не заменяет `noindex`. Если хотят выкинуть из индекса —
   URL должен быть доступен роботу с `noindex`.
6. CWV field — перенеси в `pagespeed`, не дублируй анализ.
7. Security / manual actions — P0.
8. Не сравнивай «страниц в GSC» со «страниц в Вебмастере» как KPI.

## Входы

- Скрины из `checklists/google-gsc.md`
- Живой HTML для сверки канона

## Выходы

- Чеклист + группы ошибок
- Что чинить на сайте vs что «подождать переобход» (без обещания срока)

## Мини-выход (вставить в отчёт)

```
Ресурс GSC: domain / url-prefix
Sitemap: ок / ошибка / нет скрина
Группы покрытия: …
Ручные меры / malware: …
```

## Типичные находки

- Domain-property на корне, продвигают поддомен, которого нет в sitemap.
- «Excluded by noindex» на проде после прелоунча.
- Canonical в HTML на http, GSC выбирает https — или наоборот.
- Coverage зелёный, CWV poor на mobile money.

## Как писать evidence

Имя отчёта GSC + фильтр + дата + пример URL.
Не нормализуй формулировки так, чтобы потерялся оригинал кабинета —
оригинал оставь в колонке «Формулировка».

## Ошибки агента

- Считать «Crawled – currently not indexed» всегда багом сайта.
- Сравнивать абсолютные «Indexed» Яндекса и Google.
- Обещать срок после «Request indexing».

## Стоп

- Выдуманный индекс / позиции / CTR из головы.
- API Search Console с ключами в этом репо.

## Связанное

- Чеклист: `checklists/google-gsc.md`
- Плейбук: `playbooks/panels-triage.md`
- Skill: `panel-errors`
