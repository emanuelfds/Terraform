FROM alpine

LABEL Description="Kubernetes tools - Emanuel Fernandes"

ARG TERRAFORM_VERSION=1.7.4

#-- Install Git --#
RUN apk fix && \
    apk --no-cache --update add busybox-extras make curl curl-dev git git-lfs gpg less openssh-client patch coreutils && \
    git lfs install

#-- Install Terraform --#
 RUN wget https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
     unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip && rm terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
     mv terraform /usr/bin/terraform