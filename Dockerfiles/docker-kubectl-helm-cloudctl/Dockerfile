FROM alpine

ENV KUBE_LATEST_VERSION="v1.15.0"

RUN apk add --no-cache --update ca-certificates curl jq

ADD https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl /usr/local/bin/kubectl
RUN chmod +x /usr/local/bin/kubectl

ADD https://172.16.52.184:8443/api/cli/cloudctl-linux-ppc64le /usr/local/bin/cloudctl-linux-ppc64le-3.1.2-1203
RUN chmod +x /usr/local/bin/cloudctl-linux-ppc64le-3.1.2-1203

Add https://172.16.52.184:8443/api/cli/helm-linux-amd64.tar.gz /usr/local/bin/helm
RUN chmod +x /usr/local/bin/helm
