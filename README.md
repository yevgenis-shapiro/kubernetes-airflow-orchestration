<img width="259" height="92" alt="image" src="https://github.com/user-attachments/assets/e21378d4-1007-4896-b9f3-a70c0c7bf61d" />


###  Airflow | Kubernetes ☸️
Apache Airflow is an open-source workflow orchestration platform used to programmatically author, schedule, and monitor data pipelines or other workflows.


#### 🧱 Key Components:
   - **Directed Acyclic Graphs (DAGs):**: Workflows in Airflow are defined as DAGs, where each node is a task and edges define execution order.
   - **Python-based**: Pipelines are written in Python code, so they are dynamic and version-controllable instead of being defined by static configuration.
   - **Scheduler & Executor**: The scheduler decides what tasks to run and when, while the executor actually runs them (locally, on Celery, Kubernetes, etc.).
   - **UI & Monitoring**: Airflow provides a web UI to visualize DAGs, check logs, retry failed jobs, and monitor pipeline health
   - **Integrations**: Has operators and hooks to connect with databases, cloud providers (AWS, GCP, Azure), big data frameworks (Spark, Hive), and more.



🎯 Typical Use Cases
```
ETL (Extract, Transform, Load) pipelines
Data warehouse updates (e.g., nightly batch jobs)
Machine learning model training and deployment workflows
Automating business reports
Coordinating complex cloud operations
```

🚀 
```
terraform init
terraform validate
terraform plan -var-file="template.tfvars"
terraform apply -var-file="template.tfvars" -auto-approve
```
