# Интеграция с DeepSeek Harness (DSH)

Устанавливает весь список агентов The Agency в виде навыков DeepSeek Harness. Каждый агент получает префикс `agency-` во избежание конфликтов со встроенными навыками.

## Установка

```bash
./scripts/install.sh --tool dsh
```

Файлы копируются из `integrations/dsh/` в `${DSH_HOME:-$HOME/.dsh}/skills/` (пользовательский уровень). Если конфигурация Harness находится в другом месте, задайте переменную `DSH_HOME`. Для установки навыков в рамках проекта запустите установщик с `DSH_SKILLS_DIR=.dsh/skills` из корня проекта — этот параметр имеет приоритет над `DSH_HOME`, и DSH автоматически будет читать `<project>/.dsh/skills/`.

> DSH обнаруживает навыки динамически (отслеживает каталоги): новые, переименованные или удалённые навыки попадут в каталог при следующем обновлении без перезапуска. Редактировать конфигурационный файл не требуется.

## Активация навыка

В DSH навыки доступны пользователю и модели по умолчанию. Активируйте агента командой слэш или просто упомянув его в диалоге:

```
/agency-frontend-developer review this React component
```

или:

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
./scripts/convert.sh --tool dsh
```

## Формат файла

Каждый навык — это файл `SKILL.md` со стандартным frontmatter формата Agent-Skills (обязательные поля `name` и `description`, имя строго в kebab-case) и телом агента:

```markdown
---
name: 'agency-frontend-developer'
description: 'Expert frontend developer specializing in modern web technologies, React/Vue/Angular frameworks, UI implementation, and performance optimization'
---
...тело агента...
```

Формат идентичен выводу Antigravity и Osaurus (`skill-md`), поэтому приложение Agency Agents отображает его нативно.

## Каталоги с навыками, сканируемые DSH

| Приоритет | Источник | Путь |
|---|---|---|
| 100 | проект | `<project>/.dsh/skills` |
| 200 | проект | `<project>/.agents/skills` |
| 300 | пользовательский (настраиваемый) | `customSkillDirs` в конфигурации |
| 400 | пользователь | `${DSH_HOME:-$HOME/.dsh}/skills` (установка по умолчанию) |
| 500 | пользователь | `~/.agents/skills` |

Навыки проекта (приоритет 100/200) перекрывают пользовательские (приоритет 400/500) с тем же именем, поэтому установка в проекте имеет приоритет для данного проекта.
