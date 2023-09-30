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

