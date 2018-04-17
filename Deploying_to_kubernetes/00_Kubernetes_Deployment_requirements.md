# Requirements for this tutorial

You can run this tutorial on your machine or using the built in console.

* An existing project with active billing

If the billing of your project is not active, you might have to do that in order to use the Kubernetes Engine.

* Go to the [Kubernetes Engine page](https://console.cloud.google.com/kubernetes) and select your project.

Wait for the API and related services to be enabled. 

### On the built in console

To follow this guide on the built-in console, you'll have the `gcloud` already running

### On your machine

You'll need the following

* Installed SDK. You can check it by running `gcloud --version`

* Installed `kubectl`

```gcloud components install kubectl```

* Docker CE on your local machine

You can find it in https://docs.docker.com/install/#supported-platforms

* git 

To configure your git acount you refer to https://help.github.com/articles/set-up-git33/

### Setting up your defaults

You should set the defaults for the project, so that you don't have to configure that in every component

```
gcloud config set project [PROJECT_ID]
gcloud config set compute/zone [YOUR_PREFERED_ZONE]
```

To find the list of available zones you can run

``````