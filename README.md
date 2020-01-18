####  Deploy to Google App Engine with Bitbucket Pipes

This repo contains a basic example for deploying applications to the Google App Engine using [google-app-engine-deploy](https://bitbucket.org/atlassian/google-app-engine-deploy/src/master/) pipe.
It this example we deploy a simple NodeJS app `app.js`.

#### Hot wo use thie example

##### Forking the repo
Create a fork of this repo, see [Forking a Repository](https://confluence.atlassian.com/bitbucket/forking-a-repository-221449527.html).

##### Enabling Pipelines in your repo 

To enable Piplines go to *Project*  > *Settings* > *Pipelines* and toggle the **Enable Pipelines** button. This can also be done from the **Pipelines** tab in your repository sidebar when you enable Pipelines for the first time. See also [Piplines Getting started](https://confluence.atlassian.com/bitbucket/get-started-with-bitbucket-pipelines-792298921.html) for more instructions.

##### Configuring pipe variables

To use this example you'll need to configure `KEY_FILE` and `PROJECT` pipelines variables in your repository.
How to create Key file for a Google service account you can find [here](https://cloud.google.com/iam/docs/creating-managing-service-account-keys).

For base64 encoded contents required by KEY_FILE variable use command:

Linux
```
$ base64 -w 0 < GCP_key_file
```

MAC OS X
```
$ base64 < GCP_key_file
```

See **User-defined variables** section in [Variables in pipelines](https://confluence.atlassian.com/bitbucket/variables-in-pipelines-794502608.html) for how to configure Pipelines variables. 



#### Verifying the results of the pipe run

After you've enabled Pipelines and configured all variables you can navigate to the Pipelines section of your fork and explore the current status of the builds. If the build is `successful` you should be able to navigate to your project URL where your simple service should be up and running.
