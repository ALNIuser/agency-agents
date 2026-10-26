# Интеграция с Gemini CLI

Упаковывает всех агентов The Agency в виде субагентов Gemini CLI. Агенты устанавливаются в `~/.gemini/agents/`.

## Установка

```bash
# Сначала сгенерировать файлы агентов для Gemini CLI
./scripts/convert.sh --tool gemini-cli

# Затем установить их в ~/.gemini/agents/
./scripts/install.sh --tool gemini-cli
```

## Использование агента

В Gemini CLI можно сослаться на агента по имени в промпте:

```
Use the frontend-developer agent to help me build this UI.
```

Или вызвать агент напрямую, если ваша версия Gemini CLI поддерживает это:

```bash
gemini --agent frontend-developer "How should I structure this React component?"
```

## Структура

```
~/.gemini/agents/
  frontend-developer.md
  backend-architect.md
  reality-checker.md
  ...
```

## Повторная генерация

```bash
./scripts/convert.sh --tool gemini-cli
```
