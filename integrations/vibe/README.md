# Интеграция с Mistral Vibe

В Mistral Vibe для каждого агента используются два файла:
- Файл конфигурации TOML (`~/.vibe/agents/<slug>.toml`)
- Файл промпта Markdown (`~/.vibe/prompts/<slug>.md`)

Сгенерированные файлы создаются командой `scripts/convert.sh --tool vibe` — для каждого агента The Agency создаётся пара: TOML-конфигурация в `integrations/vibe/agents/` и Markdown-промпт в `integrations/vibe/prompts/`.

## Генерация

Из корня репозитория:

```bash
./scripts/convert.sh --tool vibe
```

## Установка

Запустите установщик из целевого каталога:

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool vibe
```

Файлы будут скопированы в:

```text
~/.vibe/agents/<slug>.toml
~/.vibe/prompts/<slug>.md
```

Место назначения можно изменить с помощью переменной окружения `VIBE_HOME`:

```bash
VIBE_HOME=~/.config/vibe ./scripts/install.sh --tool vibe
```

## Формат сгенерированных файлов

Каждая пара файлов агента находится по путям:

```text
integrations/vibe/agents/<slug>.toml
integrations/vibe/prompts/<slug>.md
```

### Файл конфигурации TOML

Минимальная конфигурация агента:

```toml
agent_type = "agent"
system_prompt_id = "<slug>"
```

В файле агента можно указать `active_model`, либо использовать модель по умолчанию из конфигурации Vibe.

### Файл промпта Markdown

Файл промпта содержит:
- Заголовок с именем агента
- Описание агента
- Полное Markdown-тело исходного агента

## Использование

После установки на агенты можно ссылаться в Mistral Vibe по их `system_prompt_id` (совпадает со slug'ом файла).

Пример:
```text
Use the Code Reviewer agent to analyze this pull request.
```

## Фильтрация

Можно установить только определённые подразделения или отдельных агентов:

```bash
# Установить только агентов из подразделения 1
./scripts/install.sh --tool vibe --division 1

# Установить только агента code-reviewer
./scripts/install.sh --tool vibe --agent code-reviewer
```

## Повторная генерация

После изменения исходных агентов:

```bash
./scripts/convert.sh --tool vibe
./scripts/install.sh --tool vibe
```

## Устранение неполадок

### Mistral Vibe не обнаружен

Убедитесь, что `vibe` доступен в PATH или что каталог `~/.vibe/` уже существует:

```bash
which vibe
vibe --version
```

### Файлы интеграции не сгенерированы

Сначала сгенерируйте артефакты для Vibe, затем установите их:

```bash
./scripts/convert.sh --tool vibe
```
