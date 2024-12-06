# helm.vimalmenon.com
K8S resources for vimalmenon.com


#### To-Do
- [ ] Deploy the helm chart to CIVO
- [ ] Linting for Helm
- [ ] Create ClusterIp service
- [ ] Create ingress for API's
- [ ] Try ArgoCD


#### Command
Start a minikube cluster with a profile
```sh
minikube start -p vimalmenon
```
Delete minikube profile
```sh
minikube delete -p vimalmenon
```
Deploy the app
```sh
helm install vimalmenon .
```
Undeploy the app
```sh
helm uninstall vimalmenon
```
Get ArgoCD Password
```sh
k get secrets/argocd-initial-admin-secret -n argocd --template={{.data.password}}| base64 -d
```
