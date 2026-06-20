# SMS Gammu Viewer Card

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![GitHub Release](https://img.shields.io/github/v/release/BrainDeLook/sms-gammu-viewer-card?style=for-the-badge)](https://github.com/BrainDeLook/sms-gammu-viewer-card/releases)
[![License](https://img.shields.io/github/license/BrainDeLook/sms-gammu-viewer-card.svg?style=for-the-badge)](LICENSE)

> 🇬🇧 [English version](README.md)

Компактная карточка Lovelace, показывающая последние SMS-диалоги прямо на дашборде Home Assistant, со значком непрочитанных и переходом в полную панель [SMS Gammu Viewer](https://github.com/BrainDeLook/sms-gammu-viewer-ha) в один клик.

---

## Требования

Карточка требует установленную и настроенную интеграцию **[SMS Gammu Viewer](https://github.com/BrainDeLook/sms-gammu-viewer-ha)** — карточка читает данные из её API и бесполезна без неё.

---

## Установка

### Через HACS (рекомендуется)

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=BrainDeLook&repository=sms-gammu-viewer-card&category=plugin)

Или вручную:

1. Открой **HACS** в Home Assistant
2. Нажми ⋮ → **Пользовательские репозитории**
3. Вставь: `https://github.com/BrainDeLook/sms-gammu-viewer-card` — Категория: **Dashboard**
4. Найди **SMS Gammu Viewer Card** → **Скачать**
5. Перезапусти Home Assistant (или просто обнови браузер)

### Ручная установка

1. Скачай `sms-gammu-viewer-card.js` из [последнего релиза](https://github.com/BrainDeLook/sms-gammu-viewer-card/releases)
2. Скопируй в `<config>/www/`
3. Перейди в **Настройки → Дашборды → Ресурсы** → **+ Добавить ресурс**
4. URL: `/local/sms-gammu-viewer-card.js`, тип: **JavaScript Module**

---

## Использование

> ⚠️ **Только YAML-настройка** — визуального редактора для карточки пока нет. Добавь её через **Редактировать дашборд → Добавить карточку → Вручную (Manual)**, либо прямо в YAML дашборда.

```yaml
type: custom:sms-gammu-viewer-card
title: SMS
max_items: 5
show_unread_only: false
```

| Параметр | Тип | По умолчанию | Описание |
|---|---|---|---|
| `title` | строка | `SMS` | Заголовок карточки |
| `max_items` | число | `5` | Сколько диалогов показывать |
| `show_unread_only` | булево | `false` | Показывать только диалоги с непрочитанными |

Клик по диалогу или ссылке «Открыть все сообщения» открывает полную панель SMS Gammu Viewer.

---

## Лицензия

MIT

