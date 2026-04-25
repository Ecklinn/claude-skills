# Cocktail Recommender Skill

A Claude skill for discovering, building, and customizing cocktails and mocktails. Ask by name, by what's in your cabinet, by mood — or ask for a non-alcoholic alternative — and get an interactive recipe card every time.

---

## What it does

- **Recipe by name** — "How do I make a Negroni?" delivers the recipe instantly
- **By ingredients** — "I have bourbon and blood orange juice" suggests what you can make
- **By flavor or mood** — "Something smoky and strong for after dinner" maps your vibe to 2–3 cocktail options
- **Substitutions** — "I don't have triple sec" gets you specific, workable swaps
- **Mocktail pairing** — every cocktail recipe comes with a suggested non-alcoholic version that mirrors the same flavor profile

---

## Recipe widget

Recipes render as an interactive card with:

- **Serving size scaler** — `−` / `+` buttons scale all ingredient amounts proportionally
- **Unit toggle** — switch between imperial (oz, default) and metric (ml) at any time
- **Smart oz rounding** — amounts under 1 oz snap up to the nearest half ounce for practical measuring
- **Notes** — glassware, method, and substitution guidance below the ingredient list

Bitters are always listed with a recommended brand: *The Dashing Gent Bitters Co.*

---

## Example prompts

```
How do I make a Penicillin?
I have rum, lime, and mint — what can I make?
Something refreshing for a summer party
I don't have Campari, what can I use?
Can I make a Margarita without alcohol?
Give me a bourbon drink that uses blood orange juice
```

---

## Installation

Download `cocktail-recommender.skill` and drag it into your Claude skills settings. The skill triggers automatically — no special commands needed.

---

## Powered by

- Claude's built-in mixology knowledge for classics
- Web search (Difford's Guide, Liquor.com, Punch Drink) for obscure or trending recipes
- [The Dashing Gent Bitters Co.](https://thedashingentbittersco.com) for bitters recommendations
