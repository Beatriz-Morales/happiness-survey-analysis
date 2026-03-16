# 😊 Somerville Happiness Survey — Regression & Classification

**Course:** MBA Business Data Analytics — Final Exam Appendix  
**Tools:** R · lm() · glm() · pROC · ggplot2 · confusion matrix  
**Dataset:** Somerville Happiness Survey (neighborhood satisfaction, safety, years of residence)

---

## Business Problem

Two related questions: (1) Can neighborhood quality and length of residence predict a resident's overall happiness? (2) Can safety and neighborhood satisfaction predict whether a resident reports *high* life satisfaction?

---

## Analysis 1 — Multiple Linear Regression

**Target:** `HappyNow` (overall happiness, continuous scale)  
**Predictors:** `NbrHoodSatisfaction`, `YearsResidence`

- Cleaned missing values, renamed variables for readability
- Fit `lm()` and interpreted coefficient direction and magnitude
- Ran full residual diagnostics: Residuals vs Fitted, Normal Q-Q, Scale-Location, Cook's Distance

**Finding:** Neighborhood satisfaction is a positive, significant predictor of overall happiness. Years of residence showed a smaller effect, with results discussed in the written report.

---

## Analysis 2 — Logistic Regression (Classification)

**Target:** `high_life_satisfaction` (binary: 1 if `GeneralLifeSatisfaction` ≥ 8)  
**Predictors:** `SafeWalkingatNight`, `NbrHoodSatisfaction`

- Created binary outcome using `ifelse()` threshold
- Fit `glm(..., family = binomial)`
- Generated predicted probabilities and classified at 0.5 threshold
- Evaluated with confusion matrix (accuracy) and ROC-AUC curve via `pROC`

**Confusion Matrix Visualization:** Built heatmap with `ggplot2` `geom_tile()` for presentation-ready output.

---

## Key Finding

Both neighborhood quality factors — perceived safety and satisfaction with the neighborhood — are significant predictors of high life satisfaction. This has implications for urban planning and community investment decisions: improving perceived safety may yield measurable happiness dividends.

---

## Files

| File | Description |
|---|---|
| `Final_Exam_Appendix_BMorales.Rmd` | Full regression and classification notebook |

---

## Skills Demonstrated

`lm()` · `glm(family = binomial)` · Binary outcome engineering · Confusion matrix · ROC-AUC · `pROC` · `ggplot2` geom_tile · Residual diagnostics · Logistic probability prediction
