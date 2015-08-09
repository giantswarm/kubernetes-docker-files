FROM ubuntu:14.04

ENV KUBE_VERSION 1.0.1

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kubectl -z /opt/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kubectl
RUN chmod +x /opt/bin/kubectl

ENTRYPOINT ["/opt/bin/kubectl"]
