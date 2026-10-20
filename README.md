# Eating Well Costs More Than Eating Badly

**A global analysis of the food system and a step-by-step solution that can be replicated anywhere in the world**

---

## 1. The Problem

### 1.1 The Core Idea

It is not that people "don't know how to eat" or that they "lack willpower." Around the world, the food system is designed so that **what makes you sick is the cheapest, most available, and most advertised**, while what nourishes you is a privilege. Poor nutrition is not an individual failure: it is the predictable result of prices, subsidies, advertising, and product design.

### 1.2 How It Shows Up

**Price per calorie.** In any country, a dollar buys far more in cookies, soda, or fried snacks than in fruit or vegetables. Real food is perishable, heavy to transport, and offers low margins for the seller.

**Unequal availability.** In working-class neighborhoods worldwide, ultra-processed food outlets and fast food abound. Finding fresh, varied produce is harder, farther away, and more expensive.

**Time.** Cooking takes time that many working families do not have. Ultra-processed food is ready in minutes.

**Addictive design.** Sugar, salt, and fat are calibrated in laboratories to maximize craving, not nutrition. Advertising reinforces that craving and targets children above all.

**Misguided subsidies.** In almost every country, maize, sugar, or industrial oil is subsidized — not fruit or vegetables. The state makes what harms you cheaper.

### 1.3 Consequences

- **Double burden of malnutrition:** obesity and undernutrition coexist in the same country — and sometimes in the same household. It is a global phenomenon, present in rich and poor countries alike.
- **Chronic disease:** diabetes, hypertension, and cardiovascular problems, which hit lower-income households hardest.
- **Poverty trap:** eating badly makes you sick, being sick makes you poor, and being poor forces you to eat badly.
- **Loss of food culture:** local dishes and traditional markets lose ground to global chains.

---

## 2. The Solution, Step by Step

The proposal is called **"Eat Well, Close, and Cheap"**: a six-phase program designed to adapt to any country, city, or neighborhood. It does not depend on a specific government, culture, or budget — each phase adjusts to the local context.

### Phase 1 — Local Diagnosis (months 1–3)

1. Map food retail points in each neighborhood: how many sell fresh food and how many sell ultra-processed products.
2. Measure the **price per calorie and per nutrient** of a basic healthy basket versus an ultra-processed basket.
3. Identify the neighborhoods with the highest prevalence of diabetes, obesity, and anemia.
4. Publish the results openly, so the community and the press can see them.

**Output:** a public report with a neighborhood-level food access map.

### Phase 2 — Make What Nourishes Cheaper (months 3–12)

1. **Redirect subsidies:** shift part of the support for industrial crops toward fruits, vegetables, legumes, and small farmers.
2. **Tax sugary drinks and ultra-processed foods**, with the revenue earmarked entirely for the program.
3. **Zero VAT on fresh fruits and vegetables** from local production.
4. **Public procurement** that prioritizes local producers in schools, hospitals, and prisons.

**Output:** a healthy basket with a stable price that competes with ultra-processed food.

### Phase 3 — Shorten the Chain (months 6–18)

1. **Farmers' markets and fairs** in every neighborhood, at least twice a week.
2. **Buying cooperatives** so residents can buy in bulk at farm-gate prices.
3. **Mobile sales points** that bring fresh food to neighborhoods without a market.
4. **Shared logistics** to reduce transport costs for small producers.

**Output:** fresh food available within a 10-minute walk in most neighborhoods.

### Phase 4 — Reclaim Time and Knowledge (months 6–24)

1. **Cooking workshops** in schools, community centers, and workplaces, using local, fast, and affordable recipes.
2. **School cafeterias** serving real food, bought from local producers.
3. **School and community gardens** that teach and also produce.
4. **Accessible recipe books**, in digital and physical formats, with cost per serving.

**Output:** a generation that knows how to cook and recognizes the value of what is local.

### Phase 5 — Regulate the Environment (months 12–36)

1. **Mandatory front-of-package warning labels**, adapted to each country.
2. **Ban on advertising** of ultra-processed foods aimed at children under 12.
3. **Removal of ultra-processed foods** from vending machines and school stores.
4. **Regulation of advertising** in public spaces and on public transport.

**Output:** an environment where healthy food is the visible and easy choice.

### Phase 6 — Measure and Sustain (continuous)

1. **Annual indicators:** relative price of the healthy basket, fruit and vegetable consumption, prevalence of childhood overweight and anemia.
2. **Citizen council** with participation from farmers, nutritionists, students, and retailers.
3. **Protected budget:** the program does not depend on the government of the day.
4. **Open evaluation** and phase adjustment based on results.

**Output:** a system that corrects itself and survives political change.

---

## 3. How to Measure Success

| Indicator | Baseline | 5-Year Target |
|---|---|---|
| Relative price: healthy basket / ultra-processed basket | Greater than 1 | Less than or equal to 1 |
| Daily fruit and vegetable consumption | Low | 50% increase |
| Childhood overweight | High | 20% reduction |
| Childhood anemia | High | 30% reduction |
| Local producers in public procurement | Marginal | At least 40% |
| Food loss and waste | High | 30% reduction |

---

## 4. Why This Works

- **It targets price, not blame.** No one changes their diet if healthy food costs twice as much.
- **It targets availability.** Education is useless if there is nowhere to buy.
- **It targets culture.** It revives cooking knowledge and the value of what is local.
- **It targets the environment.** It regulates the advertising that pushes children toward what harms them.
- **It measures and corrects itself.** Without data, any policy is guesswork.
- **It is replicable.** Each phase adapts to the country, city, or neighborhood where it is applied.

