### Word counting using Map Reduce Hadoop framework in Java

This practical example is for creating map reduce implementation in AWS EMR cluster with S3.

Custom JAR is used to run the job in the cluster.

#### Step 1

Create S3 bucket in AWS and upload `books-input` folder to that S3 bucket.

#### Step 2

Open this Java project in the IntelliJIdea and go to `File > Project Structure > Add > JAR > From modules with dependencies...` and select the Main Class `WordCount` and ok to all.

#### Step 3.1 (Pre validation)

Run `WordCount.java` file to check any compilation issues and check `mvn clean package` can package it properly without any issue. 

#### Step 3.2

Now go to `Build > Build Artifact > Build` and in the `out` folder find the `wordcount.jar` and upload it to the S3 bucket.

#### Step 4

Create a AWS EMR cluster and create a new step with `Custom JAR` option. Select JAR from S3 bucket and add `books-input` folder path in arguments section along with the `s3://<bucket-name>/books-output` in the next line.

[Sample Video Guide](https://youtube.com/playlist?list=PLix7MmR3doRoV9tlNy84ZeX6fHlTavoaG)