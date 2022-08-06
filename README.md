## ☸️ kubernetes Monitoring stack with prometheus and grafana

Complete prometheus monitoring stack setup on Kubernetes.

### Before run 

* You need deploy nginx ingress in your cluster
* You need deploy certmanager in your cluster


#### 0) For deploy certmanager in your cluster use bellow command

```
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.9.1/cert-manager.yaml
```


#### 1) Deploy prometheus

```bash
kubectl apply -f .
```

#### 2) Deploy node-exporter

```
kubectl apply -f node-exporter/
```

#### 3) Deploy kube-state-metrics/

```bash
kubectl apply -f node-exporter/
```


#### 4) Deploy alert-manager

```bash
kubectl apply -f alert-manager/
```

#### 5) Deploy grafana

```bash
kubectl apply -f grafana/
```
