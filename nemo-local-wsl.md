# Local environment on Windows Subsystem for Linux Distribution for NeMo work

conda create -n nemo_onnx Python=3.7

pip install Cython

pip install nemo_toolkit[all]

conda install -c conda-forge jupyterlab #optional

sudo apt-get install sox libsndfile1 ffmpeg

pip install text-unidecode

conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch --force-reinstall

mkdir configs

