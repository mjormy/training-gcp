## Download the SDK

You can either download the tar.gz file from
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

You can choose to use an existing project or create a new one.
**Note:** You have to activate it por each project.