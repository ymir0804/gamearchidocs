# 설치 기록  

## Rancher  
- 2025-02-15 현재 기준 v1.32버전 쿠버네티스에서는 Rancher 설치 불가

## longhorn
- 현재 longhorn만 설치 예정

## nginx-ingress

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
helm install ingress-nginx ingress-nginx/ingress-nginx   --namespace ingress-nginx   --create-namespace   --set controller.ingressClassResource.name=nginx   --set controller.ingressClassResource.default=true
```


## KeyCloak
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
kubectl create namespace keycloak
kubectl create secret tls keycloak-tls-cert --cert /home/kubeadm/wildcard-fullchain.pem --key /home/kubeadm/wildcard-key.pem -n keycloak
```
