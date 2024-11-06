# use an official Python runtime as a parent image
FROM pytorch/pytorch:1.7.1-cuda11.0-cudnn8-devel

# Install PyTorch with CUDA support
# RUN pip install --no-cache-dir torch torchvision torchaudio

# Install required Python libraries
RUN pip install --no-cache-dir matplotlib ipykernel scikit-learn

# Verify CUDA installation (optional, for debugging)
RUN python3 -c "import torch; print('CUDA available:', torch.cuda.is_available())"

# Set the entrypoint to Python if used inline
ENTRYPOINT ["python3"]

