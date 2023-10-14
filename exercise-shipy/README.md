# Shipy exercise

Create GKE Cluster in GCP with appriopriate node pool - default is enought.

Tested with K8s 1.27.

Install NGNIX:

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.9.3/deploy/static/provider/cloud/deploy.yaml
```

Deploy:

```bash
kubectl apply -f shipy.yml
```

Check Ingress Controller external IP:

```bash
kubectl get svc --namespace=ingress-nginx
```

Or

``bash
kubectl get ingress -n shipy
``````

Wait until IP is ready:

```
NAME               CLASS   HOSTS   ADDRESS         PORTS   AGE
ingress-resource   nginx   *       34.118.53.253   80      51s
```

Then call that IP from a browser.