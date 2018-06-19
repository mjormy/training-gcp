# Creating our container cluster

Let's create a cluster with 3 nodes

```gcloud container clusters create first-cluster --num-nodes=3```

You can see the list of instances running 

```gcloud compute instances list```

You can check it in the console https://console.cloud.google.com/kubernetes/list?project={YOUR-PROJECT}

**Note:** If you already created your cluster on the console, you'll need to get credentials to  manage the cluster from your local machine.

```gcloud container clusters get-credentials [YOUR_CLUSTER]]```