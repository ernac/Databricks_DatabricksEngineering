3010252208
**Descrição:** Learning how creating and scheduling jobs in Databricks
**TAG:** #Databricks #COURSE #engineering #LAKEFLOW #JOBS 

# DTB - DWJL - 05 CREATING AND SCHEDULING JOBS
---

## COMMON TASK CONFIGURATION OPTIONS

Let's start with the common configuration options that you can apply to your tasks. These settings are key to building workflows that are not just automated, but also dynamic, context-aware, and easy to monitor.

We'll cover how to pass values into your tasks and how to set up alerts.

![[Pasted image 20251031081208.png]]

**Parameters & Dynamic Value References** are the foundation of flexible workflows. These can only be set at the task level and allow you to create reusable, adaptable tasks that can behave differently based on input values or runtime context.

**Retries** are your first line of defense against transient failures. You can configure retry behavior at both job and task levels, allowing for different retry strategies depending on the criticality and expected failure patterns of different parts of your workflow.

**Notification Alerts** keep your team informed and enable rapid response to issues. Like retries, these can be configured at both job and task levels, giving you granular control over who gets notified about what events.

### PARAMETER OVERVIEW

![[Pasted image 20251031081448.png]]

Understanding the parameter hierarchy is crucial for effective job design:

>==**Task Parameters** are key-value pairs or JSON arrays defined at the individual task level.== These are specific to each task and allow for fine-grained control over task behavior.

>==**Job Parameters** are defined at the job level and automatically propagate to all tasks within that job.== This creates a powerful inheritance model where you can set common defaults while still allowing task-specific overrides.

The precedence rule is critical to remember: 

- ==Job parameters always override task parameters when the same key exists==. 

This design pattern allows you to establish sensible defaults at the job level while maintaining the flexibility to customize individual tasks when needed.

![[Pasted image 20251031082030.png]]

>Task parameters are far more than simple configuration values - they're the building blocks of intelligent workflows. These key-value pairs enable sophisticated orchestration patterns:

**Conditional Execution:** Use parameters to control which branches of your workflow execute based on data conditions, environment settings, or business rules.

**Looping:** Parameters can control iteration counts, define arrays for for-each loops, and manage complex processing scenarios.

**Context Passing:** Share information between tasks by setting
parameters that downstream tasks can read, creating a data flow
alongside your control flow.

The real power comes from combining parameters with dynamic value references, allowing your workflows to adapt intelligently to changing conditions and data characteristics.

### JOB PARAMETER

![[Pasted image 20251031083235.png]]


## JOB SCHEDULES AND TRIGGERS


## AUTOMATING WORKLOADS WITH SCHEDULES AND TRIGGERS






# REFERÊNCIAS
---
[[DTB - DEPLOY WORKLOADS WITH LAKEFLOW JOBS]]
