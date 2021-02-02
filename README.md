# from-docker-to-helm

## Requirements

microk8s with ingress addon enabled.

## Docker
```
docker run -it -p 8081:80 --rm bsord/tetris
```

## Kubernetes
```
kubectl apply -f templates/deployment.yaml
kubectl apply -f templates/service.yaml
kubectl apply -f templates/ingress.yaml
```

```
kubectl get all
kubectl get ingress
```

```
kubectl delete -f templates/deployment.yaml
kubectl delete -f templates/service.yaml
kubectl delete -f templates/ingress.yaml
```

## Helm chart
```
helm upgrade --install tetris .
kubectl get all
kubectl get ingress
```
