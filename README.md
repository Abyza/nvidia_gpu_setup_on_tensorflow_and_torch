# nvidia_gpu_setup_on_tensorflow_and_torch

This is what I found and it works for me

################
This is for conda you would need yo install conda make a virtual environment in conda then run the code below
you can open the conda virtual environment in vscode
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
Anything above 2.10 is not supported on the GPU on Windows Native
python -m pip install "tensorflow<2.11"
Verify the installation:
python -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
####################

Tips
1. pip install tensorflow-gpu no longer works gpu is already included in base tensorflow install
2. make sure you have the correct version for everything considering your device gpu
3. most tutorials out there uses conda if you wishes to be in a conda environment follow other tutorials but this tutorials works on everthing
4. I use this on VS Code venv of python 
5. my device is a laptop with a 3050 nvidia gpu
6. in A.I. model training if it is an advance model it will not work on CPU
7. Some models might train with CPU only but decrease in training time is decreased very exponentially if GPU is used
8. Even if you use your GPU it may still be incapable of training more advance models.
