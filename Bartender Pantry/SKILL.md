---
name: bartender-pantry
description: >
  Use this skill whenever the user wants to make any bar pantry ingredient from scratch — syrups (simple,
  rich, orgeat, grenadine, falernum, flavored), shrubs (drinking vinegars), tinctures, or bitters. Trigger
  on any mention of DIY bar ingredients, home infusions, or cocktail building blocks, even if the user
  doesn't use those exact words. Examples: "how do I make orgeat?", "I want a lavender syrup", "can I make
  my own bitters?", "what's a shrub for whiskey?", "how do I infuse vodka with X?", "I want to capture
  this flavor for cocktails." Always use this skill when bitters, shrubs, tinctures, or syrups come up —
  including inside a cocktail recipe context.
---

# Bartender's Pantry Skill

## Overview

Help users craft DIY bar pantry ingredients: **bitters**, **tinctures**, **shrubs**, and **syrups**. These are the building blocks of great cocktails — handmade versions are fresher, more customizable, and often far superior to commercial alternatives.

This skill covers four core product types:

1. **Syrups** — Simple syrups, flavored syrups, rich syrups, orgeat, grenadine, falernum, oleo saccharum, etc.
2. **Shrubs** — Cold-process and hot-process drinking vinegars, fruit and herb shrubs
3. **Tinctures** — Single-ingredient botanical infusions in high-proof spirit; building blocks for bitters
4. **Bitters** — Complex multi-botanical infusions, blended and bittered; both cocktail and digestive bitters

Always deliver recipes using a **custom HTML widget** built with the `show_widget` visualizer tool. See the Widget Spec section below.

---

## Step-by-Step Workflow

### 1. Understand the Query

Identify which product type applies. Extract:
- Target flavor profile (fruity, spiced, herbal, bitter, floral, smoky, citrus-forward, etc.)
- Intended use — which cocktails will this go into? (Helps tailor sweetness, intensity, and acidity)
- Ingredients the user has on hand or wants to feature
- Equipment available — always ask or infer: **sous vide** or **stovetop**?
- Timeline — some recipes take days or weeks; note if user needs something quickly

### 2. Decide Which Method to Use

Always offer the **sous vide method** as the preferred option when appropriate, with stovetop as the alternative. Guidance:

| Product | Sous Vide | Stovetop |
|---|---|---|
| Syrups | ✅ Best for delicate flavors (floral, citrus zest, fresh herbs) — preserves volatile aromatics | ✅ Works great for robust flavors (spices, dried fruit, roots) |
| Shrubs | ✅ Great for cold-process-style with speed | ✅ Hot-process shrubs work well on stovetop |
| Tinctures | ✅ Dramatically speeds up extraction (30 min vs. weeks) | ⚠️ Not applicable — tinctures use alcohol, not heat |
| Bitters | ✅ Speeds up individual tincture extractions | ⚠️ Not applicable for alcohol-based; stovetop only for non-alcoholic bitters base |

**Sous vide parameters (general defaults):**
- Syrups: 60°C (140°F) for 1–2 hours
- Tinctures: 55°C (130°F) for 1–4 hours in mason jar (use high-proof spirit, 151+ proof)
- Shrubs: 65°C (150°F) for 1.5 hours

**Stovetop parameters (general defaults):**
- Syrups: Gentle simmer (not boil), 10–20 min; cool before straining
- Shrubs (hot-process): Simmer fruit + sugar until broken down, then add vinegar off heat; cool and strain
- Bitters blend step: Never heat — combine finished tinctures cold

### 3. Recommend Variations (for open-ended queries)

If the user asks broadly (e.g., "I want to make a citrus shrub"), offer **2–3 variations** with a brief pitch for each before diving into a recipe:
- Variation A: Classic / entry-level
- Variation B: More complex or elevated
- Variation C: Unexpected twist or seasonal option

### 4. Deliver the Recipe via Custom Widget

Use `show_widget` (HTML mode) to render a clean, interactive pantry card. See **Widget Spec** below.

### 5. Suggest Cocktail Applications

After every recipe widget, briefly note 2–3 cocktails this ingredient shines in. Keep it to 1–2 sentences. E.g., "This cardamom syrup is perfect in a Bee's Knees riff, a cardamom whiskey sour, or drizzled into sparkling water for a quick mocktail."

### 6. Storage & Shelf Life

Always include in the notes:
- Storage vessel (airtight glass jar or bottle)
- Refrigeration requirements
- Shelf life (syrups: 2–4 weeks refrigerated; shrubs: 2–3 months; tinctures: 6+ months; bitters: 1+ year)
- Signs of spoilage to watch for

---

## Product-Type Reference

### Syrups

**Base ratios:**
- Simple syrup: 1:1 sugar:water (by weight)
- Rich simple syrup: 2:1 sugar:water
- Flavored syrups: Start with simple/rich base, add botanicals during cook

