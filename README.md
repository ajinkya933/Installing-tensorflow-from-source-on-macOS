# Installing-tensorflow-from-source-on-macOS
This is documentation on how to install Tensorflow from source on macos


Step1: Install all dependencies:

```
pip install -U  pip six numpy wheel setuptools mock
pip install -U  keras_applications==1.0.6 --no-deps
pip install -U  keras_preprocessing==1.0.5 --no-deps
```
Step2: Install Bazel

```
sudo xcodebuild -license accept
wget "https://github.com/bazelbuild/bazel/releases/download/0.24.1/bazel-0.24.1-installer-darwin-x86_64.sh"
chmod +x bazel-0.24.1-installer-darwin-x86_64.sh
./bazel-0.24.1-installer-darwin-x86_64.sh --user
export PATH="$PATH:$HOME/bin"
bazel version
```

Step3: Install Tensorflow:
```
git clone https://github.com/tensorflow/tensorflow.git
cd tensorflow
./configure
bazel build --config=opt //tensorflow/tools/pip_package:build_pip_package
```
Step4: Config parameters
```
type $ which python3 and then enter path of python 3.6
say no to all other questions
please note bazel version 0.24.1 darwin is for MacOS
```
