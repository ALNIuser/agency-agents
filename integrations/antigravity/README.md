# Интеграция с Antigravity

Устанавливает весь список агентов The Agency в виде навыков Antigravity. Каждый агент получает префикс `agency-` во избежание конфликтов с уже существующими навыками.

## Установка

```bash
./scripts/install.sh --tool antigravity
```

Файлы копируются из `integrations/antigravity/` в `~/.gemini/config/skills/` (глобально). Для навыков, доступных только в проекте, Antigravity также считывает `<project>/.agents/skills/`.

## Активация навыка

В Antigravity активируйте агента по его slug:

```
Use the agency-frontend-developer skill to review this component.
```

Доступные slug'и соответствуют шаблону `agency-<имя-агента>`, например:
- `agency-frontend-developer`
- `agency-backend-architect`
- `agency-reality-checker`
- `agency-growth-hacker`

## Повторная генерация

После изменения исходных агентов повторно сгенерируйте файлы навыков:

```bash
./scripts/convert.sh --tool antigravity
```

## Формат файла

Каждый навык — это файл `SKILL.md` с frontmatter, совместимым с Antigravity:

```yaml
---
name: agency-frontend-developer
description: Expert frontend developer specializing in...
risk: low
source: community
date_added: '2026-03-08'
---
```
