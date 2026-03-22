# CKAD Exam - Imperative Commands Cheatsheet
# These commands save time in the exam (2 hours, hands-on)

## ⚡ Fast Pod Creation (imperative)

```bash
# Create pod quickly
kubectl run nginx-pod --image=nginx --port=80 -n dev

# Create pod with labels
kubectl run webapp --image=nginx --labels="app=webapp,tier=frontend"

# Create pod with env variable
kubectl run myapp --image=busybox --env="ENV=prod" -- sleep 3600

# Create pod and expose it immediately
kubectl run webapp --image=nginx --port=80 --expose
```

---

## ⚡ Fast Deployment Commands

```bash
# Create deployment
kubectl create deployment webapp --image=nginx --replicas=3

# Scale
kubectl scale deployment webapp --replicas=5

# Update image (triggers rolling update)
kubectl set image deployment/webapp webapp=nginx:1.22

# Rollback
kubectl rollout undo deployment/webapp

# Check rollout status
kubectl rollout status deployment/webapp

# Rollout history
kubectl rollout history deployment/webapp
```

---

## ⚡ Fast Service Exposure

```bash
# Expose deployment as ClusterIP
kubectl expose deployment webapp --port=80 --target-port=80

# Expose as NodePort
kubectl expose deployment webapp --type=NodePort --port=80 --nodePort=30080

# Quick service check
kubectl get svc
kubectl describe svc webapp
```

---

## ⚡ Generate YAML Quickly (dry-run trick!)

```bash
# Generate pod YAML without creating
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod.yaml

# Generate deployment YAML
kubectl create deployment webapp --image=nginx --dry-run=client -o yaml > deploy.yaml

# Generate service YAML
kubectl expose deployment webapp --port=80 --dry-run=client -o yaml > svc.yaml
```

---

## ⚡ ConfigMap & Secret

```bash
# Create configmap from literal
kubectl create configmap app-config --from-literal=APP_ENV=dev --from-literal=PORT=80

# Create configmap from file
kubectl create configmap nginx-conf --from-file=nginx.conf

# Create secret
kubectl create secret generic db-secret --from-literal=DB_PASS=supersecret

# View decoded secret
kubectl get secret db-secret -o jsonpath='{.data.DB_PASS}' | base64 -d
```

---

## ⚡ Useful Debug Commands

```bash
# Check pod logs
kubectl logs <pod-name> -n dev

# Previous container logs (after crash)
kubectl logs <pod-name> --previous

# Exec into container
kubectl exec -it <pod-name> -- /bin/sh

# Describe pod (see events)
kubectl describe pod <pod-name>

# Watch pods
kubectl get pods -w

# Check resource usage
kubectl top pods
kubectl top nodes
```

---

## ⚡ Jobs

```bash
# Create a job
kubectl create job myjob --image=busybox -- echo "hello"

# Create cronjob
kubectl create cronjob mycron --image=busybox --schedule="*/5 * * * *" -- echo "tick"
```

---

## 📝 CKAD Exam Tips

1. **Use `--dry-run=client -o yaml`** to generate manifests fast
2. **Always check the namespace** with `-n <namespace>`
3. **Use `kubectl explain`** to look up field names: `kubectl explain pod.spec.containers`
4. **Bookmark the Kubernetes docs** — allowed during exam
5. **Set alias at exam start:** `alias k=kubectl`
6. **Practice on killercoda.com** and **killer.sh** (exam simulator)
