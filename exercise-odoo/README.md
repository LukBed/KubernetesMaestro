# ODOO exercise

```bash
kubectl apply -f odoo.yml
kubectl port-forward svc/odoo-public 8082:80
```

Then: http://localhost:8082/web/login