# demucs-pyinstaller

## 创建虚拟环境
### 1. 使用pip
```
# 提前安装 pyinstaller
pip install pyinstaller

pip install virtualenv
````
### 2. 创建运行环境
```
virtualenv venv --no-setuptools --no-wheel
```

### 3. 激活环境
```
linux:

$ cd venv
$ source ./bin/activate
Windows 10:

> cd venv
> .\Scripts\activate.bat
```

### 4. 退出环境
```
linux:

$ deactivate

Windows 10:

> .\Scripts\deactivate.bat
```

## 安装依赖
### With CUDA support (Windows & Linux)
```
pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116 demucs SoundFile
```
### CPU only (Any OS)
```
pip install torch torchvision torchaudio demucs SoundFile pyinstaller
```

### 查看已安装的包
```
./venv/bin/pip freeze
```

### 打包
```
pyinstaller separate.py
```