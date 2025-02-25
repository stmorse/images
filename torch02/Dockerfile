FROM python:3.6

# Install system libs (modify as needed)
RUN apt-get update && apt-get install -y \
    libopenblas-dev liblapack-dev \
 && rm -rf /var/lib/apt/lists/*

# Install PyTorch 0.2 (CPU-only build)
RUN pip install --no-cache-dir \
    https://download.pytorch.org/whl/cpu/torch-0.2.0.post2-cp36-cp36m-linux_x86_64.whl

WORKDIR /app
COPY . /app

CMD ["python", "your_script.py"]

