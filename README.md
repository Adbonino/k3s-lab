## Passwords:

### ArgoCD:

```
# echo "Recuperar Password"
# sudo kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d && echo
```

### Grafana:

```
# echo "Recuperar Password"
# sudo kubectl --namespace monitoring get secret monitoring-grafana   -o jsonpath="{.data.admin-password}" | base64 -d ; echo
```

### Dashboard:

```
# echo "Recuperar Password"
# sudo kubectl -n kubernetes-dashboard create token admin-user
```