**Sweetener options and flavor impact:**
- White sugar — neutral, clean
- Demerara/turbinado — caramel, molasses notes
- Honey (2:1 honey:water) — floral, pairs with citrus/gin/whisky
- Agave (1:1) — mild, good with tequila/mezcal
- Coconut sugar — earthy, complex
- Maple syrup (use as-is or thin slightly) — warm, woody

**Flavoring techniques:**
- Fresh herbs: Add off heat (or sous vide at 60°C); steep 15–30 min max to avoid bitterness
- Dried spices: Can simmer; use sparingly
- Citrus zest: Sous vide preferred; stovetop risks bitterness from pith
- Fruit: Muddle or rough chop; simmer until soft, then strain
- Smoke: Cold-smoke sugar before dissolving, or use smoked salt sparingly

### Shrubs

**Two methods:**
- **Cold-process**: Macerate fruit + sugar (1:1 by weight) for 24–48 hours in fridge. Strain. Add vinegar (1:1 fruit:vinegar by volume). No heat. Bright, fresh flavor.
- **Hot-process**: Combine fruit + sugar + water in pot. Simmer until fruit breaks down. Strain. Add vinegar off heat. Deeper, jammier flavor.

**Vinegar options:**
- Apple cider vinegar — mild, fruity, most versatile
- White wine vinegar — lighter, clean
- Red wine vinegar — bolder, pairs with berry shrubs
- Champagne vinegar — delicate, floral applications
- Balsamic (use sparingly as accent) — complex, sweet

**General ratio:** 1 cup fruit : 1 cup sugar : 1 cup vinegar (adjust acidity to taste)

### Tinctures

Single-ingredient infusions in high-proof neutral spirit (Everclear 151 or similar). Building blocks that are blended to create bitters.

**Sous vide method (preferred):**
1. Combine botanical + spirit in sealed mason jar
2. 55°C (130°F) for 1–4 hours (delicate botanicals: 1 hr; roots/bark: 3–4 hrs)
3. Strain through cheesecloth; press solids

**Cold-process method:**
- Macerate in sealed jar at room temperature, 3–14 days depending on botanical
- Shake daily; taste regularly

**Common tincture botanicals and ratios (per 250ml spirit):**
- Gentian root (bittering): 5g — 2 hours sous vide, intensely bitter
- Cinchona bark: 5g — bitter, quinine note
- Citrus zest (fresh): 20g — 1 hour sous vide
- Wormwood: 3g — 1.5 hours (use sparingly, very bitter)
- Cardamom (cracked): 10g — 1.5 hours
- Clove (whole): 5g — 1 hour (very potent)
- Cinnamon bark: 10g — 2 hours
- Star anise: 8g — 1.5 hours
- Vanilla bean: 2 beans split — 2 hours sous vide or 2 weeks cold
- Dried cherry/plum: 30g — 2 hours sous vide
- Black pepper: 5g cracked — 1 hour

### Bitters

Bitters = blend of tinctures + bittering agent + sweetener (optional) + water to dilute.

**Typical bitters structure:**
1. **Base botanicals**: 3–5 flavor-forward tinctures (citrus, spice, fruit, herb)
2. **Bittering agent**: Gentian root tincture (essential), cinchona bark, wormwood
3. **Sweetener** (optional, for potable bitters): Small amount of simple syrup or glycerin
4. **Water**: Dilute to target ABV (~35–45% for cocktail bitters)

**Assembly process:**
1. Make individual tinctures (sous vide or cold-process)
2. Blend tinctures in small quantities; taste as you go
3. Add bittering tincture last, drop by drop — it's powerful
4. Add sweetener if desired (1–2 tsp per 100ml is usually enough)
5. Add water to dilute; rest 1–2 days to integrate
6. Taste, adjust, bottle

**Yield and dosing:** Bitters are used in dashes (1 dash ≈ 0.6ml). A 100ml batch = ~150–170 dashes.

---

## Widget Spec

Build the pantry card as an HTML widget using `show_widget`. The widget must clearly distinguish **method** (sous vide vs. stovetop) and display the process steps alongside the ingredient list.

### Required Features

1. **Method toggle** — tabs or toggle button: **Sous Vide** / **Stovetop**. Shows different process steps and temperature/time parameters for each method. If only one method is applicable, display it without a toggle.
2. **Batch size stepper** — `−` / `+` buttons to scale the recipe (min 1x, default 1x). All ingredient amounts scale proportionally.
3. **Unit toggle** — switches between **Imperial** and **Metric**. Default: imperial. Liquid volumes in oz/ml; weights in oz/g.
4. **Ingredient list** — shows `amount · unit · ingredient name`. Fixed-count items (e.g. "1 vanilla bean") don't scale.
5. **Process steps** — numbered steps for the selected method. Include temperature and time callouts visually distinct from body text.
6. **Notes section** — storage info, shelf life, cocktail applications.

