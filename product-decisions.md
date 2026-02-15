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


---

## 2. Accuracy vs Interpretability

### Option A: Complex high-accuracy model
- Better predictive performance
- Harder to explain
- Low user trust

### Option B: Interpretable model with clear signals
- Slightly lower accuracy
- Actionable insights
- Higher adoption

### Decision
Chose interpretability over marginal accuracy improvement.

### Rationale
Retail adoption depends more on *trust* than *numerical precision*.

A 2% accuracy gain does not matter if the user ignores the output.

---

## 3. Designing the Output Layer

### Problem
Raw predictions are not operationally useful.

### Decision
Introduce a **signal extraction layer** between prediction and UI.

Instead of:
> Predicted Sales = 2100

We extract:
- Visibility impact
- Store-type effect
- Category performance
- Outlet sensitivity

### Outcome
Outputs translate into decisions instead of metrics.

---

## 4. Handling Multi-Factor Influence

Retail performance is influenced by interacting variables:

- Outlet size
- Location tier
- Item visibility
- Category mix
- Pricing band

### Rejected Approach
Provide feature importance charts.

Why rejected:
Managers cannot operationalize statistical importance.

### Chosen Approach
Convert model relationships into statements:

> Increasing visibility likely improves sales in small outlets  
> Category mix matters more than price in mid-tier locations

---

## 5. Separating Prediction and Recommendation

A key design decision was preventing the model from directly prescribing actions.

### Why
Automated prescriptions reduce trust.

Users need to feel in control of decisions.

### Implementation
System provides:
- confidence-backed signals
- not automatic instructions

Human makes the final call.

---

## 6. Handling Uncertainty

### Problem
Retail environments are noisy and variable.

If the system appears overly certain, trust collapses after a few failures.

### Decision
Design outputs to imply confidence, not certainty.

Avoid:
> “This will increase sales”

Prefer:
> “This is likely influencing performance”

---

## 7. Why Not a Dashboard?

Dashboards answer retrospective questions:
> What happened?

Retail operations need prospective support:
> What should I do next?

RetailSense is intentionally designed as a decision assistant, not a reporting interface.

---

## 8. Product Success Criteria

The system is successful if:

1. Users understand *why* a store performs differently
2. Users change merchandising behavior
3. Users return to the tool for future decisions

Not if:
- R² improves by 0.03
- Model benchmarks improve

---

## 9. Future Product Extensions

If implemented in production:

- scenario simulation (what-if analysis)
- planner feedback learning loop
- store-specific recommendations
- inventory integration

---

## Final Takeaway

The hardest problem was not predicting sales.

It was designing outputs that a human operator could trust enough to act upon.

RetailSense treats machine learning as a supporting component of a decision system, not the product itself.

