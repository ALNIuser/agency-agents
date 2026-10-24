# 🎭 The Agency: AI-специалисты, готовые преобразить ваш рабочий процесс

> **Полное ИИ-агентство у вас под рукой** — от мастеров фронтенда до ниндзя Reddit-сообществ, от генераторов креатива до проверяющих реальность. Каждый агент — узкопрофильный эксперт со своим характером, процессами и проверенными результатами.
>
> **Это форк.** Данный репозиторий — русскоязычная версия проекта [agency-agents](https://github.com/msitarzewski/agency-agents) (форк `ALNIuser/agency-agents`), предназначенная для русскоязычных пользователей. Идентификаторы агентов, имена файлов, интеграции и функциональность исходного проекта сохранены.

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
| 🎬 [Bilibili Content Strategist](marketing/marketing-bilibili-content-strategist.md) | Алгоритмы B站, культура дамму, рост UP主 | Построение аудитории на Bilibili контентом, ориентированным на сообщество |
| 🎠 [Carousel Growth Engine](marketing/marketing-carousel-growth-engine.md) | Карусели TikTok/Instagram, автономная публикация | Генерация и публикация вирусного карусельного контента |
| 💼 [LinkedIn Content Creator](marketing/marketing-linkedin-content-creator.md) | Персональный бренд, лидерство мнений, профессиональный контент | Рост в LinkedIn, построение профессиональной аудитории, B2B-контент |
| 🛒 [China E-Commerce Operator](marketing/marketing-china-ecommerce-operator.md) | Taobao, Tmall, Pinduoduo, лайв-коммерция | Ведение мультиплатформенной электронной коммерции в Китае |
| 🎥 [Kuaishou Strategist](marketing/marketing-kuaishou-strategist.md) | Kuaishou, сообщество 老铁, grassroots-рост | Построение аутентичной аудитории в рынках нижнего уровня |
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
| 📡 [Multi-Platform Publisher](marketing/marketing-multi-platform-publisher.md) | Публикация в один клик на китайских платформах | Маршрутизация одной статьи в 知乎/小红书/CSDN/B站/公众号/掘金 |
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

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🎬 [Studio Producer](project-management/project-management-studio-producer.md) | High-level orchestration, portfolio management | Multi-project oversight, strategic alignment, resource allocation |
| 🐑 [Project Shepherd](project-management/project-management-project-shepherd.md) | Cross-functional coordination, timeline management | End-to-end project coordination, stakeholder management |
| ⚙️ [Studio Operations](project-management/project-management-studio-operations.md) | Day-to-day efficiency, process optimization | Operational excellence, team support, productivity |
| 🧪 [Experiment Tracker](project-management/project-management-experiment-tracker.md) | A/B tests, hypothesis validation | Experiment management, data-driven decisions, testing |
| 👔 [Senior Project Manager](project-management/project-manager-senior.md) | Realistic scoping, task conversion | Converting specs to tasks, scope management |
| 📋 [Jira Workflow Steward](project-management/project-management-jira-workflow-steward.md) | Git workflow, branch strategy, traceability | Enforcing Jira-linked Git discipline and delivery |
| 📋 [Meeting Notes Specialist](project-management/project-management-meeting-notes-specialist.md) | Structured meeting summaries | Extracting decisions, action items, open questions |

### 🧪 Testing Division

Breaking things so users don't have to.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 📸 [Evidence Collector](testing/testing-evidence-collector.md) | Screenshot-based QA, visual proof | UI testing, visual verification, bug documentation |
| 🔍 [Reality Checker](testing/testing-reality-checker.md) | Evidence-based certification, quality gates | Production readiness, quality approval, release certification |
| 📊 [Test Results Analyzer](testing/testing-test-results-analyzer.md) | Test evaluation, metrics analysis | Test output analysis, quality insights, coverage reporting |
| ⚡ [Performance Benchmarker](testing/testing-performance-benchmarker.md) | Performance testing, optimization | Speed testing, load testing, performance tuning |
| 🔌 [API Tester](testing/testing-api-tester.md) | API validation, integration testing | API testing, endpoint verification, integration QA |
| 🛠️ [Tool Evaluator](testing/testing-tool-evaluator.md) | Technology assessment, tool selection | Evaluating tools, software recommendations, tech decisions |
| 🔄 [Workflow Optimizer](testing/testing-workflow-optimizer.md) | Process analysis, workflow improvement | Process optimization, efficiency gains, automation opportunities |
| ♿ [Accessibility Auditor](testing/testing-accessibility-auditor.md) | WCAG auditing, assistive technology testing | Accessibility compliance, screen reader testing, inclusive design verification |
| 🎭 [Test Automation Engineer](testing/testing-test-automation-engineer.md) | Playwright/Cypress E2E, flake elimination, CI parallelization | Browser test suites, deterministic pipelines, trace-driven failure debugging |

### 🔒 Security Division

Defending the stack — from secure-by-design architecture to breach response.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🛡️ [Security Architect](security/security-architect.md) | Threat modeling, secure-by-design, trust boundaries | System security models, architecture reviews, defense-in-depth |
| 🔐 [Application Security Engineer](security/security-appsec-engineer.md) | SDLC security, SAST/DAST, secure code review | Securing the dev lifecycle, code-level vulnerabilities |
| 🗡️ [Penetration Tester](security/security-penetration-tester.md) | Authorized pentests, red team ops, exploitation | Finding exploitable weaknesses before attackers do |
| ☁️ [Cloud Security Architect](security/security-cloud-security-architect.md) | Zero trust, cloud-native defense-in-depth | Securing cloud infrastructure and architectures |
| 🚨 [Incident Responder](security/security-incident-responder.md) | DFIR, breach investigation, threat containment | Active breaches, forensics, crisis response |
| 🔍 [Threat Intelligence Analyst](security/security-threat-intelligence-analyst.md) | Adversary tracking, campaign mapping, ATT&CK | Understanding who's attacking and how |
| 🎯 [Threat Detection Engineer](security/security-threat-detection-engineer.md) | SIEM rules, threat hunting, ATT&CK mapping | Building detection layers and threat hunting |
| 🛡️ [Senior SecOps Engineer](security/security-senior-secops.md) | Secrets scanning, secure-by-default submissions | Defensive code-level security on every change |
| 📋 [Compliance Auditor](security/security-compliance-auditor.md) | SOC 2, ISO 27001, HIPAA, PCI-DSS | Guiding organizations through compliance certification |
| 🛡️ [Blockchain Security Auditor](security/security-blockchain-security-auditor.md) | Smart contract audits, exploit analysis | Finding vulnerabilities in contracts before deployment |
| 🔎 [AI-Generated Code Security Auditor](security/security-ai-generated-code-auditor.md) | Security review of AI/vibe-coded apps | Hardcoded secrets, broken RLS, prompt-injection sinks |
| 🔑 [Secrets & Credential Hygiene Engineer](security/security-secrets-credential-engineer.md) | Secrets & credential lifecycle | Detection, vaulting, rotation, leak response |

### 🛟 Support Division

The backbone of the operation.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 💬 [Support Responder](support/support-support-responder.md) | Customer service, issue resolution | Customer support, user experience, support operations |
| 📊 [Analytics Reporter](support/support-analytics-reporter.md) | Data analysis, dashboards, insights | Business intelligence, KPI tracking, data visualization |
| 💰 [Finance Tracker](support/support-finance-tracker.md) | Financial planning, budget management | Financial analysis, cash flow, business performance |
| 🏗️ [Infrastructure Maintainer](support/support-infrastructure-maintainer.md) | System reliability, performance optimization | Infrastructure management, system operations, monitoring |
| ⚖️ [Legal Compliance Checker](support/support-legal-compliance-checker.md) | Compliance, regulations, legal review | Legal compliance, regulatory requirements, risk management |
| 📑 [Executive Summary Generator](support/support-executive-summary-generator.md) | C-suite communication, strategic summaries | Executive reporting, strategic communication, decision support |

### 🥽 Spatial Computing Division

Building the immersive future.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🏗️ [XR Interface Architect](spatial-computing/xr-interface-architect.md) | Spatial interaction design, immersive UX | AR/VR/XR interface design, spatial computing UX |
| 💻 [macOS Spatial/Metal Engineer](spatial-computing/macos-spatial-metal-engineer.md) | Swift, Metal, high-performance 3D | macOS spatial computing, Vision Pro native apps |
| 🌐 [XR Immersive Developer](spatial-computing/xr-immersive-developer.md) | WebXR, browser-based AR/VR | Browser-based immersive experiences, WebXR apps |
| 🎮 [XR Cockpit Interaction Specialist](spatial-computing/xr-cockpit-interaction-specialist.md) | Cockpit-based controls, immersive systems | Cockpit control systems, immersive control interfaces |
| 🍎 [visionOS Spatial Engineer](spatial-computing/visionos-spatial-engineer.md) | Apple Vision Pro development | Vision Pro apps, spatial computing experiences |
| 🔌 [Terminal Integration Specialist](spatial-computing/terminal-integration-specialist.md) | Terminal integration, command-line tools | CLI tools, terminal workflows, developer tools |

### 🎯 Specialized Division

The unique specialists who don't fit in a box.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🎭 [Agents Orchestrator](specialized/agents-orchestrator.md) | Multi-agent coordination, workflow management | Complex projects requiring multiple agent coordination |
| 🔍 [LSP/Index Engineer](specialized/lsp-index-engineer.md) | Language Server Protocol, code intelligence | Code intelligence systems, LSP implementation, semantic indexing |
| 📥 [Sales Data Extraction Agent](specialized/sales-data-extraction-agent.md) | Excel monitoring, sales metric extraction | Sales data ingestion, MTD/YTD/Year End metrics |
| 📈 [Data Consolidation Agent](specialized/data-consolidation-agent.md) | Sales data aggregation, dashboard reports | Territory summaries, rep performance, pipeline snapshots |
| 📬 [Report Distribution Agent](specialized/report-distribution-agent.md) | Automated report delivery | Territory-based report distribution, scheduled sends |
| 🔐 [Agentic Identity & Trust Architect](specialized/agentic-identity-trust.md) | Agent identity, authentication, trust verification | Multi-agent identity systems, agent authorization, audit trails |
| 🔗 [Identity Graph Operator](specialized/identity-graph-operator.md) | Shared identity resolution for multi-agent systems | Entity deduplication, merge proposals, cross-agent identity consistency |
| 💸 [Accounts Payable Agent](specialized/accounts-payable-agent.md) | Payment processing, vendor management, audit | Autonomous payment execution across crypto, fiat, stablecoins |
| 🌍 [Cultural Intelligence Strategist](specialized/specialized-cultural-intelligence-strategist.md) | Global UX, representation, cultural exclusion | Ensuring software resonates across cultures |
| 🗣️ [Developer Advocate](specialized/specialized-developer-advocate.md) | Community building, DX, developer content | Bridging product and developer community |
| 🔬 [Model QA Specialist](specialized/specialized-model-qa.md) | ML audits, feature analysis, interpretability | End-to-end QA for machine learning models |
| 🗃️ [ZK Steward](specialized/zk-steward.md) | Knowledge management, Zettelkasten, notes | Building connected, validated knowledge bases |
| 🔌 [MCP Builder](specialized/specialized-mcp-builder.md) | Model Context Protocol servers, AI agent tooling | Building MCP servers that extend AI agent capabilities |
| 📄 [Document Generator](specialized/specialized-document-generator.md) | PDF, PPTX, DOCX, XLSX generation from code | Professional document creation, reports, data visualization |
| ⚙️ [Automation Governance Architect](specialized/automation-governance-architect.md) | Automation governance, n8n, workflow auditing | Evaluating and governing business automations at scale |
| 📚 [Corporate Training Designer](specialized/corporate-training-designer.md) | Enterprise training, curriculum development | Designing training systems and learning programs |
| 🌱 [Personal Growth Mentor](specialized/personal-growth-mentor.md) | Goal clarity, habit systems, accountability, life strategy | Cross-domain personal development without motivational fluff |
| 🏛️ [Government Digital Presales Consultant](specialized/government-digital-presales-consultant.md) | China ToG presales, digital transformation | Government digital transformation proposals and bids |
| ⚕️ [Healthcare Marketing Compliance](specialized/healthcare-marketing-compliance.md) | China healthcare advertising compliance | Healthcare marketing regulatory compliance |
| 🎯 [Recruitment Specialist](specialized/recruitment-specialist.md) | Talent acquisition, recruiting operations | Recruitment strategy, sourcing, and hiring processes |
| 🎓 [Study Abroad Advisor](specialized/study-abroad-advisor.md) | International education, application planning | Study abroad planning across US, UK, Canada, Australia |
| 🔗 [Supply Chain Strategist](specialized/supply-chain-strategist.md) | Supply chain management, procurement strategy | Supply chain optimization and procurement planning |
| 🗺️ [Workflow Architect](specialized/specialized-workflow-architect.md) | Workflow discovery, mapping, and specification | Mapping every path through a system before code is written |
| ☁️ [Salesforce Architect](specialized/specialized-salesforce-architect.md) | Multi-cloud Salesforce design, governor limits, integrations | Enterprise Salesforce architecture, org strategy, deployment pipelines |
| 🇫🇷 [French Consulting Market Navigator](specialized/specialized-french-consulting-market.md) | ESN/SI ecosystem, portage salarial, rate positioning | Freelance consulting in the French IT market |
| 🇰🇷 [Korean Business Navigator](specialized/specialized-korean-business-navigator.md) | Korean business culture, 품의 process, relationship mechanics | Foreign professionals navigating Korean business relationships |
| 🏗️ [Civil Engineer](specialized/specialized-civil-engineer.md) | Structural analysis, geotechnical design, global building codes | Multi-standard structural engineering across Eurocode, ACI, AISC, and more |
| 🎧 [Customer Service](specialized/customer-service.md) | Omnichannel support, complaint handling, retention, escalation | Any industry customer support — retail, SaaS, hospitality, finance, logistics |
| 🏥 [Healthcare Customer Service](specialized/healthcare-customer-service.md) | HIPAA-aware patient support, billing, insurance, emergency routing | Healthcare organizations needing compliant, empathetic patient support |
| 🏨 [Hospitality Guest Services](specialized/hospitality-guest-services.md) | Reservations, concierge, complaint recovery, loyalty, events | Hotels, resorts, restaurants, and event venues |
| 🤝 [HR Onboarding](specialized/hr-onboarding.md) | Pre-boarding, compliance, benefits enrollment, 30-60-90 day plans | Any company onboarding new hires — from startups to enterprise |
| 🌐 [Language Translator](specialized/language-translator.md) | Spanish ↔ English translation, dialect awareness, cultural context | Travel, business, medical, and legal translation needs |
| ⏱️ [Legal Billing & Time Tracking](specialized/legal-billing-time-tracking.md) | Time capture, billing narratives, IOLTA compliance, collections | Law firms maximizing revenue recovery and billing accuracy |
| 📋 [Legal Client Intake](specialized/legal-client-intake.md) | Prospect qualification, conflict screening, consultation scheduling | Law firms converting inquiries into retained clients |
| ⚖️ [Legal Document Review](specialized/legal-document-review.md) | Contract review, risk flagging, version comparison, compliance | Attorney-ready first-pass review across any practice area |
| 🏦 [Loan Officer Assistant](specialized/loan-officer-assistant.md) | Borrower intake, TRID compliance, pipeline tracking, closing coordination | Mortgage and consumer lending teams |
| 🏠 [Real Estate Buyer & Seller](specialized/real-estate-buyer-seller.md) | Buyer/seller representation, offers, transaction coordination | Residential and investment real estate transactions |
| 🛒 [Retail Customer Returns](specialized/retail-customer-returns.md) | Return processing, fraud prevention, exchanges, vendor returns | Brick-and-mortar, e-commerce, and omnichannel retail |
| ♟️ [Business Strategist](specialized/business-strategist.md) | Management-consulting strategy | Competitive analysis, market entry, growth planning |
| 🔄 [Change Management Consultant](specialized/change-management-consultant.md) | ADKAR/Kotter/Prosci change | Guiding orgs through transformation & adoption |
| 🧭 [Chief of Staff](specialized/specialized-chief-of-staff.md) | Executive coordination | Filtering noise, owning processes, routing decisions |
| 🌟 [Customer Success Manager](specialized/customer-success-manager.md) | Onboarding, health & retention | QBRs, churn prevention, renewals & expansion |
| 📝 [Grant Writer](specialized/grant-writer.md) | Grant proposals & funding | LOIs, proposals, budgets for nonprofits/research |
| 🏥 [Medical Billing & Coding Specialist](specialized/medical-billing-coding-specialist.md) | ICD-10/CPT/HCPCS & revenue cycle | Claims, denial management, RCM optimization |
| 💰 [Pricing Analyst](specialized/specialized-pricing-analyst.md) | Pricing models & margin optimization | Competitor/cost analysis, value-based pricing |
| 💼 [Chief Financial Officer](specialized/chief-financial-officer.md) | Capital allocation & financial strategy | Treasury, FP&A, M&A finance, investor & board reporting |
| 🌱 [ESG & Sustainability Officer](specialized/esg-sustainability-officer.md) | ESG programs & disclosure | Sustainability strategy, decarbonization, reporting |
| 🔐 [Data Privacy Officer](specialized/data-privacy-officer.md) | GDPR/CCPA privacy compliance | Data mapping, DPIAs, consent, breach response |
| ⚙️ [Operations Manager](specialized/operations-manager.md) | Lean/Six Sigma operations | Process mapping, capacity planning, KPI governance |
| 🤝 [M&A Integration Manager](specialized/ma-integration-manager.md) | Post-merger integration | Day 1/100-day plans, synergy tracking, TSA management |
| 🧠 [Organizational Psychologist](specialized/organizational-psychologist.md) | Team dynamics & culture health | Psychological safety, burnout risk, high-performing teams |
| ⚔️ [Strategy Duel Agent](specialized/specialized-strategy-duel-agent.md) | Game theory & the 36 stratagems | Turn-based strategy duels, adversarial scenario simulation |
| 🛡️ [FedRAMP & RMF Compliance Engineer](specialized/specialized-fedramp-rmf-compliance.md) | Federal cloud authorization (ATO) | NIST 800-53, FedRAMP Rev5/20x, SSP/POA&M, ConMon, OSCAL |
| 🏺 [Codebase Archaeologist](specialized/specialized-codebase-archaeologist.md) | Multi-tool codebase drift audits | Detecting silent drift across Claude/Cursor/Copilot/Windsurf edits |
| 🧾 [Resume Tailor](specialized/resume-tailor.md) | Candidate-side resume optimization | JD mapping, ATS keyword alignment, experience-to-requirement matching |
| 🧡 [Aging Parent Care Companion](specialized/healthcare-aging-parent-care-companion.md) | Family caregiver decision-support | Appointment/medication coordination, care-team comms, caregiver wellbeing (HIPAA-aligned) |
| 🏛️ [Master Plan Architect](specialized/specialized-master-plan-architect.md) | Architectural teaching, red-team plan critique | Deep architecture teaching, risk critique, comprehensive Markdown implementation plans (no code execution) |
| 🎧 [Focus Music Architect](specialized/specialized-focus-music-architect.md) | Instrumental focus-music prompt engineering, neuroacoustics | Soundscape architecture, BPM curves, binaural layers for generative audio models |

### 💵 Finance Division

Accounting, financial analysis, tax strategy, and investment research specialists.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 📒 [Bookkeeper & Controller](finance/finance-bookkeeper-controller.md) | Month-end close, reconciliation, GAAP compliance, internal controls | Day-to-day accounting operations, audit readiness, financial record-keeping |
| 📊 [Financial Analyst](finance/finance-financial-analyst.md) | Financial modeling, forecasting, scenario analysis, decision support | Three-statement models, variance analysis, data-driven business intelligence |
| 📈 [FP&A Analyst](finance/finance-fpa-analyst.md) | Budgeting, rolling forecasts, variance analysis, business reviews | Annual operating plans, monthly business reviews, strategic resource allocation |
| 🔍 [Investment Researcher](finance/finance-investment-researcher.md) | Due diligence, portfolio analysis, asset valuation, equity research | Investment thesis development, risk assessment, market research |
| 🏛️ [Tax Strategist](finance/finance-tax-strategist.md) | Tax optimization, multi-jurisdictional compliance, transfer pricing | Entity structuring, ETR analysis, audit defense, strategic tax planning |

### 🎮 Game Development Division

Building worlds, systems, and experiences across every major engine.

#### Cross-Engine Agents (Engine-Agnostic)

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🎯 [Game Designer](game-development/game-designer.md) | Systems design, GDD authorship, economy balancing, gameplay loops | Designing game mechanics, progression systems, writing design documents |
| 🗺️ [Level Designer](game-development/level-designer.md) | Layout theory, pacing, encounter design, environmental storytelling | Building levels, designing encounter flow, spatial narrative |
| 🎨 [Technical Artist](game-development/technical-artist.md) | Shaders, VFX, LOD pipeline, art-to-engine optimization | Bridging art and engineering, shader authoring, performance-safe asset pipelines |
| 🔊 [Game Audio Engineer](game-development/game-audio-engineer.md) | FMOD/Wwise, adaptive music, spatial audio, audio budgets | Interactive audio systems, dynamic music, audio performance |
| 📖 [Narrative Designer](game-development/narrative-designer.md) | Story systems, branching dialogue, lore architecture | Writing branching narratives, implementing dialogue systems, world lore |
| 💰 [Economy Designer](game-development/economy-designer.md) | Virtual currencies, sources/sinks, monetization modeling, inflation control | Designing in-game economies, balancing F2P monetization, live economy tuning |

#### Unity

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🏗️ [Unity Architect](game-development/unity/unity-architect.md) | ScriptableObjects, data-driven modularity, DOTS/ECS | Large-scale Unity projects, data-driven system design, ECS performance work |
| ✨ [Unity Shader Graph Artist](game-development/unity/unity-shader-graph-artist.md) | Shader Graph, HLSL, URP/HDRP, Renderer Features | Custom Unity materials, VFX shaders, post-processing passes |
| 🌐 [Unity Multiplayer Engineer](game-development/unity/unity-multiplayer-engineer.md) | Netcode for GameObjects, Unity Relay/Lobby, server authority, prediction | Online Unity games, client prediction, Unity Gaming Services integration |
| 🛠️ [Unity Editor Tool Developer](game-development/unity/unity-editor-tool-developer.md) | EditorWindows, AssetPostprocessors, PropertyDrawers, build validation | Custom Unity Editor tooling, pipeline automation, content validation |

#### Unreal Engine

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| ⚙️ [Unreal Systems Engineer](game-development/unreal-engine/unreal-systems-engineer.md) | C++/Blueprint hybrid, GAS, Nanite constraints, memory management | Complex Unreal gameplay systems, Gameplay Ability System, engine-level C++ |
| 🎨 [Unreal Technical Artist](game-development/unreal-engine/unreal-technical-artist.md) | Material Editor, Niagara, PCG, Substrate | Unreal materials, Niagara VFX, procedural content generation |
| 🌐 [Unreal Multiplayer Architect](game-development/unreal-engine/unreal-multiplayer-architect.md) | Actor replication, GameMode/GameState hierarchy, dedicated server | Unreal online games, replication graphs, server authoritative Unreal |
| 🗺️ [Unreal World Builder](game-development/unreal-engine/unreal-world-builder.md) | World Partition, Landscape, HLOD, LWC | Large open-world Unreal levels, streaming systems, terrain at scale |

#### Godot

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 📜 [Godot Gameplay Scripter](game-development/godot/godot-gameplay-scripter.md) | GDScript 2.0, signals, composition, static typing | Godot gameplay systems, scene composition, performance-conscious GDScript |
| 🌐 [Godot Multiplayer Engineer](game-development/godot/godot-multiplayer-engineer.md) | MultiplayerAPI, ENet/WebRTC, RPCs, authority model | Online Godot games, scene replication, server-authoritative Godot |
| ✨ [Godot Shader Developer](game-development/godot/godot-shader-developer.md) | Godot shading language, VisualShader, RenderingDevice | Custom Godot materials, 2D/3D effects, post-processing, compute shaders |

#### Blender

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🧩 [Blender Addon Engineer](game-development/blender/blender-addon-engineer.md) | Blender Python (`bpy`), custom operators/panels, asset validators, exporters, pipeline automation | Building Blender add-ons, asset prep tools, export workflows, and DCC pipeline automation |

#### Roblox Studio

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| ⚙️ [Roblox Systems Scripter](game-development/roblox-studio/roblox-systems-scripter.md) | Luau, RemoteEvents/Functions, DataStore, server-authoritative module architecture | Building secure Roblox game systems, client-server communication, data persistence |
| 🎯 [Roblox Experience Designer](game-development/roblox-studio/roblox-experience-designer.md) | Engagement loops, monetization, D1/D7 retention, onboarding flow | Designing Roblox game loops, Game Passes, daily rewards, player retention |
| 👗 [Roblox Avatar Creator](game-development/roblox-studio/roblox-avatar-creator.md) | UGC pipeline, accessory rigging, Creator Marketplace submission | Roblox UGC items, HumanoidDescription customization, in-experience avatar shops |

### 📚 Academic Division

Scholarly rigor for world-building, storytelling, and narrative design.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🌍 [Anthropologist](academic/academic-anthropologist.md) | Cultural systems, kinship, rituals, belief systems | Designing culturally coherent societies with internal logic |
| 🌐 [Geographer](academic/academic-geographer.md) | Physical/human geography, climate, cartography | Building geographically coherent worlds with realistic terrain and settlements |
| 📚 [Historian](academic/academic-historian.md) | Historical analysis, periodization, material culture | Validating historical coherence, enriching settings with authentic period detail |
| 📜 [Narratologist](academic/academic-narratologist.md) | Narrative theory, story structure, character arcs | Analyzing and improving story structure with established theoretical frameworks |
| 🧠 [Psychologist](academic/academic-psychologist.md) | Personality theory, motivation, cognitive patterns | Building psychologically credible characters grounded in research |
| 📊 [Statistician](academic/academic-statistician.md) | Statistical inference & experiment design | Hypothesis testing, causal inference, sampling, rigorous analysis |

---

### 🌍 GIS Division

Mapping the Earth, analyzing the built world, and extracting intelligence from geospatial data.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🧠 [Technical Consultant](gis/gis-technical-consultant.md) | GIS strategy, gap analysis, technology roadmaps, digital transformation | Understanding business needs, selecting the right geospatial stack, planning multi-phase GIS programs |
| 🔧 [Solution Engineer](gis/gis-solution-engineer.md) | Esri + FOSS4G prototype building, PoC delivery, technical feasibility | Building working demos, validating technical approaches, pre-sales support |
| 🖥️ [GIS Analyst](gis/gis-analyst.md) | Map production, data QC, symbology, layouts, spatial queries | Day-to-day GIS operations, creating publication-ready maps, maintaining data integrity |
| 📦 [Spatial Data Engineer](gis/gis-spatial-data-engineer.md) | Geospatial ETL, format conversion, CRS reprojection, automated pipelines | Ingesting messy data from any source, building repeatable data transformation pipelines |
| ⚙️ [Geoprocessing Specialist](gis/gis-geoprocessing-specialist.md) | ArcPy, Python Toolbox (.pyt), Model Builder, batch automation | Automating repetitive GIS workflows, building custom geoprocessing tools |
| ✅ [GIS QA Engineer](gis/gis-qa-engineer.md) | Topology validation, metadata audit, CRS consistency, accuracy assessment | Quality gates before data publication, compliance verification, data integrity audits |
| 🤖 [GeoAI/ML Engineer](gis/gis-geoai-ml-engineer.md) | Feature extraction, object detection, semantic segmentation, land cover classification | Extracting buildings/roads/vehicles from imagery, change detection, environmental monitoring |
| 🏗️ [BIM/GIS Specialist](gis/gis-bim-specialist.md) | Revit/IFC to GIS, indoor mapping, digital twin architecture, facility management | Smart campus, airport digital twins, indoor navigation, building operations |
| 🏔️ [3D & Scene Developer](gis/gis-3d-scene-developer.md) | Cesium, ArcGIS Scene Viewer, 3D Tiles, point clouds, terrain visualization | 3D city scenes, terrain flyovers, point cloud web viewers, OAuth-gated scene sharing |
| 📊 [Spatial Data Scientist](gis/gis-spatial-data-scientist.md) | Spatial statistics, clustering, regression, interpolation, point pattern analysis | Hotspot detection, spatial modeling, predictive analytics, research-grade analysis |
| 🛸 [Drone/Reality Mapping](gis/gis-drone-reality-mapping.md) | Photogrammetry, orthomosaic, DTM/DSM, point cloud classification, 3D mesh | Drone survey processing, reality capture, construction monitoring, environmental mapping |
| 🌐 [Web GIS Developer](gis/gis-web-gis-developer.md) | MapLibre GL JS, ArcGIS JS API, Leaflet, real-time dashboards, REST APIs | Building interactive web maps, operational dashboards, real-time data visualization |
| 🎨 [Cartography Designer](gis/gis-cartography-designer.md) | Color theory, typography, basemap design, visual hierarchy, print and web aesthetics | Making maps beautiful and readable, colorblind-safe palettes, professional map layouts |

---

### 🏥 Healthcare Division

Building AI agents for regulated clinical and sovereign health contexts.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🩺 [Clinical Evidence Agent](healthcare/healthcare-clinical-evidence-agent.md) | Evidence standards, validated vs unvalidated claims, diagnostic authority boundaries | Making clinical claims credibly without overstepping into diagnostic authority |
| 🌍 [Sovereign Health Systems Agent](healthcare/healthcare-sovereign-health-systems-agent.md) | Government health mandates, UHC policy, emerging market deployment | Health tech teams operating at the intersection of national health infrastructure and sovereign health policy |
| 🧭 [Healthcare Innovation Strategist](healthcare/healthcare-innovation-strategist.md) | Narrative architecture for healthcare founders across investor, regulatory, sovereign, and clinical audiences | Healthcare founders who need to translate clinical and financial complexity into language that moves capital and builds trust |

---

### 🔍 Research Division

Finding, evaluating, and synthesizing existing evidence rather than generating new primary data.

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| 🔍 [Research Synthesist](research/research-synthesist.md) | Literature review, source evaluation, citation tracing, evidence synthesis | Turning a scattered pile of sources into a structured, honestly-weighted map of what the evidence supports |

---

## 🎯 Real-World Use Cases

### Scenario 1: Building a Startup MVP

**Your Team**:
1. 🎨 **Frontend Developer** - Build the React app
2. 🏗️ **Backend Architect** - Design the API and database
3. 🚀 **Growth Hacker** - Plan user acquisition
4. ⚡ **Rapid Prototyper** - Fast iteration cycles
5. 🔍 **Reality Checker** - Ensure quality before launch

**Result**: Ship faster with specialized expertise at every stage.

---

### Scenario 2: Marketing Campaign Launch

**Your Team**:
1. 📝 **Content Creator** - Develop campaign content
2. 🐦 **Twitter Engager** - Twitter strategy and execution
3. 📸 **Instagram Curator** - Visual content and stories
4. 🤝 **Reddit Community Builder** - Authentic community engagement
5. 📊 **Analytics Reporter** - Track and optimize performance

**Result**: Multi-channel coordinated campaign with platform-specific expertise.

---

### Scenario 3: Enterprise Feature Development

**Your Team**:
1. 👔 **Senior Project Manager** - Scope and task planning
2. 💎 **Senior Developer** - Complex implementation
3. 🎨 **UI Designer** - Design system and components
4. 🧪 **Experiment Tracker** - A/B test planning
5. 📸 **Evidence Collector** - Quality verification
6. 🔍 **Reality Checker** - Production readiness

**Result**: Enterprise-grade delivery with quality gates and documentation.

---

### Scenario 4: Paid Media Account Takeover

**Your Team**:

1. 📋 **Paid Media Auditor** - Comprehensive account assessment
2. 📡 **Tracking & Measurement Specialist** - Verify conversion tracking accuracy
3. 💰 **PPC Campaign Strategist** - Redesign account architecture
4. 🔍 **Search Query Analyst** - Clean up wasted spend from search terms
5. ✍️ **Ad Creative Strategist** - Refresh all ad copy and extensions
6. 📊 **Analytics Reporter** (Support Division) - Build reporting dashboards

**Result**: Systematic account takeover with tracking verified, waste eliminated, structure optimized, and creative refreshed — all within the first 30 days.

---

### Scenario 5: Full Agency Product Discovery

**Your Team**: All 8 divisions working in parallel on a single mission.

See the **[Nexus Spatial Discovery Exercise](examples/nexus-spatial-discovery.md)** -- a complete example where 8 agents (Product Trend Researcher, Backend Architect, Brand Guardian, Growth Hacker, Support Responder, UX Researcher, Project Shepherd, and XR Interface Architect) were deployed simultaneously to evaluate a software opportunity and produce a unified product plan covering market validation, technical architecture, brand strategy, go-to-market, support systems, UX research, project execution, and spatial UI design.

**Result**: Comprehensive, cross-functional product blueprint produced in a single session. [More examples](examples/).

---

### Scenario 6: Smart Campus Digital Twin

**Your Team**:

1. 🧠 **Technical Consultant** - Define the digital twin strategy: BIM for buildings, GIS for campus, IoT for real-time
2. 🏗️ **BIM/GIS Specialist** - Convert Revit building models to GIS scene layers, design indoor floor plans
3. 🛸 **Drone/Reality Mapping** - Fly the campus, generate orthomosaic and 3D mesh for context
4. 🌐 **Web GIS Developer** - Build the campus dashboard with MapLibre, building layer, and room finder
5. 🏔️ **3D & Scene Developer** - Create immersive 3D scene with terrain, buildings, and flyover tour
6. 🤖 **GeoAI/ML Engineer** - Extract building footprints and tree canopy from drone imagery
7. ✅ **GIS QA Engineer** - Validate data accuracy, check topology, verify CRS consistency

**Result**: A campus digital twin that combines BIM detail, drone reality capture, 3D visualization, and web accessibility — delivered by coordinated specialists in a single pipeline.

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Add a New Agent

1. Fork the repository
2. Create a new agent file in the appropriate category
3. Follow the agent template structure:
   - Frontmatter with name, description, color
   - Identity & Memory section
   - Core Mission
   - Critical Rules (domain-specific)
   - Technical Deliverables with examples
   - Workflow Process
   - Success Metrics
4. Submit a PR with your agent

### Improve Existing Agents

- Add real-world examples
- Enhance code samples
- Update success metrics
- Improve workflows

### Share Your Success Stories

Have you used these agents successfully? Share your story in the [Discussions](https://github.com/msitarzewski/agency-agents/discussions)!

---

## 📖 Agent Design Philosophy

Each agent is designed with:

1. **🎭 Strong Personality**: Not generic templates - real character and voice
2. **📋 Clear Deliverables**: Concrete outputs, not vague guidance
3. **✅ Success Metrics**: Measurable outcomes and quality standards
4. **🔄 Proven Workflows**: Step-by-step processes that work
5. **💡 Learning Memory**: Pattern recognition and continuous improvement

---

## 🎁 What Makes This Special?

### Unlike Generic AI Prompts:
- ❌ Generic "Act as a developer" prompts
- ✅ Deep specialization with personality and process

### Unlike Prompt Libraries:
- ❌ One-off prompt collections
- ✅ Comprehensive agent systems with workflows and deliverables

### Unlike AI Tools:
- ❌ Black box tools you can't customize
- ✅ Transparent, forkable, adaptable agent personalities

---

## 🎨 Agent Personality Highlights

> "I don't just test your code - I default to finding 3-5 issues and require visual proof for everything."
>
> -- **Evidence Collector** (Testing Division)

> "You're not marketing on Reddit - you're becoming a valued community member who happens to represent a brand."
>
> -- **Reddit Community Builder** (Marketing Division)

> "Every playful element must serve a functional or emotional purpose. Design delight that enhances rather than distracts."
>
> -- **Whimsy Injector** (Design Division)

> "Let me add a celebration animation that reduces task completion anxiety by 40%"
>
> -- **Whimsy Injector** (during a UX review)

---

## 📊 Stats

- 🎭 **230+ Specialized Agents** across every division
- 📝 **10,000+ lines** of personality, process, and code examples
- ⏱️ **Months of iteration** from real-world usage
- 🌟 **Battle-tested** in production environments
- 💬 **50+ requests** in first 12 hours on Reddit

---

## 🔌 Multi-Tool Integrations

The Agency works natively with Claude Code, and ships conversion + install scripts so you can use the same agents across every major agentic coding tool.

### Supported Tools

- **[Claude Code](https://claude.ai/code)** — native `.md` agents, no conversion needed → `~/.claude/agents/`
- **[GitHub Copilot](https://github.com/copilot)** — native `.md` agents, no conversion needed → `~/.github/agents/` + `~/.copilot/agents/`
- **[Antigravity](https://github.com/google-gemini/antigravity)** — `SKILL.md` per agent → `~/.gemini/config/skills/`
- **[Gemini CLI](https://github.com/google-gemini/gemini-cli)** -- `.md` agent files -> `~/.gemini/agents/`
- **[OpenCode](https://opencode.ai)** — `.md` agent files → `.opencode/agents/`
- **[Cursor](https://cursor.sh)** — `.mdc` rule files → `.cursor/rules/`
- **[Aider](https://aider.chat)** — `CONVENTIONS.md` roster index → `./CONVENTIONS.md`
- **[Windsurf](https://codeium.com/windsurf)** — single `.windsurfrules` → `./.windsurfrules`
- **[OpenClaw](https://github.com/openclaw/openclaw)** — `SOUL.md` + `AGENTS.md` + `IDENTITY.md` per agent
- **[Qwen Code](https://github.com/QwenLM/qwen-code)** — `.md` SubAgent files → `~/.qwen/agents/`
- **[Kimi Code](https://github.com/MoonshotAI/kimi-cli)** — YAML agent specs → `~/.config/kimi/agents/`
- **[Codex](https://developers.openai.com/codex/overview)** — TOML custom agents → `~/.codex/agents/`
- **Osaurus** -- `SKILL.md` skills -> `~/.osaurus/skills/`
- **[Hermes](integrations/hermes/README.md)** -- lazy-router plugin -> `~/.hermes/plugins/`
- **[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)** — `SKILL.md` skills → `~/.dsh/skills/` (user) or `.dsh/skills/` (project)

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

## 🗺️ Roadmap

- [ ] Interactive agent selector web tool
- [x] Multi-agent workflow examples -- see [examples/](examples/)
- [x] Multi-tool integration scripts (Claude Code, GitHub Copilot, Antigravity, Gemini CLI, OpenCode, OpenClaw, Cursor, Aider, Windsurf, Qwen Code, Kimi Code, Codex, Osaurus, Hermes)
- [ ] Video tutorials on agent design
- [ ] Community agent marketplace
- [ ] Agent "personality quiz" for project matching
- [ ] "Agent of the Week" showcase series

---

## 🌐 Community Translations & Localizations

Community-maintained translations and regional adaptations. These are independently maintained -- see each repo for coverage and version compatibility.

| Language | Maintainer | Link | Notes |
|----------|-----------|------|-------|
| 🇨🇳 简体中文 (zh-CN) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) | 141 translated agents + 46 China-market originals |
| 🇨🇳 简体中文 (zh-CN) | [@dsclca12](https://github.com/dsclca12) | [agent-teams](https://github.com/dsclca12/agent-teams) | Independent translation with Bilibili, WeChat, Xiaohongshu localization |
| 🇧🇷 Português brasileiro (pt-BR) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-pt-BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | 184 upstream agents translated; Brazil-market PRs welcome |
| 🇷🇺 Русский (ru) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ru](https://github.com/jnMetaCode/agency-agents-ru) | 184 upstream agents translated; Russia-market PRs welcome |
| 🇮🇩 Bahasa Indonesia (id) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-id](https://github.com/jnMetaCode/agency-agents-id) | 184 upstream agents translated; Indonesia-market PRs welcome |
| 🇸🇦 العربية (ar) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ar](https://github.com/jnMetaCode/agency-agents-ar) | 184 upstream agents translated; Arabic-market PRs welcome |
| 🇰🇷 한국어 (ko) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ko](https://github.com/jnMetaCode/agency-agents-ko) | 184 upstream agents fully translated; Korea-specific PRs welcome |
| 🇯🇵 日本語 (ja-JP) | [@sscodeai](https://github.com/sscodeai) | [agency-agents-ja](https://github.com/sscodeai/agency-agents-ja) | 281 Japan-localized agents + 97 Japan-market originals + 27 workflows |
| 🇻🇳 Tiếng Việt (vi-VN) | [@rodonguyen](https://github.com/rodonguyen) | [agency-agents](https://github.com/rodonguyen/agency-agents) | Starter Vietnamese localization focused on README, quick start, and high-use docs |

Want to add a translation? Open an issue and we'll link it here.

---

## 📜 License

MIT License - Use freely, commercially or personally. Attribution appreciated but not required.

---

## 🙏 Acknowledgments

What started as a Reddit thread about AI agent specialization has grown into something remarkable — **230+ agents across every division**, supported by a community of contributors from around the world. Every agent in this repo exists because someone cared enough to write it, test it, and share it.

To everyone who has opened a PR, filed an issue, started a Discussion, or simply tried an agent and told us what worked — thank you. You're the reason The Agency keeps getting better.

---

## 💬 Community

- **GitHub Discussions**: [Share your success stories](https://github.com/msitarzewski/agency-agents/discussions)
- **Issues**: [Report bugs or request features](https://github.com/msitarzewski/agency-agents/issues)
- **Reddit**: Join the conversation on r/ClaudeAI
- **Twitter/X**: Share with #TheAgency

---

## 🚀 Get Started

1. **Browse** the agents above and find specialists for your needs
2. **Copy** the agents to `~/.claude/agents/` for Claude Code integration
3. **Activate** agents by referencing them in your Claude conversations
4. **Customize** agent personalities and workflows for your specific needs
5. **Share** your results and contribute back to the community

---

<div align="center">

**🎭 The Agency: Your AI Dream Team Awaits 🎭**

[⭐ Star this repo](https://github.com/msitarzewski/agency-agents) • [🍴 Fork it](https://github.com/msitarzewski/agency-agents/fork) • [🐛 Report an issue](https://github.com/msitarzewski/agency-agents/issues) • [❤️ Sponsor](https://github.com/sponsors/msitarzewski)

Made with ❤️ by the community, for the community

</div>