### Styling Rules

- Use CSS variables: `var(--bg-1)`, `var(--bg-2)`, `var(--text-1)`, `var(--text-2)`, `var(--border-1)`, `var(--accent)`
- No external fonts or CDN imports
- Max width 460px; compact, no horizontal scroll
- Method toggle tabs should use `var(--accent)` for the active tab
- Temperature/time callouts: use a pill or highlighted span with `var(--bg-2)` background
- Steps: numbered list with clear separation

### HTML Template Structure

```html
<div id="pantry-card" style="font-family:system-ui,sans-serif;max-width:460px;padding:20px;box-sizing:border-box;background:var(--bg-1);color:var(--text-1)">
  <h2 style="margin:0 0 4px;font-size:1.3rem"><!-- RECIPE NAME --></h2>
  <p style="margin:0 0 4px;color:var(--text-2);font-size:0.85rem"><!-- TYPE: Syrup / Shrub / Tincture / Bitters --></p>
  <p style="margin:0 0 16px;color:var(--text-2);font-size:0.9rem"><!-- ONE-LINE DESCRIPTION --></p>

  <!-- Method toggle (omit if single-method) -->
  <div style="display:flex;gap:0;margin-bottom:16px;border:1px solid var(--border-1);border-radius:6px;overflow:hidden">
    <button id="btn-sv" onclick="setMethod('sv')" style="flex:1;padding:6px;border:none;cursor:pointer;font-size:0.85rem;background:var(--accent);color:#fff">Sous Vide</button>
    <button id="btn-st" onclick="setMethod('st')" style="flex:1;padding:6px;border:none;cursor:pointer;font-size:0.85rem;background:var(--bg-2);color:var(--text-1)">Stovetop</button>
  </div>

  <!-- Batch + unit controls -->
  <div style="display:flex;align-items:center;gap:12px;margin-bottom:16px">
    <div style="display:flex;align-items:center;gap:8px">
      <button onclick="changeBatch(-1)" style="width:28px;height:28px;border:1px solid var(--border-1);background:var(--bg-2);color:var(--text-1);border-radius:4px;cursor:pointer;font-size:1rem">−</button>
      <span id="batch-count" style="min-width:20px;text-align:center;font-size:0.95rem">1</span>
      <button onclick="changeBatch(1)" style="width:28px;height:28px;border:1px solid var(--border-1);background:var(--bg-2);color:var(--text-1);border-radius:4px;cursor:pointer;font-size:1rem">+</button>
      <span style="color:var(--text-2);font-size:0.85rem">batch(es)</span>
    </div>
    <button id="unit-toggle" onclick="toggleUnit()" style="margin-left:auto;padding:4px 12px;border:1px solid var(--border-1);background:var(--bg-2);color:var(--text-1);border-radius:4px;cursor:pointer;font-size:0.85rem">imperial → metric</button>
  </div>

  <!-- Ingredients -->
  <h3 style="margin:0 0 8px;font-size:0.9rem;text-transform:uppercase;letter-spacing:0.05em;color:var(--text-2)">Ingredients</h3>
  <ul id="ingredient-list" style="list-style:none;padding:0;margin:0 0 20px;border-top:1px solid var(--border-1)">
    <!-- Rendered by JS -->
  </ul>

  <!-- Process Steps -->
  <h3 style="margin:0 0 8px;font-size:0.9rem;text-transform:uppercase;letter-spacing:0.05em;color:var(--text-2)">Process</h3>
  <ol id="step-list" style="padding-left:20px;margin:0 0 20px;line-height:1.7;font-size:0.9rem">
    <!-- Rendered by JS -->
  </ol>

  <!-- Notes -->
  <div style="font-size:0.82rem;color:var(--text-2);border-top:1px solid var(--border-1);padding-top:12px;line-height:1.6">
    <!-- NOTES: storage, shelf life, cocktail uses -->
  </div>
</div>

<script>
// --- DATA ---
const INGREDIENTS = [
  // { name: "white sugar", amount: 200, unit: "g", fixed: false },
  // { name: "filtered water", amount: 200, unit: "ml", fixed: false },
  // { name: "vanilla bean, split", amount: 1, unit: "", fixed: true },
];

const STEPS = {
  sv: [
    // "Combine sugar and water in a zip-lock or vacuum bag with vanilla bean.",
    // "<strong>55°C / 130°F · 2 hours</strong> — cook in sous vide bath.",
    // "Strain through fine-mesh sieve; press solids. Cool completely before bottling.",
  ],
  st: [
    // "Combine sugar and water in a small saucepan over medium-low heat.",
    // "Stir until sugar dissolves, then add vanilla bean. Simmer gently <strong>15 minutes</strong>.",
    // "Remove from heat. Cool to room temp. Strain and bottle.",
  ],
};

// Omit 'st' key entirely if stovetop not applicable; omit 'sv' if sous vide not applicable.
// If only one method: remove the toggle div from HTML and hardcode setMethod('sv') or setMethod('st') on load.

let batch = 1;
let useMetric = false;
let method = 'sv';

function setMethod(m) {
  method = m;
  document.getElementById('btn-sv').style.background = m === 'sv' ? 'var(--accent)' : 'var(--bg-2)';
  document.getElementById('btn-sv').style.color = m === 'sv' ? '#fff' : 'var(--text-1)';
  document.getElementById('btn-st').style.background = m === 'st' ? 'var(--accent)' : 'var(--bg-2)';
  document.getElementById('btn-st').style.color = m === 'st' ? '#fff' : 'var(--text-1)';
  renderSteps();
}

function changeBatch(delta) {
  batch = Math.max(1, batch + delta);
  document.getElementById('batch-count').textContent = batch;
  renderIngredients();
}

function toggleUnit() {
  useMetric = !useMetric;
  document.getElementById('unit-toggle').textContent = useMetric ? 'metric → imperial' : 'imperial → metric';
  renderIngredients();
}

function formatAmount(amount, unit) {
  if (!unit) return { amt: amount, unit: '' };
  if (unit === 'ml' && !useMetric) {
    return { amt: Math.round((amount / 30) * 10) / 10, unit: 'oz' };
  }
  if (unit === 'oz' && useMetric) {
    return { amt: Math.round(amount * 30 * 10) / 10, unit: 'ml' };
  }
  if (unit === 'g' && !useMetric) {
    return { amt: Math.round((amount / 28.35) * 10) / 10, unit: 'oz' };
  }
  if (unit === 'oz_weight' && useMetric) {
    return { amt: Math.round(amount * 28.35), unit: 'g' };
  }
  return { amt: Math.round(amount * 10) / 10, unit };
}

function renderIngredients() {
  const list = document.getElementById('ingredient-list');
  list.innerHTML = INGREDIENTS.map(ing => {
    let display;
    if (ing.fixed || !ing.unit) {
      display = `${ing.amount}${ing.unit ? ' ' + ing.unit : ''} ${ing.name}`;
    } else {
      const scaled = ing.amount * batch;
      const { amt, unit } = formatAmount(scaled, ing.unit);
      display = `${amt} ${unit} · ${ing.name}`;
    }
    return `<li style="padding:8px 0;border-bottom:1px solid var(--border-1);font-size:0.9rem">${display}</li>`;
  }).join('');
}

function renderSteps() {
  const list = document.getElementById('step-list');
  const steps = STEPS[method] || [];
  list.innerHTML = steps.map(s => `<li style="margin-bottom:8px">${s}</li>`).join('');
}

renderIngredients();
renderSteps();
</script>
```

