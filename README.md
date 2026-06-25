<h1 align="left">Hi, I'm Muhammad Umer Riaz 👋</h1>
<img src="https://komarev.com/ghpvc/?username=Muhammad-Umer-Riaz&style=flat-square&color=green&base=1000" alt="Profile Views"/>
<p align="left">
  <a href="https://www.linkedin.com/in/muhammad-umer-riaz"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:muhammad.umer2149@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

<table>
<tr>
<td valign="top" width="62%">

[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=Industrial+Engineer;Data+%26+AI+Enthusiast;MSc+IEM+%40+Tampere+University&font=Fira+Code&size=22&width=500&height=42&color=36BCF7&pause=1000&center=false)](https://git.io/typing-svg)

Industrial engineer working at the intersection of business, data, and AI. My background is in operational environments, where the impact of decisions is quickly visible. I build systems with the same approach and apply AI to real-world operational problems.

- 🏭 Lean Six Sigma · operations · production systems
- 🏗️ End-to-end data engineering on MS Fabric — medallion to Power BI
- 🤖 Two AI systems on AWS — schema-driven report engine & agentic RAG
- 📊 Data analytics portfolio across supply chain, retail, and SaaS
- 🎓 MSc thesis at Beneq — Systematic AI adoption in organisations
- 📍 Based in Tampere, Finland

</td>
<td valign="top" width="38%" align="center">
<br/>
<img src="https://media1.giphy.com/media/gXr3j6YAClXFfZABn5/giphy.gif" width="300"/>
</td>
</tr>
</table>

---

## 🤖 AI Engineering

### [Provenance — Schema-Driven Report Generation](https://github.com/Muhammad-Umer-Riaz/Provenance) — *[Live demo](https://d4q93waqw2e37.cloudfront.net)*

<p align="center">
  <img src="https://raw.githubusercontent.com/Muhammad-Umer-Riaz/Provenance/master/docs/images/screenshots/Template%20Page.png" width="100%" alt="Provenance — Templates page"/>
</p>

A field-level report generation engine. A YAML template declares every field's generation strategy — lookup, extractor, calculator, template-fill, direct-input, classifier, narrative-LLM, grounded-LLM, or hybrid — and an orchestrator routes each field to its handler. Deterministic strategies never call an LLM; narrative paragraphs do, but every draft surfaces in a three-pane review UI where the engineer edits and approves field-by-field before export. An append-only audit log records every state transition.

Built with FastAPI · React · TypeScript · Supabase (Postgres · Auth · Realtime · RLS) · OpenRouter · YAML · AWS (S3 · CloudFront · EC2)

Featured template: 47-field Supplier Qualification Report — classifier-gated verdict flow, lookup-driven risk disclosure, narrative-LLM executive summary, end-to-end DOCX/PDF/JSON export.

<br/>

### [Agentic RAG Chat](https://github.com/Muhammad-Umer-Riaz/Agentic-RAG-Chat) — *Live demo currently offline*

<p align="center">
  <img src="https://raw.githubusercontent.com/Muhammad-Umer-Riaz/Agentic-RAG-Chat/master/docs/screenshots/chat-thought-process.png" width="100%" alt="Agentic RAG Chat — agent thought process"/>
</p>

A multi-format document intelligence system. Upload PDF, DOCX, XLSX, PPTX, or images and chat with them via an agentic loop that routes each query to the right tool: hybrid vector search, Text-to-SQL for spreadsheets, web search for external knowledge, or an isolated sub-agent for full-document analysis.

Built with FastAPI · Supabase · pgvector · React · OpenRouter · Cohere · LangSmith · Docker · AWS EC2

Eval results (63 test cases, 6 prompt versions): Retrieval Hit@5 = 1.00 · Grounding = 3.42/5 · Agent task completion = 96%

---

## 🏗️ Data Engineering

### [Procurement Intelligence — End-to-End Microsoft Fabric](https://github.com/Muhammad-Umer-Riaz/Procurement_Intelligence_E2E_Microsoft_Fabric) — *EuroVac Systems GmbH supply chain platform*

<p align="center">
  <img src="https://raw.githubusercontent.com/Muhammad-Umer-Riaz/Procurement_Intelligence_E2E_Microsoft_Fabric/e604fdfc3bef172a875f62922efcbff28c710355/figures/architecture_diagram.png" width="100%" alt="Architecture diagram"/>
</p>

An end-to-end Microsoft Fabric data engineering project for a fictional Munich-based ALD/CVD semiconductor equipment manufacturer. A synthetic 11-table SAP-style ERP and three live external APIs (FRED commodity prices, NY Fed GSCPI, Frankfurter FX) flow through Bronze → Silver → Gold medallion architecture into a star schema, a Direct Lake semantic model with 19 DAX measures, and a 5-page Power BI report. A scikit-learn lead time classifier reads from Silver, logs to MLflow, and writes its predictions back to the Warehouse as a first-class fact table — joined into the same semantic model the dashboard consumes. Two Fabric Data Pipelines orchestrate the platform end-to-end.

Built with Microsoft Fabric (Lakehouse · Warehouse · Pipelines) · PySpark · Delta Lake · T-SQL · Power BI (DAX) · scikit-learn · MLflow · Python

  <table align="center">
  <tr>
  <th align="center" valign="middle">Results</th>
  <td align="center"><b>$67bn</b><br/><sub>PO value</sub></td>
  <td align="center"><b>$4.12bn</b><br/><sub>Savings</sub></td>
  <td align="center"><b>498K</b><br/><sub>PO lines</sub></td>
  <td align="center"><b>82.7%</b><br/><sub>On-time delivery</sub></td>
  <td align="center"><b>AUC 0.757</b><br/><sub>2025 hold-out</sub></td>
  <td align="center"><b>~20 min</b><br/><sub>weekly Bronze → Gold refresh on F2 trial</sub></td>
  </tr>
  </table>

<br/>

### [Olist Analytics Engineering Warehouse](https://github.com/Muhammad-Umer-Riaz/Olist_Analytics_Engineering_Warehouse) — *End-to-end ELT on E-Commerce data*

<p align="center">
  <img src="https://raw.githubusercontent.com/Muhammad-Umer-Riaz/Olist_Analytics_Engineering_Warehouse/master/figures/olist-architecture-blueprint.png" width="100%" alt="Olist warehouse architecture"/>
</p>

An end-to-end analytics-engineering warehouse on the real Olist Brazilian e-commerce dataset — nine relational tables, ~100K orders, 2016–2018. **dlt** extract-and-loads the source CSVs and a live FX API into Snowflake; **dbt Core** transforms `RAW → STAGING → INTERMEDIATE → MARTS` into a two-fact star schema with a two-layer customer grain, role-playing dates, and conformed geography. Data quality is enforced with 52 tests and an auditable rejects table. **Airflow** (Astro Runtime + Cosmos) orchestrates the whole pipeline as one DAG with model-level lineage; dlt loads, Airflow never does. The four-page **Power BI** report is authored entirely as code in the `.pbip` text format (TMDL + PBIR).

Built with dlt · Snowflake · dbt Core · Airflow (Astro Runtime · Cosmos) · Power BI (.pbip · TMDL · PBIR · DAX) · Python

  <table align="center">
  <tr>
  <th align="center" valign="middle">Results</th>
  <td align="center"><b>R$15.8M</b><br/><sub>Revenue</sub></td>
  <td align="center"><b>99,441</b><br/><sub>Orders</sub></td>
  <td align="center"><b>112,650</b><br/><sub>Order items</sub></td>
  <td align="center"><b>92.1%</b><br/><sub>On-time delivery</sub></td>
  <td align="center"><b>52</b><br/><sub>dbt tests (49 ✓ · 3 ⚠)</sub></td>
  <td align="center"><b>3m 35s</b><br/><sub>end-to-end DAG run</sub></td>
  </tr>
  </table>

---

## 📊 Data Analytics

Four end-to-end projects, each starting from a real business problem:

| # | Project | Key Result |
|---|---------|-----------|
| 01 | [Recovering Lost Sales: ASOS Stockout & Brand Strategy](https://github.com/Muhammad-Umer-Riaz/data-analyst-portfolio/tree/main/Recovering_Lost_Sales_ASOS_Stockout_Brand_Strategy) | Mid-priced brands carry highest unmet demand; priority restocking targets identified |
| 02 | [Supplier Risk & Procurement Cost Analysis](https://github.com/Muhammad-Umer-Riaz/data-analyst-portfolio/tree/main/Supplier_Risk_Procurement_Cost_Analysis) | $20.99M in delayed procurement spend quantified; 17 vendors flagged for escalation |
| 03 | [Customer Retention Intelligence: Telecom Churn Study](https://github.com/Muhammad-Umer-Riaz/data-analyst-portfolio/tree/main/Customer_Retention_Intelligence_Telecom_Churn_Study) | Model catches 76.5% of churners before they leave |
| 04 | [Supply Chain Performance Dashboard](https://github.com/Muhammad-Umer-Riaz/data-analyst-portfolio/tree/main/Supply_Chain_Performance_Dashboard) | 59.1% late delivery rate uncovered; First Class shipping has 0% on-time rate |

→ [View full portfolio](https://github.com/Muhammad-Umer-Riaz/data-analyst-portfolio)

---

## 🛠 Technical Skills

<table>
<tr>
<td valign="top" width="34%">

**Data & Analytics**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![T-SQL](https://img.shields.io/badge/T--SQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![numpy](https://img.shields.io/badge/numpy-013243?style=flat-square&logo=numpy&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=flat-square&logo=databricks&logoColor=white)
![dlt](https://img.shields.io/badge/dlt-FF6E42?style=flat-square&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Medallion Architecture](https://img.shields.io/badge/Medallion%20Architecture-1E3A8A?style=flat-square&logoColor=white)
![Star Schema](https://img.shields.io/badge/Star%20Schema-2D6A4F?style=flat-square&logoColor=white)
![Analytics Engineering](https://img.shields.io/badge/Analytics%20Engineering-0B4F6C?style=flat-square&logoColor=white)
![ELT](https://img.shields.io/badge/ELT-3D348B?style=flat-square&logoColor=white)
![matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=flat-square&logo=python&logoColor=white)
![seaborn](https://img.shields.io/badge/seaborn-4C72B0?style=flat-square&logo=python&logoColor=white)

</td>
<td valign="top" width="33%">

**AI Engineering**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=black)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-6E40C9?style=flat-square&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![LangChain](https://img.shields.io/badge/LangSmith-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-CB171E?style=flat-square&logo=yaml&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt%20Engineering-FF6B6B?style=flat-square&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-25D366?style=flat-square&logoColor=white)

</td>
<td valign="top" width="33%">

**Operations & Process**

![Lean Six Sigma](https://img.shields.io/badge/Lean%20Six%20Sigma-00853F?style=flat-square&logoColor=white)
![Root Cause Analysis](https://img.shields.io/badge/Root%20Cause%20Analysis-E63946?style=flat-square&logoColor=white)
![OEE](https://img.shields.io/badge/Overall%20Equipment%20Efficiency-FF6B35?style=flat-square&logoColor=white)
![Value Stream Mapping](https://img.shields.io/badge/Value%20Stream%20Mapping-F4A261?style=flat-square&logoColor=white)
![5S](https://img.shields.io/badge/5S-1D3557?style=flat-square&logoColor=white)
![Kanban](https://img.shields.io/badge/Kanban-0096C7?style=flat-square&logoColor=white)
![Just-in-Time](https://img.shields.io/badge/Just--in--Time-D62828?style=flat-square&logoColor=white)
![Layout Planning](https://img.shields.io/badge/Layout%20Planning-6A4C93?style=flat-square&logoColor=white)
![Process Mining](https://img.shields.io/badge/Process%20Mining%20-00B4D8?style=flat-square&logoColor=white)
![ERP](https://img.shields.io/badge/ERP%20Systems-0052CC?style=flat-square&logoColor=white)
![KPI Dashboards](https://img.shields.io/badge/KPI%20Dashboards-2B9348?style=flat-square&logoColor=white)

</td>
</tr>
</table>

---

## 🎓 Education

<table>
<tr>
<td valign="top" width="50%">

**MSc Business & Technology - IEM**

- 🇫🇮 Tampere University · 2023–2025 · GPA 4.4/5
- Thesis: *Systematic AI Adoption Through Governance Mechanisms* (Grade: 4/5, Very Good)
- Conducted in collaboration with **Beneq Oy** · Funded by the Finnish Technology Industries' Centenary Foundation

</td>
<td valign="top" width="50%">

**BSc Industrial Engineering**
<br/>
- 🇵🇰 University of Engineering & Technology Taxila · 2016–2020 · GPA 3.44/4.0
- Thesis: *Knowledge Integration in Large Scale R&D Projects* (Grade A, Excellent)
- Conducted in collaboration with **Heavy Industries Taxila**

</td>
</tr>
</table>

---

<details>
<summary><b>📜 &nbsp;Certifications</b> &nbsp;(click to expand)</summary>

<br/>

- Microsoft Certified: Data Analyst Associate (Power BI) — Microsoft
- How Transformer LLMs Work — DeepLearning.AI
- Developing AI Systems with the OpenAI API — DataCamp
- Prompt Engineering with OpenAI API — DataCamp
- Supervised Learning with scikit-learn — DataCamp
- Lean Six Sigma Green Belt — Coursera
- Supply Chain Management Specialization — Coursera
- Process Mining with Celonis — Udemy

</details>

---

## 📬 Connect

[LinkedIn](https://www.linkedin.com/in/muhammad-umer-riaz)  
muhammad.umer2149@gmail.com

---
***Thanks for Visiting my Profile***
