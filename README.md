# ⛳ CaddieIQ Shot Strategy

## 📘 Project Overview

CaddieIQ is a golf analytics product project that turns shot-level round data into practical course-management decisions.

The project answers questions like:

- Which club creates the best expected outcome from this distance?
- Which miss pattern is costing the most strokes?
- What is the safest target line for the current shot?
- What practice area has the highest scoring upside?

The goal is to move beyond raw golf stats and create a product layer that helps a golfer make better decisions on the course.

---

## 🔍 Product Problem

Golfers often collect performance data, but the output is usually descriptive:

- fairways hit
- greens in regulation
- putts
- average distance
- score history

Those metrics explain what happened, but they do not always explain what decision to make next.

CaddieIQ turns shot history into a decision-support workflow:

```text
round logs + shot pattern analysis + strokes-gained logic → club recommendation + safe miss + practice priority
```

---

## 🧰 Tools and Libraries Used

| Library | Purpose |
|---|---|
| Pandas | Cleaning and analyzing shot-level round logs |
| NumPy | Numerical calculations |
| Matplotlib | Data visualization |
| scikit-learn | Clustering / grouping logic for shot patterns |
| Python | Product logic and recommendation rules |

---

## 📦 Dataset Information

This project uses a sample shot-level round log with fields similar to what could be exported from golf stat-tracking tools.

Example fields:

- club
- carry distance / distance to target
- lie
- miss direction
- penalty outcome
- strokes gained

The notebook includes a generated sample dataset so the project can be opened and understood immediately on GitHub.

---

## 🧠 Methodology

### 1. Shot Data Preparation

Shot-level data is grouped by:

- club
- distance band
- lie
- miss direction
- penalty outcome

### 2. Pattern Analysis

The notebook identifies:

- average strokes gained by club
- most common miss direction
- highest-cost miss pattern
- strongest practice opportunity

### 3. Decision Logic

The product logic recommends:

- club selection
- target line
- safe miss
- risk tradeoff
- practice priority

---

## 🖥️ Product Translation

The product surface is designed around decisions, not just dashboards.

Example output:

```text
Recommended shot: 6i to left-center
Reason: Best risk-adjusted expected value
Safe miss: short-left
Risk flag: right miss creates highest penalty
Practice focus: wedge distance control
```

---

## 🚀 Future Improvements

- Connect real round data from Arccos / Shot Scope / manual scorecards
- Add course-specific hazard mapping
- Add clustering by player tendency
- Add expected strokes model by lie and distance
- Add personalized practice plan generator
- Build full Streamlit product dashboard
