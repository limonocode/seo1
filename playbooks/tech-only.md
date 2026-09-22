# Плейбук: только техника

Для «проверьте robots/индекс/скорость» без контент-стратегии.

## Последовательность

1. `checklists/p0-gate.md` — пункты 3–8 обязательны; панели (1–2) —
   если скринов нет, пометь «не проверено», не «ок».
2. `skills/yandex-tech/SKILL.md`
3. `skills/code-quality-perf/SKILL.md` + `checklists/code-perf-security.md`
4. `skills/pagespeed/SKILL.md` + `checklists/pagespeed.md`
5. `skills/security-surface/SKILL.md`
6. Если цель включает Google: `skills/google-gsc/SKILL.md`
   (покрытие и robots/noindex), иначе пропусти.
7. Сводка ошибок: `skills/panel-errors/SKILL.md` — только тех. коды
   (404, soft-404, redirect loop, noindex, sitemap mismatch).
8. Отчёт `templates/report-audit.md`, секции контента/гео сверни
   до «вне скоупа tech-only».

## Стоп

- Редирект-петля, неверный канон, закрытый в robots нужный раздел,
  чистый CSR на money-странице, смешанные зеркала — это блокеры.
- Не переходи к текстам и ссылкам.
