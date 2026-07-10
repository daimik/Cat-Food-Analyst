# Cat Food Evaluation Guide & Rubric

A reusable reference for judging whether a cat food is good.
**How to reuse:** upload this file into a chat, paste one or more product links (or the composition + guaranteed analysis text), and ask the assistant to evaluate them against this rubric.

Primary source method: YouTube video on judging cat food quality — <https://youtu.be/xILNc3Pqki4> — extended with additional nutrition context gathered during research.

---

## 0. INSTRUCTIONS FOR THE ASSISTANT (read first)

When the user gives you this file plus product links or label text, act as a **rigorous, skeptical cat-food analyst**. Follow these behaviours:

1. **Work from real data, not the front of the pack.** Fetch each link and read the *actual* Composition (ingredient list) and Analytical Constituents (guaranteed analysis) of the **exact variant/flavour**. Recipes differ between flavours and between countries.
2. **Ignore marketing claims** ("70% fresh meat", "salmon as main ingredient", "premium", "holistic") until verified against the ingredient order and percentages.
3. **Double-check every criterion explicitly.** Show the numbers you used. Do not hand-wave.
4. **State missing data honestly.** If calcium/phosphorus (or anything needed) is not declared, say so and mark that check "unverifiable" — do not guess.
5. **Convert to dry-matter (DM) basis** whenever comparing minerals across wet and dry foods (formula in §5). The **Ca:P ratio** and **ingredient quality** are the most reliable checks because they don't depend on moisture.
6. **Give a clear verdict**: `PASS` / `MIXED` / `FAIL`, with a bullet reason per criterion, and suggest better alternatives if it falls short.
7. **Adjust for the cat**: sterilized adult vs kitten vs senior changes the targets (§7). Ask the cat's life stage / neuter status / weight if not given.
8. **Never sacrifice accuracy to be agreeable.** If a "premium" or expensive food fails, say it fails.

Suggested output format is the template in §9.

---

## 1. THE CORE METHOD (from the video)

### Step 1 — Read the Composition, not the analysis headline
Look at the **ingredient list** (Composition), where items are listed **in descending order by weight**. This matters more than the protein/fat headline.

### Step 2 — Judge the first ingredient
| First ingredient | Rating | Notes |
|---|---|---|
| Grain first (rice, corn, wheat, any cereal) | ❌ Reject | A cat should not be fed on grain. |
| "Meat of X" / "X meat" (named muscle meat) | ✅ Good | e.g. "chicken meat", "rabbit meat". |
| "Fresh X meat" first | ⚠️ Caution | Fresh meat is ~70% water and shrinks **4–5×** when processed. In a dry food the real backbone is the **next** dried ingredient. |
| "X" whole (e.g. "chicken 70%") | 🟡 Weaker | "Chicken" = everything lumped: bones, cartilage, guts, sometimes feathers. Real muscle meat is much less than the % implies. |
| "Meal of X" / "X meal" (unnamed) | 🟠/❌ Worst | Lowest quality; all sorts of parts, poor control. Named-species meal (e.g. "salmon meal") is the acceptable *dry-food* version (see §4). |

### Step 3 — Ash / bone flag
If **protein is modest (~30%) but ash is high (~8%) and calcium is high**, the food likely has lots of ground **bone** (low-quality raw material). High ash + high calcium = red flag.

### Step 4 — Minerals (the kidney check)
Phosphorus must be **less** than calcium. If phosphorus ≥ calcium, long-term kidney risk. See limits in §3.

### Step 5 — Ca:P ratio
Target roughly **1.2 : 1 to 1.4 : 1** (calcium : phosphorus). Phosphorus always lower than calcium.

---

## 2. EXTENDED RULES (learned beyond the video)

