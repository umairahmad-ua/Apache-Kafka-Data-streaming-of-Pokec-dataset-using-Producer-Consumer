# Apache-Kafka-Pokec-to-Producer-and-Consumer-to-Firebase
# Introduction

---

**Learning Goals & Outcomes**
To Learn to analyze substantial real-world big data of a social network (1.69GB in
size).
- Explore effective use of Apache Kafka to process data.
- Applying graph mining algorithms on streaming data.
- Dynamic Visualizations.



## Input Data

Pokec is the most popular online social network in Slovakia. Pokec has been
provided for more than 10 years and connects more than 1.6 million people. Datasets
contain anonymized data of the whole network. Profile data contains gender, age,
hobbies, interest, education, etc. Profile data are in the Slovak language. Friendships in
Pokec are oriented.
This social network has connected more than 1.6 million people and posses more
than 50 attributes for each person.


# Installation Of Kafka

---



We have run the following steps to run the Kafka server.
We required java before installing kafka on local PC
Downloading the KAFKA  from https://kafka.apache.org/downloads”


-	mkdir kafka 
-	cd kafka
-	Tar –xvzf ~/Downloads/kafka.tgz --strip 1


Check the properties:

bin/kafka-server-start.sh config/server.properties but got the error 


then run Zookeeper by running the command

-	bin/zookeeper-server-start.sh config/zookeeper.properties

Run the  following command in the kafka folder

-	bin/kafka-server-start.sh config/server.properties
After this running on localhost:2181 
- 1 Kafka server (broker) running on localhost:9092
Listing out the topics and generating the new topic.
bin/kafka-topics.sh --bootstrap-server localhost:9092 –list
-	cd /tmp/kafka-logs 
-	 ls 
-	 cd city-0/ 
-	Ls





These are the screenshots of initializing Kafka

# Task 1: Data Streaming
a. You have to read and store the profile file before streaming relationship data so
that you can process nodes. To emulate streaming data you have to read the
relationship file in batches/chunks after the fixed time interval using Kafka.

---


b. You also need to store streaming data in the Database(The consumer will store the
streaming data in a Database).

# Analysis Report



In task 1 of Data streaming we are assigned to do data streaimg of pokec dataset which is about 1.6 GB and pokec dataset is not so organized and clean dataset. we performed pre-processing for that. 

we face problem while installation.Before installation of Kafka we needed JVM.but there server missing problem Firstly Kafka ran properly but nodes were blocking temporarily and every time we had to create new topic so we deleted the log files to overcome this problem.And we got to know that zookeeper should be firstly running form and we are dependent to create topic before creating producer consumer because both can not send and receive data respectively.We used Kafka Connectors but was getting many errors for the same. After that we learned about using python with kafka but we are dependent to use local setup like jupyter notebook. We couldn't use colab for kafka Streaming. 

We also faced Issues regarding storing big stream data in database, faced database connectivity issues. so we resolved that issue by using real time database which is Firebase Data base


Tools: kafka,Java,Jupyter

