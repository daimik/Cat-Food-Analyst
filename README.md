# 🐱 Cat Food Analyst

A **Claude Code subagent** (and standalone rubric) that judges whether a cat food is actually good —
by reading the *real* ingredient list and guaranteed analysis of the exact product, not the marketing
on the front of the pack. Give it a product link, a label photo, or pasted composition text, and it
returns a **PASS / MIXED / FAIL** verdict with per-criterion reasons and better alternatives.

**Who it's for:** everyday feeding of **healthy cats** — including **sterilized cats and kittens** —
to help you pick a genuinely good regular food. It works for adult, kitten, and senior life stages.

> ⚠️ **Not veterinary advice.** This is an educational tool for choosing everyday commercial cat food.
> The one exception: if your cat is **sick** or needs a **special medical diet** (kidney disease,
> urinary disease, allergies, etc.), consult a licensed veterinarian instead of picking from retail
> formulas.

---

## 🧬 Inspiration & the logic behind it

Cats are **obligate carnivores** — evolution tuned them to eat other animals, not crops. In the wild a
cat lives on **mice, small birds, and other small prey**, and that ancestral diet is the benchmark
this project measures food against.

**What a wild cat actually eats (by calories).** A meta-study of 27 feral-cat diet studies
(Plantinga, Bosch & Hendriks, *British Journal of Nutrition*, 2011) found the natural diet is roughly:

- 🥩 **~52% protein**
- 🧈 **~46% fat**
- 🌾 **~2% carbohydrate**

In other words: **almost all meat and fat, and next to no carbs.** Whole prey is also about
**~70% water** — a mouse or a small bird is mostly moisture.

**Where the "grain" idea comes from — and its limit.** Your instinct is right that *some* plant matter
reaches the cat: prey animals (mice, birds) eat seeds, grains and berries, so their **stomach and gut
contents**, plus the odd nibbled blade of grass, end up inside the cat — a natural trace of plant
fibre and micronutrients. **But the amount is tiny and incidental.** In the same research, plant
material turned up only in small traces (e.g. a few strands of grass, in about a quarter of cats), and
scientists concluded it's a **minor, largely accidental** part of the diet. So a *small* amount of
plant matter is natural — a diet *built on* grain is not. That single fact is why the rubric
**rejects grain as the #1 ingredient** but tolerates a little plant matter lower in the list.

**Two more things prey gives a cat:**
- 💧 **Water in the food.** Because prey is ~70% water, cats evolved a **weak thirst drive** — built to
  get moisture from food, not the bowl. On dry-only diets many cats stay mildly dehydrated, which
  stresses the urinary tract and kidneys (a big deal for **sterilized cats**). That's why this tool
  keeps pushing **moisture (wet food, or a wet+dry combo)**.
- ❤️ **Taurine.** Prey muscle and organs (especially **heart**) are rich in taurine — an amino acid
  cats can't make enough of and need for heart and vision. A complete food must contain it.

### From nature → what to expect from a good cat food

| In the wild (prey) | So a good cat food should… | Rubric check |
|---|---|---|
| ~52% protein, mostly muscle + organ meat | Lead with **named meat**, high animal protein | First-ingredient tier |
| ~46% fat | Have adequate animal fat | Fat % |
| ~2% carbohydrate | Be **low-carb**; minimal grain/legume | Grain & legume check |
| ~70% water | Provide **moisture** (wet or wet+dry) | Wet-vs-dry / sterilized note |
| Only trace, incidental plant matter | Not be **built on grain** (a little, low in the list, is OK) | Grain-first = reject |
| Taurine-rich organs | **Contain taurine** | Taurine check |
| Bone in the right proportion | Balanced minerals, **not bone-loaded** | Ash flag + Ca:P ratio |

The closer a product sits to that prey profile — and the more honestly its label says so — the better
it scores. The further it drifts (grain or vague "meat and animal by-products" first, low moisture,
high carbs, no declared taurine), the lower it lands.

### Why I built this

Walk down the cat-food aisle and most bags tell you the **opposite** of the prey model: cereal or a
vague "animal by-products" as the first ingredient; dry kibble bulked with peas and potato;
"70% fresh meat" claims that shrink to a fraction once cooked; premium-looking packaging hiding a
low-meat recipe. The real story is on the **back** of the pack — the ordered ingredient list and the
guaranteed analysis — which is exactly what the marketing hopes you won't read.

I built **Cat Food Analyst** so **anyone** can hold a product up against what a cat actually evolved to
eat, read the parts that matter, and get a straight **PASS / MIXED / FAIL** — instead of trusting the
front of the box.