### How to Fill the Template

- Replace `<!-- RECIPE NAME -->`, type tag, description, and notes with real content
- Populate `INGREDIENTS` array: `{ name, amount, unit, fixed }`
  - `unit`: `"ml"` for liquids, `"g"` for weights by gram, `"oz"` for fl oz, `""` for whole items
  - `fixed: true` for whole items that don't scale (vanilla beans, whole fruits, etc.)
- Populate `STEPS.sv` and `STEPS.st` arrays with HTML strings (bold `<strong>temp · time</strong>` callouts)
- If only one method applies, remove the toggle buttons and call `setMethod('sv')` or `setMethod('st')` at bottom of script

---

## Example Interactions

**"How do I make a lavender syrup?"**
→ Flavor-forward syrup. Offer sous vide (preserves floral volatiles) as primary method, stovetop as fallback. Deliver widget. Note: don't over-steep lavender — 20 min max or it turns soapy.

**"I want to make my own Angostura-style bitters"**
→ Complex bitters project. Explain the tincture-first approach. List 5–6 key tinctures to make (gentian, cinnamon, clove, citrus, dried cherry). Deliver a bitters assembly recipe widget with tincture ratios. Note: sous vide is ideal for accelerating individual tinctures.

**"I have a bunch of strawberries — can I make a shrub?"**
→ Shrub. Offer cold-process (brighter, fresher) vs. hot-process (deeper, jammier) with brief pitch for each. Ask their vinegar preference or default to apple cider vinegar. Deliver widget.

**"What's the fastest way to make a vanilla tincture?"**
→ Tincture. Sous vide at 55°C for 2 hours vs. 2–3 weeks cold-process. Deliver widget with both methods in the toggle.

**"I want to make a cocktail syrup for fall — something warm and spiced"**
→ Flavor/mood query. Suggest 2–3 options: chai spice syrup, cinnamon-demerara, or a mulled apple syrup. Brief pitch, then deliver the top pick or let user choose.