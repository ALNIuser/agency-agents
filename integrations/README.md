# 🔌 Интеграции

В этом каталоге находятся интеграции The Agency и преобразованные форматы для
поддерживаемых инструментов работы с агентами.

## Поддерживаемые инструменты

- **[Claude Code](#claude-code)** — агенты `.md`, используются напрямую из репозитория
- **[GitHub Copilot](#github-copilot)** — агенты `.md`, используются напрямую из репозитория
- **[Antigravity](#antigravity)** — `SKILL.md` для каждого агента в `antigravity/`
- **[Gemini CLI](#gemini-cli)** — файлы агентов `.md` в `gemini-cli/agents/`
- **[OpenCode](#opencode)** — файлы агентов `.md` в `opencode/`
- **[OpenClaw](#openclaw)** — рабочие пространства `SOUL.md` + `AGENTS.md` + `IDENTITY.md`
- **[Cursor](#cursor)** — файлы правил `.mdc` в `cursor/`
- **[Aider](#aider)** — индексный файл `CONVENTIONS.md` в `aider/`
- **[Windsurf](#windsurf)** — файл `.windsurfrules` в `windsurf/`
- **[Kimi Code](#kimi-code)** — спецификации агентов в формате YAML в `kimi/`
- **[Qwen Code](#qwen-code)** — субагенты `.md` для проекта в `.qwen/agents/`
- **[Codex](#codex)** — пользовательские агенты `.toml` в `codex/`
- **[Mistral Vibe](vibe/README.md)** — агенты `.toml` и файлы промптов, генерируемые в `vibe/`
- **Osaurus** — навыки `SKILL.md`, генерируемые в `osaurus/`
- **[Hermes](hermes/README.md)** — плагин ленивого маршрутизатора, генерируемый в `hermes/`

## Быстрая установка

```bash
# Автоматическая установка для всех обнаруженных инструментов
./scripts/install.sh

# Установка для конкретного инструмента пользовательского уровня
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes

# Для Gemini CLI требуется сгенерировать файлы интеграции при первом клонировании
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli

# Для Qwen Code также требуется сгенерировать файлы SubAgent при первом клонировании
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

Если вы установили OpenClaw и шлюз уже запущен, перезапустите его после установки:

```bash
openclaw gateway restart
```

Для инструментов, работающих в рамках проекта (OpenCode, Cursor, Aider, Windsurf, Qwen Code), запускайте установщик из корня целевого проекта, как показано в разделах ниже.

## Повторная генерация файлов интеграции

Если вы добавили или изменили агентов, повторно сгенерируйте все файлы интеграции:

```bash
./scripts/convert.sh
```

---

## Claude Code

The Agency изначально разрабатывался для Claude Code. Агенты работают нативно без конвертации.

```bash
cp -r <категория>/*.md ~/.claude/agents/
# или установить всё сразу:
./scripts/install.sh --tool claude-code
```

Подробнее см. [claude-code/README.md](claude-code/README.md).

---

## GitHub Copilot

The Agency также работает нативно с GitHub Copilot. Агенты можно копировать напрямую в `~/.github/agents/` и `~/.copilot/agents/` без конвертации.

```bash
./scripts/install.sh --tool copilot
```

Подробнее см. [github-copilot/README.md](github-copilot/README.md).

---

## Antigravity

Навыки устанавливаются в `~/.gemini/config/skills/`. Каждый агент становится отдельным навыком с префиксом `agency-` во избежание конфликтов имен.

```bash
./scripts/install.sh --tool antigravity
```

Подробнее см. [antigravity/README.md](antigravity/README.md).

---

## Gemini CLI

Агенты упакованы в виде субагентов Gemini CLI. Субагенты устанавливаются в `~/.gemini/agents/`. Поскольку файлы агентов являются результатом генерации, перед установкой из свежего клона необходимо выполнить `./scripts/convert.sh --tool gemini-cli`.

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

Подробнее см. [gemini-cli/README.md](gemini-cli/README.md).

---

## OpenCode

Каждый агент становится файлом `.md` для проекта в `.opencode/agents/`.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool opencode
```

Подробнее см. [opencode/README.md](opencode/README.md).

---

## OpenClaw

Каждый агент становится рабочим пространством OpenClaw, содержащим `SOUL.md`, `AGENTS.md` и `IDENTITY.md`.

Перед установкой необходимо сгенерировать рабочие пространства OpenClaw:

```bash
./scripts/convert.sh --tool openclaw
```

Затем установить их:

```bash
./scripts/install.sh --tool openclaw
```

Подробнее см. [openclaw/README.md](openclaw/README.md).

---

## Cursor

Каждый агент становится файлом правил `.mdc`. Правила работают в рамках проекта — установщик нужно запускать из корня целевого проекта.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool cursor
```

Подробнее см. [cursor/README.md](cursor/README.md).

---

## Aider

`CONVENTIONS.md` — это индексный список агентов: имя, описание и путь к полным инструкциям каждого агента. Aider хранит файл conventions в контексте всей сессии, поэтому в нём перечислены агенты, а не вставлены миллионы токенов их инструкций.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool aider
```

Подробнее см. [aider/README.md](aider/README.md).

---

## Windsurf

Все агенты объединены в один файл `.windsurfrules` в корне проекта.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool windsurf
```

Подробнее см. [windsurf/README.md](windsurf/README.md).

---

## Kimi Code

Каждый агент конвертируется в спецификацию Kimi Code CLI (формат YAML с отдельными файлами системных промптов). Агенты устанавливаются в `~/.config/kimi/agents/`.

Поскольку файлы агентов Kimi генерируются из исходных Markdown-файлов, перед установкой из свежего клона необходимо выполнить `./scripts/convert.sh --tool kimi`.

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

### Использование

После установки можно использовать агента с флагом `--agent-file`:

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

Или в конкретном проекте:

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project
```

Подробнее см. [kimi/README.md](kimi/README.md).

---

## Qwen Code

Каждый агент становится файлом SubAgent `.md` для проекта в `.qwen/agents/`.

Из свежего клона сначала сгенерируйте файлы Qwen:

```bash
./scripts/convert.sh --tool qwen
```

Затем установите их из корня целевого проекта:

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool qwen
```

Подробнее см. [qwen/README.md](qwen/README.md).

---

## Codex

Каждый агент конвертируется в отдельный файл пользовательского агента Codex формата TOML и устанавливается в `~/.codex/agents/`.

Поскольку Codex использует сгенерированные TOML-файлы, а не исходные Markdown напрямую, перед установкой из свежего клона необходимо запустить конвертер:

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

Подробнее см. [codex/README.md](codex/README.md).
