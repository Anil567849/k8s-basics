### start minikube with docker

    minikube start --driver=docker

### kubectl apply commands in order
    
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo-deployment.yaml
    kubectl apply -f mongo-configMap.yaml 
    kubectl apply -f mongoexpress-deployment.yaml
    minikube start --driver=docker

### kubectl delete commands in order
    
    kubectl delete -f mongo-secret.yaml
    kubectl delete -f mongo-deployment.yaml
    kubectl delete -f mongo-configMap.yaml 
    kubectl delete -f mongoexpress-deployment.yaml

### kubectl get commands

    kubectl get pod
    kubectl get pod --watch
    kubectl get pod -o wide
    kubectl get service
    kubectl get deployment
    kubectl get secret
    kubectl get all | grep mongodb
    kubectl get all
    kubectl get ns
    kubectl get pods -n name_of_namespace

### kubectl debugging commands

    kubectl describe pod mongodb-deployment-xxxxxx
    kubectl describe service mongodb-service
    kubectl logs mongo-express-xxxxxx

### give a URL to external service in minikube

    minikube service mongo-express-service

### minikube add ingress

    minikube addons enable ingress