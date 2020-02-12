#Connectors are packaged as Kafka Connect plugins. Kafka Connect isolates each plugin so that the plugin libraries do not conflict with each other.


#source for connector
Download ZIP file of kafka connect s3 connector from Confluent Hub

#quickstart-schema-source-for-s3.properties
Add the plugin.path=/usr/local/share/kafka/plugins (for ExampleC:/kafka_connect_s3) to the worker configuration properties file
Add offset.storage.file.filename=C:/kafka_connect_s3/tmp/connect.offsets to the worker configuration file.

#quickstart-s3.properties
Add the s3 properties (kafka topic name and bucket name) to the s3 configuration file

#AWS properties
Add  AWS_SECRET_ACCESS_KEY (same format) and AWS_ACCESS_KEY_ID (same format) of the aws to the environment variable (variable system)

#running zookeeper and kafka
Run Zookeeper in windows, (.\bin\windows\zookeeper-server-start .\config\zookeeper.properties)
Run Kafka in windows, (.\bin\windows\kafka-server-start .\config\server.properties)

#Run connector with standlone method
#bin\connect-standalone worker.properties connector1.properties

.\bin\windows\connect-standalone .\etc\quickstart-schema-source-for-s3.properties .\etc\quickstart-s3.properties

#kafka producer
create topic which is mentioned in the s3 config file and run producer for passing the messages





 
