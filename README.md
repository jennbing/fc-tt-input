This is a Matlab implementation of the training of a fully connected neural network using compressed data stored / computed in tensor-train (TT) format.

# Implementation Details

## Softwares:
- Matlab R2016b, a scientific programming software
(https://www.mathworks.com/products/matlab.html)
- MatConvNet Version 1.0 beta24, MATLAB toolbox implementing Convolutional Neural Networks (CNNs) for computer vision applications
(http://www.vlfeat.org/matconvnet/)
- AutoNN is a functional wrapper for MatConvNet, implementing automatic differentiation.
(https://github.com/vlfeat/autonn)
- TT-toolbox Version 2.2.2 is a MATLAB implementation of basic operations with tensors in low-parametric representation of high-dimensional tensors.
(https://github.com/oseledets/TT-Toolbox)
- TensorNet implementation of the Tensor Train layer (TT-layer) of a neural network.
(https://github.com/Bihaqo/TensorNet)

## Hardwares:
- Processor -> Intel(R) Core(TM) i3-4170 CPU @ 3.70GHz 3.70GHz
- Installed memory (RAM) -> 4.00GB
- System type -> 64-bit Operating System, x64-based processor

# Reproducing Experiments
> Insert files inside num_diff folder into TensorNet/experiments/mnist/  
1. Train fully connected network using MNIST data stored / computed in TT format
```
[net_tt, info_tt] = cnn_mnist_tt_tt_input('expDir', 'data/mnist-tt');  
```
2. . . . MNIST data in full array
```
[net_tt, info_tt] = cnn_mnist_tt_full_input('expDir', 'data/mnist-baseline');
```

> Insert files inside auto_diff folder into autonn/examples
1. Train fully connected network using CIFAR-10 data stored / computed in TT format
```
[net_tt, info_tt] = fcn_cifar10_autonn_tt_input('expDir', 'data/cifar10-tt');
```
2. . . . CIFAR-10 data in full array
```
[net_tt, info_tt] = fcn_cifar10_autonn_full_input('expDir', 'data/cifar10-baseline');
```
3. . . .  MNIST data stored / computed in TT format
```
[net_tt, info_tt] = fcn_mnist_autonn_tt_input('expDir', 'data/mnist-tt');
```
4. . . . MNIST data in full array
```
[net_tt, info_tt] = fcn_mnist_autonn_full_input('expDir', 'data/mnist-baseline');
```
