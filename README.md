<img width="1287" height="577" alt="1_GXjmR0-ghYha9IEMdgpLyg" src="https://github.com/user-attachments/assets/1bd1cb2f-e766-49c3-812a-b781462bdd9d" />

###  Airflow | Kubernetes ☸️
Apache Airflow is an open-source workflow orchestration platform used to programmatically author, schedule, and monitor data pipelines or other workflows.


🧱 Key Features of Crossplane 
```
✅ Unified API for Cloud Resources:
Crossplane integrates cloud resources into Kubernetes using CRDs. This means you can manage cloud infrastructure alongside Kubernetes workloads using a single API
✅ Multi-Cloud Management:
Crossplane supports multiple cloud providers like AWS, Azure, and Google Cloud. You can use the same API to manage resources across different cloud platforms
✅ Declarative Infrastructure Management:
Like Kubernetes resources, Crossplane allows you to define your desired infrastructure state declaratively. Once defined, Crossplane continuously reconciles your infrastructure to match this state.
✅ Composable Infrastructure:
Crossplane lets you bundle multiple cloud resources together into higher-level abstractions, called Compositions and Composite Resources (XRs), allowing for reusable and simplified infrastructure components.
✅ Kubernetes-Native GitOps:
Crossplane works well with GitOps practices, enabling teams to manage cloud infrastructure in the same way they manage Kubernetes workloads: declaratively and with continuous reconciliation.
✅ Community and Ecosystem:
Being an open-source project, Crossplane has a growing community and a rich ecosystem of providers and compositions that you can leverage.
```

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
