# Battle For Castile: Gateway

This micro-service proxies the different requests into the right internal micro-services.
It uses the official `nginx-ingress` helm chart.

## 1. Installation and set up

### 1.1 Install `nginx-ingress` release
```
helm install stable/nginx-ingress
```

### 1.2 Install Helm chart
```
helm install helm/battleforcastile_gateway
```
