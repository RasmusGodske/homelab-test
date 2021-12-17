
#Manage cluster:

## Create Cluster

    k3d cluster create portainer --config k3dcluster-config.yaml

## Delete Cluster
Create cluster:

    k3d cluster delete portainer


Install ArgoCD:

    helm upgrade --install --namespace argocd --create-namespace --repo https://argoproj.github.io/argo-helm argocd argo-cd --values argo_values.yaml

Get Password:

    kubectl get secrets argocd-initial-admin-secret --namespace argocd -o=jsonpath='{.data.password}' | base64 -d