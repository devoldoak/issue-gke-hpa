# Description

The current repository share a sample deployment to reproduce scaling issue with GKE which is provided by using a minReadySeconds attribute inside deployment and a horizontal pod autoscaling on the same deployment.

On the rolling update stage with a new deployment release (only changing the version label), the deployment scales-out regardless of requested size with the reason `cpu resource utilization (percentage of request) above target`. 

# Target Deployment

GKE v1.24.9-gke.2000

# Deployment instructions

kubectl apply -f deployment.yaml
