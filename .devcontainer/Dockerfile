# Use the official Ubuntu image as the base
FROM ubuntu:latest

# Set environment variables for Go
ENV GO_VERSION=1.24.2
ENV GOROOT=/usr/local/go
ENV GOPATH=/go
ENV PATH=$GOROOT/bin:$GOPATH/bin:$PATH

# Install essential packages
RUN apt-get update && apt-get install -y \
    curl \
    git \
    build-essential \
    vim \
    ca-certificates \
    software-properties-common \
    && apt-get clean

# Install Go
RUN curl -OL https://go.dev/dl/go${GO_VERSION}.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go${GO_VERSION}.linux-amd64.tar.gz && \
    rm go${GO_VERSION}.linux-amd64.tar.gz

# Verify Go installation
RUN go version

# Install Delve debugger
RUN go install github.com/go-delve/delve/cmd/dlv@latest

# Create directories for Go workspace
RUN mkdir -p /go/src /go/bin /go/pkg

# Set the working directory inside the container
WORKDIR /workspace
