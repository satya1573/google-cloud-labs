📘 Google Cloud Lab – Cloud Storage & Cloud Shell

Author: Satya Prakash
Date: October 2025
Lab Type: Google Cloud Fundamentals – Core Infrastructure

------------------------------------------------------------------------

Task 1: Created a Cloud Storage Bucket (via Console)

. Navigated to Cloud Storage → Buckets

. Created a globally unique bucket name: myfirstdemogcpbucket

. Accepted default settings and confirmed public access prevention

. Verified creation under Cloud Storage → Buckets list

--------------------------------------------------------------------------

Task 2: Accessed Cloud Shell

. Launched Cloud Shell from the top-right console icon

. Explored built-in tools: gcloud, gsutil, kubectl, bq

. Noted persistent 5 GB /home directory

---------------------------------------------------------------------------

Task 3: Created Bucket via Cloud Shell

#bash

 gcloud storage buckets create gs://myseconddemogcpbucket


. Authorized the command

. Verified bucket creation using gcloud storage buckets list

---------------------------------------------------------------------------

Task 4: Uploaded a File to the Bucket

1. Uploaded local file using Cloud Shell → More → Upload

2. Verified file with:

#bash

ls


3. Copied file to bucket:

#bash

 gcloud storage cp myfile.txt gs://myseconddemogcpbucket/


4. Verified upload in Console → Cloud Storage → Buckets

----------------------------------------------------------------------------

Task 5: Created Persistent State in Cloud Shell

#bash

 gcloud compute regions list
 INFRACLASS_REGION=us-central1
 echo $INFRACLASS_REGION


. Added variable to .bashrc for persistence:

#bash

 echo "export INFRACLASS_REGION=us-central1" >> ~/.bashrc
 source ~/.bashrc

-----------------------------------------------------------------------------

✅ Outcome:
Successfully created and managed Cloud Storage buckets using both the Console and Cloud Shell, uploaded files, and configured environment persistence.