### https://cloud.google.com/vpc/docs/private-service-connect

### https://cloud.google.com/kubernetes-engine/docs/archive/creating-kubernetes-engine-private-clusters-with-net-proxies

# Build container and publish
````
docker build -t <container-name> .
or
gcloud builds submit -t gcr.io/<PROJECT_ID>/<CONTAINER_NAME>:<TAG>
````

# Deploy container in cluster use the deployment file but change image tag

# Publish PSC from producer project
Don't use proxy protocol.
````
gcloud compute service-attachment describe <GRAB YOUR ID TO USE IN CONSUMER PROJECT>
````

# Connect PSC in consumer project
````

````

# Add proxy-url to kubeconfig file
````
apiVersion: v1
clusters:
- cluster:
    proxy-url: http://<PSC IP>:8118

````
