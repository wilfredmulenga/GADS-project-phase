## Project Phase- GADS GCP Cloud track

Here is a repo with details of the labs I took during the project phase of the GADS GCP Cloud track. The screenshots
folder contains screenshots of the confirmation email sent from Qwiklabs about the completion of a lab. I used the  
(gcloud reference)[https://cloud.google.com/sdk/gcloud/reference] to find the description of the gcloud commands.

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

In the gcloud command, the 'no-address' value in the --network-interface option means that an external IP 
will not be created for this VM.

 Task 2: Creating a Windows VM
 export ZONE='europe-west2-a'  
 export INSTANCE_NAME='windows-instance'  
 export INSTANCE_TYPE='n1-standard-2'  
 export IMAGE_FAMILY='windows-server-2016-dc-core-v20200813'  
 export IMAGE_PROJECT='windows-core'
 gcloud compute instances create $INSTANCE_NAME \    
          --zone=$ZONE \    
          --machine-type=$INSTANCE_TYPE \    
          --image-family=$IMAGE_FAMILY  \
          --image-project=$IMAGE_PROJECT

<!-- TODO: add flag to allow http & https traffic -->

To find the name of the image that I needed I used the command `gcloud compute images list` which returns  
a full list of public images with their image names, versions numbers, and image sizes.   

 Task 3: Create a custom virtual machine  
 export ZONE='us-west1-b'    
 export INSTANCE_NAME='custom-instance'   
 export INSTANCE_TYPE='n1-standard-2'    
 gcloud compute instances create $INSTANCE_NAME \      
          --zone=$ZONE \        
          --custom-cpu=6  
          --custom-memory=32    

