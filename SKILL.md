---
name: russian-language-skill
description: "Comprehensive reference library of Russian language rules — orthography, punctuation, stylistics, and grammar. Use when the task involves Russian-language text generation, proofreading, editing, translation, or linguistic analysis; when checking spelling, punctuation, or stylistic correctness of Russian text; or when teaching/explaining Russian language rules to learners."
---

# Russian Language Rules — библиотека правил русского языка

## Алгоритм выбора правила

### Шаг 1. Определите тип задачи

| Ситуация | Раздел |
|---|---|
| Нужно проверить или объяснить написание слова | `references/spelling/` (орфография) |
| Нужно расставить или объяснить знаки препинания | `references/punctuation/` (пунктуация) |
| Нужно улучшить стиль текста, выбрать тон | `references/stylistics/` (стилистика) |
| Нужно объяснить склонение, спряжение, синтаксис | `references/grammar/` (грамматика) |

### Шаг 2. Если задача по орфографии

| Ситуация | Файл |
|---|---|
| Сомнительная гласная проверяется ударением (гора́ — го́ры) | `01-checked-unstressed-vowels` |
| Сомнительная гласная НЕ проверяется ударением (словарное слово) | `02-uncheckable-vowels` |
| Чередование в корне (расти́ — ро́с, каса́ться — косну́ться) | `03-alternating-vowels` |
| Гласные после шипящих (жи/ши, ча/ща, чу/щу, о/ё) | `04-vowels-after-sibilants` |
| Гласные после ц (ци/цы, цю/ця) | `05-vowels-after-ts` |
| Буквы Э и Е (после приставок, в иноязычных словах) | `06-letters-e-e` |
| Буква Й (в начале иноязычных слов) | `07-letter-y` |
| Сомнительная согласная в корне (звонкие/глухие) | `08-voiced-voiceless-consonants` |
| Двойные согласные (в корне, на стыке приставки и корня) | `09-double-consonants` |
| Непроизносимые согласные (вств, здн, стн и др.) | `10-unpronounceable-consonants` |

### Шаг 3. Загрузите файл в контекст

1. Определите нужный файл по алгоритму выше.
2. Прочитайте соответствующий файл из `references/`.
3. Найдите в нём подходящее правило.
4. Примените правило к вашему тексту.

## Структура репозитория

```
russian-lib/
├── SKILL.md                    # Этот файл — точка входа для агента
├── .crossref.yaml              # Индекс перекрёстных ссылок (§ → файл)
├── agents/openai.yaml          # UI-метаданные
├── references/
│   ├── spelling/               # Орфография
│   │   ├── 01-checked-unstressed-vowels.md
│   │   ├── 02-uncheckable-vowels.md
│   │   ├── 03-alternating-vowels.md
│   │   ├── 04-vowels-after-sibilants.md
│   │   ├── 05-vowels-after-ts.md
│   │   ├── 06-letters-e-e.md
│   │   ├── 07-letter-y.md
│   │   ├── 08-voiced-voiceless-consonants.md
│   │   ├── 09-double-consonants.md
│   │   └── 10-unpronounceable-consonants.md
│   ├── punctuation/            # Пунктуация
│   ├── stylistics/             # Стилистика
│   └── grammar/                # Грамматика
├── scripts/                    # Скрипты
└── assets/                     # Ресурсы
```

## Соглашение о перекрёстных ссылках

Ссылки на другие правила оформляются как Markdown-ссылки вида `[§8](08-voiced-voiceless-consonants.md)`, где часть после `](` — имя файла (с путём, если файл в другом каталоге).

Для ещё не созданных файлов ссылки оформляются как `§31` (только номер параграфа, без Markdown-ссылки). Когда файл будет добавлен, ссылка заменяется на полноценную Markdown-ссылку.

Маппинг номеров параграфов на имена файлов см. в `.crossref.yaml` и в `references/spelling/README.md`.
