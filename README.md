# from-docker-to-helm

## Requirements

microk8s with ingress addon enabled.

## Docker
```
docker run -it -p 8081:80 --rm bsord/tetris
```

## Kubernetes
```
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
kubectl apply -f kubernetes/ingress.yaml
```

## Helm chart
```
helm upgrade --install tetris chart
```
