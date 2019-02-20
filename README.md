Install RabbitMQ Server: https://www.rabbitmq.com/install-windows.html
Download three files:
- Client library: http://central.maven.org/maven2/com/rabbitmq/amqp-client/5.5.1/amqp-client-5.5.1.jar
- API Dependencies: http://central.maven.org/maven2/org/slf4j/slf4j-api/1.7.25/slf4j-api-1.7.25.jar
- Simple dependencies: http://central.maven.org/maven2/org/slf4j/slf4j-simple/1.7.25/slf4j-simple-1.7.25.jar

Create a new working folder and place all the three files above into that.

Compile the Client and Server:
javac –cp amqp-client-5.5.1.jar RPCClient.java RPCServer.java

Run:
java -cp .;amqp-client-5.5.1.jar;slf4j-simple-1.7.25.jar;slf4j-api-1.7.25.jar RPCServer
java -cp .;amqp-client-5.5.1.jar;slf4j-simple-1.7.25.jar;slf4j-api-1.7.25.jar RPCClient

Try in a separated command window:
rabbitmqctl.bat list_queues name messages_ready messages_unacknowledged