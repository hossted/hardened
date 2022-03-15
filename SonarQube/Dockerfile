FROM sonarqube:latest


RUN apk update && apk add --upgrade libuuid expat
RUN apk add wget

# Download patched out elasticsearch
RUN wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.16.3-linux-x86_64.tar.gz
RUN tar xvf elasticsearch-7.16.3-linux-x86_64.tar.gz
RUN mv elasticsearch/modules/ /tmp/
RUN rm -fr elasticsearch
RUN mv elasticsearch-7.16.3 elasticsearch
RUN rm -fr elasticsearch/modules/
RUN cp -r /tmp/modules/ elasticsearch/
COPY src/elasticsearch elasticsearch/bin/elasticsearch
RUN chmod +x elasticsearch/bin/elasticsearch 

# RUN rm /opt/sonarqube/elasticsearch/lib/jackson-dataformat-cbor-2.10.4.jar && wget https://repo1.maven.org/maven2/com/fasterxml/jackson/dataformat/jackson-dataformat-cbor/2.13.2/jackson-dataformat-cbor-2.13.2.jar -P /opt/sonarqube/elasticsearch/lib/

# RUN rm /opt/sonarqube/elasticsearch/modules/transport-netty4/netty-codec-4.1.66.Final.jar && wget https://repo1.maven.org/maven2/io/netty/netty-codec/4.1.68.Final/netty-codec-4.1.68.Final.jar -P /opt/sonarqube/elasticsearch/modules/transport-netty4/

# download patched java libs

RUN rm /opt/sonarqube/lib/jdbc/postgresql/postgresql-42.3.1.jar && wget https://repo1.maven.org/maven2/org/postgresql/postgresql/42.3.3/postgresql-42.3.3.jar -O /opt/sonarqube/lib/jdbc/postgresql/postgresql-42.3.1.jar 

# RUN rm /opt/sonarqube/lib/jdbc/h2/h2-1.4.199.jar && wget https://repo1.maven.org/maven2/com/h2database/h2/2.1.210/h2-2.1.210.jar -O /opt/sonarqube/lib/jdbc/h2/h2-1.4.199.jar

