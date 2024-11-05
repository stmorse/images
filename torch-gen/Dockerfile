# start from a base image with PyTorch and CUDA 12.4 support
FROM nvidia/cuda:12.4.0-runtime-ubuntu20.04

# Set up environment variables
ENV DEBIAN_FRONTEND=noninteractive
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

# Install basic utilities and Python dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        python3 python3-pip python3-dev && \
        rm -rf /var/lib/apt/lists/*

# Install PyTorch with CUDA support
RUN pip install --no-cache-dir torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu124

# Install required Python libraries
RUN pip install --no-cache-dir \
    numpy \
    pandas \
    scikit-learn \
    matplotlib \
    sentence-transformers

# Verify CUDA installation (optional, for debugging)
RUN python3 -c "import torch; print('CUDA available:', torch.cuda.is_available())"

# Set the entrypoint to Python for easy script running (optional)
ENTRYPOINT ["python3"]

