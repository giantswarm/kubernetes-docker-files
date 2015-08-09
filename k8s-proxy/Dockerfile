FROM ubuntu:14.04

ENV KUBE_VERSION 1.0.1

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kube-proxy -z /opt/bin/kube-proxy https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kube-proxy
RUN chmod +x /opt/bin/kube-proxy

ENTRYPOINT ["/opt/bin/kube-proxy"]
