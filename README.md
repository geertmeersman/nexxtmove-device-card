# Nexxtmove Device Card

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![maintainer](https://img.shields.io/badge/maintainer-Geert%20Meersman-green?style=for-the-badge&logo=github)](https://github.com/geertmeersman)
[![buyme_coffee](https://img.shields.io/badge/Buy%20me%20an%20Omer-donate-yellow?style=for-the-badge&logo=buymeacoffee)](https://www.buymeacoffee.com/geertmeersman)

A Lovelace card for [Home Assistant](https://www.home-assistant.io/) that displays info, statistics and recent events for a [Nexxtmove](https://www.nexxtmove.com/) charging device.

## Requirements

- [Nexxtmove integration](https://github.com/geertmeersman/nexxtmove) installed via HACS

## Installation via HACS

1. Go to HACS → Frontend
2. Click ⋮ → Custom repositories
3. Add: `https://github.com/geertmeersman/nexxtmove-device-card`
4. Category: `Lovelace`
5. Install "Nexxtmove Device Card"
6. Add the resource in Settings → Dashboards → Resources:
   - URL: `/hacsfiles/nexxtmove-device-card/nexxtmove-device-card.js`
   - Type: `JavaScript module`

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=geertmeersman&repository=nexxtmove-device-card&category=lovelace)

## Configuration

The card has a visual editor — just pick the device from the dropdown.

```yaml
type: custom:nexxtmove-device-card
device_id: <device_id>
```

### Options

| Option | Default | Description |
|---|---|---|
| `device_id` | required | Nexxtmove charging device ID |
| `show_stats` | `true` | Monthly statistics (energy, cost, sessions) with expandable sessions |
| `show_non_invoiced` | `true` | Outstanding amount |
| `show_price` | `true` | Price per kWh |
| `show_max_power` | `true` | Max power |
| `show_charges` | `true` | Recent charge sessions (section) |
| `show_events` | `true` | Recent events |
