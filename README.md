# Sprawozdanie_Lab5

## Uruchomienie
kubectl apply -f manifests/01-namespace-ns-dev.yaml
kubectl apply -f manifests/02-namespace-ns-prod.yaml
kubectl apply -f manifests/11-rq-ns-dev.yaml
kubectl apply -f manifests/12-lr-ns-dev.yaml
kubectl apply -f manifests/13-rq-ns-prod.yaml

kubectl apply -f manifests/21-deploy-no-test.yaml
kubectl apply -f manifests/22-deploy-yes-test.yaml
kubectl apply -f manifests/23-deploy-zero-test.yaml
