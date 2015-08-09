FROM ubuntu:14.04

ENV KUBE_VERSION 1.0.1

RUN mkdir -p /opt/bin
RUN apt-get update
RUN apt-get install -y curl
RUN curl -L -o /opt/bin/kubelet -z /opt/bin/kubelet https://storage.googleapis.com/kubernetes-release/release/v$KUBE_VERSION/bin/linux/amd64/kubelet
RUN chmod +x /opt/bin/kubelet

ENTRYPOINT ["/opt/bin/kubelet"]
