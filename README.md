# Amdocs AI-Powered Self-Healing Network Operations (AIOps)

> An enterprise-ready, predictive AIOps platform designed to shift telecom network operations from reactive firefighting to proactive, automated self-healing. Built for the **Amdocs AI-Enabled Intelligent Connectivity** challenge.

---

## Table of Contents
- [Overview](#-overview)
- [System Architecture & Tiered Logic](#-system-architecture--tiered-logic)
- [Key Performance Metrics](#-key-performance-metrics)
- [Tech Stack & Azure Alignment](#-tech-stack--azure-alignment)
- [Repository Structure](#-repository-structure)
- [Live Demo & Quickstart](#-live-demo--quickstart)

---

## Overview
Traditional Network Operations Centers (NOCs) suffer from severe alarm fatigue and reactive break-fix cycles, addressing faults only *after* service disruption occurs. 

This project delivers a closed-loop **Self-Healing Network Operations Platform** that:
1. **Detects** live anomalies instantly using real-time telemetry.
2. **Predicts** network failures **one hour before customer impact** using advanced temporal forecasting.
3. **Monitors** fleet health via a color-coded NOC dashboard categorized into Critical, Warning, and Healthy tiers.
4. **Automates** remediation via webhooks that dispatch self-healing playbooks and IT ticketing payloads (Jira/ServiceNow).

---

## System Architecture & Tiered Logic
The platform uses a **Tiered Escalation Engine** to balance early warning capabilities with low false-alarm noise:

* **Tier 1: Diagnostic Layer ($t$ - Random Forest)**
  * Evaluates instantaneous telemetry to catch active anomalies on the spot.
* **Tier 2: Prognostic Layer ($t+1$ - Histogram-Based Gradient Boosting)**
  * Forecasts failure risk 1 hour ahead using non-linear trajectory modeling.
* **Advanced Temporal Feature Engineering:**
  * Extracts rolling volatilities, acceleration, lags, and operational friction from raw hourly telemetry streams to track how fast network nodes degrade.
* **Explainability (SHAP):**
  * Automatically generates local root-cause attributions so engineers understand *why* a node is failing (e.g., congestion vs. latency spikes).

---

## Key Performance Metrics
Validated across multi-station historical node streams (1,885 operational snapshots):
* ** 94.8% Recall (37/39 Failures Intercepted):** Successfully catches impending outages with a 60-minute proactive runway.
* ** 43.02% Precision:** Massively suppresses legacy false-alarm noise, ensuring NOC engineers only act on genuine high-risk precursors.
* ** Zero-Lag Routing:** Instant node triaging into `🔴 CRITICAL`, `⚠️ WARNING`, and `🟢 HEALTHY` operational statuses.

---

## 🛠️ Tech Stack & Azure Alignment
Built with high-performance open-source tools and fully architected for enterprise cloud deployment:

* **Core Data & ML:** Python, Pandas, NumPy, Scikit-learn (Random Forest, HGBR).
* **Explainability:** SHAP (SHapley Additive exPlanations).
* **Dashboarding & Viz:** Power BI integration.
* **Automation Layer:
* **Enterprise Cloud Mapping:

---

## Live Demo & Quick start
```
https://aiops-predictive-network-assurance-dashboard.streamlit.app/
