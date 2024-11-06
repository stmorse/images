# use Hugging Face transformers image (includes torch/gpu/cuda)
FROM huggingface/transformers-pytorch-gpu:latest

# Install additional packages and clean up apt cache
RUN apt-get update && \
    rm -rf /var/lib/apt/lists/* /var/cache/apt/* /tmp/*

# Install Python packages with pip and clean up pip cache
RUN pip install --no-cache-dir \
    scikit-learn matplotlib && \
    rm -rf /root/.cache/pip /tmp/*

# install additional required Python libraries
# RUN pip install --no-cache-dir matplotlib ipykernel scikit-learn

# verify CUDA installation during image build
RUN python3 -c "import torch; print('CUDA available:', torch.cuda.is_available())"

# Set the entrypoint to Python if used inline
ENTRYPOINT ["python3"]
