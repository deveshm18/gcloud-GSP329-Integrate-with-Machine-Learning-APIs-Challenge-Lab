#Create the new service account -> roles: Storage Admin & BigQuery Admin
#Then, create credentials to log in as your new service account. Create these credentials and save it as a JSON file "~/key.json" by using the following command:
gcloud iam service-accounts keys create ~/key.json \
  --iam-account my-serviceaccount-sa@${GOOGLE_CLOUD_PROJECT}.iam.gserviceaccount.com

#Finally, set the GOOGLE_APPLICATION_CREDENTIALS environment variable. The environment variable should be set to the full path of the credentials JSON file you created, 
#which you can see in the output from the previous command:
export GOOGLE_APPLICATION_CREDENTIALS="/home/USER/key.json"