> **Source:** Plantinga EA, Bosch G, Hendriks WH (2011). *Estimation of the dietary nutrient profile of
> free-roaming feral cats: possible implications for nutrition of domestic cats.* British Journal of
> Nutrition, 106(S1): S35–S48. Macronutrient figures are % of metabolizable energy.

---

## What it checks

- **First ingredient** — named meat vs "chicken" vs "meal" vs grain (with the 4–5× fresh-meat shrink caveat).
- **Grain & legume load** — grain first = reject; heavy peas/lentils bulking noted.
- **Ash / bone flag** — high ash + high calcium + modest protein = ground bone / low-grade meal.
- **Minerals** — calcium, phosphorus, magnesium, sodium vs life-stage targets.
- **Ca:P ratio** — phosphorus must be below calcium (~1.2–1.4 : 1); the most reliable, moisture-independent signal.
- **Complete vs complementary** — can it be a sole diet, or is it just a topper/treat?
- **Wet vs dry basis** — converts to dry-matter so wet and dry are compared fairly.
- **Taurine, red-flag ingredients, and marketing-vs-reality** cross-checks.

Full method with rationale: **[docs/evaluation-guide.md](docs/evaluation-guide.md)**
Worked examples: **[docs/examples.md](docs/examples.md)**

---

## Install & use

### Option A — As a Claude Code subagent (recommended)

Copy the agent file into your Claude Code agents directory.

**User scope** (available in every project):
```bash
mkdir -p ~/.claude/agents
curl -o ~/.claude/agents/cat-food-analyst.md \
  https://raw.githubusercontent.com/daimik/Cat-Food-Analyst/main/.claude/agents/cat-food-analyst.md
# or just copy the file from this repo
```

**Project scope** (checked into a repo, shared with your team):
```bash
mkdir -p .claude/agents
cp path/to/cat-food-analyst.md .claude/agents/
```

> File-based subagents load at session start — **restart Claude Code** after adding the file (or create
> it via the `/agents` command, which takes effect immediately).

Then just ask, and Claude Code will auto-delegate based on the agent's description, or call it explicitly:

```
Use the cat-food-analyst subagent on this: https://example.com/some-cat-food
```
```
cat-food-analyst: is this good for a sterilized cat? <link or pasted label>
```

### Option B — In a normal chat (claude.ai, API, etc.)

You don't need Claude Code. Upload **[docs/evaluation-guide.md](docs/evaluation-guide.md)** (or the
agent file) into the chat, paste one or more product links / labels, and ask it to evaluate them
against the rubric. The instructions inside the file drive the analysis.

---

## What you get back

The agent fills this template per product:

```
PRODUCT: <name / variant>   |   Type: wet/dry   |   Life stage: <>   |   Origin: <>
Complete or complementary: <>

First ingredient: <text>  → Tier <1–5>  → <ok / caution / fail>
Grain: <none / cereal position>    Legumes: <count / positions>
Ash: <%>    Bone flag: <yes/no>
Minerals: Ca <%>  P <%>  Mg <%>  Na <%>    Ca:P = <ratio>   (DM basis if converted)
Taurine: <amount / present?>
Red flags: <list or none>
Marketing vs reality: <note>

VERDICT: PASS / MIXED / FAIL
Why: <bullets>
Better alternative (if needed): <>
```

---

## Repository structure

```
cat-food-analyst/
├── README.md                          ← you are here
├── LICENSE                            ← MIT
├── CODE_OF_CONDUCT.md
├── .gitignore
├── .claude/
│   └── agents/
│       └── cat-food-analyst.md        ← the Claude Code subagent (self-contained)
└── docs/
    ├── evaluation-guide.md            ← standalone rubric + rationale (great for plain chat)
    └── examples.md                    ← worked PASS / MIXED / FAIL examples
```

---

## Reference values (quick view)

| Nutrient | Adult | Kitten (<12 mo) |
|---|---|---|
| Calcium (Ca) | ≤ 1.2% | ≤ 1.5% |
| Phosphorus (P) | ≤ 1.0% | ≤ 1.0% |
| **Ca : P ratio** | **1.2–1.4 : 1** | **1.2–1.4 : 1** |
| Magnesium (Mg) | ~0.08–0.09% | ≤ 0.1% |
| Sodium (Na) | 0.2–0.5% | 0.2–0.5% |

> Ceilings apply cleanly to **dry** food (as-fed). For **wet** food, focus on the **Ca:P ratio** or
> convert to dry matter (formula in the guide). For **sterilized cats**, the biggest lever is
> **moisture** — wet food or a wet+dry combo — not just a fancier kibble.

---

## License

[MIT](LICENSE) — free to use, modify, and share. Attribution appreciated.
