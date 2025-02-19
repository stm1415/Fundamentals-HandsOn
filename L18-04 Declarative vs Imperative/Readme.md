# L18-04

Let's deploy an Nginx container using both methods.

## Imperative

    kubectl create deployment mynginx1 --image=nginx
# When this command is executed, Kubernetes will create a deployment named `mynginx1` using the `nginx` image. The deployment will manage the creation and scaling of the pods running the Nginx server, ensuring that the specified number of replicas are always running and available. This command is useful for quickly deploying a web server or any other application containerized with Docker.

# get list of deployments
     kubectl get deploy 
## Declarative

    kubectl create -f deploy-example.yaml

## Cleanup

    kubectl delete deployment mynginx1
    kubectl delete deploy mynginx2