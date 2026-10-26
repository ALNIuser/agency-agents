# Интеграция с Windsurf

Весь список агентов The Agency объединён в один файл `.windsurfrules`. Правила работают **только в рамках проекта** — установщик нужно запускать из корня целевого проекта.

## Установка

```bash
# Запустите из корня вашего проекта
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

## Активация агента

В Windsurf можно сослаться на агента по имени в промпте:

```
Use the Frontend Developer agent to build this component.
```

## Повторная генерация

```bash
./scripts/convert.sh --tool windsurf
```
