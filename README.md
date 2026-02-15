# 🛒 Retail Demand Planning Assistant
### Using sales forecasts to support stocking decisions

Forecasting sales is only useful if it changes what a store prepares for.

This project explores how product and store data can help retail teams plan inventory and assortment decisions with more confidence.

---

## The Problem

Retail stores must decide how much of each product to stock before knowing actual demand.

Teams often rely on past averages or intuition, which leads to:
- overstocking slow items
- stockouts of popular items
- inconsistent performance across stores

A prediction number alone does not solve this —  
teams need to understand *why demand differs*.

---

## Goal

Build a system that helps planners:

1. Estimate demand for each product per store
2. Understand the factors influencing that demand
3. Reduce uncertainty in stocking decisions

The focus is planning support, not model complexity.

---

## Approach

### 1. Estimate demand

Historical sales data was used to predict expected item sales for each store.

The prediction acts as a baseline expectation — not a final decision.

---

### 2. Connect predictions to store and product attributes

Instead of treating predictions as isolated outputs, the system relates them to:

| Factor | Planning meaning |
|------|------|
| Store size | capacity to sell volume |
| Product visibility | placement effectiveness |
| Category type | purchase frequency |
| Pricing | sensitivity to demand |

This makes forecasts explainable.

---

### 3. Support planning decisions

The output allows planners to reason about:

- whether low sales indicate low demand or poor placement
- whether demand differences are store-specific
- which items need stocking adjustments

---

## Example decisions enabled

| Situation | Possible action |
|------|------|
| High predicted demand in large stores | allocate more inventory |
| Low sales but high visibility impact | reposition product |
| Store-specific demand variation | customise assortment |
| Consistently low predicted demand | reduce stock or replace item |

---

## What this demonstrates

Typical ML projects answer:

> What will sales be?

This project answers:

> How should a store prepare?

The forecast becomes a decision aid, not just a metric.

---

## How to explore

Review the notebook to see how predictions relate to product and store attributes.

Focus on understanding drivers rather than model accuracy.

---

## Repository Contents

- notebook — demand estimation and feature exploration
- data — product and store attributes
- documentation — reasoning behind planning decisions

---
