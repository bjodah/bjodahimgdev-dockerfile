# DO NOT EDIT, This Dockerfile is generated from ./tools/10_generate_Dockerfile.sh
FROM bjodah/bjodahimg:latest
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
ENV PATH /opt/miniconda2/bin:$PATH
RUN conda install conda-build gmp numpy cython cmake patchelf && \
    conda config --set always_yes yes && \
    conda config --set changeps1 no && \
    conda clean -t && \
    wget -O - http://llvm.org/apt/llvm-snapshot.gpg.key | apt-key add - && \
    echo "deb http://llvm.org/apt/trusty/ llvm-toolchain-trusty-3.8 main" | tee -a /etc/apt/sources.list && \
    apt-get update -qq && \
    apt-get --assume-yes install clang-3.8 libclang1-3.8 libllvm3.8 llvm-3.8-dev lldb-3.8 llvm-3.8 llvm-3.8-runtime clang-format-3.8 python-clang-3.8
RUN python2.7 -m pip install git+https://github.com/bjodah/cyipopt.git && \
    python3.4 -m pip install git+https://github.com/bjodah/cyipopt.git
