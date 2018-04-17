# Building the Docker image locally


### Configuring your project env variable
First, set the PROJECT_ID env variable to get your current gcloud project, which will be used to tag the container image for pushing it to your private Container Registry.

```export PROJECT_ID="$(gcloud config get-value project -q)"```

### Building the image

Now we're gonna build a docker image of your application. For that, Docker has to be running.

```docker build -t gcr.io/${PROJECT_ID}/hello-app:v1 .```

`gcr.io` Refers to the Google Container Registry
`{PROJECT_ID}`is the value we just stored

Finally we can check that our image was loaded with the command

```docker images```

To run your image locally, run

```docker run --rm -p 8080:8080 gcr.io/${PROJECT_ID}/hello-app:v1```

and test it with `curl http://localhost:8080`