
Install:
    helm upgrade --install --repo https://argoproj.github.io/argo-helm argocd argo-cd --values argo_values.yaml

Get Password:

    kubectl get secrets argocd-initial-admin-secret -o=jsonpath='{.data.password}' | base64 -d