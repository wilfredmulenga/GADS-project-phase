## Project Phase- GADS GCP Cloud track

Here is a repo with details of the labs I took during the project phase of the GADS GCP Cloud track. The screenshots
folder contains screenshots of the confirmation email sent from Qwiklabs about the completion of a lab.

31/08/2020
-  I did the lab on Google Cloud Fundamentals: Getting Started with Cloud Marketplace. In this lab,
I got to deploy a LAMP stack to a Compute Engine instance.

01/09/2020
-  I did the lab on Creating Virtual Machines. In this lab, I learnt how to create several standard
and advanced VMs.
To build what I built in the lab using the command line:  
 Task 1: Creating a utility VM  
 export ZONE='us-central1-c'  
 export INSTANCE_NAME='my-new-instance'  
 export INSTANCE_TYPE='n1-standard-1'  
 gcloud compute instances create $INSTANCE_NAME \  
          --zone=$ZONE \  
          --machine-type=$INSTANCE_TYPE \  
          --network-interface=no-address

