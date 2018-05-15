FROM gbalykov/dotnet-buildtools-prereqs:ubuntu-16.04-cross-e435274-20180426002255
MAINTAINER Gleb Balykov <g.balykov@samsung.com>

# Add armel rootfs of Tizen 4.0 for cross building coreclr and corefx
ADD rootfs.armel.tizen.build.4.0m2.tar.gz /crossrootfs
ADD rootfs.armel.tizen.test.4.0m2.tgz /crossrootfs/armel.tizen.test

RUN apt-get update
RUN apt-get install -y clang-4.0 clang++-4.0
RUN rm -rf /usr/bin/clang /usr/bin/clang++
RUN ln -s /usr/bin/clang-4.0 /usr/bin/clang
RUN ln -s /usr/bin/clang++-4.0 /usr/bin/clang++
