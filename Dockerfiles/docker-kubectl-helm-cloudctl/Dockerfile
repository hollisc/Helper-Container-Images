FROM alpine

RUN ls
RUN pwd
RUN ls -la /usr/local/bin

ENV KUBE_LATEST_VERSION="v1.15.0"

RUN apk add --no-cache --update ca-certificates curl jq

ADD https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl /usr/local/bin/kubectl
RUN chmod +x /usr/local/bin/kubectl

Add https://get.helm.sh/helm-v2.14.3-linux-amd64.tar.gz /usr/local/bin/helm
RUN chmod +x /usr/local/bin/helm

RUN ls -la /usr/local/bin

COPY resources /usr/local/bin/
RUN chmod +x /usr/local/bin/cloudctl-linux-ppc64le-3.1.2-1203

RUN ls -la /usr/local/bin
