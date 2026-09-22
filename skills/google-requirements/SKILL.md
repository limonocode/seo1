---
name: google-requirements
description: >
  Публичные ожидания Google: полезный оригинал, E-E-A-T как рамка,
  crawlable HTML, field CWV. AI Overviews = всё ещё SEO.
---

# Skill: требования Google

## Зачем

Вторичный контур для RU-сайтов, которым нужен Google. Не подменять
Яндекс-P0 «ссылочной стратегией».

## Когда

- Цель «оба» или «Google».
- Вопросы про AI Overviews / helpful content / CWV.

## Когда не

- Цель только Яндекс — достаточно короткой пометки N/A.
- Просьба купить ссылки / Reddit-спам / FAQ rich result как KPI.

## Шаги

1. Сначала тот же техбазис, что для Яндекса (`yandex-tech`):
   канон, HTTPS, SSR, mobile-first.
2. Контент: кто автор/организация, есть ли опыт и источники,
   нет ли тонких страниц под каждый ключ.
3. E-E-A-T — рамка Quality Rater, не отдельный «балльный фактор».
   Не ставь «E-E-A-T = 7/10».
4. Organization + `sameAs` на реальные профили — ок как разметка.
   Не выдумывай профили.
5. AI Overviews: офиц. гайд — crawlable публичный оригинал,
   не спец. AI-файлы. `llms.txt` не цель.
6. FAQ-разметка как структура текста — можно; как охота на rich result —
   dead-list.
7. CWV — field, `skills/pagespeed`. Лаборатория не равна ранжированию.
8. Ссылки: если пользователь не дал выгрузку — не оценивай профиль.
   Не предлагай биржу.

## Входы

- HTML, GSC (опционально), понимание типа сайта
- `checklists/p0-gate.md`, при Google ещё `google-gsc.md`

## Выходы

- Расхождения с публичными гайдами Search Central
- Список того, что Google-слой **не** проверяли

## Типичные находки

- Авторы «Admin», даты 2019, факты без источников.
- FAQ-schema пачкой на каждую статью «ради rich result».
- CSR-only блог, который «Google всё равно проиндексирует» — риск задержки
  и проблем у не-Google ботов.
- Organization без `sameAs` или с битыми соцпрофилями.

## Как писать evidence

Цитируй конкретный гайд Search Central из `references/sources-2026.md`
и кусок HTML. Не цитируй «SEJ сказал +4.6%» как норму.

## AI Overviews

Офиц. линия: generative features укоренены в Search, отдельный
хак не нужен. Нужны индексация, оригинал, прозрачность авторства.

## Ошибки агента

- Ставить Google-ссылки впереди Яндекс-P0 на RU-рынке без запроса.
- Называть E-E-A-T числом.
- Обещать FAQ-звёзды.

## Стоп

- Точные % PageRank / backlinks.
- Thin programmatic «под Google».
- P0 техника красная.

## Связанное

- Чеклист: `checklists/p0-gate.md`, `google-gsc.md`
- Источник: AI optimization guide в `references/sources-2026.md`
