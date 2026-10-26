# 🎭 The Agency: AI-специалисты, готовые преобразить ваш рабочий процесс

> **Полное ИИ-агентство у вас под рукой** — от мастеров фронтенда до ниндзя Reddit-сообществ, от генераторов креатива до проверяющих реальность. Каждый агент — узкопрофильный эксперт со своим характером, процессами и проверенными результатами.
>
> **Это форк.** Данный репозиторий — русскоязычная версия проекта [agency-agents](https://github.com/msitarzewski/agency-agents) (форк `ALNIuser/agency-agents`), предназначенная для русскоязычных пользователей. Идентификаторы агентов, имена файлов, интеграции и функциональность исходного проекта сохранены.

---

> **Полное ИИ-агентство у вас под рукой** — от мастеров фронтенда до ниндзя Reddit-сообществ, от генераторов креатива до проверяющих реальность. Каждый агент — узкопрофильный эксперт со своим характером, процессами и проверенными результатами.

[![GitHub stars](https://img.shields.io/github/stars/msitarzewski/agency-agents?style=social)](https://github.com/msitarzewski/agency-agents)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github)](https://github.com/sponsors/msitarzewski)
[![Download the app](https://img.shields.io/github/v/release/msitarzewski/agency-agents-app?label=Download%20app&color=2563eb)](https://github.com/msitarzewski/agency-agents-app/releases/latest)

> ### 🆕 Теперь есть приложение
>
> **[Agency Agents](https://agencyagents.app)** — нативное приложение для **macOS, Linux и Windows**, которое просматривает весь реестр агентов и устанавливает его в Claude Code, Cursor, Codex, Gemini, Osaurus и другие инструменты — в один клик. Без клонирования, без скриптов, с автоматическим обновлением.
>
> **→ [Скачать последнюю версию](https://github.com/msitarzewski/agency-agents-app/releases/latest) · [agencyagents.app](https://agencyagents.app)**

---

## 🚀 Что это?

Рождённое из ветки на Reddit и месяцев итераций, **The Agency** — это растущая коллекция тщательно проработанных личностей ИИ-агентов. Каждый агент:

- **🎯 Узкоспециализированный**: глубокая экспертиза в своей области (а не универсальные шаблоны промптов)
- **🧠 С характером**: уникальный голос, стиль общения и подход
- **📋 Нацеленный на результат**: реальный код, процессы и измеримые итоги
- **✅ Готовый к продакшену**: проверенные в бою рабочие процессы и метрики успеха

**Представьте это так**: вы собираете команду мечты, только это ИИ-специалисты, которые никогда не спят, никогда не жалуются и всегда доводят дело до конца.

---

## ⚡ Быстрый старт

### Вариант 1: Установить приложение (рекомендуется)

Самый быстрый способ начать — без клонирования и без терминала. [**Agency Agents**](https://agencyagents.app) — нативное десктопное приложение (macOS · Linux · Windows), которое просматривает весь реестр и устанавливает агентов в Claude Code, Cursor, Codex, Gemini CLI, OpenCode, Qwen и Osaurus за вас, а затем поддерживает их в актуальном состоянии.

**[⬇ Скачать последнюю версию](https://github.com/msitarzewski/agency-agents-app/releases/latest)** — или на Mac:

```bash
brew install --cask msitarzewski/agency-agents/agency-agents
```

Предпочитаете командную строку? Варианты на основе скриптов ниже устанавливают тех же агентов.

### Вариант 2: Использовать с Claude Code

```bash
# Установить всех агентов в каталог Claude Code
./scripts/install.sh --tool claude-code

# Или скопировать категорию вручную, если нужен только один подраздел
cp engineering/*.md ~/.claude/agents/

# Затем активируйте любого агента в сессиях Claude Code:
# "Hey Claude, activate Frontend Developer mode and help me build a React component"
```

### Вариант 3: Использовать как справочник

Каждый файл агента содержит:
- Идентичность и черты характера
- Основную миссию и рабочие процессы
- Технические результаты с примерами кода
- Метрики успеха и стиль общения

Просмотрите агентов ниже и скопируйте/адаптируйте нужных!

### Вариант 4: Использовать с другими инструментами (GitHub Copilot, Antigravity, Gemini CLI, OpenCode, OpenClaw, Cursor, Aider, Windsurf, Kimi Code, Codex, Osaurus, Hermes, Mistral Vibe, DeepSeek Harness)

```bash
# Шаг 1 — сгенерировать файлы интеграции для всех поддерживаемых инструментов
./scripts/convert.sh

# Шаг 2 — установить интерактивно (автоматически определяет, что у вас установлено)
./scripts/install.sh

# Или нацелиться на конкретный инструмент напрямую
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool gemini-cli
./scripts/install.sh --tool opencode
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool cursor
./scripts/install.sh --tool aider
./scripts/install.sh --tool windsurf
./scripts/install.sh --tool kimi
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes
./scripts/install.sh --tool vibe
./scripts/install.sh --tool dsh
```

**Установите только нужные команды** (не всем нужен каждый подраздел):

```bash
./scripts/install.sh                                    # интерактивный мастер: выберите инструменты + команды
./scripts/install.sh --tool claude-code --division engineering,security
./scripts/install.sh --tool cursor --agent frontend-developer,ui-designer
./scripts/install.sh --list teams                       # увидеть каждую команду + количество агентов
./scripts/install.sh --tool opencode --division engineering --dry-run
```

`--agent` и `--agents-file` принимают slug агента (как его выводит `--list agents`), его отображаемое имя или имя файла без `.md` — тот же id, который используют [реестры runbook](strategy/runbooks.json) — поэтому команда runbook устанавливается в точности как перечислена:

```bash
python3 -c 'import json, sys
for r in json.load(open("strategy/runbooks.json"))["runbooks"]:
    if r["slug"] == sys.argv[1]: [print(a) for g in r["roster"] for a in g["agents"]]' startup-mvp > team.txt
./scripts/install.sh --tool claude-code --agents-file team.txt
```

> **Примечание для OpenCode:** среда выполнения OpenCode в настоящее время регистрирует только ~119 агентов и молча отбрасывает остальные ([ошибка в upstream](https://github.com/anomalyco/opencode/issues/27988)). Установка подмножества с помощью `--division` удерживает вас ниже этого лимита. Установщик предупреждает, когда выбор превышает лимит.

Подробности см. в разделе [Интеграции с несколькими инструментами](#-multi-tool-integrations) ниже.

---

## 🎨 Реестр The Agency

### 💻 Подразделение Engineering

Строим будущее — по одному коммиту за раз.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎨 [Frontend Developer](engineering/engineering-frontend-developer.md) | React/Vue/Angular, реализация UI, производительность | Современные веб-приложения, пиксельно-точные интерфейсы, оптимизация Core Web Vitals |
| 🏗️ [Backend Architect](engineering/engineering-backend-architect.md) | Проектирование API, архитектура баз данных, масштабируемость | Серверные системы, микросервисы, облачная инфраструктура |
| 📱 [Mobile App Builder](engineering/engineering-mobile-app-builder.md) | iOS/Android, React Native, Flutter | Нативные и кроссплатформенные мобильные приложения |
| 🤖 [AI Engineer](engineering/engineering-ai-engineer.md) | ML-модели, развёртывание, интеграция ИИ | Возможности машинного обучения, пайплайны данных, приложения на основе ИИ |
| 🚀 [DevOps Automator](engineering/engineering-devops-automator.md) | CI/CD, автоматизация инфраструктуры, облачные операции | Разработка пайплайнов, автоматизация развёртывания, мониторинг |
| 🌐 [Network Engineer](engineering/engineering-network-engineer.md) | Cisco IOS/IOS-XE, Juniper Junos, Palo Alto PAN-OS | Настройка маршрутизаторов/коммутаторов/межсетевых экранов, BGP/OSPF, ACL, диагностика по выводу show |
| ⚡ [Rapid Prototyper](engineering/engineering-rapid-prototyper.md) | Быстрая разработка POC, MVP | Быстрые проверки концепции, хакатон-проекты, быстрая итерация |
| 💎 [Senior Developer](engineering/engineering-senior-developer.md) | Laravel/Livewire, продвинутые паттерны | Сложные реализации, архитектурные решения |
| 🔧 [Filament Optimization Specialist](engineering/engineering-filament-optimization-specialist.md) | UX админки Filament PHP, структурный редизайн форм, оптимизация ресурсов | Реструктуризация ресурсов/форм/таблиц Filament для более быстрых и чистых админ-процессов |
| ⚡ [Autonomous Optimization Architect](engineering/engineering-autonomous-optimization-architect.md) | Маршрутизация LLM, оптимизация затрат, теневое тестирование | Автономные системы, которым нужен интеллектуальный выбор API и защитные ограничения по затратам |
| 🔩 [Embedded Firmware Engineer](engineering/engineering-embedded-firmware-engineer.md) | Bare-metal, RTOS, прошивки ESP32/STM32/Nordic | Встраиваемые системы промышленного уровня и IoT-устройства |
| 🚨 [Incident Response Commander](engineering/engineering-incident-response-commander.md) | Управление инцидентами, пост-мортемы, дежурства | Управление прод-инцидентами и повышение готовности к инцидентам |
| ⛓️ [Solidity Smart Contract Engineer](engineering/engineering-solidity-smart-contract-engineer.md) | EVM-контракты, оптимизация газа, DeFi | Безопасные смарт-контракты с оптимизацией газа и протоколы DeFi |
| 🧭 [Codebase Onboarding Engineer](engineering/engineering-codebase-onboarding-engineer.md) | Быстрое онбординг разработчиков, исследование кодовой базы только для чтения, фактологическое объяснение | Помощь новым разработчикам быстро понять незнакомые репозитории: чтение кода, трассировка путей и изложение фактов о структуре и поведении |
| 📚 [Technical Writer](engineering/engineering-technical-writer.md) | Документация для разработчиков, справочники API, туториалы | Чёткая и точная техническая документация |
| 💬 [WeChat Mini Program Developer](engineering/engineering-wechat-mini-program-developer.md) | Экосистема WeChat, мини-программы, интеграция платежей | Создание производительных приложений для экосистемы WeChat |
| 👁️ [Code Reviewer](engineering/engineering-code-reviewer.md) | Конструктивное код-ревью, безопасность, сопровождаемость | Ревью PR, гейты качества кода, наставничество через ревью |
| 🗄️ [Database Optimizer](engineering/engineering-database-optimizer.md) | Проектирование схем, оптимизация запросов, стратегии индексирования | Тюнинг PostgreSQL/MySQL, отладка медленных запросов, планирование миграций |
| 🌿 [Git Workflow Master](engineering/engineering-git-workflow-master.md) | Стратегии ветвления, conventional commits, продвинутый Git | Проектирование Git-процессов, очистка истории, управление ветками, дружественное к CI |
| 🏛️ [Software Architect](engineering/engineering-software-architect.md) | Проектирование систем, DDD, архитектурные паттерны, анализ компромиссов | Архитектурные решения, моделирование домена, стратегия эволюции системы |
| 🛡️ [SRE](engineering/engineering-sre.md) | SLO, бюджеты ошибок, наблюдаемость, хаос-инжиниринг | Надёжность продакшена, снижение рутины, планирование мощностей |
| 🧬 [AI Data Remediation Engineer](engineering/engineering-ai-data-remediation-engineer.md) | Самовосстанавливающиеся пайплайны, изолированные SLM, семантическая кластеризация | Исправление повреждённых данных в масштабе с нулевой потерей данных |
| 🔧 [Data Engineer](engineering/engineering-data-engineer.md) | Пайплайны данных, архитектура lakehouse, ETL/ELT | Построение надёжной инфраструктуры данных и хранилищ |
| 🔗 [Feishu Integration Developer](engineering/engineering-feishu-integration-developer.md) | Открытая платформа Feishu/Lark, боты, рабочие процессы | Создание интеграций для экосистемы Feishu |
| 🧱 [CMS Developer](engineering/engineering-cms-developer.md) | Темы WordPress и Drupal, плагины/модули, архитектура контента | Реализация и кастомизация CMS по принципу code-first |
| 📧 [Email Intelligence Engineer](engineering/engineering-email-intelligence-engineer.md) | Парсинг писем, извлечение MIME, структурированные данные для ИИ-агентов | Превращение сырых цепочек писем в контекст, готовый к рассуждению |
| 🎙️ [Voice AI Integration Engineer](engineering/engineering-voice-ai-integration-engineer.md) | Пайплайны распознавания речи, Whisper, ASR, диаризация говорящих | Сквозные пайплайны транскрипции, предобработка аудио, структурированная выдача транскриптов |
| 🖧 [IT Service Manager](engineering/engineering-it-service-manager.md) | Управление сервисами по ITIL 4 | Управление инцидентами/проблемами/изменениями, SLA, CMDB |
| 🪡 [Minimal Change Engineer](engineering/engineering-minimal-change-engineer.md) | Минимально необходимые изменения | Исправление только того, что просили, без расширения объёма |
| 📜 [OrgScript Engineer](engineering/engineering-orgscript-engineer.md) | Грамматика OrgScript и валидация AST | Проектирование/парсинг определений бизнес-логики OrgScript |
| 🧬 [Prompt Engineer](engineering/engineering-prompt-engineer.md) | Проектирование и оптимизация промптов LLM | Превращение расплывчатых инструкций в надёжное поведение ИИ |
| 🕸️ [Multi-Agent Systems Architect](engineering/engineering-multi-agent-systems-architect.md) | Проектирование и управление мультиагентными пайплайнами | Топология, контекст, доверие, восстановление после сбоев для агентных систем |
| 🛒 [Drupal Shopping Cart Engineer](engineering/engineering-drupal-shopping-cart.md) | Магазины на Drupal Commerce | Каталог, платежи, оформление заказа, заказы на Drupal 10/11 |
| 🛍️ [WordPress Shopping Cart Engineer](engineering/engineering-wordpress-shopping-cart.md) | Магазины на WooCommerce | Каталог, платежи, оформление заказа, конверсия на WordPress |
| 💳 [Payments & Billing Engineer](engineering/engineering-payments-billing-engineer.md) | Интеграция PSP, идемпотентные платёжные потоки, биллинг подписок | Интеграции Stripe/Adyen/Braintree, обработка вебхуков, дуннинг, сверка |
| 🌍 [Internationalization Engineer](engineering/engineering-i18n-engineer.md) | ICU MessageFormat, раскладки RTL/bidi, форматирование CLDR, псевдолокализация | Подготовка приложений к переводу, форматирование с учётом локали, поддержка RTL, аудиты i18n |
| ⚡ [Drupal Performance Engineer](engineering/engineering-drupal-performance.md) | Производительность Drupal и Core Web Vitals | Кэширование, тюнинг БД/запросов, пайплайн рендеринга, профилирование Drupal под высокой нагрузкой |
| ⚡ [WordPress Performance Engineer](engineering/engineering-wordpress-performance.md) | Производительность WordPress и Core Web Vitals | Кэширование, оптимизация запросов/ассетов, тюнинг плагинов, профилирование WP под высокой нагрузкой |
| ♿ [Section 508 Accessibility Specialist](engineering/engineering-section-508-specialist.md) | Доступность по федеральному стандарту США 508 / WCAG | ARIA, тестирование со скринридерами, составление VPAT/ACR, устранение нарушений |
| 🏛️ [USWDS Developer](engineering/engineering-uswds-developer.md) | US Web Design System (федеральный) | Доступные UI-компоненты для госсектора и паттерны дизайн-систем |
| 🔎 [Search Relevance Engineer](engineering/engineering-search-relevance-engineer.md) | Ранжирование и релевантность поиска | Понимание запросов, эмбеддинги, ранжирование/оценка, настройка релевантности |
| 🔐 [Identity & Access Engineer](engineering/engineering-identity-access-engineer.md) | AuthN/AuthZ и IAM | OAuth/OIDC/SAML, SSO, RBAC/ABAC, безопасность токенов и сессий |
| 🤝 [Realtime Collaboration Engineer](engineering/engineering-realtime-collaboration-engineer.md) | Реалтайм-синхронизация и присутствие | CRDT/OT, разрешение конфликтов, живые курсоры, офлайн-синхронизация |
| 💻 [Desktop App Engineer](engineering/engineering-desktop-app-engineer.md) | Кроссплатформенные десктопные приложения | Electron/Tauri, нативная интеграция, упаковка, автообновление |
| 🚀 [Mobile Release Engineer](engineering/engineering-mobile-release-engineer.md) | Релизы мобильных приложений и CI/CD | Публикация в App Store/Play, подпись, поэтапный выкат, разбор крэшей |
| 🎬 [Video Streaming Engineer](engineering/engineering-video-streaming-engineer.md) | Видеостриминг и транскодирование | HLS/DASH, ABR, кодеки, доставка через CDN, стриминг с низкой задержкой |
| 💰 [FinOps Engineer](engineering/engineering-finops-engineer.md) | Инжиниринг затрат на облако | Распределение затрат, оптимизация размеров, юнит-экономика, контроль бюджета и аномалий |
| 🧩 [WebAssembly Engineer](engineering/engineering-webassembly-engineer.md) | WebAssembly и WASI | Rust/C++ → WASM, песочницы, привязки хоста, производительность |
| 🔌 [API Platform Engineer](engineering/engineering-api-platform-engineer.md) | API-шлюзы и платформы | Проектирование шлюзов, версионирование, ограничение частоты запросов, порталы разработчика |
| 🛟 [Database Reliability Engineer](engineering/engineering-database-reliability-engineer.md) | Надёжность баз данных (DBRE) | HA/репликация, автоматический failover, резервные копии PITR, операции без простоев |
| 🛠️ [Developer Tooling Engineer](engineering/engineering-developer-tooling-engineer.md) | CLI и инструменты разработчика | Инструменты командной строки, внутренний DX, процессы сборки/разработки |
| 📡 [IoT Fleet Engineer](engineering/engineering-iot-fleet-engineer.md) | Парки IoT и edge-устройств | Провижининг/идентификация устройств, телеметрия MQTT, OTA-обновления |
| 🔍 [RAG Pipeline Engineer](engineering/engineering-rag-pipeline-engineer.md) | Продакшен RAG-пайплайны | Чанкинг, качество извлечения, гибридный поиск, переранжирование, итерации на основе оценки |
| 🗄️ [GaussDB Expert Engineer](engineering/engineering-gaussdb-expert.md) | Huawei GaussDB OLTP | Производительность корпоративного OLTP, HA и миграция на GaussDB от Huawei |
| 🕵️ [Privacy Engineer](engineering/engineering-privacy-engineer.md) | Обнаружение PII, минимизация данных, контроль согласий, пайплайны DSAR/удаления | Реализация приватности в коде, право на забвение в сервисах, автоматизация хранения |
| 🦀 [Rust Refactoring Specialist](engineering/engineering-rust-refactoring-specialist.md) | Рефакторинг Rust с учётом поведения | Реформирование crate/trait/module на основе доказательств и с сохранением поведения |
| 🧪 [LLM Post-Training Engineer](engineering/engineering-llm-post-training-engineer.md) | Стек пост-обучения (SFT/DPO/GRPO/RLVR) | Гейтинг экспериментов на основе доказательств, целостность чекпоинтов, классификация сбоев |
| 📈 [Data Visualization Engineer](engineering/engineering-data-visualization-engineer.md) | Честная с точки зрения восприятия визуализация данных | Выбор типа диаграммы, палитры для дальтоников, производительный рендеринг D3/Vega |
| 🧠 [Knowledge Graph Engineer](engineering/engineering-knowledge-graph-engineer.md) | Графы знаний, извлечение связей между сущностями, RAG с графами | Структурирование документов в запрашиваемые графы Neo4j с помощью LangGraph; происхождение, отслеживание противоречий, извлечение подграфов |
| 🌏 [China Network Engineer](engineering/engineering-china-network-engineer.md) | Huawei VRP, H3C Comware, Ruijie RGOS, Hillstone StoneOS | Проектирование маршрутизации/коммутации/межсетевых экранов, NAT, границы, соответствующие MLPS 2.0, окна изменений с планами отката |
| 🛤️ [Platform Engineer](engineering/engineering-platform-engineer.md) | Внутренние платформы разработчика, золотые пути, IDP, инфраструктура самообслуживания | Скаффолдинг «мощёной дороги», измерение опыта разработчика, роадмапы «платформа как продукт» |
| 📑 [PDF Engine Architect](engineering/engineering-pdf-engine-architect.md) | Детерминированная компиляция HTML в PDF, тегированный PDF/UA и PDF/A | Пулы рендеринга Playwright, динамический размер страниц, вывод документов архивного качества |
| 🎯 [ATS Validator Architect](engineering/engineering-ats-validator-architect.md) | Парсируемость резюме, пайплайны приёма в ATS | Оценка релевантности BM25/TF-IDF, аудиты линеаризации разметки, соответствие EU AI Act и NYC LL144 |
| 📑 [Universal Document Compiler](engineering/engineering-universal-document-compiler.md) | Независимые от схемы AST документов, вывод раскладки по форме данных, постраничная публикация | Компиляция произвольных YAML-деревьев в предложения, техзадания и досье для руководства |
| 🛠️ [ServiceNow Developer & Mentor](engineering/engineering-servicenow-developer-mentor.md) | Business Rules, Script Includes, GlideAjax, ACL, Flow Designer | Разработка на ServiceNow и пошаговая диагностика инстансов |

### 🎨 Подразделение Design

Делаем это красиво, удобно и восхитительно.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎯 [UI Designer](design/design-ui-designer.md) | Визуальный дизайн, библиотеки компонентов, дизайн-системы | Создание интерфейсов, консистентность бренда, проектирование компонентов |
| 🔍 [UX Researcher](design/design-ux-researcher.md) | Юзер-тестирование, анализ поведения, исследования | Понимание пользователей, юзабилити-тестирование, дизайн-инсайты |
| 🏛️ [UX Architect](design/design-ux-architect.md) | Техническая архитектура, CSS-системы, реализация | Дружественные разработчику основы, руководство по реализации |
| 🎭 [Brand Guardian](design/design-brand-guardian.md) | Идентичность бренда, консистентность, позиционирование | Стратегия бренда, развитие идентичности, гайдлайны |
| 📖 [Visual Storyteller](design/design-visual-storyteller.md) | Визуальные нарративы, мультимедийный контент | Убедительные визуальные истории, сторителлинг бренда |
| ✨ [Whimsy Injector](design/design-whimsy-injector.md) | Индивидуальность, восторг, игровые взаимодействия | Добавление радости, микро-взаимодействия, пасхалки, характер бренда |
| 📷 [Image Prompt Engineer](design/design-image-prompt-engineer.md) | Промпты для генерации ИИ-изображений, фотография | Промпты для фотографии в Midjourney, DALL-E, Stable Diffusion |
| 🌈 [Inclusive Visuals Specialist](design/design-inclusive-visuals-specialist.md) | Репрезентация, смягчение предвзятости, аутентичные образы | Генерация культурно точных ИИ-изображений и видео |
| 🎭 [Persona Walkthrough Specialist](design/design-persona-walkthrough.md) | Когнитивные проходки на основе персон | Симуляция реакций и трений пользователя на каждой позиции прокрутки |
| 🧱 [UI Finish-Gate Reviewer](design/design-ui-finish-gate-reviewer.md) | Гейт финишного качества против «типового» UI | Отлов взаимозаменяемого UI перед релизом с помощью доказательств и письменного дизайн-контракта |

### 💰 Подразделение Paid Media

Превращаем рекламный бюджет в измеримые бизнес-результаты.

| Агент | Специализация | Когда использовать |
| --- | --- | --- |
| 💰 [PPC Campaign Strategist](paid-media/paid-media-ppc-strategist.md) | Реклама Google/Microsoft/Amazon, архитектура аккаунтов, ставки | Построение аккаунтов, распределение бюджета, масштабирование, диагностика эффективности |
| 🔍 [Search Query Analyst](paid-media/paid-media-search-query-analyst.md) | Анализ поисковых запросов, минус-слова, маппинг интента | Аудиты запросов, устранение слива бюджета, поиск ключевых слов |
| 📋 [Paid Media Auditor](paid-media/paid-media-auditor.md) | Аудиты аккаунтов по 200+ пунктам, конкурентный анализ | Перехват аккаунтов, ежеквартальные обзоры, конкурентные питчи |
| 📡 [Tracking & Measurement Specialist](paid-media/paid-media-tracking-specialist.md) | GTM, GA4, отслеживание конверсий, CAPI | Новые внедрения, аудиты отслеживания, миграции платформ |
| ✍️ [Ad Creative Strategist](paid-media/paid-media-creative-strategist.md) | Тексты RSA, креативы Meta, ассеты Performance Max | Запуски креативов, тестовые программы, обновление при усталости рекламы |
| 📺 [Programmatic & Display Buyer](paid-media/paid-media-programmatic-buyer.md) | GDN, DSP, партнёрские медиа, ABM-дисплей | Планирование дисплея, работа с партнёрами, ABM-программы |
| 📱 [Paid Social Strategist](paid-media/paid-media-paid-social-strategist.md) | Meta, LinkedIn, TikTok, кроссплатформенные соцсети | Соцреклама, выбор платформ, стратегия аудитории |

### 💼 Подразделение Sales

Превращаем пайплайн в выручку через мастерство, а не рутину в CRM.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎯 [Outbound Strategist](sales/sales-outbound-strategist.md) | Поиск на основе сигналов, многоканальные последовательности, таргетинг ICP | Построение пайплайна через аутрич на основе исследований, а не на объёме |
| 🔍 [Discovery Coach](sales/sales-discovery-coach.md) | SPIN, Gap Selling, Sandler — дизайн вопросов и структура звонков | Подготовка к discovery-звонкам, квалификация возможностей, коучинг продавцов |
| ♟️ [Deal Strategist](sales/sales-deal-strategist.md) | Квалификация MEDDPICC, конкурентное позиционирование, планирование победы | Оценка сделок, выявление рисков пайплайна, построение стратегий победы |
| 🛠️ [Sales Engineer](sales/sales-engineer.md) | Технические демо, определение объёма POC, конкурентные карточки | Технические победы на пресейле, подготовка демо, конкурентное позиционирование |
| 🏹 [Proposal Strategist](sales/sales-proposal-strategist.md) | Ответы на RFP, темы победы, структура нарратива | Написание предложений, которые убеждают, а не просто соответствуют |
| 📊 [Pipeline Analyst](sales/sales-pipeline-analyst.md) | Прогнозирование, здоровье пайплайна, скорость сделок, RevOps | Обзоры пайплайна, точность прогнозов, операции с выручкой |
| 🗺️ [Account Strategist](sales/sales-account-strategist.md) | Land-and-expand, QBR, маппинг стейкхолдеров | Расширение после продажи, планирование аккаунтов, рост NRR |
| 🏋️ [Sales Coach](sales/sales-coach.md) | Развитие продавцов, коучинг звонков, фасилитация обзоров пайплайна | Улучшение каждого продавца и каждой сделки через структурированный коучинг |
| 🎯 [Sales Outreach](specialized/sales-outreach.md) | Холодный поиск, многокасательные каденции, обработка возражений, предложения | B2B-аутрич верхней воронки — от холодного письма до назначенного discovery-звонка |
| 🧲 [Offer & Lead Gen Strategist](sales/sales-offer-lead-gen-strategist.md) | Офферы и лид-магниты | Построение офферов и генерация лидов верхней воронки |

### 📢 Подразделение Marketing

Растим вашу аудиторию — по одному искреннему взаимодействию за раз.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🚀 [Growth Hacker](marketing/marketing-growth-hacker.md) | Быстрое привлечение пользователей, вирусные петли, эксперименты | Взрывной рост, привлечение пользователей, оптимизация конверсии |
| 📝 [Content Creator](marketing/marketing-content-creator.md) | Мультиплатформенный контент, редакционные календари | Контент-стратегия, копирайтинг, сторителлинг бренда |
| 🐦 [Twitter Engager](marketing/marketing-twitter-engager.md) | Взаимодействие в реальном времени, лидерство мнений | Стратегия Twitter, кампании LinkedIn, профессиональные соцсети |
| 🛰️ [X/Twitter Intelligence Analyst](marketing/marketing-x-twitter-intelligence-analyst.md) | Социальный мониторинг, детекция трендов, мониторинг аккаунтов | Интеллект о рисках бренда, конкурентах и аудитории в X/Twitter |
| 📱 [TikTok Strategist](marketing/marketing-tiktok-strategist.md) | Вирусный контент, оптимизация под алгоритмы | Рост в TikTok, вирусный контент, аудитория Gen Z/миллениалы |
| 📸 [Instagram Curator](marketing/marketing-instagram-curator.md) | Визуальный сторителлинг, построение сообщества | Стратегия Instagram, развитие эстетики, визуальный контент |
| 🤝 [Reddit Community Builder](marketing/marketing-reddit-community-builder.md) | Искреннее вовлечение, ценный контент | Стратегия Reddit, доверие сообщества, аутентичный маркетинг |
| 🌱 [Developer Community Builder](marketing/marketing-developer-community-builder.md) | Архитектура Discord/форумов, программы контрибьюторов, здоровье сообщества | Построение сообществ разработчиков, которые участники реально ценят |
| 📱 [App Store Optimizer](marketing/marketing-app-store-optimizer.md) | ASO, оптимизация конверсии, заметность | Маркетинг приложений, оптимизация стора, рост приложения |
| 🌐 [Social Media Strategist](marketing/marketing-social-media-strategist.md) | Кроссплатформенная стратегия, кампании | Общая соцстратегия, мультиплатформенные кампании |
| 📕 [Xiaohongshu Specialist](marketing/marketing-xiaohongshu-specialist.md) | Лайфстайл-контент, стратегия на трендах | Рост в Xiaohongshu, эстетичный сторителлинг, аудитория Gen Z |
| 💬 [WeChat Official Account Manager](marketing/marketing-wechat-official-account.md) | Вовлечение подписчиков, контент-маркетинг | Стратегия WeChat OA, построение сообщества, оптимизация конверсии |
| 🧠 [Zhihu Strategist](marketing/marketing-zhihu-strategist.md) | Лидерство мнений, вовлечение на основе знаний | Построение авторитета в Zhihu, стратегия Q&A, генерация лидов |
| 🇨🇳 [Baidu SEO Specialist](marketing/marketing-baidu-seo-specialist.md) | Оптимизация под Baidu, SEO для Китая, соответствие ICP | Ранжирование в Baidu и выход на поисковый рынок Китая |
| 🎬 [Bilibili Content Strategist](marketing/marketing-bilibili-content-strategist.md) | Алгоритмы Bilibili, культура комментариев, рост авторского контента | Построение аудитории на Bilibili с помощью контента, ориентированного на сообщество |
| 🎠 [Carousel Growth Engine](marketing/marketing-carousel-growth-engine.md) | Карусели TikTok/Instagram, автономная публикация | Генерация и публикация вирусного карусельного контента |
| 💼 [LinkedIn Content Creator](marketing/marketing-linkedin-content-creator.md) | Персональный бренд, лидерство мнений, профессиональный контент | Рост в LinkedIn, построение профессиональной аудитории, B2B-контент |
| 🛒 [China E-Commerce Operator](marketing/marketing-china-ecommerce-operator.md) | Taobao, Tmall, Pinduoduo, лайв-коммерция | Ведение мультиплатформенной электронной коммерции в Китае |
| 🎥 [Kuaishou Strategist](marketing/marketing-kuaishou-strategist.md) | Kuaishou, сообщество, органический рост | Построение аутентичной аудитории в небольших городах и регионах |
| 🔍 [SEO Specialist](marketing/marketing-seo-specialist.md) | Техническое SEO, контент-стратегия, линкбилдинг | Устойчивый рост органического поиска |
| 📘 [Book Co-Author](marketing/marketing-book-co-author.md) | Книги по лидерству мнений, гострайтинг, публикация | Стратегическое соавторство книг для основателей и экспертов |
| 🌏 [Cross-Border E-Commerce Specialist](marketing/marketing-cross-border-ecommerce.md) | Amazon, Shopee, Lazada, трансграничная логистика | Стратегия трансграничной электронной коммерции полного цикла |
| 🎵 [Douyin Strategist](marketing/marketing-douyin-strategist.md) | Платформа Douyin, короткие видео, алгоритмы | Рост аудитории на ведущей китайской платформе коротких видео |
| 🎙️ [Livestream Commerce Coach](marketing/marketing-livestream-commerce-coach.md) | Обучение ведущих, оптимизация лайв-румов, конверсия | Построение высокоэффективных операций лайв-коммерции |
| 🎧 [Podcast Strategist](marketing/marketing-podcast-strategist.md) | Контент-стратегия подкастов, оптимизация платформ | Стратегия и операции на китайском рынке подкастов |
| 🔒 [Private Domain Operator](marketing/marketing-private-domain-operator.md) | WeCom, частный трафик, операции с сообществами | Построение частных доменов в корпоративном WeChat |
| 🎬 [Short-Video Editing Coach](marketing/marketing-short-video-editing-coach.md) | Постпродакшен, процессы монтажа, спецификации платформ | Практическое обучение монтажу коротких видео и оптимизация |
| 🔥 [Weibo Strategist](marketing/marketing-weibo-strategist.md) | Sina Weibo, трендовые темы, вовлечение фанатов | Полный спектр операций и рост в Weibo |
| 🎙️ [Global Podcast Strategist](marketing/marketing-global-podcast-strategist.md) | Позиционирование шоу, рост аудитории, монетизация | Запуск подкаста, алгоритмы платформ, спонсорство, построение сообщества |
| 🔮 [AI Citation Strategist](marketing/marketing-ai-citation-strategist.md) | AEO/GEO, видимость в ИИ-рекомендациях, аудит цитирований | Повышение видимости бренда в ChatGPT, Claude, Gemini, Perplexity |
| 🇨🇳 [China Market Localization Strategist](marketing/marketing-china-market-localization-strategist.md) | Полная локализация под рынок Китая, GTM в Douyin/Xiaohongshu/WeChat | Превращение трендовых сигналов в исполнимые стратегии выхода на рынок Китая |
| 🎬 [Video Optimization Specialist](marketing/marketing-video-optimization-specialist.md) | Стратегия под алгоритмы YouTube, чаптеры, концепции обложек | Рост канала YouTube, видео-SEO, оптимизация удержания аудитории |
| 🏗️ [AEO Foundations Architect](marketing/marketing-aeo-foundations.md) | Инфраструктура AI Engine Optimization | llms.txt, robots.txt с учётом ИИ, файлы обнаружения агентов |
| 🤖 [Agentic Search Optimizer](marketing/marketing-agentic-search-optimizer.md) | WebMCP и агентное выполнение задач | Делаем сайты пригодными для ИИ-агентов браузинга |
| 📧 [Email Marketing Strategist](marketing/marketing-email-strategist.md) | Жизненный цикл писем и доставляемость | CRM-кампании, автоматизация, сегментация |
| 📡 [Multi-Platform Publisher](marketing/marketing-multi-platform-publisher.md) | Публикация в один клик на китайских платформах | Маршрутизация одной статьи в Zhihu/Xiaohongshu/CSDN/Bilibili/WeChat Official Accounts/Juejin |
| 📣 [PR & Communications Manager](marketing/marketing-pr-communications-manager.md) | PR, отношения со СМИ и кризисные коммуникации | Пресс-релизы, лидерство мнений, репутация |

### 📊 Подразделение Product

Строим правильную вещь в правильное время.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎯 [Sprint Prioritizer](product/product-sprint-prioritizer.md) | Agile-планирование, приоритизация функций | Планирование спринтов, распределение ресурсов, управление бэклогом |
| 🔍 [Trend Researcher](product/product-trend-researcher.md) | Рыночный интеллект, конкурентный анализ | Исследование рынка, оценка возможностей, выявление трендов |
| 💬 [Feedback Synthesizer](product/product-feedback-synthesizer.md) | Анализ пользовательской обратной связи, извлечение инсайтов | Анализ фидбека, пользовательские инсайты, приоритеты продукта |
| 🔬 [DX Engineer](product/product-dx-engineer.md) | Трение онбординга, эргономика SDK, сообщения об ошибках | Сокращение времени разработчика до первого успеха |
| 🧠 [Behavioral Nudge Engine](product/product-behavioral-nudge-engine.md) | Поведенческая психология, дизайн подталкиваний, вовлечение | Максимизация мотивации пользователя через поведенческую науку |
| 🧭 [Product Manager](product/product-manager.md) | Полное владение жизненным циклом продукта | Дискавери, PRD, планирование роадмапа, GTM, измерение результата |

### 🎬 Подразделение Project Management

Поезда ходят по расписанию (и в рамках бюджета).

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎬 [Studio Producer](project-management/project-management-studio-producer.md) | Оркестрация высокого уровня, управление портфелем | Надзор за несколькими проектами, стратегическое выравнивание, распределение ресурсов |
| 🐑 [Project Shepherd](project-management/project-management-project-shepherd.md) | Кросс-функциональная координация, управление таймлайном | Сквозная координация проекта, управление стейкхолдерами |
| ⚙️ [Studio Operations](project-management/project-management-studio-operations.md) | Ежедневная эффективность, оптимизация процессов | Операционное совершенство, поддержка команды, продуктивность |
| 🧪 [Experiment Tracker](project-management/project-management-experiment-tracker.md) | A/B-тесты, валидация гипотез | Управление экспериментами, принятие решений на данных, тестирование |
| 👔 [Senior Project Manager](project-management/project-manager-senior.md) | Реалистичная оценка объёма, декомпозиция задач | Превращение спецификаций в задачи, управление объёмом работ |
| 📋 [Jira Workflow Steward](project-management/project-management-jira-workflow-steward.md) | Git-процессы, стратегия ветвления, трассируемость | Обеспечение дисциплины доставки через связку Jira-Git |
| 📋 [Meeting Notes Specialist](project-management/project-management-meeting-notes-specialist.md) | Структурированные протоколы встреч | Выделение решений, пунктов действий, открытых вопросов |

### 🧪 Подразделение Testing

Ломаем, чтобы пользователи не ломали.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 📸 [Evidence Collector](testing/testing-evidence-collector.md) | QA на основе скриншотов, визуальные доказательства | UI-тестирование, визуальная верификация, документирование багов |
| 🔍 [Reality Checker](testing/testing-reality-checker.md) | Сертификация на основе доказательств, гейты качества | Готовность к продакшену, одобрение качества, сертификация релиза |
| 📊 [Test Results Analyzer](testing/testing-test-results-analyzer.md) | Оценка тестов, анализ метрик | Анализ результатов тестов, инсайты по качеству, отчёты о покрытии |
| ⚡ [Performance Benchmarker](testing/testing-performance-benchmarker.md) | Нагрузочное тестирование, оптимизация | Тестирование скорости, нагрузочные тесты, настройка производительности |
| 🔌 [API Tester](testing/testing-api-tester.md) | Валидация API, интеграционное тестирование | API-тестирование, проверка эндпоинтов, интеграционное QA |
| 🛠️ [Tool Evaluator](testing/testing-tool-evaluator.md) | Оценка технологий, выбор инструментов | Оценка инструментов, рекомендации ПО, техрешения |
| 🔄 [Workflow Optimizer](testing/testing-workflow-optimizer.md) | Анализ процессов, улучшение рабочих процессов | Оптимизация процессов, повышение эффективности, поиск возможностей автоматизации |
| ♿ [Accessibility Auditor](testing/testing-accessibility-auditor.md) | Аудит WCAG, тестирование со вспомогательными технологиями | Соответствие доступности, тестирование со скринридерами, проверка инклюзивного дизайна |
| 🎭 [Test Automation Engineer](testing/testing-test-automation-engineer.md) | E2E на Playwright/Cypress, устранение нестабильности, параллелизация в CI | Наборы браузерных тестов, детерминированные пайплайны, отладка с трассировками |

### 🔒 Подразделение Security

Защита стека — от безопасной архитектуры до реагирования на инциденты.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🛡️ [Security Architect](security/security-architect.md) | Моделирование угроз, security-by-design, границы доверия | Модели безопасности систем, ревью архитектуры, многоуровневая защита |
| 🔐 [Application Security Engineer](security/security-appsec-engineer.md) | Безопасность в SDLC, SAST/DAST, код-ревью по безопасности | Защита процесса разработки, уязвимости на уровне кода |
| 🗡️ [Penetration Tester](security/security-penetration-tester.md) | Авторизованные пентесты, red team, эксплуатация | Поиск уязвимостей до атакующих |
| ☁️ [Cloud Security Architect](security/security-cloud-security-architect.md) | Zero Trust, облачная защита по принципу «глубокая оборона» | Защита облачной инфраструктуры и архитектур |
| 🚨 [Incident Responder](security/security-incident-responder.md) | DFIR, расследование взломов, сдерживание угроз | Активные инциденты, криминалистика, кризисное реагирование |
| 🔍 [Threat Intelligence Analyst](security/security-threat-intelligence-analyst.md) | Отслеживание атакующих, маппинг кампаний, ATT&CK | Понимание кто и как атакует |
| 🎯 [Threat Detection Engineer](security/security-threat-detection-engineer.md) | Правила SIEM, охота за угрозами, маппинг ATT&CK | Построение слоёв детектирования и охота за угрозами |
| 🛡️ [Senior SecOps Engineer](security/security-senior-secops.md) | Сканирование секретов, безопасные по умолчанию изменения | Защитный код-ревью на каждом изменении |
| 📋 [Compliance Auditor](security/security-compliance-auditor.md) | SOC 2, ISO 27001, HIPAA, PCI-DSS | Проведение организаций через сертификацию соответствия |
| 🛡️ [Blockchain Security Auditor](security/security-blockchain-security-auditor.md) | Аудит смарт-контрактов, анализ эксплойтов | Поиск уязвимостей в контрактах до деплоя |
| 🔎 [AI-Generated Code Security Auditor](security/security-ai-generated-code-auditor.md) | Аудит кода, сгенерированного ИИ/вайбом | Захардкоженные секреты, сломанный RLS, уязвимости prompt-injection |
| 🔑 [Secrets & Credential Hygiene Engineer](security/security-secrets-credential-engineer.md) | Жизненный цикл секретов и учёток | Обнаружение, хранение в vault, ротация, реагирование на утечки |

### 🛟 Подразделение Support

Основа всей работы.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 💬 [Support Responder](support/support-support-responder.md) | Клиентский сервис, решение проблем | Поддержка клиентов, пользовательский опыт, операционная поддержка |
| 📊 [Analytics Reporter](support/support-analytics-reporter.md) | Анализ данных, дашборды, инсайты | Бизнес-аналитика, KPI, визуализация данных |
| 💰 [Finance Tracker](support/support-finance-tracker.md) | Финпланирование, управление бюджетом | Финанализ, денежный поток, бизнес-показатели |
| 🏗️ [Infrastructure Maintainer](support/support-infrastructure-maintainer.md) | Надёжность систем, оптимизация производительности | Управление инфраструктурой, системные операции, мониторинг |
| ⚖️ [Legal Compliance Checker](support/support-legal-compliance-checker.md) | Комплаенс, регулирование, правовой анализ | Юридическое соответствие, нормативные требования, управление рисками |
| 📑 [Executive Summary Generator](support/support-executive-summary-generator.md) | Коммуникация с C-level, стратегические сводки | Отчёты для руководства, стратегическая коммуникация, поддержка принятия решений |

### 🥽 Подразделение Spatial Computing

Строим будущее погружения.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🏗️ [XR Interface Architect](spatial-computing/xr-interface-architect.md) | Проектирование пространственного взаимодействия, иммерсивный UX | Дизайн интерфейсов AR/VR/XR, UX пространственных вычислений |
| 💻 [macOS Spatial/Metal Engineer](spatial-computing/macos-spatial-metal-engineer.md) | Swift, Metal, высокопроизводительная 3D-графика | Пространственные вычисления macOS, нативные приложения Vision Pro |
| 🌐 [XR Immersive Developer](spatial-computing/xr-immersive-developer.md) | WebXR, браузерные AR/VR | Браузерные иммерсивные опыты, WebXR-приложения |
| 🎮 [XR Cockpit Interaction Specialist](spatial-computing/xr-cockpit-interaction-specialist.md) | Кокпит-управление, иммерсивные системы | Системы управления кокпитом, иммерсивные интерфейсы управления |
| 🍎 [visionOS Spatial Engineer](spatial-computing/visionos-spatial-engineer.md) | Разработка под Apple Vision Pro | Приложения для Vision Pro, опыты пространственных вычислений |
| 🔌 [Terminal Integration Specialist](spatial-computing/terminal-integration-specialist.md) | Интеграция терминала, CLI-инструменты | CLI-инструменты, терминальные рабочие процессы, инструменты разработчика |

### 🎯 Подразделение Specialized

Уникальные специалисты, которые не вписываются в остальные категории.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎭 [Agents Orchestrator](specialized/agents-orchestrator.md) | Координация мультиагентных систем, управление рабочими процессами | Сложные проекты, требующие координации множества агентов |
| 🔍 [LSP/Index Engineer](specialized/lsp-index-engineer.md) | Language Server Protocol, кодовый интеллект | Системы кодового интеллекта, реализация LSP, семантическая индексация |
| 📥 [Sales Data Extraction Agent](specialized/sales-data-extraction-agent.md) | Мониторинг Excel, извлечение продажных метрик | Сбор продажных данных, метрики MTD/YTD/год |
| 📈 [Data Consolidation Agent](specialized/data-consolidation-agent.md) | Агрегация продажных данных, отчёты для дашбордов | Сводки по территориям, производительность продавцов, снимки пайплайна |
| 📬 [Report Distribution Agent](specialized/report-distribution-agent.md) | Автоматизированная доставка отчётов | Доставка отчётов по территориям, плановые рассылки |
| 🔐 [Agentic Identity & Trust Architect](specialized/agentic-identity-trust.md) | Идентичность агентов, аутентификация, проверка доверия | Системы идентичности мультиагентов, авторизация, аудит-трейлы |
| 🔗 [Identity Graph Operator](specialized/identity-graph-operator.md) | Разрешение общей идентичности в мультиагентных системах | Дедупликация сущностей, предложения по слиянию, согласованность идентичности |
| 💸 [Accounts Payable Agent](specialized/accounts-payable-agent.md) | Обработка платежей, управление поставщиками, аудит | Автономные платежи в крипте, фиате, стейблкоинах |
| 🌍 [Cultural Intelligence Strategist](specialized/specialized-cultural-intelligence-strategist.md) | Глобальный UX, репрезентация, культурные барьеры | Адаптация ПО под разные культуры |
| 🗣️ [Developer Advocate](specialized/specialized-developer-advocate.md) | Построение сообщества, DX, контент для разработчиков | Связь между продуктом и сообществом разработчиков |
| 🔬 [Model QA Specialist](specialized/specialized-model-qa.md) | Аудит ML, анализ признаков, интерпретируемость | End-to-end QA машинного обучения |
| 🗃️ [ZK Steward](specialized/zk-steward.md) | Управление знаниями, Zettelkasten, заметки | Построение связных и проверенных баз знаний |
| 🔌 [MCP Builder](specialized/specialized-mcp-builder.md) | MCP-серверы, инструментарий ИИ-агентов | Создание MCP-серверов для расширения возможностей агентов |
| 📄 [Document Generator](specialized/specialized-document-generator.md) | Генерация PDF, PPTX, DOCX, XLSX из кода | Профессиональные документы, отчёты, визуализация данных |
| ⚙️ [Automation Governance Architect](specialized/automation-governance-architect.md) | Управление автоматизацией, n8n, аудит рабочих процессов | Оценка и управление бизнес-автоматизацией в масштабе |
| 📚 [Corporate Training Designer](specialized/corporate-training-designer.md) | Корпоративное обучение, разработка программ | Проектирование обучающих систем и программ |
| 🌱 [Personal Growth Mentor](specialized/personal-growth-mentor.md) | Ясность целей, привычки, ответственность, жизненная стратегия | Личностное развитие без мотивационных клише |
| 🏛️ [Government Digital Presales Consultant](specialized/government-digital-presales-consultant.md) | Пресейл для госзаказа Китая, цифровая трансформация | Предложения и заявки на цифровизацию госструктур |
| ⚕️ [Healthcare Marketing Compliance](specialized/healthcare-marketing-compliance.md) | Соответствие рекламы медуслуг в Китае | Соблюдение нормативов в медицинском маркетинге |
| 🎯 [Recruitment Specialist](specialized/recruitment-specialist.md) | Подбор персонала, операционное управление наймом | Стратегия найма, поиск, процессы подбора |
| 🎓 [Study Abroad Advisor](specialized/study-abroad-advisor.md) | Международное образование, планирование поступления | Планирование обучения за рубежом в США, Великобритании, Канаде, Австралии |
| 🔗 [Supply Chain Strategist](specialized/supply-chain-strategist.md) | Управление цепочками поставок, стратегия закупок | Оптимизация цепочек поставок и закупочная стратегия |
| 🗺️ [Workflow Architect](specialized/specialized-workflow-architect.md) | Выявление, маппинг и спецификация рабочих процессов | Моделирование всех путей системы до написания кода |
| ☁️ [Salesforce Architect](specialized/specialized-salesforce-architect.md) | Мультиоблачный Salesforce, ограничения, интеграции | Архитектура Salesforce предприятия, стратегия org, пайплайны деплоя |
| 🇫🇷 [French Consulting Market Navigator](specialized/specialized-french-consulting-market.md) | Экосистема ESN/SI, portage salarial, ценообразование | Фриланс-консалтинг на французском IT-рынке |
| 🇰🇷 [Korean Business Navigator](specialized/specialized-korean-business-navigator.md) | Корейская бизнес-культура, процесс 품의, отношения | Навигация в корейских бизнес-отношениях для иностранцев |
| 🏗️ [Civil Engineer](specialized/specialized-civil-engineer.md) | Расчёт конструкций, геотехника, международные нормы | Мультистандартное проектирование (Eurocode, ACI, AISC и др.) |
| 🎧 [Customer Service](specialized/customer-service.md) | Омниканальная поддержка, работа с жалобами, удержание, эскалации | Поддержка клиентов в любой отрасли |
| 🏥 [Healthcare Customer Service](specialized/healthcare-customer-service.md) | HIPAA-совместимая поддержка пациентов, биллинг, страхование | Поддержка в здравоохранении с соблюдением регуляций |
| 🏨 [Hospitality Guest Services](specialized/hospitality-guest-services.md) | Бронирование, консьерж, работа с жалобами, лояльность | Отели, курорты, рестораны, мероприятия |
| 🤝 [HR Onboarding](specialized/hr-onboarding.md) | Пре-онбординг, комплаенс, льготы, планы 30-60-90 дней | Онбординг в компаниях любого размера |
| 🌐 [Language Translator](specialized/language-translator.md) | Перевод испанский↔английский, диалекты, культурный контекст | Перевод для туризма, бизнеса, медицины, юриспруденции |
| ⏱️ [Legal Billing & Time Tracking](specialized/legal-billing-time-tracking.md) | Учёт времени, биллинговые нарративы, IOLTA, взыскания | Оптимизация выручки юридических фирм |
| 📋 [Legal Client Intake](specialized/legal-client-intake.md) | Квалификация клиентов, проверка конфликтов, запись на консультацию | Превращение обращений в заключённые дела |
| ⚖️ [Legal Document Review](specialized/legal-document-review.md) | Ревью договоров, выявление рисков, сравнение версий | Предварительная правовая экспертиза |
| 🏦 [Loan Officer Assistant](specialized/loan-officer-assistant.md) | Приём заявок, соответствие TRID, пайплайн, координация закрытия | Ипотечное и потребительское кредитование |
| 🏠 [Real Estate Buyer & Seller](specialized/real-estate-buyer-seller.md) | Представительство покупателей/продавцов, офферы, сделки | Жилая и инвестиционная недвижимость |
| 🛒 [Retail Customer Returns](specialized/retail-customer-returns.md) | Возвраты, предотвращение мошенничества, обмены | Розница и e-commerce |
| ♟️ [Business Strategist](specialized/business-strategist.md) | Стратегический консалтинг | Конкурентный анализ, выход на рынок, рост |
| 🔄 [Change Management Consultant](specialized/change-management-consultant.md) | ADKAR/Kotter/Prosci | Управление изменениями и внедрением |
| 🧭 [Chief of Staff](specialized/specialized-chief-of-staff.md) | Координация у руководства | Фильтрация, процессы, маршрутизация решений |
| 🌟 [Customer Success Manager](specialized/customer-success-manager.md) | Онбординг, здоровье клиента, удержание | QBR, предотвращение оттока, продление, расширение |
| 📝 [Grant Writer](specialized/grant-writer.md) | Грантовые заявки и финансирование | LOI, заявки, бюджеты для НКО/исследований |
| 🏥 [Medical Billing & Coding Specialist](specialized/medical-billing-coding-specialist.md) | ICD-10/CPT/HCPCS, цикл доходов | Клаймы, работа с отказами, оптимизация RCM |
| 💰 [Pricing Analyst](specialized/specialized-pricing-analyst.md) | Ценообразование и маржинальность | Конкурентный/затратный анализ, ценностное ценообразование |
| 💼 [Chief Financial Officer](specialized/chief-financial-officer.md) | Капитал, финансовая стратегия | Казначейство, FP&A, M&A, отчётность инвесторам и совету |
| 🌱 [ESG & Sustainability Officer](specialized/esg-sustainability-officer.md) | ESG-программы и отчётность | Стратегия устойчивого развития, декарбонизация, отчётность |
| 🔐 [Data Privacy Officer](specialized/data-privacy-officer.md) | Соответствие GDPR/CCPA | Картирование данных, DPIA, согласия, реагирование на инциденты |
| ⚙️ [Operations Manager](specialized/operations-manager.md) | Lean/Six Sigma | Картирование процессов, планирование мощностей, KPI |
| 🤝 [M&A Integration Manager](specialized/ma-integration-manager.md) | Постслияние-интеграция | Планы Day 1/100 дней, синергии, TSA |
| 🧠 [Organizational Psychologist](specialized/organizational-psychologist.md) | Динамика команд и культура | Психологическая безопасность, выгорание, высокоэффективные команды |
| ⚔️ [Strategy Duel Agent](specialized/specialized-strategy-duel-agent.md) | Теория игр и 36 стратагем | Походовые стратегические дуэли, симуляция сценариев |
| 🛡️ [FedRAMP & RMF Compliance Engineer](specialized/specialized-fedramp-rmf-compliance.md) | Авторизация облака для госструктур (ATO) | NIST 800-53, FedRAMP Rev5/20x, SSP/POA&M, ConMon, OSCAL |
| 🏺 [Codebase Archaeologist](specialized/specialized-codebase-archaeologist.md) | Аудит дрейфа кодовой базы | Обнаружение тихого дрейфа между Claude/Cursor/Copilot/Windsurf |
| 🧾 [Resume Tailor](specialized/resume-tailor.md) | Оптимизация резюме со стороны кандидата | Сопоставление с JD, ATS-ключевые слова, соответствие требованиям |
| 🧡 [Aging Parent Care Companion](specialized/healthcare-aging-parent-care-companion.md) | Поддержка семьи по уходу за пожилыми родителями | Координация приёмов/лекарств, взаимодействие с командой ухода (с учётом HIPAA) |
| 🏛️ [Master Plan Architect](specialized/specialized-master-plan-architect.md) | Обучение архитектуре, редтим-проверка планов | Глубокое обучение архитектуре, критический анализ рисков, подробные Markdown-планы без выполнения кода |
| 🎧 [Focus Music Architect](specialized/specialized-focus-music-architect.md) | Промпт-инжиниринг музыки для фокуса, нейроакустика | Архитектура саундскейпов, кривые BPM, бинауральные слои для генеративного аудио |

### 💵 Подразделение Finance

Бухгалтерия, финансовый анализ, налоговая стратегия и инвестиционные исследования.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 📒 [Bookkeeper & Controller](finance/finance-bookkeeper-controller.md) | Месячное закрытие, сверка, соответствие GAAP, внутренний контроль | Ежедневный учёт, готовность к аудиту, ведение финансовых записей |
| 📊 [Financial Analyst](finance/finance-financial-analyst.md) | Финмоделирование, прогнозирование, сценарный анализ, поддержка решений | Трёхформатные модели, анализ отклонений, бизнес-аналитика на данных |
| 📈 [FP&A Analyst](finance/finance-fpa-analyst.md) | Бюджетирование, скользящие прогнозы, анализ отклонений, бизнес-обзоры | Годовой операционный план, ежемесячные бизнес-обзоры, стратегическое распределение ресурсов |
| 🔍 [Investment Researcher](finance/finance-investment-researcher.md) | Due diligence, анализ портфеля, оценка активов, акционерный анализ | Разработка инвестиционной идеи, оценка рисков, рыночные исследования |
| 🏛️ [Tax Strategist](finance/finance-tax-strategist.md) | Налоговая оптимизация, трансграничное соответствие, трансфертное ценообразование | Структурирование юрлиц, анализ эффективной ставки, защита при проверках, стратегическое налоговое планирование |

### 🎮 Подразделение разработки игр

Создаём миры, системы и игровые впечатления для всех основных игровых движков.

#### Агенты для разных игровых движков

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🎯 [Game Designer](game-development/game-designer.md) | Проектирование систем, Game Design Document (GDD), балансировка экономики, игровые циклы | Проектирование механик, систем прогрессии, написание дизайн-документов |
| 🗺️ [Level Designer](game-development/level-designer.md) | Планировка уровней, темп геймплея, проектирование игровых столкновений и боевых сценариев, нарратив через окружение | Создание уровней, проектирование игровых столкновений и боевых сценариев, развитие повествования через окружение |
| 🎨 [Technical Artist](game-development/technical-artist.md) | Шейдеры, VFX, LOD, оптимизация ассетов под игровой движок | Объединение художественной разработки и технической реализации: создание шейдеров, настройка пайплайна и оптимизация ассетов |
| 🔊 [Game Audio Engineer](game-development/game-audio-engineer.md) | FMOD/Wwise, адаптивная музыка, пространственный звук, бюджеты аудио | Проектирование интерактивных аудиосистем, динамической музыки, оптимизация звука |
| 📖 [Narrative Designer](game-development/narrative-designer.md) | Системы повествования, ветвящиеся диалоги, архитектура лора | Проектирование ветвящихся диалогов и сюжетных систем, разработка связного мира |
| 💰 [Economy Designer](game-development/economy-designer.md) | Виртуальные валюты, источники поступления и механизмы расходования ресурсов, монетизация, контроль инфляции | Проектирование и балансировка внутриигровой экономики, настройка F2P-монетизации, балансировка экономики игры после запуска |

#### Unity

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🏗️ [Unity Architect](game-development/unity/unity-architect.md) | ScriptableObjects, архитектура на основе данных, DOTS/ECS | Крупные проекты на Unity, проектирование систем на основе данных, оптимизация с помощью ECS |
| ✨ [Unity Shader Graph Artist](game-development/unity/unity-shader-graph-artist.md) | Shader Graph, HLSL, URP/HDRP, Renderer Features | Создание собственных материалов и шейдеров в Unity, шейдеры для VFX, постобработка |
| 🌐 [Unity Multiplayer Engineer](game-development/unity/unity-multiplayer-engineer.md) | Netcode for GameObjects, Unity Relay/Lobby, авторитетная серверная модель, предсказание на клиенте | Сетевые игры на Unity, клиентское предсказание, интеграция с Unity Gaming Services |
| 🛠️ [Unity Editor Tool Developer](game-development/unity/unity-editor-tool-developer.md) | EditorWindows, AssetPostprocessors, PropertyDrawers, валидация сборки | Инструменты для редактора Unity, автоматизация конвейера разработки, валидация контента |

#### Unreal Engine

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| ⚙️ [Unreal Systems Engineer](game-development/unreal-engine/unreal-systems-engineer.md) | C++/Blueprint, Gameplay Ability System (GAS), ограничения Nanite, управление памятью | Сложные игровые системы в Unreal Engine, GAS, разработка на C++ на уровне движка |
| 🎨 [Unreal Technical Artist](game-development/unreal-engine/unreal-technical-artist.md) | Material Editor, Niagara, PCG, Substrate | Материалы в Unreal Engine, VFX на Niagara, процедурная генерация контента |
| 🌐 [Unreal Multiplayer Architect](game-development/unreal-engine/unreal-multiplayer-architect.md) | Репликация акторов, GameMode/GameState, выделенный сервер | Сетевые игры в Unreal Engine, графы репликации, серверно-авторитетная архитектура |
| 🗺️ [Unreal World Builder](game-development/unreal-engine/unreal-world-builder.md) | World Partition, Landscape, HLOD, LWC | Большие открытые миры в Unreal Engine, системы стриминга, работа с ландшафтом |

#### Godot

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 📜 [Godot Gameplay Scripter](game-development/godot/godot-gameplay-scripter.md) | GDScript 2.0, сигналы, композиция, строгая типизация | Игровые системы в Godot, композиция сцен, производительный GDScript |
| 🌐 [Godot Multiplayer Engineer](game-development/godot/godot-multiplayer-engineer.md) | MultiplayerAPI, ENet/WebRTC, RPC, серверно-авторитетная модель | Сетевые игры в Godot, репликация сцен, серверно-авторитетная архитектура |
| ✨ [Godot Shader Developer](game-development/godot/godot-shader-developer.md) | Язык шейдеров Godot, VisualShader, RenderingDevice | Создание материалов в Godot, 2D/3D-эффекты, постобработка, compute-шейдеры |

#### Blender

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🧩 [Blender Addon Engineer](game-development/blender/blender-addon-engineer.md) | Blender Python (`bpy`), пользовательские операторы и панели, валидация ассетов, экспорт, автоматизация конвейера | Разработка аддонов для Blender, подготовка ассетов, экспорт, автоматизация конвейера разработки |

#### Roblox Studio

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| ⚙️ [Roblox Systems Scripter](game-development/roblox-studio/roblox-systems-scripter.md) | Luau, RemoteEvents/Functions, DataStore, серверно-авторитетная модульная архитектура | Безопасные игровые системы в Roblox Studio, клиент-серверное взаимодействие, сохранение данных |
| 🎯 [Roblox Experience Designer](game-development/roblox-studio/roblox-experience-designer.md) | Игровые циклы, монетизация, удержание D1/D7, онбординг | Проектирование игрового опыта в Roblox Studio, Game Passes, ежедневные награды, удержание игроков |
| 👗 [Roblox Avatar Creator](game-development/roblox-studio/roblox-avatar-creator.md) | UGC-пайплайн, риггинг аксессуаров, публикация в Creator Marketplace | Предметы UGC для Roblox, настройка HumanoidDescription, магазины аватаров |

### 📚 Подразделение Academic

Академическая строгость для мирового строительства, сторителлинга и нарративного дизайна.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🌍 [Anthropologist](academic/academic-anthropologist.md) | Культурные системы, родство, ритуалы, верования | Проектирование культурно связных обществ с внутренней логикой |
| 🌐 [Geographer](academic/academic-geographer.md) | Физическая/социальная география, климат, картография | Построение географически правдоподобных миров с реалистичным рельефом и поселениями |
| 📚 [Historian](academic/academic-historian.md) | Исторический анализ, периодизация, материальная культура | Валидация исторической достоверности, аутентичные детали эпохи |
| 📜 [Narratologist](academic/academic-narratologist.md) | Теория нарратива, структура истории, арки персонажей | Анализ и улучшение структуры сюжета с опорой на теорию |
| 🧠 [Psychologist](academic/academic-psychologist.md) | Теория личности, мотивация, когнитивные паттерны | Создание психологически достоверных персонажей на основе исследований |
| 📊 [Statistician](academic/academic-statistician.md) | Статистический вывод и дизайн экспериментов | Проверка гипотез, каузальный анализ, репрезентативные выборки |

### 🌍 Подразделение GIS

Картируем Землю, анализируем застроенную среду и извлекаем разведданные из геопространственных данных.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🧠 [Technical Consultant](gis/gis-technical-consultant.md) | GIS-стратегия, gap-анализ, дорожные карты, цифровая трансформация | Определение бизнес-требований, выбор геопространственного стека, планирование GIS-программ |
| 🔧 [Solution Engineer](gis/gis-solution-engineer.md) | Прототипы на Esri + FOSS4G, PoC, техническая реализуемость | Работающие демо, валидация подходов, пресейл-поддержка |
| 🖥️ [GIS Analyst](gis/gis-analyst.md) | Картосоставление, контроль качества, символика, вёрстка, пространственные запросы | Операции GIS, публикационно-готовые карты, поддержка целостности данных |
| 📦 [Spatial Data Engineer](gis/gis-spatial-data-engineer.md) | Геопространственный ETL, конвертация форматов, репроекция СК, автоматизация | Обработка разнородных данных, повторяемые пайплайны трансформации |
| ⚙️ [Geoprocessing Specialist](gis/gis-geoprocessing-specialist.md) | ArcPy, Python Toolbox (.pyt), Model Builder, батч-автоматизация | Автоматизация рутинных задач, кастомные инструменты геообработки |
| ✅ [GIS QA Engineer](gis/gis-qa-engineer.md) | Топология, метаданные, СК, оценка точности | Контроль качества перед публикацией, проверка соответствия, аудит целостности |
| 🤖 [GeoAI/ML Engineer](gis/gis-geoai-ml-engineer.md) | Выделение объектов, детекция, семантическая сегментация, классификация | Выделение зданий/дорог/транспорта, выявление изменений, экологический мониторинг |
| 🏗️ [BIM/GIS Specialist](gis/gis-bim-specialist.md) | Revit/IFC в GIS, indoor-картирование, цифровой двойник, эксплуатация | Умные кампусы, цифровые двойники аэропортов, навигация внутри, эксплуатация зданий |
| 🏔️ [3D & Scene Developer](gis/gis-3d-scene-developer.md) | Cesium, ArcGIS Scene Viewer, 3D Tiles, облака точек, визуализация рельефа | 3D-городские сцены, облёты, веб-просмотр облаков точек |
| 📊 [Spatial Data Scientist](gis/gis-spatial-data-scientist.md) | Пространственная статистика, кластеризация, регрессия, интерполяция | Выявление горячих точек, пространственное моделирование, предиктивная аналитика |
| 🛸 [Drone/Reality Mapping](gis/gis-drone-reality-mapping.md) | Фотограмметрия, ортомозаика, ЦММ/ЦМР, классификация облака точек | Обработка БПЛА, реалити-кепча, мониторинг стройки, экологические исследования |
| 🌐 [Web GIS Developer](gis/gis-web-gis-developer.md) | MapLibre GL JS, ArcGIS JS API, Leaflet, дашборды, REST API | Интерактивные карты, операционные дашборды, визуализация в реальном времени |
| 🎨 [Cartography Designer](gis/gis-cartography-designer.md) | Цвет, типографика, базовая карта, иерархия, печать и веб | Красивые и читаемые карты, палитры для дальтоников, профессиональная вёрстка |

### 🏥 Подразделение Healthcare

ИИ-агенты для регулируемой клинической и суверенной здравоохранительной среды.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🩺 [Clinical Evidence Agent](healthcare/healthcare-clinical-evidence-agent.md) | Стандарты доказательности, проверенные/непроверенные утверждения, границы диагностических полномочий | Обоснованные клинические утверждения без превышения диагностических полномочий |
| 🌍 [Sovereign Health Systems Agent](healthcare/healthcare-sovereign-health-systems-agent.md) | Госпрограммы здравоохранения, ОМП, развивающиеся рынки | Здравоохранительные проекты в контексте национальной инфраструктуры и суверенной политики |
| 🧭 [Healthcare Innovation Strategist](healthcare/healthcare-innovation-strategist.md) | Нарратив для здравоохранительных стартапов под инвесторов, регуляторов, госорганы | Трансляция клинико-финансовой сложности на язык, который привлекает капитал и доверие |

### 🔍 Подразделение Research

Поиск, оценка и синтез существующих доказательств, а не генерация первичных данных.

| Агент | Специализация | Когда использовать |
|-------|-----------|-------------|
| 🔍 [Research Synthesist](research/research-synthesist.md) | Обзор литературы, оценка источников, трассировка ссылок, синтез доказательств | Структурированный честный обзор того, что действительно поддерживает доказательная база |

---

## 🎯 Реальные примеры использования

### Сценарий 1: Создание MVP стартапа

**Ваша команда**:
1. 🎨 **Frontend Developer** — фронтенд на React
2. 🏗️ **Backend Architect** — проектирование API и БД
3. 🚀 **Growth Hacker** — привлечение пользователей
4. ⚡ **Rapid Prototyper** — быстрая итерация
5. 🔍 **Reality Checker** — проверка качества перед запуском

**Результат**: Быстрый запуск с экспертизой на каждом этапе.

### Сценарий 2: Запуск маркетинговой кампании

**Ваша команда**:
1. 📝 **Content Creator** — контент кампании
2. 🐦 **Twitter Engager** — стратегия и запуск в X/Twitter
3. 📸 **Instagram Curator** — визуальный контент и истории
4. 🤝 **Reddit Community Builder** — аутентичное вовлечение в сообществе
5. 📊 **Analytics Reporter** — отслеживание и оптимизация

**Результат**: Координированная мультиплатформенная кампания с учётом особенностей каждой площадки.

### Сценарий 3: Разработка корпоративной фичи

**Ваша команда**:
1. 👔 **Senior Project Manager** — планирование и декомпозиция
2. 💎 **Senior Developer** — сложная реализация
3. 🎨 **UI Designer** — дизайн-система и компоненты
4. 🧪 **Experiment Tracker** — планирование A/B-тестов
5. 📸 **Evidence Collector** — верификация качества
6. 🔍 **Reality Checker** — готовность к продакшену

**Результат**: Корпоративный релиз с качественными гейтами и документацией.

### Сценарий 4: Захват платёжного медиа-аккаунта

**Ваша команда**:
1. 📋 **Paid Media Auditor** — комплексная оценка аккаунта
2. 📡 **Tracking & Measurement Specialist** — проверка корректности трекинга конверсий
3. 💰 **PPC Campaign Strategist** — переработка структуры аккаунта
4. 🔍 **Search Query Analyst** — очистка пустых расходов
5. ✍️ **Ad Creative Strategist** — обновление креативов
6. 📊 **Analytics Reporter** (Support) — дашборд отчётности

**Результат**: Системный захват аккаунта с верифицированным трекингом, устранённым сливом, оптимизированной структурой и обновлёнными креативами за 30 дней.

### Сценарий 5: Полноценный продуктовый дискавери от агентства

**Ваша команда**: Все 8 подразделений работают параллельно над одной задачей.

См. [Nexus Spatial Discovery Exercise](examples/nexus-spatial-discovery.md) — полный пример с 8 агентами (Product Trend Researcher, Backend Architect, Brand Guardian, Growth Hacker, Support Responder, UX Researcher, Project Shepherd, XR Interface Architect), одновременно оценивающими продуктовую возможность и готовящими единый план.

**Результат**: Кросс-функциональный продуктовый план, созданный за одну сессию. [Больше примеров](examples/).

### Сценарий 6: Цифровой двойник умного кампуса

**Ваша команда**:
1. 🧠 **Technical Consultant** — стратегия цифрового двойника (BIM + GIS + IoT)
2. 🏗️ **BIM/GIS Specialist** — конвертация Revit-моделей в слои GIS
3. 🛸 **Drone/Reality Mapping** — ортомозаика и 3D-меш
4. 🌐 **Web GIS Developer** — дашборд на MapLibre с поиском по помещениям
5. 🏔️ **3D & Scene Developer** — иммерсивная 3D-сцена с облётом
6. 🤖 **GeoAI/ML Engineer** — выделение зданий и кроны деревьев
7. ✅ **GIS QA Engineer** — проверка точности и топологии

**Результат**: Цифровой двойник кампуса с интеграцией BIM, реалити-кепчером, 3D-визуализацией и веб-доступом.

---

## 🤝 Участие в проекте

Присоединяйтесь — будем рады помощи:

### Добавить нового агента

1. Сделайте форк репозитория
2. Создайте файл агента в соответствующем подразделении
3. Следуйте структуре шаблона агента:
   - Frontmatter с `name`, `description`, `color`
   - Раздел Identity & Memory
   - Основная миссия (Core Mission)
   - Критические правила (Critical Rules)
   - Технические результаты с примерами
   - Процесс работы
   - Метрики успеха
4. Отправьте Pull Request

### Улучшить существующих агентов

- Добавьте реальные примеры
- Улучшите примеры кода
- Актуализируйте метрики успеха
- Улучшите рабочие процессы

### Поделиться историей успеха

Если вы успешно использовали агентов — поделитесь историей в [Discussions](https://github.com/msitarzewski/agency-agents/discussions)!

## 📖 Философия дизайна агентов

Каждый агент создаётся с учётом:

1. **🎭 Сильный характер**: Не шаблон, а уникальный голос и стиль
2. **📋 Чёткие результаты**: Конкретные выходы, а не общие советы
3. **✅ Метрики успеха**: Измеримые критерии качества
4. **🔄 Проверенные процессы**: Пошаговые рабочие процессы
5. **💡 Память обучения**: Распознавание паттернов и постоянное улучшение

## 🎁 Что делает этот проект особенным?

**В отличие от универсальных промптов:**
- ❌ «Сделай вид, что ты разработчик»
- ✅ Глубокая специализация с характером и процессами

**В отличие от библиотек промптов:**
- ❌ Набор разрозненных промптов
- ✅ Целостные агентные системы с процессами и результатами

**В отличие от AI-инструментов:**
- ❌ Чёрный ящик без возможности настройки
- ✅ Прозрачные, форкаемые, адаптируемые личности агентов

## 🎨 Яркие особенности агентов

> «Я тестирую не просто так — по умолчанию нахожу 3–5 проблем и требую визуальных доказательств для всего»
>
> — **Evidence Collector** (Testing Division)

> «Вы не просто продвигаетесь в Reddit — вы становитесь ценным членом сообщества, который при этом представляет бренд»
>
> — **Reddit Community Builder** (Marketing Division)

> «Любой игривый элемент должен выполнять функциональную или эмоциональную задачу. Создавайте приятные детали, которые усиливают, а не отвлекают»
>
> — **Whimsy Injector** (Design Division)

## 📊 Статистика

- 🎭 **230+ специализированных агентов** во всех подразделениях
- 📝 **10 000+ строк** описаний, процессов и примеров кода
- ⏱️ **Месяцы итераций** на основе реального использования
- 🌟 **Проверены в боевых условиях**
- 💬 **50+ запросов** за первые 12 часов на Reddit

## 🔌 Интеграции с инструментами

Проект изначально работает с Claude Code, а также содержит скрипты конвертации и установки для использования тех же агентов в большинстве популярных агентных инструментов.

### Поддерживаемые инструменты

- **[Claude Code](https://claude.ai/code)** — нативные `.md`-агенты, конвертация не нужна → `~/.claude/agents/`
- **[GitHub Copilot](https://github.com/copilot)** — нативные `.md`-агенты → `~/.github/agents/` + `~/.copilot/agents/`
- **[Antigravity](https://github.com/google-gemini/antigravity)** — `SKILL.md` на каждого агента → `~/.gemini/config/skills/`
- **[Gemini CLI](https://github.com/google-gemini/gemini-cli)** — `.md`-файлы агентов → `~/.gemini/agents/`
- **[OpenCode](https://opencode.ai)** — `.md`-агенты → `.opencode/agents/`
- **[Cursor](https://cursor.sh)** — `.mdc`-правила → `.cursor/rules/`
- **[Aider](https://aider.chat)** — индекс `CONVENTIONS.md` → `./CONVENTIONS.md`
- **[Windsurf](https://codeium.com/windsurf)** — единый `.windsurfrules` → `./.windsurfrules`
- **[OpenClaw](https://github.com/openclaw/openclaw)** — `SOUL.md` + `AGENTS.md` + `IDENTITY.md` на каждого агента
- **[Qwen Code](https://github.com/QwenLM/qwen-code)** — `.md` SubAgent → `~/.qwen/agents/`
- **[Kimi Code](https://github.com/MoonshotAI/kimi-cli)** — YAML-спецификации → `~/.config/kimi/agents/`
- **[Codex](https://developers.openai.com/codex/overview)** — TOML-агенты → `~/.codex/agents/`
- **Osaurus** — `SKILL.md` навыки → `~/.osaurus/skills/`
- **[Hermes](integrations/hermes/README.md)** — ленивый роутер-плагин → `~/.hermes/plugins/`
- **[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)** — `SKILL.md` навыки → `~/.dsh/skills/` (пользователь) или `.dsh/skills/` (проект)

---

### ⚡ Quick Install

**Step 1 -- Generate integration files:**
```bash
./scripts/convert.sh
# Faster (parallel, output order may vary): ./scripts/convert.sh --parallel
```

**Step 2 -- Install (interactive, auto-detects your tools):**
```bash
./scripts/install.sh
# Faster (parallel, output order may vary): ./scripts/install.sh --no-interactive --parallel
```

The installer scans your system for installed tools, shows a checkbox UI, and lets you pick exactly what to install:

```
  +------------------------------------------------+
  |   The Agency -- Tool Installer                 |
  +------------------------------------------------+

  System scan: [*] = detected on this machine

  [x]  1)  [*]  Claude Code     (claude.ai/code)
  [x]  2)  [*]  Copilot         (~/.github + ~/.copilot)
  [x]  3)  [*]  Antigravity     (~/.gemini/antigravity)
  [ ]  4)  [ ]  Gemini CLI      (~/.gemini/agents)
  [ ]  5)  [ ]  OpenCode        (opencode.ai)
  [ ]  6)  [ ]  OpenClaw        (~/.openclaw/agency-agents)
  [x]  7)  [*]  Cursor          (.cursor/rules)
  [ ]  8)  [ ]  Aider           (CONVENTIONS.md)
  [ ]  9)  [ ]  Windsurf        (.windsurfrules)
  [ ] 10)  [ ]  Qwen Code       (~/.qwen/agents)
  [ ] 11)  [ ]  Kimi Code       (~/.config/kimi/agents)
  [ ] 12)  [ ]  Codex           (~/.codex/agents)
  [ ] 13)  [ ]  Osaurus         (~/.osaurus/skills)
  [ ] 14)  [ ]  Hermes          (~/.hermes/plugins)

  [1-14] toggle   [a] all   [n] none   [d] detected
  [Enter] install   [q] quit
```

**Or install a specific tool directly:**
```bash
./scripts/install.sh --tool cursor
./scripts/install.sh --tool opencode
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes
```

**Non-interactive (CI/scripts):**
```bash
./scripts/install.sh --no-interactive --tool all
```

**Faster runs (parallel)** — On multi-core machines, use `--parallel` so each tool is processed in parallel. Output order across tools is non-deterministic. Works with both interactive and non-interactive install: e.g. `./scripts/install.sh --interactive --parallel` (pick tools, then install in parallel) or `./scripts/install.sh --no-interactive --parallel`. Job count defaults to `nproc` (Linux), `sysctl -n hw.ncpu` (macOS), or 4; override with `--jobs N`.

```bash
./scripts/convert.sh --parallel                    # convert all tools in parallel
./scripts/convert.sh --parallel --jobs 8           # cap parallel jobs
./scripts/install.sh --no-interactive --parallel   # install all detected tools in parallel
./scripts/install.sh --interactive --parallel      # pick tools, then install in parallel
./scripts/install.sh --no-interactive --parallel --jobs 4
```

---

### Tool-Specific Instructions

<details>
<summary><strong>Claude Code</strong></summary>

Agents are copied directly from the repo into `~/.claude/agents/` -- no conversion needed.

```bash
./scripts/install.sh --tool claude-code
```

Then activate in Claude Code:
```
Use the Frontend Developer agent to review this component.
```

See [integrations/claude-code/README.md](integrations/claude-code/README.md) for details.
</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Agents are copied directly from the repo into `~/.github/agents/` and `~/.copilot/agents/` -- no conversion needed.

```bash
./scripts/install.sh --tool copilot
```

Then activate in GitHub Copilot:
```
Use the Frontend Developer agent to review this component.
```

See [integrations/github-copilot/README.md](integrations/github-copilot/README.md) for details.
</details>

<details>
<summary><strong>Antigravity (Gemini)</strong></summary>

Each agent becomes a skill in `~/.gemini/config/skills/agency-<slug>/`.

```bash
./scripts/install.sh --tool antigravity
```

Activate in Gemini with Antigravity:
```
@agency-frontend-developer review this React component
```

See [integrations/antigravity/README.md](integrations/antigravity/README.md) for details.
</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

Installs as Gemini CLI subagents.
On a fresh clone, generate the Gemini agent files before running the installer.

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

See [integrations/gemini-cli/README.md](integrations/gemini-cli/README.md) for details.
</details>

<details>
<summary><strong>OpenCode</strong></summary>

Agents are placed in `.opencode/agents/` in your project root (project-scoped).

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

Or install globally:
```bash
mkdir -p ~/.config/opencode/agents
cp integrations/opencode/agents/*.md ~/.config/opencode/agents/
```

Activate in OpenCode:
```
@backend-architect design this API.
```

See [integrations/opencode/README.md](integrations/opencode/README.md) for details.
</details>

<details>
<summary><strong>Cursor</strong></summary>

Each agent becomes a `.mdc` rule file in `.cursor/rules/` of your project.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

Rules are auto-applied when Cursor detects them in the project. Reference them explicitly:
```
Use the @security-engineer rules to review this code.
```

See [integrations/cursor/README.md](integrations/cursor/README.md) for details.
</details>

<details>
<summary><strong>Aider</strong></summary>

`CONVENTIONS.md` is the roster index — every agent's name, description, and the
path to its full instructions. Aider keeps a conventions file in context for the
whole session, and the full agent bodies together are about a million tokens, so the
file lists the agents rather than inlining them.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

Then reference agents in your Aider session:
```
Use the Frontend Developer agent to refactor this component.
```

When you want an agent's full instructions, read its file in:
```
/read-only /path/to/agency-agents/engineering/engineering-frontend-developer.md
```

See [integrations/aider/README.md](integrations/aider/README.md) for details.
</details>

<details>
<summary><strong>Windsurf</strong></summary>

All agents are compiled into `.windsurfrules` in your project root.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

Reference agents in Windsurf's Cascade:
```
Use the Reality Checker agent to verify this is production ready.
```

See [integrations/windsurf/README.md](integrations/windsurf/README.md) for details.
</details>

<details>
<summary><strong>OpenClaw</strong></summary>

Each agent becomes a workspace with `SOUL.md`, `AGENTS.md`, and `IDENTITY.md` in `~/.openclaw/agency-agents/`.

```bash
./scripts/convert.sh --tool openclaw
./scripts/install.sh --tool openclaw
```

If the `openclaw` CLI is available, the installer registers each workspace automatically.
Run `openclaw gateway restart` after installation so the new agents are activated.

See [integrations/openclaw/README.md](integrations/openclaw/README.md) for details.

</details>

<details>
<summary><strong>Qwen Code</strong></summary>

SubAgents are installed to `.qwen/agents/` in your project root (project-scoped).

> Requires Qwen Code 0.25.1 or later. Earlier releases can't launch agents whose code examples contain `${…}` placeholders ([#1081](https://github.com/msitarzewski/agency-agents/issues/1081)).

```bash
# Convert and install (run from your project root)
cd /your/project
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

**Usage in Qwen Code:**
- Reference by name: `Use the frontend-developer agent to review this component`
- Or let Qwen auto-delegate based on task context
- Manage via `/agents` command in interactive mode

> 📚 [Qwen SubAgents Docs](https://qwenlm.github.io/qwen-code-docs/en/users/features/sub-agents/)

</details>

<details>
<summary><strong>Kimi Code</strong></summary>

Agents are converted to Kimi Code CLI format (YAML + system prompt) and installed to `~/.config/kimi/agents/`.

```bash
# Convert and install
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

**Usage with Kimi Code:**
```bash
# Use an agent
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml

# In a project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "Review this React component"
```

See [integrations/kimi/README.md](integrations/kimi/README.md) for details.

</details>

<details>
<summary><strong>Codex</strong></summary>

Each agent is converted into a Codex custom agent TOML file and installed to `~/.codex/agents/`.

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

Then reference the custom agent by name in Codex:
```
Use the Frontend Developer agent to review this component.
```

See [integrations/codex/README.md](integrations/codex/README.md) for details.
</details>

<details>
<summary><strong>DeepSeek Harness</strong></summary>

Each agent becomes a DSH skill (`SKILL.md` with Agent-Skills frontmatter) in `${DSH_HOME:-$HOME/.dsh}/skills/agency-<slug>/`. Skills are discovered live — no restart needed.

```bash
./scripts/convert.sh --tool dsh
./scripts/install.sh --tool dsh
```

Custom user home:
```bash
DSH_HOME=~/.config/dsh ./scripts/install.sh --tool dsh
```

Project-scoped install (run from your project root):
```bash
DSH_SKILLS_DIR=.dsh/skills ./scripts/install.sh --tool dsh
```

Activate in DeepSeek Harness — user- and model-invocable by default:
```
/agency-frontend-developer review this React component
```

See [integrations/dsh/README.md](integrations/dsh/README.md) for details.
</details>

---

### Regenerating After Changes

When you add new agents or edit existing ones, regenerate all integration files:

```bash
./scripts/convert.sh                    # regenerate all (serial)
./scripts/convert.sh --parallel         # regenerate all in parallel (faster)
./scripts/convert.sh --tool codex       # regenerate just one tool
./scripts/convert.sh --tool cursor      # regenerate just one tool
```

---

## 🗺️ Дорожная карта

- [ ] Интерактивный селектор агентов
- [x] Примеры мультиагентных рабочих процессов — см. [examples/](examples/)
- [x] Скрипты интеграции с множеством инструментов
- [ ] Видео-уроки по проектированию агентов
- [ ] Маркетплейс агентов сообщества
- [ ] «Викторина для подбора агента» под задачу
- [ ] Серия «Агент недели»

## 🌐 Локализации сообщества

Переводы и адаптации поддерживаются сообществом. См. соответствующие репозитории.

| Язык | Поддерживает | Ссылка | Примечания |
|----------|-----------|------|-------|
| 🇨🇳 Упрощённый китайский (zh-CN) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) | 141 переведённый агент и 46 оригинальных агентов для китайского рынка |
| 🇨🇳 Упрощённый китайский (zh-CN) | [@dsclca12](https://github.com/dsclca12) | [agent-teams](https://github.com/dsclca12/agent-teams) | Независимый перевод с локализацией под Bilibili/WeChat/Xiaohongshu |
| 🇧🇷 Português brasileiro (pt-BR) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-pt-BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | 184 агента переведены |
| 🇷🇺 Русский (ru) | [@ALNIuser](https://github.com/ALNIuser) | [agency-agents](https://github.com/ALNIuser/agency-agents) | Русскоязычная версия (этот репозиторий) |
| 🇮🇩 Bahasa Indonesia (id) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-id](https://github.com/jnMetaCode/agency-agents-id) | 184 агента переведены |
| 🇸🇦 العربية (ar) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ar](https://github.com/jnMetaCode/agency-agents-ar) | 184 агента переведены |
| 🇰🇷 한국어 (ko) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ko](https://github.com/jnMetaCode/agency-agents-ko) | 184 агента переведены полностью |
| 🇯🇵 日本語 (ja-JP) | [@sscodeai](https://github.com/sscodeai) | [agency-agents-ja](https://github.com/sscodeai/agency-agents-ja) | 281 агент под Японию + 97 оригинальных + 27 workflow |
| 🇻🇳 Tiếng Việt (vi-VN) | [@rodonguyen](https://github.com/rodonguyen) | [agency-agents](https://github.com/rodonguyen/agency-agents) | Частичная локализация README/быстрого старта |

Хотите добавить перевод? Откройте issue — мы добавим ссылку.

## 📜 Лицензия

MIT License — свободно для коммерческого и личного использования. Указание авторства приветствуется, но не обязательно.

## 🙏 Благодарности

Всё началось с ветки на Reddit о специализации ИИ-агентов и превратилось в нечто большее — **230+ агентов во всех подразделениях** при поддержке сообщества по всему миру. Каждый агент появился благодаря тому, что кто-то потратил время, чтобы его написать, протестировать и поделиться.

Спасибо всем, кто делал PR, открывал issue, участвовал в Discussions или просто пробовал агентов и делился обратной связью. Именно вы делаете The Agency лучше.

## 💬 Сообщество

- **GitHub Discussions**: [Поделиться успехами](https://github.com/msitarzewski/agency-agents/discussions)
- **Issues**: [Сообщить о баге или предложить идею](https://github.com/msitarzewski/agency-agents/issues)
- **Reddit**: r/ClaudeAI
- **Twitter/X**: #TheAgency

## 🚀 Начать

1. **Просмотрите** агентов и найдите нужных
2. **Скопируйте** в `~/.claude/agents/` для интеграции с Claude Code
3. **Активируйте** агента в диалоге с Claude
4. **Настройте** под свои задачи
5. **Поделитесь** результатами и внесите вклад

<div align="center">

**🎭 The Agency: Ваша команда мечты из ИИ-агентов 🎭**

[⭐ Поставить звезду](https://github.com/msitarzewski/agency-agents) • [🍴 Форкнуть](https://github.com/msitarzewski/agency-agents/fork) • [🐛 Сообщить о проблеме](https://github.com/msitarzewski/agency-agents/issues) • [❤️ Спонсировать](https://github.com/sponsors/msitarzewski)

Сделано с ❤️ сообществом для сообщества

</div>
