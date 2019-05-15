FROM eitanyaffe/hpipe_base:v1.2

ENV MAKESHIFT_ROOT /ms_root

RUN mkdir ${MAKESHIFT_ROOT}
WORKDIR ${MAKESHIFT_ROOT}

# clone code from git
RUN \
git clone https://github.com/eitanyaffe/makeshift-core.git && \
git clone https://github.com/eitanyaffe/makeshift-modules.git && \
git clone --branch dev https://github.com/eitanyaffe/hpipe:dev

# compile binaries
WORKDIR ${MAKESHIFT_ROOT}/hpipe/pipeline
RUN make init

