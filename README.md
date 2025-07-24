# SLOGuardian
Combining Go (for CRD/controller logic) and Python (for ML inference and observability handling) in a real-world hybrid Kubernetes system.

# 🔍 SLOGuardian

> A Kubernetes-native SLO forecasting and enforcement controller powered by machine learning.

**SLOGuardian** is a custom Kubernetes controller that allows platform teams and SREs to define, monitor, and enforce SLOs using predictive analytics. It integrates with Prometheus and a Python-based inference engine to proactively detect SLO breaches before they occur, enabling smarter alerting and auto-scaling strategies.

---

## 🚀 Features

- 📦 **Custom Resource Definition (CRD)** for defining SLOs
- 🧠 **ML-based Forecasting** engine (Python + FastAPI)
- 📊 **Prometheus Integration** for real-time metric scraping
- 🔁 **Kubernetes Controller (Go)** that evaluates SLO states
- ⚠️ **Action Engine** to emit alerts, patch status, and enable auto-scaling
- 📡 Modular architecture (Go controller + Python microservice)

---
## 🛠️ How It Works

1. User creates a `SLOGuardian` Custom Resource (CR) describing an SLO and model config.
2. Go-based controller watches for CR changes.
3. Controller calls the Python inference engine with metric and model details.
4. Inference engine queries Prometheus, forecasts risk, and returns an action.
5. Controller applies the decision (e.g., alert, scale, patch status).

---

## 🧪 Example Use Cases

- Proactively alerting on future SLO breaches
- Detecting anomalous traffic patterns
- Enabling smart auto-scaling with predictive models
- ML-governed observability workflows for SRE teams

---

## 💬 Roadmap

- [x] CRD Definition and Go Controller Scaffolding
- [ ] Python Inference Engine with dummy model
- [ ] Integration with Prometheus
- [ ] Real-time forecasting (Prophet or LSTM)
- [ ] Grafana dashboards for prediction/actuals
- [ ] Helm chart for deployment
