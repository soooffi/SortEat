![Sorteat](cover.png)

# Sorteat — HCI Project @Polimi & HINT Lab

Human-Computer Interaction project at Politecnico di Milano & HINT Lab, A.Y. 2025/2026
**Final grade: 30/30**

A mobile-first app that turns a shared kitchen into a virtual smart kitchen: one that remembers what's in the fridge, what's about to expire, and who owes whom for the groceries.

**[Try the live prototype →](https://sorteat-high-fidelity.vercel.app/)**

---

## The Problem

Four sentences you have said in your own kitchen this month:

| What people say | What Sorteat does |
|---|---|
| *"I didn't know the milk had gone off."* | Automatic expiry alerts, urgent items surfaced first |
| *"I bought stuff we already had."* | Shared inventory you can check from the supermarket aisle |
| *"I have no idea what to cook with this."* | Recipes ranked by what is already in the house |
| *"Who owes me for the shopping?"* | Automatic balance tracking between flatmates |

Food waste in shared homes is not a knowledge problem. It is a coordination and cognitive-load problem, and that premise drove every design decision here.

One principle governed the whole project:

> Remove every superfluous thought and action from the user: automate repetitive decisions, and surface only the information that matters, at the moment it matters.

Every screen had to justify itself against that sentence.

---

## The Design Process

Four months, five deliverables, one full user-centred design cycle. Nothing here started from a screen — the screens were the last thing we drew.

### 1. Research and problem framing — [`consegna-1`](./consegna-1)

<!-- TODO: correggi con quello che avete fatto davvero -->
We started from the domain, not the solution: desk research on food waste in shared households, competitor analysis of existing pantry and grocery apps, and interviews with people living in flatshares. The output was a problem definition and a set of user needs, which is where the four pain points above come from.

**Key finding:** waste in shared homes is rarely about ignorance. It is about *coordination* — nobody knows what is in the fridge, whose it is, or who paid for it.

### 2. Personas, scenarios and requirements — [`consegna-2`](./consegna-2)

<!-- TODO: correggi -->
Research was turned into personas and scenarios. Mariia, Giorgia and Luca are not decoration: each one carries a different relationship with food, money and the shared space, and each of the three core tasks is anchored to one of them. From the scenarios we derived functional requirements and prioritised them.

### 3. Task analysis and information architecture — [`consegna-3`](./consegna-3)

<!-- TODO: correggi -->
We decomposed the priority tasks step by step, mapped the information architecture, and settled the navigation model — the four sections (Home, Inventory, Recipes, Space) and the two parallel entry points into the inventory.

### 4. Low-fidelity prototype and first evaluation — [`consegna-4`](./consegna-4)

<!-- TODO: correggi -->
Paper and wireframe prototypes, evaluated before writing a single line of code. This is the phase that killed the most ideas: features that looked reasonable on paper turned out to add steps rather than remove them, and were cut against the guiding principle.

### 5. High-fidelity prototype and usability testing — [`consegna-5`](./consegna-5)

<!-- TODO: correggi -->
The working prototype, followed by usability testing with real participants on the three core tasks. Findings were fed back into a final round of changes.

**[Read the usability testing report →](./docs)**
<!-- TODO: sostituisci con il link GitHub Pages -->

---

## Try It Yourself

The prototype is fully interactive. You are logged in as **Mariia**, sharing a flat with **Giorgia** and **Luca**.

**1. "Do I actually need to buy this?"** — *Luca is at the supermarket in front of the milk. Buy it and he might find an open carton at home; skip it and there is no breakfast tomorrow.*
Open **Inventory**, search `latte`. The card shows quantity, an expiry badge, and who owns it. If it belongs to a flatmate it carries a lock and their avatar, and **Ask [name]** turns a potential conflict into a one-tap request.

**2. "What do I cook tonight?"** — *Mariia is at a market staring at porcini mushrooms. She can taste the risotto; she cannot remember if she has Carnaroli rice or parmesan.*
Open **Recipes**, tap *Risotto ai funghi*. Every ingredient is tagged against the real inventory: grey for in stock, orange for expiring soon, red for missing, an avatar for owned by someone else. From there: cook now, drag it into the weekly meal planner, or push the missing items to the shared shopping list.

**3. "I just got back from the shop."** — *Giorgia has eight items to log and zero desire to type.*
In **Inventory**, tap the green **+**. Receipt scan returns a review screen where every field is editable inline — quantity, price, expiry, shared/private ownership. Items added to the inventory disappear from the shopping list automatically.

---

## Key Interaction Decisions

**Ownership as a first-class concept.** Every item is shared or private, with a lock and an owner avatar. This single primitive removes an entire class of household conflict, and makes "ask before you take" one tap instead of an awkward text.

**Expiry as colour, not as a date.** People do not parse dates under time pressure; they parse traffic lights. Urgency uses the same colour language across inventory, recipes and notifications.

**The review step is the product.** Receipt scanning is only worth building if correcting it is faster than typing. Editing is inline, deletion is one tap, and nothing is committed until the user confirms.

---

## Prototype Scope

A high-fidelity prototype built for usability evaluation, not a production app. No backend (mock data in `localStorage`), no authentication (the current user is fixed as Mariia), simulated notifications and receipt OCR, illustrative balance figures.


