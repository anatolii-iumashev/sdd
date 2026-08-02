---
name: sdd
description: Spec-Driven Development — цикл работы с фичами через спецификации. Под-скиллы: sdd-rfc (создать RFC в docs/rfc/), sdd-implement (начать реализацию по RFC), sdd-apply (завершить: RFC в архив, сводка в docs/specs/).
trigger_phrases:
  - "sdd"
  - "spec driven"
  - "spec-driven"
  - "спека"
  - "спецификация"
  - "rfc"
  - "напиши RFC"
  - "design doc"
  - "техническое задание"
  - "ТЗ"
  - "опиши фичу"
related_skills: []
---

# SDD — Spec-Driven Development

Цикл работы с фичами и изменениями через спецификации:

```
sdd-rfc  →  sdd-implement  →  sdd-apply
(спека rfc)     (реализация)      (финализация - сохранение в specs итоговых результатов)
```

1. **RFC** — фиксируем проблему, цели, состав решения и критерии приёмки в `docs/rfc/`
2. **Implement** — реализуем по RFC, сверяясь с критериями приёмки
3. **Apply** — RFC уходит в архив, итоговая сводка (что реально сделано) — в `docs/specs/`

## Под-скиллы

| Задача | Скилл | Инструкции |
|--------|-------|------------|
| Создать RFC / спецификацию | `sdd-rfc` | [./rfc/SKILL.md](./rfc/SKILL.md) |
| Начать реализацию по RFC | `sdd-implement` | [./implement/SKILL.md](./implement/SKILL.md) |
| Завершить фичу: архив + сводка | `sdd-apply` | [./apply/SKILL.md](./apply/SKILL.md) |

## Конвенции

- Все пути — относительно корня проекта, в котором идёт работа.
- Активные RFC: `docs/rfc/<slug>.md`
- Архив RFC: `docs/rfc/archive/<slug>.md`
- Итоговые спеки: `docs/specs/<slug>.md`
- `<slug>` — короткое имя фичи kebab-case, одинаковое на всех этапах цикла.
- Статус жизненного цикла хранится во frontmatter RFC: `draft → review → approved → implementing → done`

## Маршрутизация

- «напиши RFC», «опиши фичу», «сделай спеку», «ТЗ» → **sdd-rfc**
- «начинаем делать», «реализуем по RFC», «возьми в работу» → **sdd-implement**
- «завершаем», «применяем», «фича готова, закрой спеку» → **sdd-apply**

Если непонятно, на каком этапе фича — посмотреть статус во frontmatter файла в `docs/rfc/`.
