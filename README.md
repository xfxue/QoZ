# QoZ: Dynamic Quality Metric Oriented Error Bounded Lossy Compression for Scientific Datasets

## Introduction

This is the source code of the QoZ data compression introduced in the paper: QoZ: Dynamic Quality Metric Oriented Error Bounded Lossy Compression for Scientific Datasets ([IEEE paper link](https://ieeexplore.ieee.org/abstract/document/10046076))([arXiv paper link](https://arxiv.org/abs/2310.14133)). QoZ can be regarded as an extension of SZ3 ([SZ3 Code](https://github.com/szcompressor/SZ3)), which has multiple quality optimization targets and achieves better rate-distortion than SZ3 in most cases.

## Dependencies

Please install the following dependencies:

* cmake>=3.13
* gcc>=6.0

## 3rd party libraries/tools

* Zstd >= 1.3.5 (https://facebook.github.io/zstd/). Not mandatory to be mannually installed as Zstandard v1.4.5 is included and will be used if libzstd can not be found by pkg-config.

## Installation

* mkdir build && cd build
* cmake -DCMAKE_INSTALL_PREFIX:PATH=[INSTALL_DIR] ..
* make
* make install

Then, you'll find all the executables in [INSTALL_DIR]/bin and the header files in [INSTALL_DIR]/include. A Cmake version >= 3.13.0 is needed, and we recommend using gcc version 9.x to compile the code. 
Before you proceed to the following evaluations, please add the installation path of QoZ to your system path so that you can directly run the qoz command in your machine for further evaluations.

## Single compression/decompression testing Examples

You can use the executable 'qoz' command to compress/decompress. Just run the "qoz" command without any argument to check the instructions for its arguments.
The qoz executable includes the SZ3.1 compression, but the qoz features are automatically involved. You can add the argument "-q 0" to disable them to compare the compression results with SZ3-based compression (adding -q 0 will make the qoz command perform the same as SZ3.1).
Notice: Currently, the QoZ features only support 2D and 3D input data. QoZ will use SZ 3.1 to compress input data in other dimensions.

## Version History

* QoZ 1.1: Improvements over 1.0.
* QoZ 1.0: The SC '22 Version.

## Bug Report

If you have encountered any errors or abnormal results when using QoZ, please contact Jinyang Liu via jliu447@ucr.edu. 

## Citations

**Kindly note**: If you mention QoZ 1.0/1.1 in your paper, the most appropriate citation is the following reference:


**[SC 22]** Jinyang Liu, Sheng Di, Sian Jin, Kai Zhao, Xin Liang, Zizhong Chen, and Franck Cappello. "[Dynamic quality metric oriented error bounded lossy compression for scientific datasets.](https://ieeexplore.ieee.org/abstract/document/10046076)" In SC22: International Conference for High Performance Computing, Networking, Storage and Analysis, pp. 1-15. IEEE, 2022.





