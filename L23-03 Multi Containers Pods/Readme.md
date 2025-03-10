# L23-03

Let’s create multiple containers in a Pod using a YAML file.  We'll use the Busybox container to get the default page served by the Nginx container.

## Create the pod

    kubectl create -f two-containers.yaml

## Get some info

    kubectl get pods -o wide
    kubectl describe pod two-containers

## Connect to the BusyBox container

    kubectl exec -it two-containers --container mybox -- /bin/sh

## Fetch the HTML page served by the Nginx container

This will output the content of the Web page in the terminal.

    wget -qO- localhost

## Quit

    exit

## Cleanup

    kubectl delete -f two-containers.yaml --force --grace-period=0

## Understanding
BusyBox is a lightweight, multi-purpose Linux utility that provides a collection of common UNIX commands in a single executable. It is often referred to as the "Swiss Army Knife" of embedded Linux systems because it includes simplified versions of many standard Linux utilities like ls, cat, echo, grep, wget, and more.