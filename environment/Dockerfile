# DO NOT EDIT, This Dockerfile is generated from ./tools/10_generate_Dockerfile.sh
FROM bjodah/bjodahimg:latest
MAINTAINER Björn Dahlgren <bjodah@DELETEMEgmail.com>
ENV PATH /opt/miniconda2/bin:$PATH
RUN conda install conda-build gmp numpy cython cmake patchelf && \
    conda config --set always_yes yes && \
    conda config --set changeps1 no && \
    conda clean -t
RUN python2.7 -m pip install git+https://github.com/bjodah/cyipopt.git && \
    python3.4 -m pip install git+https://github.com/bjodah/cyipopt.git
