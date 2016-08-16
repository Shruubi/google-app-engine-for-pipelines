# gcloud-pipelines - Google App Engine Integration for Bitbucket Pipelines

One of the more frustrating things about using Google App Engine is the lack
of good CI/CD tools available that not only integrate with App Engine, but
also integrate with Bitbucket.

Google doesn't provide any documentation for setting up an automated deployment
process, so we've had to mostly figure it out for ourselves. To make life easier
for everyone else, we're uploading the `bitbucket-pipelines.yml` file that will
make sure this process works.

--------------------------------------------------------------------------
### Setup

First, you need to enable your app to work with gcloud. Do the following:

1. on the app engine panel, open the menu and select "API Manager"
2. enable the "App Engine Admin API"
3. open credentials and select Service Account Key and create a .json file and 
use App Engine default service account as the account
4. download the .json file and move it into your repository
5. open "Manage service accounts" and copy the email address associated 
with App Engine default service account

Take your .json file and the bitbucket-pipelines.yml file and put it in the
top level of your repository. You will need to make sure you edit the YAML 
file with your details.

### License

This project is licensed under the GNU GPLv3. Refer to `LICENSE` for the
full license text.
