FROM mcr.microsoft.com/devcontainers/cpp:1-ubuntu-20.04

ARG REINSTALL_CMAKE_VERSION_FROM_SOURCE="3.22.2"

# Optionally install the cmake for vcpkg
COPY ./reinstall-cmake.sh /tmp/

RUN if [ "${REINSTALL_CMAKE_VERSION_FROM_SOURCE}" != "none" ]; then \
    chmod +x /tmp/reinstall-cmake.sh && /tmp/reinstall-cmake.sh ${REINSTALL_CMAKE_VERSION_FROM_SOURCE}; \
    fi \
    && rm -f /tmp/reinstall-cmake.sh

# [Optional] Uncomment this section to install additional vcpkg ports.
# RUN su vscode -c "${VCPKG_ROOT}/vcpkg install <your-port-name-here>"

# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install gcc g++ gfortran liblapack3 libtbb2 libcliquer1 libopenblas-dev libgsl23 patchelf

#  Install SoPlex
RUN cd /tmp \
    && git clone https://github.com/scipopt/soplex.git \
    && cd soplex\
    && mkdir -p build\
    && cd build\
    && cmake .. \
    && sudo make \
    && sudo make install


RUN cd /tmp\
    && wget 'https://www.scipopt.org/download/release/SCIPOptSuite-8.0.4-Linux-ubuntu.deb' \
    && sudo apt install ./SCIPOptSuite-8.0.4-Linux-ubuntu.deb -y

