# Product Decisions — RetailSense

This document explains the reasoning behind the product design choices made while building RetailSense.

The goal of the system was not to maximize model accuracy, but to create a decision-support tool that retail operators would actually trust and use.

---

## 1. Framing the Product Problem

### Initial Approach (Rejected)
Build a sales prediction model that forecasts outlet sales.

### Why This Fails
Prediction alone does not help retail operators.

A store manager cannot act on:
> “Expected sales = 2,183 units”

They need to know:
> “What should I change in the store?”

### Final Product Direction
Shift from **prediction product** → **decision-support product**

The model becomes an intermediate layer, not the output.
