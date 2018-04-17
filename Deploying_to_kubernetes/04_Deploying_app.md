# Deploying your app

The kubectl run command below causes Kubernetes to create a Deployment named hello-web on your cluster. The Deployment manages multiple copies of your application, called replicas, and schedules them to run on the individual nodes in your cluster. In this case, the Deployment will be running only one Pod of your application.

```kubectl run hello-web --image=gcr.io/${PROJECT_ID}/hello-app:v1 --port 8080```

```kubectl get pods```

By default, the containers you run on Kubernetes Engine are not accessible from the Internet, because they do not have external IP addresses. You must explicitly expose your application to traffic from the Internet, run the following command:

```kubectl expose deployment hello-web --type=LoadBalancer --port 80 --target-port 8080```

### Scaling 

```kubectl scale deployment hello-web --replicas=3```

```kubectl get deployment hello-web```

### Deploy a new version

```docker build -t gcr.io/${PROJECT_ID}/hello-app:v2 ```
```kubectl set image deployment/hello-web hello-web=gcr.io/${PROJECT_ID}/hello-app:v2``