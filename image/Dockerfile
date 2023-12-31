# Start from a base image
FROM alpine:3.14

# Install dependencies
RUN apk --no-cache add \
    curl \
    python3 \
    py3-pip \
    bash \
    libc6-compat \
    openssh-client \
    git

# Install gcloud
ENV CLOUD_SDK_VERSION 359.0.0
ENV PATH /google-cloud-sdk/bin:$PATH
RUN curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-${CLOUD_SDK_VERSION}-linux-x86_64.tar.gz && \
    tar xzf google-cloud-sdk-${CLOUD_SDK_VERSION}-linux-x86_64.tar.gz && \
    rm google-cloud-sdk-${CLOUD_SDK_VERSION}-linux-x86_64.tar.gz && \
    ln -s /lib /lib64 && \
    gcloud config set core/disable_usage_reporting true && \
    gcloud config set component_manager/disable_update_check true && \
    gcloud config set metrics/environment github_docker_image && \
    gcloud --version

# Install kubectl
RUN gcloud components install kubectl

# Verify the installations
RUN gcloud --version && kubectl version --client
