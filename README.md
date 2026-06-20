# SMS Gammu Viewer Card

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![GitHub Release](https://img.shields.io/github/v/release/BrainDeLook/sms-gammu-viewer-card?style=for-the-badge)](https://github.com/BrainDeLook/sms-gammu-viewer-card/releases)
[![License](https://img.shields.io/github/license/BrainDeLook/sms-gammu-viewer-card.svg?style=for-the-badge)](LICENSE)

> 🇷🇺 [Русская версия](README_RU.md)

A compact Lovelace card showing your most recent SMS conversations directly on the Home Assistant dashboard, with an unread badge and one-click access to the full [SMS Gammu Viewer](https://github.com/BrainDeLook/sms-gammu-viewer-ha) panel.

---

## Requirements

This card requires the **[SMS Gammu Viewer](https://github.com/BrainDeLook/sms-gammu-viewer-ha)** integration to be installed and configured — the card reads data from its API and is useless without it.

---

## Installation

### Via HACS (recommended)

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=BrainDeLook&repository=sms-gammu-viewer-card&category=plugin)

Or manually:

1. Open **HACS** in Home Assistant
2. Click ⋮ → **Custom repositories**
3. Paste: `https://github.com/BrainDeLook/sms-gammu-viewer-card` — Category: **Dashboard**
4. Find **SMS Gammu Viewer Card** → **Download**
5. Restart Home Assistant (or just refresh the browser)

### Manual installation

1. Download `sms-gammu-viewer-card.js` from the [latest release](https://github.com/BrainDeLook/sms-gammu-viewer-card/releases)
2. Copy it to `<config>/www/`
3. Go to **Settings → Dashboards → Resources** → **+ Add Resource**
4. URL: `/local/sms-gammu-viewer-card.js`, type: **JavaScript Module**

---

## Usage

Add the card via the dashboard UI editor (search for "SMS Gammu Viewer Card"), or in YAML:

```yaml
type: custom:sms-gammu-viewer-card
title: SMS
max_items: 5
show_unread_only: false
```

| Option | Type | Default | Description |
|---|---|---|---|
| `title` | string | `SMS` | Card header text |
| `max_items` | number | `5` | Number of conversations to show |
| `show_unread_only` | boolean | `false` | Only show conversations with unread messages |

Clicking any conversation or the "Open all messages" link navigates to the full SMS Gammu Viewer panel.

---

## License

MIT
