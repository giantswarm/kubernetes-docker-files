FROM ubuntu:14.04

ENV KUBE_VERSION 1.2.4

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kube-apiserver -z /opt/bin/kube-apiserver https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kube-apiserver
RUN chmod +x /opt/bin/kube-apiserver

COPY ./keys/kube-serviceaccount.key /opt/bin/kube-serviceaccount.key

ENTRYPOINT ["/opt/bin/kube-apiserver"]
