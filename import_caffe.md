# import caffe
```
# in caffe root dir
make all
make pycaffe
make distribute
# make dir for custom python modules, install caffe
mkdir ~/python
mv distribute/python/caffe ~/python
# set PYTHONPATH (this should go in your .bashrc or whatever
export PYTHONPATH=${HOME}/python:$PYTHONPATH
```
install protocbuf
```
pip install protobuf
```



