# bartender-pantry

A Claude skill for crafting DIY bar pantry ingredients from scratch — bitters, tinctures, shrubs, and syrups — with interactive recipe cards that support both sous vide and stovetop methods.

---

## What it does

When installed, this skill gives Claude deep knowledge of home bartender pantry production. Ask about making any bar building-block ingredient and Claude will deliver an interactive recipe card with:

- **Scalable batch sizes** — scale up or down with a stepper control
- **Unit toggle** — switch between imperial and metric
- **Method toggle** — sous vide or stovetop steps, with temperature and time callouts
- **Storage guidance** — shelf life, refrigeration, and spoilage signs
- **Cocktail applications** — 2–3 drinks to use the ingredient in

---

## Supported ingredient types

| Type | Examples |
|---|---|
| **Syrups** | Simple, rich, orgeat, grenadine, falernum, oleo saccharum, flavored (floral, spiced, fruit) |
| **Shrubs** | Cold-process and hot-process drinking vinegars; fruit, herb, and spice shrubs |
| **Tinctures** | Single-botanical infusions in high-proof spirit; building blocks for bitters |
| **Bitters** | Multi-botanical cocktail bitters and digestive bitters, assembled from tinctures |

---

## Trigger phrases

This skill activates on queries like:

- "How do I make orgeat?"
- "I want to make a lavender syrup"
- "Can I make bitters at home?"
- "What's a good shrub for whiskey cocktails?"
- "How do I infuse vodka with cardamom?"
- "I want to capture the flavor of fresh ginger in a syrup"
- "How do I preserve these strawberries for cocktails?"

It also triggers when bitters, shrubs, or syrups come up in the context of a cocktail recipe.

---

## Method guidance

The skill always presents both methods where applicable and recommends the best fit for the ingredient:

| Product | Sous Vide | Stovetop |
|---|---|---|
| Syrups | Preferred for delicate flavors (floral, citrus, fresh herbs) | Great for robust flavors (spices, dried fruit, roots) |
| Shrubs | Cold-process speed with precision temperature | Hot-process; jammy, deeper flavor |
| Tinctures | Dramatically faster (1–4 hrs vs. weeks) | Not applicable — alcohol-based |
| Bitters | Best for individual tincture extractions | Blending step is always cold |

---

## Output format

Every recipe is rendered as an interactive HTML widget in the chat — not a plain list. The widget includes:

- Ingredient list with scaled amounts
- Numbered process steps with highlighted temperature/time callouts
- Notes panel with storage, shelf life, and cocktail uses

---

## Installation

Install the `.skill` file via the Skills section in Claude settings. No additional dependencies required.

---

## Example interaction

**User:** How do I make orgeat?

**Claude:** Delivers a full interactive orgeat recipe card with almond milk extraction, sugar ratio, orange blossom water quantities, and separate sous vide (90 min at 60°C) and stovetop steps — all scalable by batch size with imperial/metric toggle.
