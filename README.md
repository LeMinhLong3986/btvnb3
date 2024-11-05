## Cách thực hiện lab1

1. Khởi động minikube:
   ```bash
   minikube start
2. Triển khai Deployment:
   ```bash
   kubectl apply -f manifests/nginx-deployment.yaml
3. Triển khai Service:
   ```bash
   kubectl apply -f manifests/nginx-deployment.yaml
4. Truy cập vào Service
   ```bash
   minikube service nginx-service
5. Truy cập vào trang web ở đường dẫn URL dưới dòng "Starting tunnel for service nginx-service" trong Terminal

## Cách thực hiện lab2

1. Khởi động Minikube và đảm bảo nó đang sử dụng Docker driver:
   ```bash
   minikube start --driver=docker
2. Cấu hình Docker Daemon cho Minikube:
   ```bash
   & minikube -p minikube docker-env --shell=powershell | Invoke-Expression

3. Build Docker Image:
   ```bash
   docker build -t static-web .

4. Áp dụng cấu hình Deployment trên Kubernetes:
   ```bash
   kubectl apply -f deployment.yaml

5. Áp dụng cấu hình Service trên Kubernetes:
   ```bash
   kubectl apply -f service.yaml

6. Truy cập vào ứng dụng:
   ```bash
   minikube service static-web-service

7. Truy cập vào trang web ở đường dẫn URL dưới dòng "Starting tunnel for service static-web-service" trong Terminal vì sử dụng tunnel (127.0.0.1:port) thường đáng tin cậy hơn trên Windows.

## Cách thực hiện lab3

1. Khởi động Minikube và đảm bảo nó đang sử dụng Docker driver:
   ```bash
   minikube start --driver=docker
2. Cấu hình Docker Daemon cho Minikube:
   ```bash
   & minikube -p minikube docker-env --shell=powershell | Invoke-Expression

3. Build Docker Image:
   ```bash
   docker build -t static-web-custom .

4. Áp dụng cấu hình Deployment trên Kubernetes:
   ```bash
   kubectl apply -f deployment.yaml

5. Áp dụng cấu hình Service trên Kubernetes:
   ```bash
   kubectl apply -f service.yaml

6. Truy cập vào ứng dụng web1:
   ```bash
   minikube service web1

7. Truy cập vào ứng dụng web2:
   ```bash
   minikube service web2

8. Truy cập vào trang web ở đường dẫn URL dưới dòng "Starting tunnel for service web1/web2" trong Terminal vì sử dụng tunnel (127.0.0.1:port) thường đáng tin cậy hơn trên Windows.