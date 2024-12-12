# helm.vimalmenon.com

K8S resources for vimalmenon.com

#### To-Do

- [ ] Deploy the helm chart to Civo
- [ ] Ingress for Civo
- [ ] Ingress controller for Civo
- [ ] Linting for Helm
- [ ] Create branch on push to main
- [ ] Add ArgoCD to Ingress
- [ ] Manage secrets in ArgoCD
- [ ] Setup grafana
- [ ] Setup K8S in PI
- [ ] Find a way to deploy different env
- [ ] Create Config Map
- [ ] Create Secret

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

Enable ingress

```sh
minikube addons enable ingress -p vimalmenon
```

Enable ingress-dns

```sh
minikube addons enable ingress-dns -p vimalmenon
```

Minikube Tunnel

```sh
minikube tunnel -p vimalmenon
```

Get ArgoCD Password

```sh
kubectl get secrets/argocd-initial-admin-secret -n argocd --template={{.data.password}}| base64 -d | pbcopy
```
