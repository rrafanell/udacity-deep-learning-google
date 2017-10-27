## Support links

### Lesson 3: Regularization

 * [NotMNIST dataset challenge](http://yaroslavvb.blogspot.com.es/2011/09/notmnist-dataset.html?showComment=1391023266211#c8758720086795711595)

### Lesson 4: Convolutions

 * [Reference convolution solution](https://github.com/alex-petrenko/udacity-deep-learning/blob/14714ee4151b798cde0a31a94ac65e08b87d0f65/assignment_04_convolutions.py)
 * [classic LeNet5 architecture](http://yann.lecun.com/exdb/lenet)

### Lesson 5: Word2Vec & CBOW

 * [NLP with deep learning and tensorflow CBOW](http://www.thushv.com/natural_language_processing/word2vec-part-2-nlp-with-deep-learning-with-tensorflow-cbow)

### Lesson 6: LSTM & Seq2Seq

 * [Reference LSTM assignment](https://github.com/vrasneur/udacity-deep_learning/blob/master/6_lstm.ipynb)
 * [Reference Seq2Seq assignment](https://discussions.udacity.com/t/assignment-6-problem-3-benchmarks/158517/15)

### Installing Tensorflow

Install from sources:

 * https://www.tensorflow.org/install/install_sources

The following repository contains custom builds of tensorflow. To install one of these on your system, download the correct file according to your version of python and gcc:

 * https://github.com/lakshayg/tensorflow-build

#### Optimization of Tensorflow for the laptop (AVX, AVX2, SSE4.1 & SSE 4.2):

  * http://www.andrewclegg.org/tech/TensorFlowLaptopCPU.html
  * https://www.youtube.com/watch?v=1Gd6e5BLkwo&feature=youtu.be
  
The following optimization parameters had been used to compile Tensorflow for a **MacBook Pro (Retina, 15-inch, Late 2013)**:

Configure with:

```bash
$ bazel build -c opt --copt=-mavx --copt=-mavx2 --copt=-msse4.2 --copt=-msse4.1 --copt=-msse3 --copt=-mfma -k //tensorflow/tools/pip_package:build_pip_package
```

Build with:

```
$ bazel-bin/tensorflow/tools/pip_package/build_pip_package /tmp/tensorflow_pkg
```

