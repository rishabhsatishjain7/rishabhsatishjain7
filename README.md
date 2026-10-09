# 👋 Hi, I'm Rishabh Satish Jain

Recent graduate with a B.Tech in Information Technology from **Vellore Institute of Technology** (May 2026). I build backend systems and data pipelines that turn messy, real-world data into something you can trust and act on, with a focus on concurrency-safe services, event-driven architecture, and applied machine learning.

**Tech:** Java · Python · SQL · Spring Boot · FastAPI · Redis · Kafka · Docker · Kubernetes (k3s) · Terraform · AWS · GitHub Actions · Airflow · XGBoost · SHAP

---

## 🚀 Featured Projects

### 🛡️ [SafeGate: Concurrency-Safe Purchase Gateway](https://github.com/rishabhsatishjain7/SafeGate)
`Java` `Spring Boot` `Redis` `Docker` `GitHub Actions` `Prometheus` `Grafana`

A Spring Boot purchase API that stays correct under traffic spikes. It combines Redis token-bucket rate limiting with pessimistic and optimistic locking to prevent overselling.

- Proven by deterministic multi-threaded invariant tests.
- Load-tested with 10 concurrent clients (16 workers, 50-slot queue): exactly 5 of 10 purchases accepted for 5 units of stock, **0 oversells**.
- Instrumented with Micrometer, Prometheus, and Grafana; fixed a never-incremented rejection counter that hid rejected purchases from operators.
- GitHub Actions CI with JaCoCo: **75.5%** instruction coverage across unit, integration, and concurrency tests.

🔗 **Repository:** https://github.com/rishabhsatishjain7/SafeGate

---

### 📦 [Aetherline: Distributed Order Processing Platform](https://github.com/rishabhsatishjain7/Aetherline)
`Python` `Kafka` `Kubernetes` `Terraform` `AWS` `GitHub Actions`

A proof-of-concept 5-service event-driven platform on Kafka. It uses the transactional outbox pattern and idempotent consumers for effectively-once processing, so no order or payment event is lost or duplicated.

- Eliminated a concurrent-idempotency race across replicated consumers by replacing check-then-act deduplication with atomic claim-row inserts on unique constraints; verified with multi-threaded race tests.
- Provisioned AWS with Terraform and an OIDC-authenticated GitHub Actions pipeline; cut infrastructure cost by about **70%** by choosing k3s on EC2 over EKS.
- Redesigned the API gateway to **fail closed** (failures block requests, never pass them through); validated with a 17-test CI suite.

🔗 **Repository:** https://github.com/rishabhsatishjain7/Aetherline

---

### 📈 [FinSight: Financial Distress Screening Platform](https://github.com/rishabhsatishjain7/FinSight)
`Python` `SQL` `XGBoost` `SHAP` `Airflow` `FastAPI` `PostgreSQL` `Gemini API`

A financial due-diligence pipeline that ingests SEC EDGAR XBRL filings (multi-tag fallback, schema-evolution handling) and computes 30+ financial ratios and sector-relative Z-scores across 14 companies, 4 sectors, and 7 years. New companies need only a config entry.

- XGBoost distress classifier with SHAP explainability and label-leakage guards.
- Gemini analyst narratives grounded in computed facts (RAG) and automated PDF reports with SHAP and ratio-trend charts.
- Two Airflow DAGs (daily pipeline, weekly retrain), results stored in SQLite/PostgreSQL, and a read-only FastAPI dashboard with risk badges, SHAP drivers, and PDF downloads.
- **89 automated tests**, including a 12-thread concurrent-write test; 12 defects documented with root cause, fix, and regression test.

🔗 **Repository:** https://github.com/rishabhsatishjain7/FinSight

---

## 📫 Get in Touch

- 📧 Email: [rishisjain0205@gmail.com](mailto:rishisjain0205@gmail.com)
- 💼 LinkedIn: [rishabh-satish-jain-94113b267](https://www.linkedin.com/in/rishabh-satish-jain-94113b267)
- 🐙 GitHub: [rishabhsatishjain7](https://github.com/rishabhsatishjain7)