- **Wet vs dry mineral basis.** Wet food is ~75–82% water, so its *as-fed* mineral % looks tiny (e.g. Ca 0.25%) and passes the ceilings automatically — that's dilution, not merit. For wet food, the meaningful checks are the **Ca:P ratio** (moisture-independent) and the **first-ingredient quality**. The video's absolute ceilings (Ca ≤1.2%, P ≤1%) are effectively **dry-food as-fed** numbers.
- **Complete vs complementary.**
  - **"Complete" / "полнорационный" / "Alleinfutter"** → can be the sole diet.
  - **"Complementary" / "single feed" / "Ergänzungsfutter"** → topper/treat only, NOT a full diet (won't have balanced vitamins/minerals/taurine). Many fillet-in-jelly/broth products and freeze-dried snacks are complementary. Always check.
- **Dry food reality.** In any kibble the protein backbone is **dried meat/meal** — "fresh meat first" as the dominant protein is physically impossible at ~10% moisture. So the realistic best for dry is **named-species meat meal** (e.g. "wild boar meat meal", "salmon meal") + **low ash** + **good Ca:P**, ideally grain-free.
- **Taurine** is essential for cats (heart, vision). A complete food must contain it (added or naturally from heart/organ meat). Higher declared taurine (e.g. 1500 mg/kg) is a good sign; very low (e.g. 500 mg/kg) is modest.
- **Legume bulking.** Grain-free dry foods often replace grain with peas, pea protein, chickpeas, lentils, pea flour. That's technically "grain-free" but it's still a large **plant** fraction, not meat. Count how many legume items appear and how high.
- **Marketing traps to cross-check:**
  - "X% fresh meat" on the front → recompute after 4–5× shrink.
  - "[Fish] as main ingredient" → check if another meat actually has a higher %.
  - "No grain" on a bag that's mostly peas/potato.
  - Nice front photo of muscle meat while composition says "meat and animal by-products".

---

## 3. REFERENCE VALUES (as-fed label targets)

| Nutrient | Adult cat | Kitten (<12 mo) | Note |
|---|---|---|---|
| Calcium (Ca) | ≤ 1.2% | ≤ 1.5% | Kittens need more for bone growth. |
| Phosphorus (P) | ≤ 1.0% | ≤ 1.0% | Must be **lower** than calcium. |
| **Ca : P ratio** | **1.2–1.4 : 1** | **1.2–1.4 : 1** | Most reliable, moisture-independent check. |
| Magnesium (Mg) | ~0.08–0.09% | ≤ 0.1% | Lower is better for urinary health (esp. sterilized). |
| Sodium (Na) | 0.2–0.5% | 0.2–0.5% | Urinary/therapeutic diets may run higher on purpose. |
| Taurine | present | present | Essential; higher = better. |

> These ceilings apply cleanly to **dry** food (as-fed). For **wet** food, expect much lower as-fed % due to water — focus on the **Ca:P ratio** instead, and/or convert to dry matter (§5).

---

## 4. MEAT DECLARATION QUALITY TIERS (best → worst)

1. **Named species + full breakdown** — e.g. "Poultry 69% (muscle meat 15%, heart, liver, stomach, neck)". Highest transparency. *(catz finefood, Animonda Carny.)*
2. **Named species meat, no breakdown** — e.g. "53% chicken meat". Good.
3. **Named-species dried meat / meal** — e.g. "dehydrated rabbit meat", "salmon meal", "turkey meal". Realistic top tier for **dry** food; acceptable if ash is low (deboned) and species is named.
4. **"Meat and animal by-products (X% named)"** — vague EU catch-all; only the named % is transparent, the rest is unspecified. *(e.g. Monge Grill.)*
5. **Unnamed "meat meal" / "animal derivatives" / "meat-and-bone meal"** — worst; avoid.

---

## 5. DRY-MATTER (DM) CONVERSION

Use this to compare minerals fairly across wet and dry, or to compare a wet food to dry-basis ceilings.

```
DM fraction        = (100 − moisture%) / 100
Nutrient on DM (%) = as-fed% / DM fraction
```

**Examples**
- Wet food, Ca 0.25%, moisture 80% → DM fraction 0.20 → Ca (DM) = 0.25 / 0.20 = **1.25%**
- Dry food, Ca 1.0%, moisture 6% → DM fraction 0.94 → Ca (DM) = 1.0 / 0.94 = **1.06%**

Energy sanity check for portioning: `kcal/day ≈ dry grams × (kcal per kg ÷ 1000)`. A pouch's kcal is on its label; typical 85 g lean pouch ≈ 78–85 kcal.

---

## 6. STEP-BY-STEP EVALUATION CHECKLIST

For each product:

1. **Identify:** name, exact variant, wet/dry, life stage (adult/kitten/senior), country of manufacture.
2. **Complete vs complementary?** (sole diet allowed or topper only)
3. **Pull real data:** full Composition + Analytical Constituents of that variant (fetch the link).
4. **First ingredient** → apply §1 Step 2 + §4 tiers.
5. **Grain check** → any cereal first = reject; cereal lower down = note (not automatic fail); count legumes.
6. **Ash / bone flag** → high ash + high calcium + modest protein = bone-loading.
7. **Minerals** → list Ca, P, Mg, Na vs §3; compute **Ca:P ratio**; convert to DM if comparing wet↔dry.
8. **Taurine** present? amount?
9. **Red-flag ingredients** → unnamed by-products, added sugar, milk powder, heavy legumes, artificial colours/flavours/preservatives.
10. **Marketing vs reality** → cross-check front-of-pack claims against the actual % order.
11. **Verdict** → PASS / MIXED / FAIL, reasons per criterion, better alternatives if needed.

---

## 7. LIFE-STAGE & SPECIAL CASES

- **Sterilized / neutered adult:** prioritise **moisture** (wet food or wet+dry combo — reduces urinary/kidney risk), **controlled calories** (they gain weight easily), **low magnesium**, urinary pH support. Feed toward the lower end of the portion range and watch weight.
- **Kitten (<12 months):** needs **kitten or all-life-stages "complete"** food; higher calcium allowed (≤1.5%), higher protein/fat/energy; **DHA** (from fish/salmon oil) supports brain & vision. Keep on kitten food until ~12 months, then transition over ~1 week.
- **Senior / CKD-prone:** tighter phosphorus control; a Ca:P around 1.3–1.4:1 is fine for healthy cats but CKD cats need vet-guided low-phosphorus diets.
- **General:** always fresh water available; on dry-only diets watch water intake closely; open wet pouches keep ~1–3 days refrigerated.

---

## 8. VERIFIED BRAND NOTES (from prior research — re-verify current labels)

> Formulas change by country and over time. Treat these as starting points and re-check the specific bag/can.

### Wet — complete (usable as main food)
- **catz finefood Classic / Purrrr (Germany)** — ✅ Strongest verifiable pick. Named meat + breakdown first, grain-free, no sugar, ash ~2–3%. Declares Ca 0.2–0.3% / P 0.15–0.25% → Ca:P ≈ 1.25:1. Taurine 1500 mg/kg. Lean flavours (Geflügel/Wild ~90–99 kcal/100g) best for sterilized; fish flavours to rotate. *Rind & Kalb reads as all-life-stages (also OK for kittens).*
- **Animonda Carny (Germany)** — 🟡 Good ingredients (named meat + organs, grain-free, low ash) but **Ca/P not declared** → ratio unverifiable. Uses rapeseed oil (weak omega source). **Carny Kitten** = complete for kittens, adds fish oil.
- **Wild Freedom (zooplus, EU)** — ✅ "Chicken meat" first, Ca 0.26–0.32% / P 0.19–0.24% (Ca:P ~1.3:1), ash ~1.7–1.9%, grain-free. Slightly less transparent (no muscle/offal split).
- **Monge Grill (Italy)** — 🟡 Complete, grain-free, DHA added, low ash, but first ingredient is the vague "meat and animal by-products (X% named)" category + milk powder; taurine modest (500 mg/kg); Ca/P not declared. Mid-tier.

### Wet — complementary (TOPPER only, not sole diet)
- **Grandorf fillet/Filet (Italy)** — clean 100% fillet in broth/jelly, but labelled **complementary** → use as topper for moisture/palatability, not as the only food.

### Dry (best-achievable; protein backbone is meal by nature)
- **Grandorf Rabbit & Turkey Sterilised — Holistic (Belgium)** — ✅ ~49% named dehydrated meat first (honest label, no "fresh %" inflation), ash only **6%** (deboned, no meat-and-bone meal), Ca 1.0 / P 0.8 → Ca:P 1.25:1, Mg 0.09%. Caveat: **brown rice** is 3rd (single-grain, not grain-free).
- **Grandorf Fresh Sterilised — Duck/Salmon (Belgium)** — ✅ Grain-free version (sweet potato + peas), Ca ~1.1 / P 0.8, ash ~7%.
- **Carnilove Sterilised — Lamb & Wild Boar (Czech Rep.)** — ✅ Excellent minerals for a dry (Ca 0.8 / P 0.7, Mg 0.04%), grain/potato-free, reduced K/Mg for urinary. Caveat: named **meat meal** base + ~19% peas. *(Note: some Carnilove "True Fresh"/updated variants run Ca 1.4 / P 1.1 and ash 8–9% — worse; always check the exact bag.)*
- **Carnilove Kitten — Salmon & Turkey (Czech Rep.)** — ✅ Ca 1.3 / P 1.0 (Ca:P 1.3:1), grain-free, salmon oil for DHA.
- **Others not yet verified here:** Leonardo, Wildcat, Farmina N&D, Bozita, Josera, Sanabelle, MAC's — run them through the checklist before recommending.

### Treats
- **catz finefood PURE Snacks (freeze-dried hearts, Germany)** — ✅ 100% single-protein meat (heart = taurine-rich), grain-free, no sugar. **Beef hearts** leaner (472 kcal/100g) — better for sterilized; **chicken hearts** fattier (535 kcal/100g). Treats = ≤10% of daily calories; give water (freeze-dried).

---

## 9. QUICK VERDICT TEMPLATE (assistant fills this per product)

```
PRODUCT: <name / variant>   |   Type: wet/dry   |   Life stage: <>   |   Origin: <>
Complete or complementary: <>

First ingredient: <text>  → Tier <1–5>  → <ok / caution / fail>
Grain: <none / cereal position>   Legumes: <count/positions>
Ash: <%>   Bone flag: <yes/no>
Minerals: Ca <%>  P <%>  Mg <%>  Na <%>   Ca:P = <ratio>   (DM basis if converted)
Taurine: <amount / present?>
Red flags: <list or none>
Marketing vs reality: <note>

VERDICT: PASS / MIXED / FAIL
Why: <bullets>
Better alternative (if needed): <>
```

---

## 10. ONE-LINE PRINCIPLES

- Judge the **guaranteed analysis of the exact variant**, never the front label.
- **Named meat first**, phosphorus **below** calcium, **low ash**, complete (not complementary).
- For **sterilized** cats, moisture beats everything — wet or wet+dry combo.
- In **dry** food, best you can get is named-species meat meal + low ash + good Ca:P.
- When a number is missing, mark it unverifiable — don't invent it.
