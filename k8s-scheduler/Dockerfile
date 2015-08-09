FROM ubuntu:14.04

ENV KUBE_VERSION 1.0.1

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kube-scheduler -z /opt/bin/kube-scheduler https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kube-scheduler
RUN chmod +x /opt/bin/kube-scheduler

ENTRYPOINT ["/opt/bin/kube-scheduler"]
