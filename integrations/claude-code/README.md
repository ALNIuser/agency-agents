# Интеграция с Claude Code

The Agency изначально разрабатывался для Claude Code. Конвертация не требуется — агенты работают нативно в существующем формате `.md` с YAML frontmatter.

## Установка

```bash
# Скопировать всех агентов в каталог агентов Claude Code
./scripts/install.sh --tool claude-code

# Или скопировать вручную отдельную категорию
cp engineering/*.md ~/.claude/agents/
```

## Активация агента

В любой сессии Claude Code можно обратиться к агенту по имени:

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Список агентов

Агенты сгруппированы по подразделениям. Полный список смотрите в [корневом README](../../README.md).
