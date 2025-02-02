# Using Artifactory as the object store (Alpha)

If you are interested in using an existing instance of Artifactory as your object store instead of Minio,
we are providing this capability as an early preview/alpha for testing.

To set this up, you will need to have the following:

* Know the URL to the Artifactory instance
* Know (or generate) an API key to authenticate to the instance
* Create a repo for the Habitat artifacts

Once you have the above, modify the your `bldr.env` based on the same config in `bldr.env.sample` in order to enable Artifactory.

Once you have `bldr.env` updated, you can do an install normally using the `install.sh` script.

After logging into the Depot Web UI and creating your origins, you can try uploading some packages and check your Artifactory instance to ensure that they are present in the repo you specified.

If you run into any issues, please see the Support section below.

## Running a local Artifactory

If you just want to do a quick test, you can also run a local Artifactory instance. In order to do that, you can do the following:

```bash
sudo hab svc load core/artifactory
```

This will spin up an Artifactory instance, and you can use the following to log in: http://localhost:8081/artifactory/webapp/#/home

