# Интеграция с GitHub Copilot

The Agency работает с GitHub Copilot «из коробки». Конвертация не требуется — агенты используют существующий формат `.md` с YAML frontmatter.

## Установка

```bash
# Скопировать всех агентов в каталоги агентов GitHub Copilot
./scripts/install.sh --tool copilot

# Или скопировать вручную отдельную категорию
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

## Активация агента

В любой сессии GitHub Copilot можно обратиться к агенту по имени:

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Список агентов

Агенты сгруппированы по подразделениям. Полный список смотрите в [корневом README](../../README.md).
