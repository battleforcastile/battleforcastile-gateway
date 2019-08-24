# Battle For Castile: Gateway

This micro-service proxies the different requests into the right internal micro-services.
It uses the official `nginx-ingress` helm chart.

## 1. Installation and set up

### 1.1 Install `nginx-ingress` release
```
helm install stable/nginx-ingress
```

### 1.2 Apply required CRDs
```
kubectl apply -f https://raw.githubusercontent.com/jetstack/cert-manager/release-0.8/deploy/manifests/00-crds.yaml
```

### 1.3 Add Jetstack Helm repository
```
helm repo add jetstack https://charts.jetstack.io
```

### 1.4 Install Cert-Manager into the cert-manager namespace
```
helm install --name cert-manager --namespace cert-manager jetstack/cert-manager
```

### 1.5 Install repo Helm chart
```
helm install helm/battleforcastile_gateway
```
