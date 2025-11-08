2810250841
**Descrição:** Core components of a databricks lakeflow job
**TAG:** #Databricks #COURSE #engineering #LAKEFLOW #JOBS 

# DTB - DWLJ - 04 JOB CORE COMPONENTS
---

# BUILDING BLOCKS OF LAKEFLOW JOBS

## JOBS AND TASKS

![[Pasted image 20251028084615.png]]

![[Pasted image 20251028084633.png]]


Here are the two most fundamental concepts you need to understand:

### JOB

>A Job is the primary resource for scheduling, coordinating, and running operations such as data processing, ETL, analytics, and machine learning workloads within the Databricks environment. 

Think of a job as the container that holds your entire workflow.

### TASK

>A task is a single unit of work within a job that executes a specific workload such as a notebook, script, query, and more. Tasks are the individual building blocks that do the actual work.

The relationship is hierarchical: each job consists of one or more tasks, which are the individual units of work that make up the job. 

### TASK TYPES

![[Pasted image 20251028085108.png]]

Jobs consist of one or more tasks, and there are many different task types available. 

You can use Databricks ==Notebooks in any supported language,
Python Scripts, Python Wheels for packaged code, SQL Files and Queries for data transformations, DLT (Declarative Pipelines), dbt for data transformation, Java JAR files, Spark Submit jobs for legacy Spark applications, AI/BI Dashboards for visualization, and even Power Bl integration ==.

This variety ensures that you can orchestrate virtually any type of workload within your job.

### TASK OPTIONS

![[Pasted image 20251028093805.png]]
>When you create a job, you can set specific configurations for each particular task. The options available depend on the task type you select. Common configuration options include defining the path to your code, adding libraries, setting parameters, enabling notifications, and configuring retry policies.

These configurations allow you to better orchestrate each particular task according to your specific requirements.

## EXISTING TASKS AND OPTIONS

- Notebook
	- Source
	- Path
	- Compute options
	- Parameters
	- Notifications

- SQL Task
	- Task name
	- SQL query
	- SQL warehouse
	- Parameters
	- Notifications
	- Retries

### LANGUAGES SUPPORTED

- SQL
- PYTHON
- SCALA
- R
- JAVA - VIA JAR FILE


### CONTROL FLOWS AND TRIGGERS

![[Pasted image 20251028094350.png]]

### CONTROL FLOWS

- SEQUENTIAL
- PARALLEL
- CONDITIONAL (IF/ELSE)
- MODULAR DESIGN
- FOR EACH LOOPS

### TRIGGER TYPES

- MANUAL TRIGGERS
- SCHEDULED TRIGGERS - USING CRON EXPRESSIONS
- API TRIGGERS - PROGRAMATIC EXECUTION
- FILE ARRIVAL TRIGGERS - EVENT-DRIVINN PROCESSING
- TABLE TRIGGERS - DATA CHANGE EVENTS
- CONTINOUS TRIGGERS - STREAMING

## TYPES OF COMPUTE

![[Pasted image 20251028094717.png]]

### INTERACTIVE CLUSTERS

> Development, ad-hoc analysis and exploration

- Don't use it in production because they are not cost-efficient

### JOB CLUSTERS

> Production grade and Operational Use-Cases

- 50% cheaper because they terminate when the job ends.
- Subject to cloud providers start-up times
- Can be reused across tasks for a better price performance
### SERVERLESS

> Simple, fast, reliable and cost-efficient

- Simpler and reliable
- fast and auto-scalling; better user experience at a lower cost
- performance optimizations - lower overral TCO.

![[Pasted image 20251028095530.png]]
### SQL WAREHOUSE

> Compute for SQL queries and BI, Serverless by default

- For SQL queries, dashboards and BI

### SELECTING COMPUTE

![[Pasted image 20251028095636.png]]

# TASK ORCHESTRATION

## WHAT IS A DAG

> Directd acylic graph - conceptual representation of series of activies, including data processing flows.

- Directed - unambiguous direction for each edge
- Acyclic - contains no cycles
- Graph - collection of vertices connected by edges.

![[Pasted image 20251029203156.png]]

## TASK ORCHESTRATION OVERVIEW

![[Pasted image 20251029203259.png]]

![[Pasted image 20251029203314.png]]

## COMMON WORLOADS PATTERNS


![[Pasted image 20251029203414.png]]

# COURSE PROJECT OVERVIEW

## DIAGRAM OF THE PROJECT

![[Pasted image 20251029203617.png]]

1. This diagram shows our complete course project architecture. We'll build a retail data processing pipeline that Demonstrates all the concepts we're learning.

2. Starting with retail data in cloud storage, we'll ingest customers, sales, and orders data using different task types. We'll join customers & orders and customers & sales using notebook tasks. The workflow includes an If/Else block for checking duplicates with true and false conditions. 

3. We'll implement a For Each task for state-wise iteration on customer orders data. Finally, we'll create a retail dashboard using a dashboard task.

4. This project incorporates SQL tasks, notebook tasks, conditional logic, iterative processing, and dashboard creation - giving you hands-on experience with all major Lakeflow Jobs features.


# CREATING A JOB USING LAKEFLOW JOBS UI

![[Pasted image 20251030220334.png]]


![[Pasted image 20251030220440.png]]


# REFERÊNCIAS
---
[[DTB - DEPLOY WORKLOADS WITH LAKEFLOW JOBS]]