FROM debian:8-slim

RUN apt-get update 
RUN apt-get install -y libaio1 unzip

COPY ../../instantclient-basiclite-linux.x64-12.1.0.2.0.zip /opt/oracle

RUN unzip /opt/oracle/instantclient-basiclite-linux.x64-12.1.0.2.0.zip
# RUN mv   /usr/lib/oracle/

# ENV LD_LIBRARY_PATH /usr/lib:/usr/local/lib:/usr/lib/oracle/

RUN apt-get purge unzip

RUN apt-get clean --dry-run

# RUN ln -s /usr/lib/oracle/libclntsh.so.12.1 /usr/lib/oracle/libclntsh.so
# RUN ln -s /usr/lib/oracle/libocci.so.12.1 /usr/lib/oracle/libocci.so

CMD ["ping", "localhost"]