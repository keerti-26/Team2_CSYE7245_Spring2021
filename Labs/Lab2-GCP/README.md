### Lab - GCP-Datalab/Dataflow/BigQuery 

### Team Members
#Keerti | #Priyanka Malpekar | #Tanvi Gurav
--- | --- | --- | 
001050173| 001302741| 001306848

#### Requirements

```
-In the Google Cloud Console, on the project selector page, select or create a Google Cloud project.
-Enabled the BigQuery, AI Platform, Cloud Source Repositories, Dataflow, and Datalab APIs.
```
#### What is GCP
Google Cloud Platform (GCP), offered by Google, is a suite of cloud computing services that runs on the same infrastructure that Google
uses internally for its end-user products, such as Google Search, Gmail, file storage, and YouTube. Alongside a set of management tools,
it provides a series of modular cloud services including computing, data storage, data analytics and machine learning.


#### Dataset
We used public Natality dataset to create an ML model to predict a baby's weight given a number of factors about the pregnancy and the baby's mother.
Clone the below training-analyst-path on Datalab instance and use babyweight notebook for our data processing and model creation.
```
https://github.com/GoogleCloudPlatform/training-data-analyst  
training-data-analyst/blogs/babyweight/babyweight.ipynb 
```
#### Launching Datalab

Open Cloud Shell. Unless otherwise noted, you execute the rest of the tutorial from inside Cloud Shell.

Run the following command to retrieve your project ID. Make a note of it for use later in this tutorial.
``` 
gcloud config list project --format "value(core.project)"
```
Create a Datalab instance:
```
datalab create --zone us-central1-a mydatalab
```
It can take a minute or more to create the instance. After the instance is created, Datalab displays the following output.
```
The connection to Datalab is now open and will remain
until this command is killed.
Click on the *Web Preview* (up-arrow button at top-left), select
*port 8081*, and start using Datalab.
We have to created a file format for data that will be stored in table
```
#### Cloning Datalab Notebook
In Datalab, create a new notebook by clicking the +Notebook icon in the upper left. The notebook opens in a new tab.
Copy and paste the following command in the first cell of the new notebook. 
```
!git clone https://github.com/GoogleCloudPlatform/training-data-analyst
```
In Datalab, open the notebook training-data-analyst/blogs/babyweight/babyweight.ipynb.

#### Perform preprocessing and Visualization
Project ID and Bucket setup in notebook
In the first cell, set the variable PROJECT to your project ID.
```
BUCKET = 'sunlit-adviser-303301-ml'
PROJECT = 'sunlit-adviser-303301'
REGION = 'us-central1'
```
Set the variable BUCKET to your bucket name in the first cell. For your bucket name, use your project ID as a prefix and my-bucket:
 project-ID-my-bucket
Leave REGION as us-central1.




