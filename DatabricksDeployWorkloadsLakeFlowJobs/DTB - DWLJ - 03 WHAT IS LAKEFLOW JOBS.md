2810250721
**Descrição:** Description of lakeflow jobs in Databricks
**TAG:** #Databricks #COURSE #engineering #LAKEFLOW #JOBS 

# DTB - DWLJ - 03 WHAT IS LAKEFLOW JOBS
---

# ORCHESTRATING WORKLOADS

![[Pasted image 20251028082613.png]]

>This diagram captures a fundamental challenge in modern data architecture: choosing the right orchestration approach for lakehouse workloads. 

The left panel shows multiple options including open source solutions (Apache Airflow, Prefect, Dagster, dbt), cloud-native services (AWS, Azure, Google Cloud), and custom in-house frameworks.

Diagram on right illustrates a typical data workflow with multiple steps:

- Ingesting sessions and clicks data, joining them, performing featurization and aggregation, analysis, and training models.

- Then you have various downstream uses including Bl & Data Warehousing, Data Streaming, and Data Science & ML.

The question mark here represents a critical challenge: there are many ways to orchestrate these workloads, but which approach is best?

---
# EXTERNAL ORCHESTRATORS

>Many organizations use external orchestration tools, but this creates significant challenges. Data teams become less productive because these tools are hard to use for many practitioners. Bad data quality lowers the value of downstream applications.

You also face higher costs of ownership and lower reliability. When issues occur, it's difficult to understand root cause. 

The complex architecture becomes hard to manage and maintain.
Most importantly, these external tools are not unified with your Lakehouse, creating integration challenges and data silos.

# WHAT IS LAKEFLOW JOBS?

![[Pasted image 20251028083511.png]]

>This is where Lakeflow Jobs comes in. It provides unified orchestration for data, analytics, and Al workloads directly on the Data Intelligence Platform. 

The key benefits are simple authoring, actionable insights, and proven reliability. 

>Because it's native to the platform, it integrates seamlessly with data ingestion & transformation, the processing engine (Photon), governance (Unity Catalog), storage (Delta Lake), data warehousing, and machine learning capabilities.

The workflow shown here - from sessions and clicks through join, featurize, aggregate, analyze, and train - all runs natively within the same platform, eliminating the integration challenges of external tools.

# LAKEFLOW JOBS

![[Pasted image 20251028083749.png]]

- This slide shows the complete architecture of Lakeflow Jobs. At the center is the Workflow engine that coordinates everything.

- The compute layer supports various workload types: ETL, ML/AI, and Analytics/Bl operations.

- You have multiple trigger types: Scheduled (time-based), Continuous (always-running), File Arrival (event-driven), and Table Updates.

- Two critical components support the entire system: Observability for monitoring and troubleshooting, and Control Flow for managing task dependencies and execution order.
# REFERÊNCIAS
---
[[DTB - DEPLOY WORKLOADS WITH LAKEFLOW JOBS]]