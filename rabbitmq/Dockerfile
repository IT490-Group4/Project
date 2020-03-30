FROM rabbitmq:3
RUN apt-get update -y
	#apt-get install -y rabbitmq-server
    #apt-get install -y python-pip python-dev
	#apt-get install -y python-pip pika
EXPOSE 5672
EXPOSE 5673
EXPOSE 5674
EXPOSE 15672
EXPOSE 15673
EXPOSE 15674
EXPOSE 5672 15672 25672 4369 9100 9101 9102 9103 9104 9105

COPY . /app
COPY rabbitmq-cluster /usr/local/bin/
COPY pre-entrypoint.sh /
WORKDIR /app
ENTRYPOINT ["/pre-entrypoint.sh"]
CMD rabbitmq-plugins enable rabbitmq_management
CMD ["rabbitmq-cluster"]


