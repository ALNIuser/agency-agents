# Интеграция с OpenCode

> **❌ Не делайте так:**
>
> ```bash
> # НЕПРАВИЛЬНО — приведёт к ошибкам валидации схемы
> cp agency-agents/engineering/*.md .opencode/agents/
> ```
>
> **✅ Делайте так:**
>
> ```bash
> /path/to/agency-agents/scripts/install.sh --tool opencode
> ```
>
> Исходные файлы используют именованные цвета и поле `tools`, которые OpenCode не поддерживает.
> Установщик автоматически конвертирует их в шестнадцатеричные коды `#RRGGBB` и удаляет несовместимые поля.

Агенты OpenCode — это файлы `.md` с YAML frontmatter, размещённые в каталоге `.opencode/agents/`. Конвертер сопоставляет именованные цвета с hex-кодами и добавляет `mode: subagent`, чтобы агенты вызывались по требованию через `@agent-name`, не загромождая основной список агентов.

## Установка

```bash
# Запустите из корня вашего проекта
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

В результате в каталоге проекта будут созданы файлы `.opencode/agents/<slug>.md`.

## Активация агента

В OpenCode вызовите субагента с префиксом `@`:

```
@frontend-developer help build this component.
```

```
@reality-checker review this PR.
```

Также можно выбрать агента из списка выбора агентов в интерфейсе OpenCode.

## Формат агента

Каждый сгенерированный файл агента содержит:

```yaml
---
name: Frontend Developer
description: Expert frontend developer specializing in modern web technologies...
mode: subagent
color: "#00FFFF"
---
```

- **mode: subagent** — агент доступен по требованию, не отображается в основном списке переключения по Tab
- **color** — шестнадцатеричный код (именованные цвета из исходных файлов конвертируются автоматически)

## Проектный или глобальный доступ

Агенты в `.opencode/agents/` доступны **только в рамках проекта**. Чтобы сделать их доступными глобально во всех проектах, сначала сгенерируйте файлы агентов, затем установите с параметром `--path`:

```bash
./scripts/convert.sh --tool opencode
./scripts/install.sh --tool opencode --path ~/.config/opencode/agents
```

## Повторная генерация

```bash
./scripts/convert.sh --tool opencode
```
