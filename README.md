<img width="1287" height="577" alt="1_GXjmR0-ghYha9IEMdgpLyg" src="https://github.com/user-attachments/assets/1bd1cb2f-e766-49c3-812a-b781462bdd9d" />

###  Airflow | Kubernetes ☸️
Apache Airflow is an open-source workflow orchestration platform used to programmatically author, schedule, and monitor data pipelines or other workflows.


#### 🧱 Key Components:
   - **Directed Acyclic Graphs (DAGs):**: Workflows in Airflow are defined as DAGs, where each node is a task and edges define execution order.
   - **Python-based**: Pipelines are written in Python code, so they are dynamic and version-controllable instead of being defined by static configuration.
   - **Scheduler & Executor**: The scheduler decides what tasks to run and when, while the executor actually runs them (locally, on Celery, Kubernetes, etc.).
   - **UI & Monitoring**: Airflow provides a web UI to visualize DAGs, check logs, retry failed jobs, and monitor pipeline health
   - **Integrations**: Has operators and hooks to connect with databases, cloud providers (AWS, GCP, Azure), big data frameworks (Spark, Hive), and more.


🔨 Example : Config 

## AWS
```
apiVersion: aws.upbound.io/v1beta1
kind: ProviderConfig
metadata:
  name: default
spec:
  credentials:
    source: Secret
    secretRef:
      namespace: crossplane-system
      name: aws-secret
      key: creds
```
## Google
```
apiVersion: gcp.upbound.io/v1beta1
kind: ProviderConfig
metadata:
  name: default
spec:
  projectID: 
  credentials:
    source: Secret
    secretRef:
      namespace: crossplane-system
      name: gcp-secret
      key: creds
```
