# Local environment on Windows Subsystem for Linux Distribution for NeMo work

conda create -n nemo_onnx Python=3.7

pip install Cython

pip install nemo_toolkit[all]

conda install -c conda-forge jupyterlab #optional

sudo apt-get install sox libsndfile1 ffmpeg

pip install text-unidecode

pip install torchaudio>=0.10.0 -f https://download.pytorch.org/whl/torch_stable.html

