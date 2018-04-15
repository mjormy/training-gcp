# Pushing the image to the Registry

### Uploading the image to your Container Registry

```gcloud auth configure-docker```

```docker push [HOSTNAME]/[PROJECT-ID]/[IMAGE][:TAG]

docker push gcr.io/${PROJECT_ID}/hello-app:v1```

After that you can check you image running this command

```gcloud container images list-tags gcr.io/ormy-deploy-kub/hello-app```

And checking in your console 

https://console.cloud.google.com/gcr/images/[YOUR_PROJECT]