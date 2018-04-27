FROM microsoft/dotnet-buildtools-prereqs:ubuntu-16.04-cross-e435274-20180426002255
MAINTAINER Gleb Balykov <g.balykov@samsung.com>

# Add armel rootfs of Tizen 4.0 for cross building coreclr and corefx
RUN apt-get update && apt-get install -y binutils-arm-linux-gnueabi
