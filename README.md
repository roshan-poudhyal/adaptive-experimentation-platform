# Adaptive Experimentation Platform for Feature Rollouts

> Product-first, statistically rigorous experimentation system inspired by FAANG-style decision platforms

---

## 🚀 Overview

This project implements a **production-style adaptive experimentation platform** used to evaluate product feature rollouts under real-world constraints.

The system simulates user behavior, runs controlled A/B experiments, applies statistical validation, enforces guardrails, supports early stopping, and analyzes **heterogeneous treatment effects (HTE)** across user segments.  
An interactive **Streamlit dashboard** enables real-time exploration of experiment trade-offs.

---

## 🎯 Problem Statement

In large-scale products, feature rollouts must balance:

- Performance improvements  
- User experience safety (latency, errors)  
- Statistical confidence  
- Experimentation cost and duration  
- Fairness across different user segments  

Simple A/B tests using averages are often insufficient and can mask **segment-level regressions**.

This platform addresses those challenges using **adaptive experimentation techniques**.

---

## 🧠 Key Features

### ✅ Experiment Simulation
- User-level sticky assignment (Control vs Treatment)
- Multi-day experiment execution
- Configurable number of users, days, and randomness

### ✅ Metrics
- **Primary metric:** Task completion time  
- **Secondary metrics:** Acceptance rate, latency, error rate  

### ✅ Statistical Validation
- Bootstrap confidence intervals (95%)
- Distribution-free, robust inference
- Reproducible results via controlled random seeds

### ✅ Early Stopping (Sequential Testing)
- Automatically detects strong evidence
- Stops experiments early to reduce cost
- Recommends optimal stop day

### ✅ Guardrail Enforcement
- Latency and error-rate thresholds
- Prevents unsafe rollouts even if performance improves

### ✅ Heterogeneous Treatment Effects (HTE)
- Segment users by engagement level
- Analyze treatment impact per segment
- Detect hidden regressions masked by averages
- FAANG-style fairness and safety analysis

### ✅ Interactive Dashboard (Streamlit)
- Real-time parameter tuning
- Visual experiment monitoring
- Segment-wise comparisons
- Demo-ready UI

---

## 🏗️ Architecture

adaptive-experimentation-platform/
│
├── data_simulation/ # User & session simulation

├── experiment_design/ # Variant assignment logic

├── metrics/ # Metric computation

├── stats_engine/ # Bootstrap CI & sequential tests

├── decision_engine/ # Rollout decision logic

├── analysis/ # HTE segmentation & analysis

├── dashboard/ # Streamlit app

├── report/ # Experiment report

├── run_experiment.py # Main experiment runner

└── README.md

---

## 📊 Dashboard Preview

The Streamlit dashboard allows you to:
- Adjust experiment duration and traffic
- Modify guardrail thresholds
- Observe metric trends over time
- Inspect segment-wise effects visually

This mirrors internal experimentation tools used at companies like **Microsoft, Google, and Meta**.

---

