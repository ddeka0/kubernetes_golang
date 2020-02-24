# kubernetes_golang

#### Instruction to run in ubuntu 18.04:
  
      0. Install Minikune and Kubectl
      1. minikube start --vm-driver=virtualbox
      2. eval $(minikube -p minikube docker-env)
      3. cd add
      4. docker build . -t ddeka0/add-service:v1.0
      5. cd ..
      6. cd api
      7. docker build . -t ddeka0/api-service:v1.0
      8. cd ..
      9. kubectl create -f deployment/summation-service.yaml
      10. kubectl create -f deployment/api-service.yaml
      
#### Checking API:

      1. minikube service api-service --url
      2. Go to browser and check the API (for example http://192.168.99.100:30080/add/<a value>/<b value>)