---

## 5. Closing Line

*"It is not a lack of willpower: the cheap food makes you sick and the healthy food costs more. As long as eating well is a privilege, poor nutrition will remain a public policy disguised as a personal choice."*

---

**Suggested license:** Creative Commons BY-SA 4.0, so anyone can adapt the program to their city or country.

# TAM, SAM, SOM: "Eat Well, Close and Cheap"

A market-sizing guide for the six-phase food program, using real numbers for Ecuador and Quito.

## What this is

TAM, SAM, and SOM are a funnel. It narrows from the whole opportunity to the slice you can realistically win.

| Term | Full name | Question it answers |
|---|---|---|
| **TAM** | Total Addressable Market | If everyone who could need this were served, how big is the market? |
| **SAM** | Serviceable Addressable Market | Of that total, how much can my model reach (geography,

"""
TAM / SAM / SOM for "Eat Well, Close and Cheap" (Ecuador -> Quito -> 3 pilot parishes).

Run:  python tam_sam_som.py
No third-party packages needed.

Sizing is in PEOPLE and in the annual FOOD-SPEND POOL those people represent
(not revenue). Edit the INPUTS section to adapt it to another place.
"""

from dataclasses import dataclass

# ----------------------------------------------------------------------
# INPUTS (real figures; sources in comments)
# ----------------------------------------------------------------------

# TAM: all residents of Ecuador. INEC Census 2022 (INEC later adjusted this
# to ~17.7 million for undercount, so this figure is conservative).
ECUADOR_POPULATION = 16_938_986

# SAM: Quito Metropolitan District, INEC Census 2022.
QUITO_POPULATION = 2_679_722

# SOM: illustrative pilot parishes, Census 2022 parish tables (Quito municipality).
# These were picked for size, NOT verified disease burden: confirm in Phase 1.
PILOT_PARISHES = {
    "Calderon": 250_877,
    "Guamani": 99_998,
    "Chillogallo": 68_496,
}

# Food spending: INEC Canasta Familiar Basica, July 2026, national.
# Food and drinks = USD 355.27/month for a reference household of 4 people.
FOOD_SPEND_PER_HOUSEHOLD_MONTH = 355.27
PEOPLE_PER_REFERENCE_HOUSEHOLD = 4

# Health context for the TAM (ENSANUT surveys), for reporting only.
HEALTH_BURDEN = {
    "Adults overweight or obese (ENSANUT 2011-13)": "about 63%",
    "Under-5 chronic malnutrition (ENSANUT 2018)": "23%",
    "Preschool anemia (ENSANUT 2012)": "about 1 in 4",
}


# ----------------------------------------------------------------------
# MODEL
# ----------------------------------------------------------------------

@dataclass
class Level:
    name: str
    label: str
    people: int
    annual_food_spend_usd: float


def annual_food_spend_per_person() -> float:
    monthly = FOOD_SPEND_PER_HOUSEHOLD_MONTH / PEOPLE_PER_REFERENCE_HOUSEHOLD
    return monthly * 12


def build_funnel() -> list[Level]:
    per_person = annual_food_spend_per_person()
    som_people = sum(PILOT_PARISHES.values())

    levels = [
        Level("TAM", "Ecuador, all residents", ECUADOR_POPULATION, 0.0),
        Level("SAM", "Quito Metropolitan District", QUITO_POPULATION, 0.0),
        Level("SOM", "3 pilot parishes", som_people, 0.0),
    ]
    for lv in levels:
        lv.annual_food_spend_usd = lv.people * per_person

    assert levels[2].people <= levels[1].people <= levels[0].people, (
        "Funnel must narrow: SOM <= SAM <= TAM"
    )
    return levels


# ----------------------------------------------------------------------
# REPORT
# ----------------------------------------------------------------------

def money(x: float) -> str:
    if x >= 1e9:
        return f"${x / 1e9:,.2f} B"
    return f"${x / 1e6:,.0f} M"


def main() -> None:
    tam, sam, som = build_funnel()
    per_person = annual_food_spend_per_person()

    print("TAM / SAM / SOM: Eat Well, Close and Cheap")
    print("=" * 74)
    print(f"Food spend per person: ${per_person:,.2f}/year "
          f"(${per_person / 12:,.2f}/month, INEC basket, national average)\n")

    header = f"{'Level':<5} {'Scope':<30} {'People':>12} {'% of TAM':>9} {'% of prev':>10} {'Food pool/yr':>13}"
    print(header)
    print("-" * len(header))

    prev = None
    for lv in (tam, sam, som):
        pct_tam = lv.people / tam.people * 100
        pct_prev = "" if prev is None else f"{lv.people / prev.people * 100:.1f}%"
        print(f"{lv.name:<5} {lv.label:<30} {lv.people:>12,} {pct_tam:>8.1f}% "
              f"{pct_prev:>10} {money(lv.annual_food_spend_usd):>13}")
        prev = lv

    print("\nSOM breakdown (illustrative parishes):")
    for parish, pop in PILOT_PARISHES.items():
        print(f"  {parish:<12} {pop:>9,}  ({pop / som.people * 100:.1f}% of SOM)")

    print("\nHealth burden in the TAM:")
    for k, v in HEALTH_BURDEN.items():
        print(f"  {k}: {v}")

    print("\nNotes:")
    print("  - Food pool = people x national average food spend. It is the money")
    print("    these people already spend on food, not program revenue.")
    print("  - Quito-specific food spend would be more precise; the national")
    print("    average is used because the Quito food component was not found.")
    print("  - Pilot parishes are illustrative: validate them in Phase 1.")


if __name__ == "__main__":
    main()
