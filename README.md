# Nexxtmove Device Card

Lovelace kaart voor [Home Assistant](https://www.home-assistant.io/) die info, statistieken en recente events toont van een [Nexxtmove](https://www.nexxtmove.com/) charging device.

## Vereisten

- [Nexxtmove integratie](https://github.com/geertmeersman/nexxtmove) geïnstalleerd via HACS

## Installatie via HACS

1. Ga naar HACS → Frontend
2. Klik op ⋮ → Aangepaste repositories
3. Voeg toe: `https://github.com/geertmeersman/nexxtmove-device-card`
4. Categorie: `Lovelace`
5. Installeer "Nexxtmove Device Card"
6. Voeg de resource toe in Instellingen → Dashboards → Resources:
   - URL: `/hacsfiles/nexxtmove-device-card/nexxtmove-device-card.js`
   - Type: `JavaScript module`

## Configuratie

```yaml
type: custom:nexxtmove-device-card
device_id: <device_id>
```

### Opties

| Optie | Standaard | Beschrijving |
|---|---|---|
| `device_id` | verplicht | ID van het Nexxtmove charging device |
| `show_stats` | `true` | Maandstatistieken (energie, kosten, sessies) |
| `show_non_invoiced` | `true` | Openstaand bedrag |
| `show_price` | `true` | Prijs per kWh |
| `show_max_power` | `true` | Max vermogen |
| `show_charges` | `true` | Recente laadsessies (sectie) |
| `show_events` | `true` | Recente events |

De kaart heeft een visuele editor in de Lovelace UI — kies gewoon het device uit de dropdown.
