FROM python:3.10-slim

ENV NVIDIA_VISIBLE_DEVICES=all
ENV LD_LIBRARY_PATH=/usr/local/nvidia/lib64

WORKDIR /DNA-Diffusion
COPY . .

RUN apt-get update && \
    apt-get install -y \
    build-essential \
    zlib1g-dev \
    git

RUN pip install --upgrade pip && \
    # https://github.com/htseq/htseq/blob/4ea41e5bfee4d94dd5da62816130e805e31f3a87/setup.py#L82
    pip install numpy && \
    pip install -e .
