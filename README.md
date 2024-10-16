# DEVOPS_TradingStrategyAnalysis
DEVOPS_TradingStrategyAnalysis



# Port-forwarding for argo cd : 

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

```bash
kubectl port-forward svc/argocd-server -n argocd 8090:443
```


# Port-forwarding for argo workflow : 

```bash
kubectl -n argo port-forward deployment/argo-server 8095:2746
```

# Port-forwarding for the app : 
```bash
kubectl port-forward service/trading-strategy-analysis-service 8020:8020 -n quant-apps
```


# go into apps : 

argo workflow : https://localhost:8095
argo cd : https://localhost:8090
app : argo cd : https://localhost:8020
