# Product Decisions

This project began as a sales prediction exercise.

The stated objective was to estimate future sales for each product at each store location.  
But while working through the data, a practical issue appeared — store teams don’t act on a prediction number itself.

They act on planning questions:
- How much inventory should we allocate?
- Which items should we prioritise per store?
- Which factors actually influence performance?

So the goal shifted from predicting sales to supporting planning decisions using the prediction.

---

## What problem does this actually solve?

The original question:
> What will the sales value be?

The operational question:
> What should we prepare for?

A forecast only becomes useful when it changes stocking or assortment behaviour.  
The product therefore focuses on understanding *drivers of demand* alongside estimating it.

---

## Who would use this?

Store planners and category managers.

Their workflow:
1. Estimate demand for an item
2. Understand why demand differs across stores
3. Adjust stocking decisions

They don’t need model internals — they need confidence in planning.

---

## Why not optimise only for model accuracy?

A slightly better prediction does not necessarily improve decisions.  
Planning improves when uncertainty and influencing factors are visible.

So the system highlights relationships such as:
- store size and demand capacity
- product visibility and sales performance
- category behaviour across locations

Accuracy matters, but explainability matters more for adoption.

---

## Why include product and store attributes?

A single predicted number cannot explain variation between stores.

By connecting predictions with attributes, users can reason about:
- whether demand is transferable
- whether performance depends on store conditions
- whether the issue is supply or placement

This turns forecasting into planning support.

---

## What would ship first?

First version:
- estimate product demand per store
- show main influencing factors
- allow comparison across stores

No automatic ordering recommendations yet.

---

## What would come later?

Later versions could:
- suggest order quantities
- highlight stocking risks
- simulate allocation changes

But only after users trust the forecast behaviour.

---

## Guiding idea

A forecast is useful only when it informs preparation.

The goal is not predicting sales — the goal is reducing planning uncertainty.
