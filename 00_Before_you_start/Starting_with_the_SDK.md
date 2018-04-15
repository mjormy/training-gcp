## Download the SDK

You can either download and decompress the tar.gz file from
https://cloud.google.com/sdk/downloads

Or

* Run `curl`
```
curl https://sdk.cloud.google.com | bash
exec -l $SHELL
```
* Run `apt-get` o `yum`

**Note:** This options don't include `kubectl` and deploy commands. You can install them individually.

## Init the sdk

By running 
```
./google-cloud-sdk/bin/gcloud init
```

You'll be re-directed to a web browser to log in with your credentials.

You can also run

```
./google-cloud-sdk/bin/gcloud init --console-only
```

## Activating the sdk for a certain project

When runing `gcloud init`, you can choose to use an existing project or create a new one.

To see the current configuration of your SDK you can run
```
gcloud config configurations list
```

To set (or reset) the project on your configuration you run
```gcloud config set project my-other-project```

**Note:** You have to activate it por each project you want to use the SDK with.

## Establishing default compute zone

```gcloud config set compute/zone us-east1-c```

## Adding a new configuration

To add a new configuration, run
```gcloud config configurations create my-new-config```

## Other resources

On multiple configurations
https://www.the-swamp.info/blog/configuring-gcloud-multiple-projects/
