FROM debian:8-slim

ENV ORACLE_CLIENT_TYPE basiclite
ENV ORACLE_CLIENT_VERSION 12.2 
ENV ORACLE_CLIENT_FULL_VERSION 12.2.0.1.0
ENV ZIP_NAME instantclient-$ORACLE_CLIENT_TYPE-linux.x64-$ORACLE_CLIENT_FULL_VERSION.zip 
ENV INSTANT_DIR instantclient_12_2
ENV LD_LIBRARY_PATH /usr/lib:/usr/local/lib:/usr/lib/oracle/

RUN apt-get update && apt-get install -y --no-install-recommends \
    libaio1 \
    unzip \ 
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir /opt/oracle && cd /opt/oracle

RUN wget https://raw.githubusercontent.com/mrfoe7/minify-oracle-client/master/clients/$ORACLE_CLIENT_VERSION/$ZIP_NAME

RUN unzip $ZIP_NAME
RUN mv $INSTANT_DIR /usr/lib/oracle/ && rm -rf /opt/oracle

RUN apt-get purge -y --auto-remove unzip wget

RUN apt-get clean --dry-run

RUN ln -s /usr/lib/oracle/libclntsh.so.$ORACLE_CLIENT_VERSION /usr/lib/oracle/libclntsh.so
RUN ln -s /usr/lib/oracle/libocci.so.$ORACLE_CLIENT_VERSION/usr/lib/oracle/libocci.so