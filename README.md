## Requirements:
>* Mac computers with Apple silicon or AMD GPUs
>* macOS 12.0 or later (Get the latest beta)
>* Python 3.9 or later (3.9.6)
>* Xcode command-line tools: xcode-select --install

## Create virtual environment and activate
``` 
python3 -m venv venv
source venv/bin/activate
```

## Install library requirements.txt
```
pip install -r requirements.txt
```

## Run Test in termnal (python):
```python
import tensorflow as tf
tf.test.is_gpu_available() #This will return True if GPU is enable
```
---
## OR python file (VS code):
```python
import tensorflow as tf
print("Num GPUs Available: ", len(tf.configlist_physical_devices('GPU')))
#This will return "Num GPUs Available:  1" if there is GPU in your device
```
***
# (Options) if you want to try to install the libraries without requiements.txt
## Install TensorFlow
``` 
pip install tensorflow==2.14.0
or
pip install tensorflow_macos==2.14.0
```

## Install Tensorflow metal for mac (Enable GPU)
```cmd
pip install tensorflow_metal
or 
pip install tensorflow_metal==1.1.0
```

## Bug
To fix the bug about:
```
TypeError: Unable to convert function return value to a Python type! The signature was
        () -> handle
```
Run:
```
pip install numpy==1.24.0
```
Or Search:
```
A module that was compiled using NumPy 1.x cannot be run in
NumPy 2.0.2 as it may crash. To support both 1.x and 2.x
versions of NumPy, modules must be compiled with NumPy 2.0.
Some module may need to rebuild instead e.g. with 'pybind11>=2.12'
```