# Интеграция с Cursor

Преобразует весь список агентов The Agency в файлы правил Cursor формата `.mdc`. Правила работают **только в рамках проекта** — установщик нужно запускать из корня целевого проекта.

## Установка

```bash
# Запустите из корня вашего проекта
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

В проекте будут созданы файлы `.cursor/rules/<agent-slug>.mdc`.

## Активация правила

В Cursor можно сослаться на агента в промпте:

```
@frontend-developer Review this React component for performance issues.
```

Или сделать правило всегда активным, изменив его frontmatter:

```yaml
---
description: Expert frontend developer...
globs: "**/*.tsx,**/*.ts"
alwaysApply: true
---
```

## Повторная генерация

```bash
./scripts/convert.sh --tool cursor
```
