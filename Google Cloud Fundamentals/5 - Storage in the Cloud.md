# Storage in the Cloud
## Cloud Storage
Offers developers and organizations durable and highly available object storage.

**But what is Object Storage?**
![Alt text](image-10.png)
![Alt text](image-11.png)
The keys in object storage are in the form or URLs, which means object storage interacts well with web technologies.

Data commonly stored as objects include videos, pictures and audio recordings.

![Alt text](image-12.png)
**Cloud Storage is well suited for serving website content, archival and disaster recovery, and direct download of files.**
Cloud Storage is primarily used whenever binary large-object (BLOB) storage is needed for online content such as videos, backup and archiving, or as a storage of intermediate results (such as in processing workflows).

### Cloud Storage Buckets
Cloud Storage files are organized into buckets.
A bucket needs a globally unique identifier and a specific geographic location for where it should be stored.

Objects stored in Cloud Storage are immutable, which means that you can't edit them but instead create new versions whenever changes are made.

There's the possibility to decide whether or not to enable versioning for your bucket. With versioning enabled, you can keep track of the change history for your objects
![Alt text](image-13.png)

### Lifecycle Policies in Cloud Storage
Because storing and retrieving large amount of objects can become expensive or you may want to automatically delete specific data after a certain amount of time, there's lifecycle policies featured in Cloud Storage.
![Alt text](image-14.png)

## Cloud Storage: Storage Classes and data transfers
There are four primary storage classes in Cloud Storage
![Alt text](image-15.png)
![Alt text](image-16.png)

## Cloud SQL  
![Alt text](image-17.png)
There's no mundane infrastructure tasks which you have to do. Google handles applying patches/updates, manages backups, and configures replications.
All this to reduce the amount of mundane tasks you have to do and instead you can focus on building great applications.

![Alt text](image-18.png)

## Cloud Spanner  
![Alt text](image-19.png)

## Firestore
Firestore is a flexible, horizontally scalable, NoSQL cloud database.
![Alt text](image-20.png)

**When using Firestore, this is what you're charged for**
![Alt text](image-21.png)
You can also estimate your costs by using Google's Billing Calculator.

![Alt text](image-22.png)

## Cloud Bigtable
Cloud Bigtable is Googles NoSQL BigData database service.  
![Alt text](image-23.png)

Here's when customers often choose Cloud Bigtable as their storage
![Alt text](image-24.png)

## Comparing Storage Options in GCP
![Alt text](image-25.png)

### LAB NOTES
**Configurations for the VM containing the running Apache Webserver** 
Internal IP = 10.142.0.2
External IP = http://35.231.117.73/

**Creating a Cloud Storage bucket using the gcloud storage command line**  
  
*Inside the Cloud Shell:*
  
For convenience, enter your chosen location into an environment variable called LOCATION:
```sh
export LOCATION=EU
```
  
Enter this command to make a bucket named after your project ID, where $DEVSHELL_PROJECT_ID is your GCP Project ID:
```sh
gcloud storage buckets create -l $LOCATION gs://$DEVSHELL_PROJECT_ID
```
  
Retrieve a banner image from a publicly accessible Cloud Storage location:
```sh
gcloud storage cp gs://cloud-training/gcpfci/my-excellent-blog.png my-excellent-blog.png
```  
  
Copy the banner image to your newly created Cloud Storage bucket:
```sh
gcloud storage cp my-excellent-blog.png gs://$DEVSHELL_PROJECT_ID/my-excellent-blog.png
```  
  
Modify the Access Control List of the object you just created so that it's readable by everyone:
```sh
gsutil acl ch -u allUsers:R gs://$DEVSHELL_PROJECT_ID/my-excellent-blog.png
```
  
Here's the URL to the image I have stored in Cloud Storage: https://storage.googleapis.com/qwiklabs-gcp-02-52e51ec4d04c/my-excellent-blog.png  
![Alt text](image-26.png)

**Create a MySQL Database using Cloud SQL**  
I created a MySQL database using Cloud SQL.
The default admin user is added when creating the database but I also created another user.
Then, I connect the db with the VM by adding a network to our database using the external IP of our VM (35.231.117.73/32)