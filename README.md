# Sprawozdanie_Lab5

## Uruchomienie
<code>kubectl apply -f manifests/01-namespace-ns-dev.yaml</code>

<code>kubectl apply -f manifests/02-namespace-ns-prod.yaml</code>

<code>kubectl apply -f manifests/11-rq-ns-dev.yaml</code>

<code>kubectl apply -f manifests/12-lr-ns-dev.yaml</code>

<code>kubectl apply -f manifests/13-rq-ns-prod.yaml</code>

### <code>kubectl get ns</code>
<img width="418" height="176" alt="image" src="https://github.com/user-attachments/assets/56ada522-0fec-4a65-af9a-2e65ddbe80ee" />

### <code>kubectl get resourcequota -n ns-dev</code>
<img width="1038" height="83" alt="image" src="https://github.com/user-attachments/assets/4dea8b27-32c4-4a40-adf2-6cc1a6a4a3c4" />

### <code>kubectl get limitrange -n ns-dev</code>
<img width="561" height="82" alt="image" src="https://github.com/user-attachments/assets/48d77ec8-3527-418d-b639-1be5808c2d78" />

### <code>kubectl get resourcequota -n ns-prod</code>
<img width="1052" height="88" alt="image" src="https://github.com/user-attachments/assets/261f82e4-be8a-4a84-b074-b2b3645a2b52" />

## Deployment <code>no-test</code>
### <code>kubectl apply -f manifests/21-deploy-no-test.yaml</code>
<img width="701" height="57" alt="image" src="https://github.com/user-attachments/assets/3bdbe533-ed3c-4f75-8f45-9ac7ea066aaf" />

### <code>kubectl get deploy -n ns-dev</code>
<img width="534" height="86" alt="image" src="https://github.com/user-attachments/assets/33c4665b-605c-410d-b465-1936006dd9df" />

### <code>kubectl get pods -n ns-dev</code>
<img width="516" height="57" alt="image" src="https://github.com/user-attachments/assets/de179262-e15a-4d55-a542-5382f86b99af" />

### <code>kubectl describe deployment no-test -n ns-dev</code>
<img width="1015" height="842" alt="image" src="https://github.com/user-attachments/assets/57bd3eef-b9b3-4e51-84d4-a6d951687f24" />

## Deployment <code>yes-test</code>
### <code>kubectl apply -f manifests/22-deploy-yes-test.yaml</code>
<img width="731" height="63" alt="image" src="https://github.com/user-attachments/assets/ddb47204-2f44-48da-9836-05137ed79917" />

### <code>kubectl get deploy,po -n ns-dev</code>
<img width="677" height="170" alt="image" src="https://github.com/user-attachments/assets/a6c3fd2b-9f67-4e09-8d47-4c3dacdb95f6" />

### <code>kubectl describe pod -l app=yes-test -n ns-dev</code>
<img width="799" height="711" alt="image" src="https://github.com/user-attachments/assets/cbdc2361-0016-449f-a0df-7401e55de063" />

### <code>kubectl logs -l app=yes-test -n ns-dev</code>
<img width="712" height="326" alt="image" src="https://github.com/user-attachments/assets/6777ac53-e147-4e50-a339-2c7caa7ac797" />

## Deployment <code>zero-test</code>
### <code>kubectl apply -f manifests/23-deploy-zero-test.yaml</code>
<img width="729" height="52" alt="image" src="https://github.com/user-attachments/assets/ae960c11-9869-43bc-9da6-d26bed7865ff" />

### <code>kubectl get deploy,po -n ns-dev</code>
<img width="643" height="206" alt="image" src="https://github.com/user-attachments/assets/d9c48d37-fdea-4034-8806-72e1d5b2c193" />

### <code>kubectl describe pod -l app=zero-test -n ns-dev</code>
<img width="1351" height="702" alt="image" src="https://github.com/user-attachments/assets/09a3e229-9952-4a6c-b95d-d5c5b1be8bd5" />

<code>kubectl get pod -l app=zero-test -n ns-dev -o=jsonpath="{.items[0].spec.containers[0].resources}"</code>
<img width="1123" height="252" alt="image" src="https://github.com/user-attachments/assets/2cf056a7-5666-43a5-a77c-eaba9553e983" />



