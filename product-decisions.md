# Product Decisions

This project started as a sales prediction task.

While working through the dataset, the limitation became clear — predicting a number does not help a store manager decide what to change in the store.

Stores operate under constraints:
limited shelf space, limited promotions, limited inventory.

So the goal shifted from forecasting sales to supporting merchandising decisions.

---

## What problem does this actually solve?

The original question:
> How much will a product sell?

The practical question:
> What should the store do differently?

A prediction alone does not tell whether to:
- increase stock
- change placement
- promote the item
- replace the product

The product therefore focuses on explaining performance, not only estimating it.

---

## Who would use this?

Store managers and merchandising teams.

Their workflow:
1. Look at product performance
2. Compare across stores or categories
3. Decide an action

They need guidance, not just accuracy.

---

## Why not optimise purely for prediction accuracy?

A highly accurate model still leaves decisions unclear.  
Two products can have similar predicted sales but require opposite actions.

Instead, the system highlights performance drivers:
- visibility
- store type
- pricing sensitivity
- category behaviour

This allows human judgement.

---

## Why focus on drivers instead of rankings?

Ranking products only answers:
> which items perform better

Understanding drivers answers:
> what can be improved

This turns the tool from reporting into decision support.

---

## What would ship first?

First version:
- explain product performance
- compare stores
- identify improvement opportunities

No automatic stocking recommendations yet.

---

## What would come later?

Later versions could:
- suggest inventory levels
- recommend placement changes
- simulate promotion impact

But only after teams understand why products behave differently.

---

## Guiding idea

Retail decisions are constrained decisions. And hence, before automating stocking, teams must understand what influences demand.
