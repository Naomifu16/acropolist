# Acropolist

A phone-friendly map for my Athens trip: dots coloured by category (food, bars, museums, sights…), a black ring around friends' recommendations, and a search box. General recommendations are Google Maps rating 4.5+ with 1,000+ reviews, checked 14 Nov 2026.

- `index.html` – the app (Leaflet, no build step)
- `places.json` – all the pins
- `days.json` – the day plans
- `flights.json` – the flights

## Adding a place

Add an entry to `places.json`:

```json
{ "name": "Tavern Klimataria", "source": "friend", "by": "Friend's name", "category": "Food", "type": "Taverna",
  "note": "What to order", "lat": 37.98058, "lng": 23.72453, "url": "https://maps.app.goo.gl/..." }
```

`source` is `friend` or `general`. `type` (what kind of place it is, shown in the popup), `rating` and `reviews` (Google Maps), `by`, `note`, `url` and `story` (a short history or anecdote shown in the popup) are optional.

## Tabs

- **Map** – the pins, filters and search.
- **Trip** – flights from `flights.json` (each `{ "number": "A3 929", "date": "...", "time": "...", "from": "...", "to": "..." }`, with a live-status link) and proposed days from `days.json`. Each day has `title`, `where` (the group heading), `summary`, `stops` (`time`, `text`, and optionally `place`, the exact name of a pin to link to) and `tips`.
- **Guide** – history and practical notes (plain HTML in `index.html`), plus every pin that has a `story`.

## Run locally

```bash
python3 -m http.server 8000
```
