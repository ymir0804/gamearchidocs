# Helm을 이용한 설치 방법
## 1. 초기 설치
```bash
helm repo add jetstack https://charts.jetstack.io
helm install cert-manager jetstack/cert-manager \
  --namespace cert-manager --create-namespace \
  --version v1.16.3 \
  -f values.yaml

  # DuckDNS 웹훅 설치 (csp33 저장소 사용)
helm repo add csp33 https://csp33.github.io/cert-manager-duckdns-webhook
helm install cert-manager-duckdns-webhook csp33/cert-manager-duckdns-webhook \
  --namespace cert-manager \
  -f values.yaml
  ```
