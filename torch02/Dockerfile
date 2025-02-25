FROM python:3.6

# Install system libs (modify as needed)
RUN apt-get update && apt-get install -y \
    libopenblas-dev liblapack-dev \
 && rm -rf /var/lib/apt/lists/*

# Install PyTorch 0.2 (CPU-only build)
RUN pip install --no-cache-dir \
    https://download.pytorch.org/whl/cu75/torch-0.2.0.post3-cp36-cp36m-manylinux1_x86_64.whl

RUN pip install --no-cache-dir matplotlib

WORKDIR /app

#CMD ["python"]

