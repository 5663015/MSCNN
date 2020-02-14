# MSCNN
This is the open code of paper: [Multi-Scale Convolutional Neural Network: A Unified Architecture Improving Effect of Domain Adaptation for Fault Diagnosis]()

## Introduction

In recent years, deep learning has been widely applied in fault diagnosis, and in order to solve the problem of inconsistent distribution of the original training dataset and the online-collecting testing dataset, transfer learning has also received extensive attention. Convolutional Neural Networks (CNN) are the most widely used network architecture among existing transfer learning approaches due to its powerful feature extraction capability. However most existing CNN extracts features from a single scale, which results in a limited range of receptive fields, and more advanced features cannot be extracted. Inspired by dilated convolution, we propose a unified CNN architecture for transfer fault diagnosis named Multi-Scale CNN (MSCNN). In the first layer, the input signals are processed by three convolution kernels with different dilation rate, which can extract more informative features at different scales. We apply MSCNN for three domain adaptation methods, and the diagnosis accuracy is improved compared to the common CNN without increasing the size of network. 

## Usage

### Requirement

- Tensorflow 2.0
- scikit-learn 0.21
- numpy 1.17

### Run base experiments

To run base experiments of dataset CWRU and Paderborn, type following commands:

```
python main.py --task xxx --model xxx --adapt_loss xxx
```

For `task` , it must be `cwru` or `paderborn`.

For `model`, it must be `cnn`, `mscnn_a` or `mscnn_b`.

For `adapt_loss`, it must be `source`, `mmd`, `coral` or `cmd`.

