# Acropolist

A phone-friendly map for my Athens trip: friends' recommendations in orange, general recommendations in blue (Google Maps rating 4.5+ with 1,000+ reviews, checked 14 Nov 2026).

- `index.html` – the app (Leaflet, no build step)
- `places.json` – all the pins

## Adding a place

Add an entry to `places.json`:

```json
{ "name": "Tavern Klimataria", "source": "friend", "by": "Friend's name", "category": "Food",
  "note": "What to order", "lat": 37.98058, "lng": 23.72453, "url": "https://maps.app.goo.gl/..." }
```

`source` is `friend` or `general`. `by`, `note` and `url` are optional.

## Run locally

```bash
python3 -m http.server 8000
```
