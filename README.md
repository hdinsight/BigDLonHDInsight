# Introduction to Deep Learning on HDInsight with Intel Deep Learning framework: BigDL (R) Intel

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Microsoft_logo_%282012%29.svg/1280px-Microsoft_logo_%282012%29.svg.png" height="60px">&nbsp;&nbsp;&nbsp;<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Intel-logo.svg/2000px-Intel-logo.svg.png" height="60px">

## Presenters
* Denny Lee, Principal Program Manager, CosmosDB 
* Tom Drabas, Data Scientist, WDG

## In close cooperation with Intel
* Sergey Ermolin, Power/Performance Optimization
* Ding Ding, Software Engineer
* Jiao Wang, Software Engineer
* Jason Dai, Senior Principle Engineer and CTO, Big Data Technologies
* Yiheng, Wang, Software Engineer
* Xianyan Jia, Software Engineer

## Special thanks to
* Felix Cheung, Principal Software Engineer
* Xiaoyong Zhu, Program Manager
* Alejandro Guerrero Gonzalez, Senior Software Engineer

---------

# Setting up the environment

### 1. Clone the Github repository

The folders in this repo:

1. **data** folder - contains a set of 4 files that can be downloaded from http://yann.lecun.com/exdb/mnist/:
    1. *train-images-idx3-ubyte* - set of training images in a binary format with a specific schema (we'll get to that)
    2. *train-labels-idx1-ubyte* - corresponding set of training labels
    3. *t10k-images-idx3-ubyte* - set of testing (validation) images
    4. *t10k-labels-idx1-ubyte* - corresponding set of testing (validation) labels
2. **jars** folder - contains two compiled jars for the BigDL:
    1. *bigdl-0.2.0-SNAPSHOT-spark-2.0-jar-with-dependencies.jar* - BigDL compiled for Spark 2.0
    2. *bigdl-0.2.0-SNAPSHOT-spark-2.1-jar-with-dependencies.jar* - BigDL compiled for Spark 2.1
3. **notebook** folder - contains the notebook for the workshop

### 2. Upload BigDL jar

Grab the jar from the **jars** folder appropriate for your version of Spark.

1. Go to Azure Dashboard and click on your cluster. Scroll down to the Storage accounts ![Storage options](http://tomdrabas.com/data/BigDL/StorageAccount.png)
2. Click on the default storage account ![Default storage](http://tomdrabas.com/data/BigDL/DefaultStorageAccount.png)
3. Go to Blobs ![Blobs](http://tomdrabas.com/data/BigDL/Blobs.png)
4. Select the default container 
![Container](http://tomdrabas.com/data/BigDL/DefaultContainer_obs.png)
5. Upload the jar appropriate for your version of Spark to the root of the folder ![Upload](http://tomdrabas.com/data/BigDL/Upload_obs.png)
6. Check if uploaded successfully ![Uploaded](http://tomdrabas.com/data/BigDL/UploadedJar.png)

### 3. Upload the data

Similarly to uploading the BigDL upload the data from the **data** folder. Upload the data into the `/tmp` folder in your default storage.