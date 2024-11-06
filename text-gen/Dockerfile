# use Hugging Face transformers image (includes torch/gpu/cuda)
FROM huggingface/transformers-pytorch-gpu:latest

# install additional required Python libraries
RUN pip install --no-cache-dir matplotlib ipykernel scikit-learn

# verify CUDA installation during image build
RUN python3 -c "import torch; print('CUDA available:', torch.cuda.is_available())"

# Set the entrypoint to Python if used inline
ENTRYPOINT ["python3"]
