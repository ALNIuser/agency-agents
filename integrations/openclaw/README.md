# Интеграция с OpenClaw

Агенты OpenClaw устанавливаются в виде рабочих пространств, содержащих файлы `SOUL.md`, `AGENTS.md` и `IDENTITY.md`. Установщик копирует каждое рабочее пространство в `~/.openclaw/agency-agents/` и регистрирует его, если доступен CLI `openclaw`.

Перед установкой необходимо сгенерировать рабочие пространства OpenClaw:

```bash
./scripts/convert.sh --tool openclaw
```

## Установка

```bash
./scripts/install.sh --tool openclaw
```

## Активация агента

После установки агенты доступны по `agentId` в сессиях OpenClaw.

Если шлюз OpenClaw уже запущен, перезапустите его после установки:

```bash
openclaw gateway restart
```

## Повторная генерация

```bash
./scripts/convert.sh --tool openclaw
```
