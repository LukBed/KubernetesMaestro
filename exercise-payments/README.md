# Payments exercise

```bash
kubectl apply -f payments.yml
kubectl logs -l app=payments-app -n payments
```

Expected output:
```
MERCHANT_ID: 123456
PAYMENT_GATEWAY_API_KEY: k8smaestro
```