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

caffe里面，原来以为是不可以随便调整学习率的，现在看来是可以的。base_lr是适用于所有层的学习率，而针对单个层，可以通过增加两个blobs_lr,用来调整该层的学习率，为什么是两个呢，因为一个调整weight的学习率，一个是调整偏执b的学习率。那么该层的学习率就变成了，base_lr*blobs_lr,base_lr*blobs_lr了。太赞了，caffe的功能真的很强大，加强学习。

AbsVal, Accuracy, ArgMax, BNLL, BatchNorm, Concat, ContrastiveLoss, Convolution, Data, Deconvolution, Dropout, DummyData, Eltwise, Embed, EuclideanLoss, Exp, Filter, Flatten, HDF5Data, HDF5Output, HingeLoss, Im2col, ImageData, InfogainLoss, InnerProduct, LRN, Log, MVN, MemoryData, MultinomialLogisticLoss, PReLU, Pooling, Power, Python, ReLU, Reduction, Reshape, SPP, Sigmoid, SigmoidCrossEntropyLoss, Silence, Slice, Softmax, SoftmaxWithLoss, Split, TanH, Threshold, Tile, WindowData


-------------------------------
http://blog.csdn.net/jiandanjinxin/article/details/50409448

http://blog.csdn.net/jiandanjinxin/article/details/50410290

http://lijiancheng0614.github.io/2015/08/21/2015_08_21_CAFFE_Features/


http://research.beenfrog.com/code/2015/03/28/read-leveldb-lmdb-for-caffe-with-python.html

http://www.cnblogs.com/platero/p/3967208.html
