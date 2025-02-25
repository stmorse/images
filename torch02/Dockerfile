M nvidia/cuda:8.0-cudnn5-runtime-ubuntu16.04

# Install Python 3.6 from deadsnakes and other deps
RUN apt-get update && apt-get install -y software-properties-common \
    && add-apt-repository ppa:deadsnakes/ppa \
    && apt-get update && apt-get install -y \
       python3.6 python3.6-dev python3-pip \
       libopenblas-dev liblapack-dev \
    && rm -rf /var/lib/apt/lists/*

# Install GPU-enabled PyTorch 0.2 (CUDA 8.0)
RUN pip3 install --no-cache-dir \
    https://download.pytorch.org/whl/cu80/torch-0.2.0.post2-cp36-cp36m-linux_x86_64.whl

WORKDIR /app
COPY . /app

CMD ["python3.6", "your_script.py"]

