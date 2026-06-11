---
name: russian-language-skill
description: "Comprehensive reference library of Russian language rules — orthography, punctuation, stylistics, and grammar. Use when the task involves Russian-language text generation, proofreading, editing, translation, or linguistic analysis; when checking spelling, punctuation, or stylistic correctness of Russian text; or when teaching/explaining Russian language rules to learners."
---

# Russian Language Rules — библиотека правил русского языка

## Алгоритм выбора правила

### Шаг 1. Определите тип задачи

| Ситуация | Раздел |
|---|---|
| Нужно проверить или объяснить написание слова | references/spelling/ (орфография) |
| Нужно расставить или объяснить знаки препинания | references/punctuation/ (пунктуация) |
| Нужно улучшить стиль текста, выбрать тон | references/stylistics/ (стилистика) |
| Нужно объяснить склонение, спряжение, синтаксис | references/grammar/ (грамматика) |

### Шаг 2. Если задача по орфографии

| Ситуация | Файл |
|---|---|
| Сомнительная гласная проверяется ударением (гора́ — го́ры) | 01-checked-unstressed-vowels |
| Сомнительная гласная НЕ проверяется ударением (словарное слово) | 02-uncheckable-vowels |
| Чередование в корне (расти́ — ро́с, каса́ться — косну́ться) | 03-alternating-vowels |

### Шаг 3. Загрузите файл в контекст

1. Определите нужный файл по алгоритму выше.
2. Прочитайте соответствующий файл из `references/`.
3. Найдите в нём подходящее правило.
4. Примените правило к вашему тексту.

## Структура репозитория

```
russian-lib/
├── SKILL.md                    # Этот файл — точка входа для агента
├── agents/openai.yaml          # UI-метаданные
├── references/
│   ├── spelling/               # Орфография
│   │   ├── 01-checked-unstressed-vowels.md
│   │   ├── 02-uncheckable-vowels.md
│   │   └── 03-alternating-vowels.md
│   ├── punctuation/            # Пунктуация
│   ├── stylistics/             # Стилистика
│   └── grammar/                # Грамматика
├── scripts/                    # Скрипты
└── assets/                     # Ресурсы
```
