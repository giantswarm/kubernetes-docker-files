FROM ubuntu:14.04

ENV KUBE_VERSION 1.0.1

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kube-controller-manager -z /opt/bin/kube-controller-manager https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kube-controller-manager
RUN chmod +x /opt/bin/kube-controller-manager

COPY ./keys/kube-serviceaccount.key /opt/bin/kube-serviceaccount.key

ENTRYPOINT ["/opt/bin/kube-controller-manager"]
