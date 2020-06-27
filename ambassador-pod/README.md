1. Create ambassador config
1. Create  fruit service pod with the main container and the proxy container
    1. Use configMap to store proxy configuration 
1. Create a test busybox pod
1. kubectl exec -it fruit-busybox -- curl $(kubectl get pod fruit-service -n my-ns -o=custom-columns=IP:.status.podIP --no-headers):80
1. OR Get the IP of the fruit service pod:
    curl <ip:80>
    curl: <ip:8775>