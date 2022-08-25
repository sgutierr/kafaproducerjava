Create a topic named total-connected-devices through a template call create-topic

oc process \
 -f resources/create-topic.yaml \
 -p TOPIC_NAME='total-connected-devices' \
 | oc apply -f -

1. Modify ProducerApp adding connection settings and the capability to send random messages
2. Compile the application: [user@host plain]$ ./mvnw clean package