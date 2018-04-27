FROM gbalykov/dotnet-buildtools-prereqs:ubuntu-16.04-cross-e435274-20180426002255
MAINTAINER Gleb Balykov <g.balykov@samsung.com>

# Instal qemu prerequisites
RUN apt-get update && apt-get install -y pkg-config libglib2.0-0 libglib2.0-dev libglib2.0-bin libglib2.0-cil libglib2.0-cil-dev libglib2.0-data libpixman-1-0 libpixman-1-dev bison flex

# Install latest qemu 2.12.0
RUN which qemu-arm-static
RUN qemu-arm-static -version
ADD qemu-2.12.0.tar.xz /qemu-2.12.0
RUN cd /qemu-2.12.0/qemu-2.12.0; mkdir build; cd build; ../configure; make; make install
RUN which qemu-arm-static 
RUN qemu-arm-static -version
