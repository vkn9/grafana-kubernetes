# Deploy grafana lên kubernetes

## Tạo pvc để mount disk tránh mất dữ liệu khi pod restart hoặc cài lại (Sửa các thông tin trong file pvc.yaml cho phù hợp với nhu cầu)

```yaml
kubectl create -f pvc.yaml
```

## Đẩy deployment của grafana (Sửa thông tin trong file deployment.yaml cho phù hợp)

```yaml
kubectl create -f deployment.yaml
```

## Đẩy service của grafana (Sửa thông tin trong file service.yaml cho phù hợp)

```yaml
kubectl create -f service.yaml
```

## Có thể đổi type service thành LoadBalancer để có ip public hoặc port forward về . port grafana là 3000
