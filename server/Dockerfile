FROM buildpack-deps:stretch

ARG JDK_TAG=8u191
ARG JDK_B=b12

ADD https://github.com/ojdkbuild/contrib_jdk8u-ci/releases/download/jdk${JDK_TAG}-${JDK_B}/jdk-${JDK_TAG}-ojdkbuild-linux-x64.zip /

RUN apt-get update && apt-get install -y --no-install-recommends \
		unzip \
	&& rm -rf /var/lib/apt/lists/*

RUN set -x \
 && mkdir -p /opt \
 && cd /opt       \
 && unzip -qq /jdk-${JDK_TAG}-ojdkbuild-linux-x64.zip \
 && ln -s jdk-${JDK_TAG}-ojdkbuild-linux-x64 jdk-1.8  \
 && cd /                       \
 && tar -cJf rootfs.tar.xz opt \
 && rm -rf /opt

