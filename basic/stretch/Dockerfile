FROM debian:8-slim

RUN apt-get update 
RUN apt-get install --no-cache -y libaio1

COPY installclient-basic-

ENV LD_LIBRARY_PATH /usr/lib:/usr/local/lib:/usr/lib/oracle/

RUN apt-get clean --dry-run

RUN ln -s /usr/lib/oracle/libclntsh.so.12.1 /usr/lib/oracle/libclntsh.so
RUN ln -s /usr/lib/oracle/libocci.so.12.1 /usr/lib/oracle/libocci.so