# Copyright (c) 2022 codeperf.

FROM ubuntu:18.04

RUN apt-get update && \ 
    DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y gnupg2 ca-certificates

# install perf 
RUN apt-get update; \
  apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget

RUN apt-get install -y --no-install-recommends \
  linux-tools-$(uname -r) linux-headers-$(uname -r)

# check perf is available
RUN perf list

# # repository to install BCC
# RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 4052245BD4284CDD
# RUN echo "deb https://repo.iovisor.org/apt/bionic bionic main" > /etc/apt/sources.list.d/iovisor.list

# RUN apt-get update && \
#   DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
#   bcc-tools libbcc-examples linux-headers-$(uname -r)
