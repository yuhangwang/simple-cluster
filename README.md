Simple Clustering
===============================

## What is this?

This is a simple implementation of the state-of-the-art clustering methods such as k-means.
The implementations based on many papers that are mentioned below.

## Features

* Supported k-means algorithm with the following specific terms
  * k-means++: see **[k-means++: the advantages of careful seeding](http://dl.acm.org/citation.cfm?id=1283494)**
  * Fast convergence with geometric prunning: see **[Making k-means even faster](http://epubs.siam.org/doi/pdf/10.1137/1.9781611972801.12)**
* Supported [CMake](http://www.cmake.org/).
* Supported only L2 metric distance.
* Supported KD-tree with ANN search.
* Supported GNU C++ Compiler and clang compiler.

## Installation

### Prerequisites

* An Unix or Windows([Cygwin](https://www.cygwin.com/) not native Windows with an MSVC compiler) Operating System. Tested on Mac OS X 10.9 and Ubuntu 14.04.
* [CMake](http://www.cmake.org/) 2.8 or newer. For UNIX users, check your CMake version in terminal by `cmake -version`.
* An GNU C++ Compiler or clang compiler that support C++ 11.
* [OpenCV](http://opencv.org/downloads.html) 2.4.8 or newer. This library is used for testing only. Just for comparing the performance with our implementations.

### Build
We use CMake as the build system. On terminal,
```bash
$ git clone git@github.com:marker68/simple-cluster.git simple-cluster
$ cd ./simple-cluster
$ cmake -H. -Bbuild && cmake --build build -- -j3
```
This script will create the following files in your `bin/` directory.

```bash
$ ls  bin
CMakeFiles  libgtest_main.a      test_kdtree  test_utilities
libgtest.a  libsimplecluster.so  test_kmeans
```
* `libgtest_main.a,libgtest.a`: [Google Testing Framework](https://code.google.com/p/googletest/)'s static library files. We are using Google Test for testing.
* `libsimplecluster.{so,dylib,dll}`: dynamic library(shared library) files for SimpleCluster.
* `test_utilities, test_kdtree, test_kmeans`: test programs. See their source code in `test/` directory to know how to use this library.

## Documentation

This project uses Doxygen to generate its documentation. 
To generate the documentation:
```bash
$ cd ./doc
$ doxygen config.doxygen
```
The documentation files will be generated in HTML and LaTeX format.

## Change log

* **At version 1.0(2014/10/05)**:
    * Supported k-means algorithm.
    * Supported [CMake](http://www.cmake.org/).
    * Supported only L2 metric distance.
    * Supported KD-tree with ANN search.
    * Supported GNU C++ Compiler and clang compiler.
