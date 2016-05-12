FROM debian:jessie

ENV DEBIAN_FRONTEND noninteractive
ENV KUBE_VERSION 1.2.4

RUN apt-get update
RUN apt-get -yy -q install curl iptables ca-certificates

RUN curl -L -o /kube-proxy -z /kube-proxy https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kube-proxy
RUN chmod a+rx /kube-proxy

ENTRYPOINT ["/kube-proxy"]
