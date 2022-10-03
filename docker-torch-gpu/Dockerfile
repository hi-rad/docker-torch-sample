ARG DIST_ID
FROM nvidia/cuda:11.6.0-runtime-${DIST_ID}
ARG DEBIAN_FRONTEND=noninteractive
ADD . /code
WORKDIR /code
# Install Python and its tools
RUN apt update && apt install -y --no-install-recommends \
    git \
    build-essential \
    python3.9 \
    python3-pip \
    python3-setuptools

RUN pip3 -q install pip --upgrade
RUN pip3 install -r requirements.txt --find-links https://download.pytorch.org/whl/cu116
