FROM alpine

ENV KUBE_LATEST_VERSION="v1.15.0"
ENV HELM_VERSION="v2.14.2"

RUN apk add --no-cache --update ca-certificates curl jq

RUN wget -q https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl -O /usr/local/bin/kubectl \
&& chmod +x /usr/local/bin/kubectl

RUN wget -q https://storage.googleapis.com/kubernetes-helm/helm-${HELM_VERSION}-linux-amd64.tar.gz -O - | tar -xzO linux-amd64/helm > /usr/local/bin/helm \
&& chmod +x /usr/local/bin/helm

COPY resources /usr/local/bin/
RUN chmod 755 /usr/local/bin/cloudctl-linux-amd64-3.1.2-1203
RUN mv /usr/local/bin/cloudctl-linux-amd64-3.1.2-1203 /usr/local/bin/cloudctl

RUN cloudctl --help
RUN ls -la /usr/local/bin
