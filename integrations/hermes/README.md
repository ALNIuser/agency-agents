# Плагин-маршрутизатор Agency Agents для Hermes

Сгенерирован командой `scripts/convert.sh --tool hermes`.

Эта интеграция устанавливает один плагин Hermes с именем `agency-agents-router`, вместо добавления сотен сгенерированных навыков в `skills.external_dirs`. При запуске Hermes видит небольшой фиксированный набор инструментов, а полный список агентов The Agency хранится на диске в `data/agents.json` и загружается по требованию.

Сгенерированное количество агентов: 282

## Инструменты, доступные Hermes

- `agency_agents_search` — поиск подходящих специалистов по запросу или подразделению.
- `agency_agents_inspect` — просмотр метаданных или полного описания специалиста.
- `agency_agents_load` — формирование промпта выбранного специалиста под текущую задачу.
- `agency_agents_delegate` — делегирование задачи через публичный жизненный цикл субагентов Hermes.

Каждый инструмент зарегистрирован со полной схемой function-tool Hermes, включая имя, описание и JSON-параметры. Доступные аргументы:

| Инструмент | Аргументы |
| --- | --- |
| `agency_agents_search` | `query` (обязательный), опционально `division`, `limit` |
| `agency_agents_inspect` | `agent` или `slug`, опционально `include_body` |
| `agency_agents_load` | `agent` или `slug`, опционально `task` |
| `agency_agents_delegate` | `agent` или `slug`, `task` (обязательный) |

Типичный сценарий: найти специалиста по задаче, получить `slug`, затем просмотреть, загрузить или делегировать ему задачу. Hermes может выполнить это по естественному языковому запросу — прямые вызовы инструментов не обязательны.

## Инструкция для использования специалистов в Hermes

Если проекту в Hermes нужны специалисты The Agency, явно попросите Hermes использовать плагин/маршрутизатор `agency-agents-router` и загружать только тех специалистов, которые необходимы на текущем этапе. Не просите Hermes установить или предзагрузить весь список агентов в виде навыков.

Рекомендуемая инструкция для проекта:

```text
Use the agency-agents-router plugin. Search the Agency roster for the right
specialists, then load or delegate only the specific agents needed for each
part of the project. For multi-discipline projects, use multiple selected
specialists across the project, but keep routing lazy: do not preload the
full Agency roster and do not add agency-agents to skills.external_dirs.
```

Пример:

```text
For this Data Swami build, use the agency-agents-router plugin to pick
relevant Agency specialists. Search first, then delegate to selected agents
such as frontend, backend, UX, QA, data engineering, and product strategy as
needed. Load/delegate each specialist on demand rather than loading all
Agency agents at startup.
```

## Установка

```bash
./scripts/convert.sh --tool hermes
./scripts/install.sh --tool hermes
```

Установщик копирует сгенерированный плагин в:

```text
${HERMES_HOME:-~/.hermes}/plugins/agency-agents-router
```

Затем он включает `agency-agents-router` в разделе `plugins.enabled` конфигурации Hermes. В `skills.external_dirs` записи не добавляются.

После установки перезапустите Hermes или начните новую сессию, чтобы плагин и схемы инструментов были загружены. Если Hermes отображает инструменты без описанных аргументов, повторно сгенерируйте и переустановите плагин из актуальной копии Agency Agents, затем перезапустите Hermes.
