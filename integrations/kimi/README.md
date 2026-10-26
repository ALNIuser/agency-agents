# Интеграция с Kimi Code CLI

Преобразует всех агентов The Agency в спецификации Kimi Code CLI. Для каждого агента создаётся каталог, содержащий `agent.yaml` (спецификация агента) и `system.md` (системный промпт).

## Установка

### Предварительные требования

- Установленный [Kimi Code CLI](https://github.com/MoonshotAI/kimi-cli)

### Установка агентов

```bash
# Сгенерировать файлы интеграции (требуется при первом клонировании)
./scripts/convert.sh --tool kimi

# Установить агентов
./scripts/install.sh --tool kimi
```

Агенты копируются в `~/.config/kimi/agents/`.

## Использование

### Активация агента

Для загрузки конкретного агента используйте флаг `--agent-file`:

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

### В проекте

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "Review this React component for performance issues"
```

### Список установленных агентов

```bash
ls ~/.config/kimi/agents/
```

## Структура агента

Каждый каталог агента содержит:

```
~/.config/kimi/agents/frontend-developer/
├── agent.yaml    # Спецификация агента (инструменты, субагенты)
└── system.md     # Системный промпт с личностью и инструкциями
```

### Формат agent.yaml

```yaml
version: 1
agent:
  name: frontend-developer
  extend: default  # Наследует встроенного агента Kimi по умолчанию
  system_prompt_path: ./system.md
  tools:
    - "kimi_cli.tools.shell:Shell"
    - "kimi_cli.tools.file:ReadFile"
    # ... все инструменты по умолчанию
```

## Повторная генерация

После изменения исходных агентов:

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

## Устранение неполадок

### Файл агента не найден

Убедитесь, что сначала выполнен `convert.sh`, а затем `install.sh`:

```bash
./scripts/convert.sh --tool kimi
```

### Kimi CLI не обнаружен

Убедитесь, что `kimi` доступен в PATH:

```bash
which kimi
kimi --version
```

### Ошибка в YAML

Проверьте корректность сгенерированных файлов:

```bash
python3 -c "import yaml; yaml.safe_load(open('integrations/kimi/frontend-developer/agent.yaml'))"
```
